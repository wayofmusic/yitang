---
title: GEMINI 演示
node_token: TG9pwzU9gieLyhkI6BvcKtyfnMb
source: https://www.feishu.cn/wiki/TG9pwzU9gieLyhkI6BvcKtyfnMb
space: 一堂学习
obj_type: docx
synced: 2026-09-26 05:30
course_line: AI能力线
stage: AI认知与基本功
train: AI认知与基本功
form: 课程逐字稿
audience: 全员
series: AI俱乐部周三LIVE
---
**GOOGLE STUDIO：**[https://aistudio.google.com/apps](https://www.google.com/url?q=https://aistudio.google.com/apps&sa=D&source=editors&ust=1768730029509251&usg=AOvVaw21z4vpIE2UgILs4wtmbMOG)  **(記得登入GOOGLE帳號)**

**以下為用於 GOOGLE STUDIO的程式碼**

# PDF转成可编辑PPT的网页

预览界面

https://gemini.google.com/share/6c98553abd39

### 演示界面

```HTML
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- PDF.js 核心 -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.min.js"></script>
    <!-- PptxGenJS (PPTX 生成) -->
    <script src="https://cdn.jsdelivr.net/npm/pptxgenjs@3.12.0/dist/pptxgen.bundle.js"></script>
    <!-- JSZip (用于 PPTX 合并逻辑) -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jszip/3.10.1/jszip.min.js"></script>
    <style>
        /* 同时引入 简体(SC) 和 繁体(TC) 以及 英文 Roboto */
        @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@400;500;700;900&family=Noto+Sans+TC:wght@400;500;700;900&family=Roboto:wght@400;500;700;900&display=swap');

        body {
            font-family: 'Roboto', 'Noto Sans SC', 'Noto Sans TC', sans-serif;
            background-color: #f8fafc;
        }

        /* 全局文字大小修正为 11px */
        .text-size-11 { font-size: 11px !important; }

        .loader { border: 3px solid #f3f3f3; border-top: 3px solid #2563eb; border-radius: 50%; width: 20px; height: 20px; animation: spin 1s linear infinite; }
        @keyframes spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }

        .pdf-view-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(var(--pdf-page-width, 100px), 1fr)); gap: 0.75rem; }

        .slots-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(var(--slot-width, 100px), 1fr));
            gap: 1rem;
        }
        .custom-scrollbar::-webkit-scrollbar { height: 5px; width: 5px; }
        .custom-scrollbar::-webkit-scrollbar-thumb { background: #cbd5e1; border-radius: 10px; }

        /* 页面卡片动态外框与背景变化 */
        .page-card { transition: all 0.2s ease; border: 2px solid transparent; flex-shrink: 0; position: relative; }
        .page-card:hover { transform: translateY(-2px); }

        .slot-card { transition: all 0.2s ease; border: 1px solid #e2e8f0; }
        .slot-card:hover { border-color: #3b82f6; box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1); }

        /* 输入框样式 - 调整为 font-bold 而非太粗 */
        .input-compact { @apply border border-slate-200 rounded px-2 py-1 outline-none focus:border-blue-400 focus:ring-1 focus:ring-blue-100 transition-all font-bold text-slate-700 bg-white shadow-sm; font-size: 11px; }

        .waiting-badge { background: #64748b; color: white; padding: 1px 6px; border-radius: 4px; font-bold; font-size: 11px; }
        .log-console { background: #0f172a; color: #10b981; font-family: 'Roboto Mono', monospace; font-size: 11px; padding: 8px; border-radius: 8px; height: 120px; overflow-y: auto; box-shadow: inset 0 2px 4px rgba(0,0,0,0.3); }
        .log-line { margin-bottom: 1px; }
        .log-line::before { content: "> "; opacity: 0.5; }
    </style>
</head>
<body class="min-h-screen text-slate-900 pb-6 text-size-11">
    <div class="max-w-[1600px] mx-auto px-4 py-3 font-bold">
        <!-- 标题与状态 -->
        <header class="mb-4 flex flex-col md:flex-row justify-between items-center gap-2">
            <div class="flex items-baseline gap-2">
                <!-- 这里保留较粗的字重作为标题，但不再强制全黑体 -->
                <h1 class="text-xl font-extrabold text-slate-900 tracking-tight italic leading-none">同道AI实验室｜NLM PDF <span class="text-blue-600">PRO V1.5</span></h1>
                高精度布局还原系统
            </div>
            <div class="bg-white px-2 py-1 rounded-lg shadow-sm border border-slate-100 flex items-center gap-2">
                <span class="font-bold text-slate-400 uppercase tracking-widest leading-none text-size-11">STATUS</span>
                <span class="font-bold text-emerald-600 flex items-center gap-1 leading-none text-size-11">
                    <span class="w-1 h-1 bg-emerald-500 rounded-full animate-pulse"></span> 系统版本 V1.5 已启动
                </span>
            </div>
        </header>
        <!-- 第一区：PDF 解析区 (工作台 1) -->
        <section class="mb-6 bg-white p-3 rounded-2xl border border-slate-100 shadow-sm">
            <div class="flex flex-col md:flex-row md:items-center justify-between mb-2 gap-2 border-b border-slate-50 pb-2">
                <div class="flex items-center gap-2">
                    <div class="w-5 h-5 bg-slate-900 text-white rounded flex items-center justify-center font-bold text-size-11">1</div>
                    <h2 class="font-bold text-slate-800 tracking-tight text-center text-size-11">PDF 高精细解析</h2>
                </div>

                <div id="pdf-controls" class="hidden flex flex-wrap items-center gap-2">
                    <div class="flex items-center gap-1.5 pl-2">
                        <span class="font-bold text-slate-400 tracking-widest uppercase leading-none text-size-11">缩放</span>
                        <input type="range" id="pdf-zoom-range" min="100" max="400" value="100" class="h-1 w-24 bg-slate-200 rounded-lg appearance-none cursor-pointer accent-blue-600">
                    </div>
                    全部导入工作台2
                </div>
            </div>
            <div id="pdf-drop-zone" class="border-2 border-dashed border-slate-100 rounded-xl p-3 text-center cursor-pointer hover:border-blue-300 hover:bg-slate-50 transition-all group relative">
                <input type="file" id="pdf-file-input" class="hidden" accept="application/pdf">
                <div id="pdf-empty-state" class="py-1">
                    点击或拖放 PDF 开始解析
                </div>
                <div id="pdf-preview-container" class="hidden text-left">
                    <div class="flex items-center justify-between bg-slate-50 px-2 py-1 rounded-lg mb-2">
                        <span id="page-count-tag" class="bg-slate-900 text-white px-1.5 py-0.5 rounded font-bold uppercase tracking-tighter text-size-11">0 PAGES</span>
                        <div class="flex gap-1.5 items-center flex-wrap justify-end">
                            <input type="text" id="pdf-export-name" value="A1" placeholder="檔名..." class="input-compact w-20">

                                <span id="pptx-btn-text">视觉还原 PPTX</span>
                                <div id="pptx-loader" class="loader !w-2.5 !h-2.5 !border-white !border-t-transparent hidden"></div>

                            还原下载 (备份)
                            清除数据
                        </div>
                    </div>
                    <div id="pdf-pages-list" class="pdf-view-grid custom-scrollbar"></div>
                </div>
            </div>
        </section>
        <!-- 第二区：图片去文字工作台 (工作台 2) -->
        <section class="mb-6 bg-white p-3 rounded-2xl border border-slate-100 shadow-sm">
            <div class="flex flex-col md:flex-row md:items-center justify-between mb-3 gap-2 border-b border-slate-50 pb-2">
                <div class="flex items-center gap-2">
                    <div class="w-5 h-5 bg-blue-600 text-white rounded flex items-center justify-center font-bold text-size-11">2</div>
                    <h2 class="font-bold text-slate-800 tracking-tight text-size-11">图片去文字工作台</h2>
                </div>

                <div class="flex items-center gap-2 flex-wrap">
                    <div id="result-export-group" class="hidden flex items-center gap-2">
                        <input type="text" id="results-export-name" value="B1" placeholder="檔名..." class="input-compact w-24">
                        导出结果 PPTX
                    </div>
                    <div class="flex items-center gap-3 bg-slate-50 px-3 py-1 rounded-xl border border-slate-200">
                        <div class="flex items-center gap-2">
                            <label class="font-bold text-slate-400 tracking-widest uppercase text-size-11">工作台网格</label>
                            <input type="range" id="slot-zoom-range" min="100" max="400" value="100" class="h-1 w-24 bg-slate-200 rounded-lg appearance-none cursor-pointer accent-blue-600">
                        </div>
                        <div class="w-px h-3 bg-slate-300"></div>
                        清空工作台
                    </div>
                    批次去文字
                </div>
            </div>
            <div id="master-drop-zone" class="border-2 border-dashed border-slate-100 rounded-xl p-3 text-center cursor-pointer hover:border-blue-300 hover:bg-slate-50 transition-all mb-3 group relative overflow-hidden">
                <input type="file" id="master-file-input" class="hidden" accept="image/*" multiple>
                <div class="flex items-center justify-center gap-2">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 text-blue-500" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2.5"></svg>
                    导入图片进行处理
                </div>
            </div>
            <div id="slots-container" class="slots-grid"></div>
        </section>
        <!-- 第三区：PPTX 魔法合并区 -->
        <section class="bg-white p-3 rounded-2xl border border-slate-100 shadow-sm">
            <div class="flex flex-col md:flex-row md:items-center justify-between mb-3 border-b border-slate-50 pb-2 gap-2">
                <div class="flex items-center gap-2">
                    <div class="w-5 h-5 bg-emerald-600 text-white rounded flex items-center justify-center font-bold text-size-11">3</div>
                    <h2 class="font-bold text-slate-800 tracking-tight leading-none text-size-11">PPTX 内容魔法合并</h2>
                </div>
                <div class="flex items-center gap-2">
                    <input type="text" id="merge-export-name" value="Merged_Result" placeholder="檔名..." class="input-compact w-32 text-size-11">
                    <span class="font-bold text-emerald-600 bg-emerald-50 px-1.5 py-0.5 rounded italic text-size-11">文字内容 + 背景模板</span>
                </div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-3 mb-3">
                <div id="pptx-text-drop" class="border border-dashed border-slate-200 rounded-xl p-3 text-center cursor-pointer hover:border-blue-400 bg-slate-50 transition-all flex flex-col items-center justify-center min-h-[80px]">
                    <input type="file" id="pptx-text-input" class="hidden" accept=".pptx">
                    1. 选择文字来源文件 (还原出的 PPTX)
                    <span id="pptx-text-name" class="text-slate-400 italic mt-1 truncate max-w-full text-size-11">尚未选择档案</span>
                </div>
                <div id="pptx-bg-drop" class="border border-dashed border-slate-200 rounded-xl p-3 text-center cursor-pointer hover:border-emerald-400 bg-slate-50 transition-all flex flex-col items-center justify-center min-h-[80px]">
                    <input type="file" id="pptx-bg-input" class="hidden" accept=".pptx">
                    2. 选择背景基底文件 (视觉模版)
                    <span id="pptx-bg-name" class="text-slate-400 italic mt-1 truncate max-w-full text-size-11">尚未选择档案</span>
                </div>
            </div>
            <div class="flex flex-col items-center gap-3">
                执行合并
                <div id="merge-log-container" class="w-full hidden">
                    <div class="flex items-center justify-between mb-1">
                        <span class="font-bold text-slate-400 uppercase italic text-size-11">处理进度日志</span>
                        下载合并结果
                    </div>
                    <div id="pptx-logs" class="log-console custom-scrollbar text-size-11"></div>
                </div>
            </div>
        </section>
    </div>
    <!-- 槽位模板 (工作台 2 使用) -->
    <template id="slot-template">
        <div class="slot-card bg-white rounded-xl p-2 flex flex-col shadow-sm">
            <div class="flex justify-between items-center mb-1">
                <span class="font-bold text-blue-600 slot-label uppercase tracking-tighter text-size-11 italic">ITEM 01</span>
                ×
            </div>
            <div class="space-y-1.5 flex-grow">
                <div class="aspect-video bg-slate-50 rounded-lg overflow-hidden border border-slate-50 relative group shadow-inner">
                    <div class="slot-loader absolute inset-0 bg-white/80 hidden flex flex-col items-center justify-center">
                        <div class="loader mb-1"></div>
                        <span class="font-bold text-blue-600 uppercase text-size-11 tracking-widest">Processing</span>
                    </div>
                    <div class="slot-waiting absolute inset-0 bg-slate-900/10 hidden flex flex-col items-center justify-center font-bold"><span class="waiting-badge text-size-11">QUEUED</span></div>
                </div>
                <div class="aspect-video bg-slate-50 rounded-lg overflow-hidden border border-slate-50 relative flex items-center justify-center text-center shadow-inner">
                    <div class="placeholder text-slate-200 italic font-bold uppercase text-size-11">Waiting Result</div>
                </div>
            </div>
            <div class="flex gap-1.5 mt-2.5">
                去文字处理

                    <svg xmlns="http://www.w3.org/2000/svg" class="h-3 w-3" fill="none" viewBox="0 0 24 24" stroke="currentColor"></svg>

            </div>
        </div>
    </template>
    <div id="toast" class="fixed bottom-4 left-1/2 -translate-x-1/2 bg-slate-900 text-white px-4 py-2 rounded-lg shadow-xl opacity-0 transition-all pointer-events-none z-50 font-bold text-size-11"></div>
    <script>
        window.addEventListener('DOMContentLoaded', () => {
            const apiKey = "";
            const MODEL_OCR = "gemini-2.5-flash-preview-09-2025";
            const MODEL_IMAGE = "gemini-2.5-flash-image-preview";
            pdfjsLib.GlobalWorkerOptions.workerSrc = 'https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.worker.min.js';
            const toast = document.getElementById('toast');
            const pdfPagesList = document.getElementById('pdf-pages-list');
            const pdfPreviewContainer = document.getElementById('pdf-preview-container');
            const pdfControls = document.getElementById('pdf-controls');
            const pdfZoomRange = document.getElementById('pdf-zoom-range');
            const slotsContainer = document.getElementById('slots-container');
            const slotZoomRange = document.getElementById('slot-zoom-range');
            const processAllBtn = document.getElementById('process-all-btn');
            const clearAllSlotsBtn = document.getElementById('clear-all-slots-btn');
            const resultExportGroup = document.getElementById('result-export-group');
            const pptxLogs = document.getElementById('pptx-logs');
            const mergeLogContainer = document.getElementById('merge-log-container');
            const downloadMergedBtn = document.getElementById('download-merged-btn');
            const startMergeBtn = document.getElementById('start-merge-btn');
            const pdfDownloadBackupBtn = document.getElementById('pdf-download-backup-btn');
            let currentPdfPageUrls = [];
            let slots = [];
            let textPptxFile = null;
            let bgPptxFile = null;
            let mergedBlob = null;
            let lastRestoreBlob = null;
            function showToast(msg, isError = false) {
                if (!toast) return;
                toast.textContent = msg;
                toast.style.backgroundColor = isError ? '#ef4444' : '#0f172a';
                toast.classList.replace('opacity-0', 'opacity-100');
                setTimeout(() => toast.classList.replace('opacity-100', 'opacity-0'), 3000);
            }
            const wait = (ms) => new Promise(res => setTimeout(res, ms));
            async function fetchWithRetry(url, options, maxRetries = 6) {
                const delays = [1000, 2000, 4000, 8000, 16000, 32000];
                for (let i = 0; i < maxRetries; i++) {
                    try {
                        const response = await fetch(url, options);
                        if (response.ok) return await response.json();
                        if (response.status === 429) { await wait(delays[i]); continue; }
                        const errorJson = await response.json();
                        throw new Error(errorJson.error?.message || `HTTP ${response.status}`);
                    } catch (e) {
                        if (i === maxRetries - 1) throw e;
                        await wait(delays[i]);
                    }
                }
            }
            function createNewSlot(imageUrl = null) {
                const index = slots.length;
                const clone = document.getElementById('slot-template').content.cloneNode(true);
                const card = clone.querySelector('.slot-card');
                const data = {
                    id: Date.now() + Math.random(),
                    el: card,
                    originalImg: card.querySelector('.original-img'),
                    resultImg: card.querySelector('.result-img'),
                    loader: card.querySelector('.slot-loader'),
                    waitingOverlay: card.querySelector('.slot-waiting'),
                    originalBase64: null
                };
                card.querySelector('.slot-label').textContent = `ITEM ${String(index + 1).padStart(2, '0')}`;
                card.querySelector('.process-btn').onclick = () => processSingleSlot(data);
                card.querySelector('.remove-btn').onclick = () => removeSlot(data);
                if (imageUrl) {
                    data.originalBase64 = imageUrl.split(',')[1];
                    data.originalImg.src = imageUrl;
                    card.querySelector('.placeholder').classList.add('hidden');
                }
                slots.push(data);
                slotsContainer.appendChild(card);
                updateGlobalControls();
                return data;
            }
            function removeSlot(data) {
                data.el.remove();
                slots = slots.filter(s => s.id !== data.id);
                slots.forEach((s, i) => {
                    s.el.querySelector('.slot-label').textContent = `ITEM ${String(i + 1).padStart(2, '0')}`;
                });
                updateGlobalControls();
            }
            function clearAllSlots() {
                slotsContainer.innerHTML = '';
                slots = [];
                updateGlobalControls();
                showToast('工作台已清空');
            }
            function updateGlobalControls() {
                const hasProcessable = slots.some(s => s.originalBase64 && !s.resultImg.src.startsWith('data'));
                const hasResults = slots.some(s => s.resultImg.src.startsWith('data:image'));
                clearAllSlotsBtn.classList.toggle('hidden', slots.length === 0);
                processAllBtn.classList.toggle('hidden', !hasProcessable);
                resultExportGroup.classList.toggle('hidden', !hasResults);
            }
            slotZoomRange.oninput = () => {
                slotsContainer.style.setProperty('--slot-width', `${slotZoomRange.value}px`);
            };
            document.getElementById('pdf-file-input').onchange = (e) => processPdf(e.target.files[0]);
            document.getElementById('pdf-drop-zone').onclick = (e) => {
                if(!e.target.closest('#pdf-preview-container')) document.getElementById('pdf-file-input').click();
            };
            document.getElementById('clear-pdf-btn').onclick = (e) => {
                e.stopPropagation();
                pdfPagesList.innerHTML = '';
                currentPdfPageUrls = [];
                pdfPreviewContainer.classList.add('hidden');
                pdfControls.classList.add('hidden');
                pdfDownloadBackupBtn.classList.add('hidden');
                document.getElementById('pdf-empty-state').classList.remove('hidden');
                lastRestoreBlob = null;
                showToast('PDF 数据已清除');
            };
            async function processPdf(file) {
                if(!file || file.type !== 'application/pdf') return;
                showToast('正在解析 PDF...');
                currentPdfPageUrls = [];
                pdfPreviewContainer.classList.remove('hidden');
                pdfControls.classList.remove('hidden');
                pdfPagesList.innerHTML = '';
                document.getElementById('pdf-empty-state').classList.add('hidden');
                try {
                    const arrayBuffer = await file.arrayBuffer();
                    const pdf = await pdfjsLib.getDocument({ data: arrayBuffer }).promise;
                    document.getElementById('page-count-tag').textContent = `${pdf.numPages} PAGES`;
                    for (let i = 1; i <= pdf.numPages; i++) {
                        const page = await pdf.getPage(i);
                        const viewport = page.getViewport({ scale: 2 });
                        const canvas = document.createElement('canvas');
                        const ctx = canvas.getContext('2d');
                        canvas.height = viewport.height; canvas.width = viewport.width;
                        await page.render({ canvasContext: ctx, viewport }).promise;
                        const dataUrl = canvas.toDataURL('image/png');
                        const pageId = `pdf_page_${Date.now()}_${i}`;

                        const pageData = { id: pageId, url: dataUrl };
                        currentPdfPageUrls.push(pageData);
                        const div = document.createElement('div');
                        div.className = 'page-card bg-white p-1 rounded-lg shadow-sm relative group cursor-grab';
                        div.setAttribute('data-page-id', pageId);
                        div.innerHTML = `<div class="relative overflow-hidden rounded">  ＋ </div>`;

                        div.querySelector('.add-btn').onclick = (e) => { e.stopPropagation(); createNewSlot(dataUrl); showToast('已导入工作台'); };

                        pdfPagesList.appendChild(div);
                    }
                    updatePdfZoom();
                } catch (err) { showToast('PDF 解析失败', true); }
            }
            function updatePdfZoom() {
                pdfPagesList.style.setProperty('--pdf-page-width', `${pdfZoomRange.value}px`);
            }
            pdfZoomRange.oninput = updatePdfZoom;
            // 还原下载按钮功能
            pdfDownloadBackupBtn.onclick = () => {
                if (!lastRestoreBlob) return showToast('尚未产生还原数据', true);
                const customName = document.getElementById('pdf-export-name').value.trim();
                const fileName = customName ? `${customName}_Backup.pptx` : `Restore_Backup_${Date.now()}.pptx`;
                const a = document.createElement('a');
                a.href = URL.createObjectURL(lastRestoreBlob);
                a.download = fileName;
                a.click();
                showToast('备份文件已下载');
            };
            document.getElementById('pdf-to-pptx-btn').onclick = async () => {
                if (currentPdfPageUrls.length === 0) return showToast('请先解析 PDF', true);
                const btn = document.getElementById('pdf-to-pptx-btn');
                const txt = document.getElementById('pptx-btn-text');
                const ldr = document.getElementById('pptx-loader');
                const customName = document.getElementById('pdf-export-name').value.trim();

                btn.disabled = true; ldr.classList.remove('hidden'); pdfDownloadBackupBtn.classList.add('hidden');

                try {
                    const pptx = new PptxGenJS();
                    pptx.layout = 'LAYOUT_WIDE';
                    for (let i = 0; i < currentPdfPageUrls.length; i++) {
                        const pageData = currentPdfPageUrls[i];
                        txt.textContent = `辨识中 (${i+1}/${currentPdfPageUrls.length})`;
                        const base64 = pageData.url.split(',')[1];

                        const blocks = await callAiOcr(base64);

                        const slide = pptx.addSlide(); slide.background = { fill: "FFFFFF" };
                        if (blocks && Array.isArray(blocks)) {
                            blocks.forEach(block => {
                                if (!block.text || !block.box_2d) return;
                                let [ymin, xmin, ymax, xmax] = block.box_2d;
                                if (ymax <= 1 && xmax <= 1) { ymin *= 1000; xmin *= 1000; ymax *= 1000; xmax *= 1000; }
                                slide.addText(block.text, {
                                    x: `${(xmin / 10).toFixed(2)}%`,
                                    y: `${(ymin / 10).toFixed(2)}%`,
                                    w: `${((xmax - xmin) / 10).toFixed(2)}%`,
                                    h: `${((ymax - ymin) / 10).toFixed(2)}%`,
                                    fontSize: block.font_size || 12,
                                    color: block.color?.replace('#','') || '000000',
                                    bold: block.is_bold || false, align: block.align || 'left', valign: 'middle'
                                });
                            });
                        }
                        await wait(1800);
                    }
                    const fileName = customName ? `${customName}.pptx` : `Restore_${Date.now()}.pptx`;
                    lastRestoreBlob = await pptx.write("blob");
                    const downloadUrl = URL.createObjectURL(lastRestoreBlob);
                    const a = document.createElement('a'); a.href = downloadUrl; a.download = fileName; a.click();
                    pdfDownloadBackupBtn.classList.remove('hidden');
                    showToast('还原完成');
                } catch (err) { showToast(`还原失败: ${err.message}`, true); }
                finally { btn.disabled = false; ldr.classList.add('hidden'); txt.textContent = '视觉还原 PPTX'; }
            };
            async function callAiOcr(base64) {
                let prompt = "请辨识图片中所有文字。回传 JSON ARRAY，每个对象包含：text, box_2d [ymin, xmin, ymax, xmax], font_size, is_bold, align, color。坐标比例 0-1000。";
                prompt += " 【优化指令】源文档包含 NotebookLM 生成之特征。请特别注意处理双字段排版与标题层级。若有右下角的 'NOTEBOOKLM' 水印字样，请务必辨识并精确标注位置。";

                const payload = {
                    contents: [{ parts: [{ text: prompt }, { inlineData: { mimeType: "image/png", data: base64 } }] }],
                    generationConfig: {
                        responseMimeType: "application/json",
                        responseSchema: {
                            type: "ARRAY",
                            items: {
                                type: "OBJECT",
                                properties: {
                                    text: { type: "STRING" },
                                    box_2d: { type: "ARRAY", items: { type: "NUMBER" } },
                                    font_size: { type: "NUMBER" },
                                    is_bold: { type: "BOOLEAN" },
                                    align: { type: "STRING" },
                                    color: { type: "STRING" }
                                },
                                required: ["text", "box_2d"]
                            }
                        }
                    }
                };
                const data = await fetchWithRetry(`https://generativelanguage.googleapis.com/v1beta/models/${MODEL_OCR}:generateContent?key=${apiKey}`, {
                    method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify(payload)
                });
                const textResult = data.candidates?.[0]?.content?.parts?.[0]?.text;
                return textResult ? JSON.parse(textResult) : [];
            }
            async function processSingleSlot(s) {
                if (!s.originalBase64) return;
                s.loader.classList.remove('hidden');
                try {
                    let prompt = "Please remove all main text from this image and output a clean background version. Fill gaps naturally with background texture or context.";
                    const payload = {
                        contents: [{ parts: [{ text: prompt }, { inlineData: { mimeType: "image/png", data: s.originalBase64 } }] }]
                    };
                    const response = await fetchWithRetry(`https://generativelanguage.googleapis.com/v1beta/models/${MODEL_IMAGE}:generateContent?key=${apiKey}`, {
                        method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify(payload)
                    });
                    const b64 = response.candidates?.[0]?.content?.parts?.find(p => p.inlineData)?.inlineData?.data;
                    if (b64) {
                        s.resultImg.src = `data:image/png;base64,${b64}`;
                        s.resultImg.classList.remove('hidden');
                        s.el.querySelector('.placeholder').classList.add('hidden');
                        const dBtn = s.el.querySelector('.download-btn');
                        dBtn.disabled = false;
                        dBtn.onclick = () => {
                            const a = document.createElement('a'); a.href = s.resultImg.src; a.download = `cleaned_${Date.now()}.png`; a.click();
                        };
                    }
                } catch (e) { showToast('处理失败', true); }
                finally { s.loader.classList.add('hidden'); updateGlobalControls(); }
            }
            processAllBtn.onclick = async () => {
                const pending = slots.filter(s => s.originalBase64 && !s.resultImg.src.startsWith('data'));
                if (pending.length === 0) return;
                showToast(`正在批处理 ${pending.length} 张图片...`);
                pending.forEach(s => s.waitingOverlay.classList.remove('hidden'));
                for (const s of pending) {
                    s.waitingOverlay.classList.add('hidden');
                    await processSingleSlot(s);
                    await wait(1800);
                }
                showToast('批处理完成');
            };
            document.getElementById('export-results-pptx-btn').onclick = () => {
                const results = slots.filter(s => s.resultImg.src.startsWith('data:image'));
                if (results.length === 0) return showToast('无可导出内容', true);
                const customName = document.getElementById('results-export-name').value.trim();
                const pptx = new PptxGenJS();
                pptx.layout = 'LAYOUT_WIDE';
                results.forEach(s => {
                    pptx.addSlide().addImage({ data: s.resultImg.src, x: 0, y: 0, w: '100%', h: '100%' });
                });
                const fileName = customName ? `${customName}.pptx` : `Export_${Date.now()}.pptx`;
                pptx.writeFile({ fileName });
                showToast(`已成功导出 ${fileName}`);
            };
            function addPptxLog(msg) {
                const div = document.createElement('div');
                div.className = 'log-line'; div.textContent = msg;
                pptxLogs.appendChild(div); pptxLogs.scrollTop = pptxLogs.scrollHeight;
            }
            document.getElementById('pptx-text-drop').onclick = () => document.getElementById('pptx-text-input').click();
            document.getElementById('pptx-bg-drop').onclick = () => document.getElementById('pptx-bg-input').click();
            document.getElementById('pptx-text-input').onchange = (e) => {
                textPptxFile = e.target.files[0];
                document.getElementById('pptx-text-name').textContent = textPptxFile ? textPptxFile.name : '尚未选择';
            };
            document.getElementById('pptx-bg-input').onchange = (e) => {
                bgPptxFile = e.target.files[0];
                document.getElementById('pptx-bg-name').textContent = bgPptxFile ? bgPptxFile.name : '尚未选择';
            };
            startMergeBtn.onclick = async () => {
                if (!textPptxFile || !bgPptxFile) return showToast('请先选择档案', true);
                startMergeBtn.disabled = true; mergeLogContainer.classList.remove('hidden');
                downloadMergedBtn.classList.add('hidden'); pptxLogs.innerHTML = '';
                addPptxLog('启动合并程序...');
                try {
                    const textZip = new JSZip(); const bgZip = new JSZip();
                    const textContent = await textZip.loadAsync(textPptxFile);
                    const bgContent = await bgZip.loadAsync(bgPptxFile);
                    const getSlideNum = (path) => parseInt(path.match(/slide(\d+)\.xml/)[1]);
                    const textSlides = Object.keys(textContent.files).filter(p => p.match(/ppt\/slides\/slide\d+\.xml/)).sort((a,b) => getSlideNum(a) - getSlideNum(b));
                    const bgSlides = Object.keys(bgContent.files).filter(p => p.match(/ppt\/slides\/slide\d+\.xml/)).sort((a,b) => getSlideNum(a) - getSlideNum(b));
                    const parser = new DOMParser(); const serializer = new XMLSerializer();
                    const limit = Math.min(textSlides.length, bgSlides.length);
                    for (let i = 0; i < limit; i++) {
                        addPptxLog(`移植第 ${i+1} 页内容...`);
                        const tXml = await textContent.file(textSlides[i]).async("string");
                        const bXml = await bgContent.file(bgSlides[i]).async("string");
                        const tDoc = parser.parseFromString(tXml, "application/xml");
                        const bDoc = parser.parseFromString(bXml, "application/xml");
                        const getSpTree = (doc) => {
                            const trees = doc.getElementsByTagName("*");
                            for(let el of trees) if(el.localName === 'spTree') return el;
                            return null;
                        };
                        const tTree = getSpTree(tDoc); const bTree = getSpTree(bDoc);
                        if (tTree && bTree) {
                            const nodes = Array.from(tTree.childNodes);
                            nodes.forEach(node => {
                                const name = node.localName || node.nodeName.split(':').pop();
                                if (['sp', 'grpSp', 'graphicFrame', 'pic'].includes(name)) {
                                    bTree.appendChild(bDoc.importNode(node, true));
                                }
                            });
                            bgContent.file(bgSlides[i], serializer.serializeToString(bDoc));
                        }
                    }
                    mergedBlob = await bgContent.generateAsync({ type: "blob" });
                    addPptxLog('完成！'); downloadMergedBtn.classList.remove('hidden');
                    showToast('合并成功');
                } catch (err) { addPptxLog(`错误: ${err.message}`); showToast('失败', true); }
                finally { startMergeBtn.disabled = false; }
            };
            downloadMergedBtn.onclick = () => {
                if (!mergedBlob) return;
                const customName = document.getElementById('merge-export-name').value.trim();
                const a = document.createElement('a');
                a.href = URL.createObjectURL(mergedBlob);
                const fileName = customName ? `${customName}.pptx` : `Merged_${Date.now()}.pptx`;
                a.download = fileName; a.click();
            };
            clearAllSlotsBtn.onclick = () => clearAllSlots();
            document.getElementById('add-all-pages-btn').onclick = () => {
                if (currentPdfPageUrls.length === 0) return showToast('无解析数据', true);
                currentPdfPageUrls.forEach(item => createNewSlot(item.url));
                showToast(`已导入 ${currentPdfPageUrls.length} 个页面`);
            };
            document.getElementById('master-drop-zone').onclick = () => document.getElementById('master-file-input').click();
            document.getElementById('master-file-input').onchange = (e) => {
                Array.from(e.target.files).forEach(file => {
                    if (file.type.startsWith('image/')) {
                        const reader = new FileReader();
                        reader.onload = (ev) => createNewSlot(ev.target.result);
                        reader.readAsDataURL(file);
                    }
                });
            };

            updatePdfZoom();
            slotsContainer.style.setProperty('--slot-width', `${slotZoomRange.value}px`);
            updateGlobalControls();
        });
    </script>
</body>
</html>
```

### 2.1的code

```HTML
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- PDF.js Core -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.min.js"></script>
    <!-- PptxGenJS (PPTX Generation) -->
    <script src="https://cdn.jsdelivr.net/npm/pptxgenjs@3.12.0/dist/pptxgen.bundle.js"></script>
    <!-- JSZip (For PPTX Merging) -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jszip/3.10.1/jszip.min.js"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&family=Noto+Sans+SC:wght@400;700;900&display=swap');

        :root {
            --primary: #2563eb;
            --accent: #7c3aed;
            --success: #10b981;
            --bg-main: #f8fafc;
        }

        body {
            font-family: 'Inter', 'Noto Sans SC', sans-serif;
            background-color: var(--bg-main);
            color: #1e293b;
        }

        .text-size-11 { font-size: 11px !important; }

        .loader {
            border: 2px solid #f3f3f3;
            border-top: 2px solid var(--primary);
            border-radius: 50%;
            width: 16px;
            height: 16px;
            animation: spin 0.8s linear infinite;
        }
        @keyframes spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }

        .pdf-view-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(var(--pdf-page-width, 140px), 1fr));
            gap: 1rem;
        }

        .slots-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(var(--slot-width, 160px), 1fr));
            gap: 1.25rem;
        }

        .custom-scrollbar::-webkit-scrollbar { height: 6px; width: 6px; }
        .custom-scrollbar::-webkit-scrollbar-thumb { background: #cbd5e1; border-radius: 10px; }

        .page-card {
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            border: 2px solid transparent;
            background: white;
        }
        .page-card.para-active {
            border-color: var(--primary);
            box-shadow: 0 0 0 4px rgba(37, 99, 235, 0.1);
        }
        .page-card:hover { transform: translateY(-4px); box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1); }

        .para-badge {
            position: absolute;
            top: 8px;
            right: 8px;
            background: var(--primary);
            color: white;
            padding: 2px 6px;
            border-radius: 9999px;
            font-size: 9px;
            font-weight: 800;
            opacity: 0;
            transition: opacity 0.2s;
            pointer-events: none;
            z-index: 30;
        }
        .para-active .para-badge { opacity: 1; }

        .input-compact {
            border: 1px solid #e2e8f0;
            border-radius: 6px;
            padding: 4px 8px;
            outline: none;
            font-weight: 700;
            font-size: 11px;
            transition: all 0.2s;
        }
        .input-compact:focus { border-color: var(--primary); ring: 2px rgba(37, 99, 235, 0.1); }

        .log-console {
            background: #0f172a;
            color: #10b981;
            font-family: 'ui-monospace', monospace;
            font-size: 11px;
            padding: 12px;
            border-radius: 12px;
            height: 160px;
            overflow-y: auto;
        }
        .log-line { margin-bottom: 2px; border-left: 2px solid transparent; padding-left: 8px; }
        .log-line.info { border-left-color: var(--primary); }
        .log-line.success { border-left-color: var(--success); }

        .glass-panel {
            background: rgba(255, 255, 255, 0.8);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.3);
        }
    </style>
</head>
<body class="min-h-screen pb-12">

    <div class="max-w-[1500px] mx-auto px-6 py-6">
        <!-- Header -->
        <header class="mb-8 flex flex-col md:flex-row justify-between items-end gap-4">
            <div>
                <div class="flex items-center gap-3 mb-1">
                    <div class="bg-blue-600 text-white p-1.5 rounded-lg shadow-lg">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"></svg>
                    </div>
                    <h1 class="text-2xl font-black text-slate-900 tracking-tight italic">同道LAB｜NLM PDF <span class="text-blue-600">PRO V2.1</span></h1>
                </div>
                高级布局还原与视觉去文字系统
            </div>

            <div class="flex items-center gap-4">
                <div class="bg-white px-3 py-1.5 rounded-full shadow-sm border border-slate-200 flex items-center gap-2">
                    <span class="w-2 h-2 bg-emerald-500 rounded-full animate-pulse"></span>
                    <span class="font-bold text-slate-600 uppercase tracking-widest text-[10px]">系统引擎已启动</span>
                </div>
            </div>
        </header>

        <div class="grid grid-cols-1 gap-8">

            <!-- SECTION 1: PDF Analysis -->
            <section class="bg-white rounded-3xl border border-slate-200 shadow-sm overflow-hidden">
                <div class="px-6 py-4 bg-slate-50 border-b border-slate-100 flex items-center justify-between">
                    <div class="flex items-center gap-3">
                        <span class="bg-slate-900 text-white w-6 h-6 rounded-md flex items-center justify-center font-black text-xs">01</span>
                        <h2 class="font-black text-slate-800 tracking-tight">PDF 高精细识别工作区</h2>
                    </div>

                    <div id="pdf-controls" class="hidden flex items-center gap-4">
                        <div class="flex bg-slate-200/50 p-1 rounded-lg">
                            全段落模式
                            取消段落
                        </div>
                        <div class="h-4 w-px bg-slate-200"></div>
                        <div class="flex items-center gap-2">
                            <span class="text-[10px] font-black text-slate-400 uppercase">缩放</span>
                            <input type="range" id="pdf-zoom-range" min="120" max="400" value="160" class="h-1 w-20 bg-slate-200 rounded-lg appearance-none cursor-pointer accent-blue-600">
                        </div>
                        全部导入去文字
                    </div>
                </div>

                <div class="p-6">
                    <div id="pdf-drop-zone" class="border-2 border-dashed border-slate-200 rounded-2xl p-8 text-center cursor-pointer hover:border-blue-400 hover:bg-blue-50/30 transition-all group">
                        <input type="file" id="pdf-file-input" class="hidden" accept="application/pdf">
                        <div id="pdf-empty-state">
                            <div class="mb-3 flex justify-center">
                                <div class="w-12 h-12 bg-blue-100 text-blue-600 rounded-2xl flex items-center justify-center group-hover:scale-110 transition-transform">
                                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"></svg>
                                </div>
                            </div>
                            点击或拖拽 PDF 开始智能识别
                            支持多页批量处理与 NotebookLM 结构优化
                        </div>

                        <div id="pdf-preview-container" class="hidden text-left">
                            <div class="flex flex-wrap items-center justify-between gap-4 mb-6 p-4 bg-slate-50 rounded-xl border border-slate-100">
                                <div class="flex items-center gap-2">
                                    <span id="page-count-tag" class="bg-slate-900 text-white px-2 py-1 rounded font-black text-[10px] tracking-widest">0 页</span>
                                    <input type="text" id="pdf-export-name" value="还原项目" class="input-compact w-40">
                                </div>

                                <div class="flex items-center gap-3">
                                    <div class="flex items-center gap-2 bg-white px-2 py-1.5 rounded-lg border border-slate-200">
                                        <input type="checkbox" id="pdf-ocr-precision-check" class="w-4 h-4 rounded text-blue-600 focus:ring-0">
                                        <label for="pdf-ocr-precision-check" class="font-bold text-slate-600 text-[11px] cursor-pointer">逐行扫描</label>
                                    </div>
                                    <div class="flex items-center gap-2 bg-white px-2 py-1.5 rounded-lg border border-slate-200">
                                        <input type="checkbox" id="pdf-ocr-paragraph-check" class="w-4 h-4 rounded text-blue-600 focus:ring-0">
                                        <label for="pdf-ocr-paragraph-check" class="font-bold text-slate-600 text-[11px] cursor-pointer">全局段落</label>
                                    </div>
                                    <div class="flex items-center gap-2 bg-purple-50 px-2 py-1.5 rounded-lg border border-purple-100">
                                        <input type="checkbox" id="pdf-ocr-notebooklm-check" checked class="w-4 h-4 rounded text-purple-600 focus:ring-0">
                                        <label for="pdf-ocr-notebooklm-check" class="font-black text-purple-700 text-[11px] cursor-pointer">NotebookLM 结构</label>
                                    </div>

                                        <span id="pptx-btn-text">视觉还原 PPTX</span>
                                        <div id="pptx-loader" class="loader !border-white !border-t-transparent hidden"></div>

                                    重置
                                </div>
                            </div>
                            <div id="pdf-pages-list" class="pdf-view-grid custom-scrollbar"></div>
                        </div>
                    </div>
                </div>
            </section>

            <!-- SECTION 2: Image Cleansing -->
            <section class="bg-white rounded-3xl border border-slate-200 shadow-sm overflow-hidden">
                <div class="px-6 py-4 bg-slate-50 border-b border-slate-100 flex items-center justify-between">
                    <div class="flex items-center gap-3">
                        <span class="bg-blue-600 text-white w-6 h-6 rounded-md flex items-center justify-center font-black text-xs">02</span>
                        <h2 class="font-black text-slate-800 tracking-tight">图片背景去文字工作台</h2>
                    </div>

                    <div class="flex items-center gap-4">
                        <div id="result-export-group" class="hidden flex items-center gap-2">
                            <input type="text" id="results-export-name" value="纯净背景" class="input-compact w-32">
                            导出背景 PPTX
                        </div>
                        <div class="flex items-center gap-2">
                            <span class="text-[10px] font-black text-slate-400 uppercase">网格</span>
                            <input type="range" id="slot-zoom-range" min="150" max="400" value="200" class="h-1 w-20 bg-slate-200 rounded-lg appearance-none cursor-pointer accent-blue-600">
                        </div>
                        执行批量去文字
                    </div>
                </div>

                <div class="p-6">
                    <div id="master-drop-zone" class="border-2 border-dashed border-slate-100 rounded-2xl p-6 text-center cursor-pointer bg-slate-50/50 hover:bg-slate-50 transition-all mb-6">
                        <input type="file" id="master-file-input" class="hidden" accept="image/*" multiple>
                        + 导入外部图片进行处理
                    </div>
                    <div id="slots-container" class="slots-grid"></div>
                </div>
            </section>

            <!-- SECTION 3: Magic Merger -->
            <section class="bg-white rounded-3xl border border-slate-200 shadow-sm overflow-hidden">
                <div class="px-6 py-4 bg-slate-50 border-b border-slate-100 flex items-center justify-between">
                    <div class="flex items-center gap-3">
                        <span class="bg-emerald-600 text-white w-6 h-6 rounded-md flex items-center justify-center font-black text-xs">03</span>
                        <h2 class="font-black text-slate-800 tracking-tight">PPTX 内容魔法合并 (重叠还原)</h2>
                    </div>
                    <div class="flex items-center gap-2">
                        <input type="text" id="merge-export-name" value="最终演示文稿" class="input-compact w-40">
                        <span class="font-black text-emerald-600 bg-emerald-50 px-2 py-1 rounded text-[10px] uppercase tracking-wider">智能分层</span>
                    </div>
                </div>

                <div class="p-8">
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-8">
                        <div id="pptx-text-drop" class="border-2 border-dashed border-slate-200 rounded-2xl p-6 text-center cursor-pointer bg-slate-50 hover:border-blue-400 transition-all">
                            <input type="file" id="pptx-text-input" class="hidden" accept=".pptx">
                            <div class="w-10 h-10 bg-white rounded-xl shadow-sm border border-slate-100 flex items-center justify-center mx-auto mb-3">
                                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-blue-500" fill="none" viewBox="0 0 24 24" stroke="currentColor"></svg>
                            </div>
                            1. 文字源文件 (还原出的 PPTX)
                            <span id="pptx-text-name" class="text-slate-400 text-[10px] font-medium mt-2 block italic">尚未选择文件</span>
                        </div>
                        <div id="pptx-bg-drop" class="border-2 border-dashed border-slate-200 rounded-2xl p-6 text-center cursor-pointer bg-slate-50 hover:border-emerald-400 transition-all">
                            <input type="file" id="pptx-bg-input" class="hidden" accept=".pptx">
                            <div class="w-10 h-10 bg-white rounded-xl shadow-sm border border-slate-100 flex items-center justify-center mx-auto mb-3">
                                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-emerald-500" fill="none" viewBox="0 0 24 24" stroke="currentColor"></svg>
                            </div>
                            2. 背景底稿文件 (视觉模板)
                            <span id="pptx-bg-name" class="text-slate-400 text-[10px] font-medium mt-2 block italic">尚未选择文件</span>
                        </div>
                    </div>

                    <div class="flex flex-col items-center">
                        执行 AI 结构合并

                        <div id="merge-log-container" class="w-full mt-8 hidden">
                            <div class="flex items-center justify-between mb-2">
                                <span class="text-[10px] font-black text-slate-400 uppercase italic">处理日志</span>
                                立即下载结果
                            </div>
                            <div id="pptx-logs" class="log-console custom-scrollbar"></div>
                        </div>
                    </div>
                </div>
            </section>
        </div>
    </div>

    <!-- TEMPLATE: Slot Card -->
    <template id="slot-template">
        <div class="slot-card bg-white rounded-2xl p-3 flex flex-col shadow-sm border border-slate-100 group">
            <div class="flex justify-between items-center mb-2">
                <span class="font-black text-blue-600 slot-label text-[10px] italic tracking-tighter">ITEM 00</span>
                ×
            </div>
            <div class="space-y-2 flex-grow">
                <div class="aspect-[4/3] bg-slate-50 rounded-xl overflow-hidden border border-slate-100 relative shadow-inner">
                    <div class="slot-loader absolute inset-0 bg-white/90 hidden flex flex-col items-center justify-center z-20">
                        <div class="loader mb-2 !w-5 !h-5"></div>
                        <span class="font-black text-blue-600 text-[9px] uppercase tracking-widest">去文字处理中...</span>
                    </div>
                    <div class="slot-waiting absolute inset-0 bg-slate-900/10 hidden flex items-center justify-center z-10">
                        <span class="bg-slate-800 text-white text-[9px] font-black px-2 py-1 rounded-full shadow-lg uppercase tracking-tighter">排队中</span>
                    </div>
                </div>
                <div class="aspect-[4/3] bg-slate-100 rounded-xl overflow-hidden border border-dashed border-slate-200 relative flex items-center justify-center group-hover:border-blue-200 transition-all">
                    <div class="placeholder text-slate-300 font-black text-[10px] italic uppercase text-center px-4">处理完成后显示结果</div>
                </div>
            </div>
            <div class="flex gap-2 mt-3">
                去文字

                    <svg xmlns="http://www.w3.org/2000/svg" class="h-3.5 w-3.5" fill="none" viewBox="0 0 24 24" stroke="currentColor"></svg>

            </div>
        </div>
    </template>

    <div id="toast" class="fixed bottom-6 left-1/2 -translate-x-1/2 glass-panel text-slate-900 px-6 py-3 rounded-2xl shadow-2xl opacity-0 transition-all pointer-events-none z-50 font-black text-xs border border-slate-200 flex items-center gap-3">
        <span id="toast-icon"></span>
        <span id="toast-msg"></span>
    </div>

    <script>
        const apiKey = "";
        const MODEL_OCR = "gemini-2.5-flash-preview-09-2025";
        const MODEL_IMAGE = "gemini-2.5-flash-image-preview";

        pdfjsLib.GlobalWorkerOptions.workerSrc = 'https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.worker.min.js';

        const toast = document.getElementById('toast');
        const toastMsg = document.getElementById('toast-msg');
        const pdfPagesList = document.getElementById('pdf-pages-list');
        const pdfPreviewContainer = document.getElementById('pdf-preview-container');
        const pdfControls = document.getElementById('pdf-controls');
        const pdfZoomRange = document.getElementById('pdf-zoom-range');
        const slotsContainer = document.getElementById('slots-container');
        const slotZoomRange = document.getElementById('slot-zoom-range');
        const processAllBtn = document.getElementById('process-all-btn');
        const resultExportGroup = document.getElementById('result-export-group');
        const pptxLogs = document.getElementById('pptx-logs');
        const mergeLogContainer = document.getElementById('merge-log-container');
        const downloadMergedBtn = document.getElementById('download-merged-btn');
        const startMergeBtn = document.getElementById('start-merge-btn');

        let currentPdfPageUrls = [];
        let slots = [];
        let textPptxFile = null;
        let bgPptxFile = null;
        let mergedBlob = null;

        function showToast(msg, type = 'info') {
            toastMsg.textContent = msg;
            toast.style.opacity = '1';
            toast.style.transform = 'translate(-50%, -10px)';

            if(type === 'error') toast.classList.add('border-red-500', 'text-red-600');
            else toast.classList.remove('border-red-500', 'text-red-600');

            setTimeout(() => {
                toast.style.opacity = '0';
                toast.style.transform = 'translate(-50%, 0)';
            }, 3000);
        }

        const wait = (ms) => new Promise(res => setTimeout(res, ms));

        async function fetchWithRetry(url, options, maxRetries = 5) {
            const delays = [1000, 2000, 4000, 8000, 16000];
            for (let i = 0; i < maxRetries; i++) {
                try {
                    const response = await fetch(url, options);
                    if (response.ok) return await response.json();
                    if (response.status === 429) { await wait(delays[i]); continue; }
                    const errorJson = await response.json();
                    throw new Error(errorJson.error?.message || `HTTP ${response.status}`);
                } catch (e) {
                    if (i === maxRetries - 1) throw e;
                    await wait(delays[i]);
                }
            }
        }

        function createNewSlot(imageUrl = null) {
            const index = slots.length;
            const clone = document.getElementById('slot-template').content.cloneNode(true);
            const card = clone.querySelector('.slot-card');
            const data = {
                id: Date.now() + Math.random(),
                el: card,
                originalImg: card.querySelector('.original-img'),
                resultImg: card.querySelector('.result-img'),
                loader: card.querySelector('.slot-loader'),
                waitingOverlay: card.querySelector('.slot-waiting'),
                originalBase64: null
            };

            card.querySelector('.slot-label').textContent = `第 ${String(index + 1).padStart(2, '0')} 页`;
            card.querySelector('.process-btn').onclick = () => processSingleSlot(data);
            card.querySelector('.remove-btn').onclick = () => {
                card.remove();
                slots = slots.filter(s => s.id !== data.id);
                updateGlobalControls();
            };

            if (imageUrl) {
                data.originalBase64 = imageUrl.split(',')[1];
                data.originalImg.src = imageUrl;
                card.querySelector('.placeholder').classList.add('hidden');
            }

            slots.push(data);
            slotsContainer.appendChild(card);
            updateGlobalControls();
            return data;
        }

        function updateGlobalControls() {
            const hasProcessable = slots.some(s => s.originalBase64 && !s.resultImg.src.startsWith('data'));
            const hasResults = slots.some(s => s.resultImg.src.startsWith('data:image'));
            processAllBtn.classList.toggle('hidden', !hasProcessable);
            resultExportGroup.classList.toggle('hidden', !hasResults);
        }

        slotZoomRange.oninput = () => slotsContainer.style.setProperty('--slot-width', `${slotZoomRange.value}px`);
        pdfZoomRange.oninput = () => pdfPagesList.style.setProperty('--pdf-page-width', `${pdfZoomRange.value}px`);

        document.getElementById('pdf-drop-zone').onclick = (e) => {
            if(!e.target.closest('#pdf-preview-container')) document.getElementById('pdf-file-input').click();
        };

        document.getElementById('pdf-file-input').onchange = (e) => {
            const file = e.target.files[0];
            if(file) processPdf(file);
        };

        async function processPdf(file) {
            showToast('正在智能加载 PDF...');
            currentPdfPageUrls = [];
            pdfPagesList.innerHTML = '';
            pdfPreviewContainer.classList.remove('hidden');
            pdfControls.classList.remove('hidden');
            document.getElementById('pdf-empty-state').classList.add('hidden');

            try {
                const arrayBuffer = await file.arrayBuffer();
                const pdf = await pdfjsLib.getDocument({ data: arrayBuffer }).promise;
                document.getElementById('page-count-tag').textContent = `${pdf.numPages} 页`;

                for (let i = 1; i <= pdf.numPages; i++) {
                    const page = await pdf.getPage(i);
                    const viewport = page.getViewport({ scale: 2 });
                    const canvas = document.createElement('canvas');
                    const ctx = canvas.getContext('2d');
                    canvas.height = viewport.height; canvas.width = viewport.width;
                    await page.render({ canvasContext: ctx, viewport }).promise;
                    const dataUrl = canvas.toDataURL('image/png');
                    const pageId = `pdf_p_${i}_${Date.now()}`;

                    const pageData = { id: pageId, url: dataUrl, localParagraphMode: false };
                    currentPdfPageUrls.push(pageData);

                    const div = document.createElement('div');
                    div.className = 'page-card rounded-xl shadow-sm relative group overflow-hidden';
                    div.setAttribute('data-page-id', pageId);
                    div.innerHTML = `
                        <div class="para-badge">段落模式</div>
                        <div class="absolute inset-0 bg-black/40 opacity-0 group-hover:opacity-100 transition-opacity flex flex-col items-center justify-center gap-3">
                            <div class="flex items-center gap-2 bg-white/20 backdrop-blur-md px-3 py-1.5 rounded-full border border-white/30">
                                <input type="checkbox" class="local-para-check w-4 h-4 rounded text-blue-500">
                                <span class="text-white text-[10px] font-black uppercase">段落优化</span>
                            </div>
                            导入去文字区
                        </div>
                    `;

                    const chk = div.querySelector('.local-para-check');
                    chk.onchange = (e) => {
                        pageData.localParagraphMode = e.target.checked;
                        div.classList.toggle('para-active', e.target.checked);
                    };
                    div.querySelector('.add-btn').onclick = () => {
                        createNewSlot(dataUrl);
                        showToast('已加入工作台');
                    };
                    pdfPagesList.appendChild(div);
                }
            } catch (err) { showToast('PDF 识别失败', 'error'); }
        }

        document.getElementById('pdf-to-pptx-btn').onclick = async () => {
            if (currentPdfPageUrls.length === 0) return;
            const btn = document.getElementById('pdf-to-pptx-btn');
            const txt = document.getElementById('pptx-btn-text');
            const ldr = document.getElementById('pptx-loader');
            const projectName = document.getElementById('pdf-export-name').value;

            const precision = document.getElementById('pdf-ocr-precision-check').checked;
            const globalPara = document.getElementById('pdf-ocr-paragraph-check').checked;
            const nlmMode = document.getElementById('pdf-ocr-notebooklm-check').checked;

            btn.disabled = true; ldr.classList.remove('hidden');

            try {
                const pptx = new PptxGenJS();
                pptx.layout = 'LAYOUT_WIDE';

                for (let i = 0; i < currentPdfPageUrls.length; i++) {
                    const page = currentPdfPageUrls[i];
                    txt.textContent = `识别进度 ${i+1}/${currentPdfPageUrls.length}`;
                    const blocks = await callAiOcr(page.url.split(',')[1], precision, globalPara || page.localParagraphMode, nlmMode);

                    const slide = pptx.addSlide();
                    blocks.forEach(b => {
                        let [ymin, xmin, ymax, xmax] = b.box_2d;
                        if (ymax <= 1) { ymin *= 1000; xmin *= 1000; ymax *= 1000; xmax *= 1000; }
                        slide.addText(b.text, {
                            x: `${(xmin/10).toFixed(2)}%`, y: `${(ymin/10).toFixed(2)}%`,
                            w: `${((xmax-xmin)/10).toFixed(2)}%`, h: `${((ymax-ymin)/10).toFixed(2)}%`,
                            fontSize: b.font_size || 11, color: b.color?.replace('#','') || '000000',
                            bold: b.is_bold || false, align: b.align || 'left', valign: 'middle'
                        });
                    });
                    await wait(1800); // Rate limit guard
                }
                pptx.writeFile({ fileName: `${projectName}.pptx` });
                showToast('文字还原 PPTX 已完成下载');
            } catch (e) { showToast(`处理失败: ${e.message}`, 'error'); }
            finally { btn.disabled = false; ldr.classList.add('hidden'); txt.textContent = '视觉还原 PPTX'; }
        };

        async function callAiOcr(base64, precision, paragraph, nlm) {
            let prompt = "识别此图片中的文字。输出 JSON 数组，包含对象：{text, box_2d [ymin, xmin, ymax, xmax], font_size, is_bold, align, color}。坐标使用 0-1000 的标准值。";
            if (nlm) prompt += " 来源：NotebookLM 摘要。识别主标题和双栏布局。如果右下角存在 'NOTEBOOKLM' 水印，请务必精确标出。";
            if (precision) prompt += " 模式：逐行扫描以获得最大密度。";
            if (paragraph) prompt += " 模式：将相关的文本段落归类。";

            const payload = {
                contents: [{ parts: [{ text: prompt }, { inlineData: { mimeType: "image/png", data: base64 } }] }],
                generationConfig: {
                    responseMimeType: "application/json",
                    responseSchema: {
                        type: "ARRAY",
                        items: {
                            type: "OBJECT",
                            properties: {
                                text: { type: "STRING" },
                                box_2d: { type: "ARRAY", items: { type: "NUMBER" } },
                                font_size: { type: "NUMBER" },
                                is_bold: { type: "BOOLEAN" },
                                align: { type: "STRING" },
                                color: { type: "STRING" }
                            },
                            required: ["text", "box_2d"]
                        }
                    }
                }
            };

            const result = await fetchWithRetry(`https://generativelanguage.googleapis.com/v1beta/models/${MODEL_OCR}:generateContent?key=${apiKey}`, {
                method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify(payload)
            });
            const text = result.candidates?.[0]?.content?.parts?.[0]?.text;
            return text ? JSON.parse(text) : [];
        }

        async function processSingleSlot(s) {
            if (!s.originalBase64 || s.resultImg.src.startsWith('data')) return;
            s.loader.classList.remove('hidden');
            try {
                const prompt = "请将此图片重建为干净的背景模板。删除所有文字和前景 UI 元素，用背景纹理自然填充这些区域。保持演示文稿幻灯片的专业风格。";
                const payload = {
                    contents: [{ parts: [{ text: prompt }, { inlineData: { mimeType: "image/png", data: s.originalBase64 } }] }],
                    generationConfig: { responseModalities: ['IMAGE'] }
                };
                const response = await fetchWithRetry(`https://generativelanguage.googleapis.com/v1beta/models/${MODEL_IMAGE}:generateContent?key=${apiKey}`, {
                    method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify(payload)
                });
                const b64 = response.candidates?.[0]?.content?.parts?.find(p => p.inlineData)?.inlineData?.data;
                if (b64) {
                    s.resultImg.src = `data:image/png;base64,${b64}`;
                    s.resultImg.classList.remove('hidden');
                    s.el.querySelector('.placeholder').classList.add('hidden');
                    const dBtn = s.el.querySelector('.download-btn');
                    dBtn.disabled = false;
                    dBtn.onclick = () => {
                        const a = document.createElement('a'); a.href = s.resultImg.src; a.download = `背景图_${Date.now()}.png`; a.click();
                    };
                }
            } catch (e) { showToast('背景处理失败', 'error'); }
            finally { s.loader.classList.add('hidden'); updateGlobalControls(); }
        }

        processAllBtn.onclick = async () => {
            const pending = slots.filter(s => s.originalBase64 && !s.resultImg.src.startsWith('data'));
            showToast(`启动批量去文字 (${pending.length} 张)...`);
            pending.forEach(s => s.waitingOverlay.classList.remove('hidden'));
            for (const s of pending) {
                s.waitingOverlay.classList.add('hidden');
                await processSingleSlot(s);
                await wait(2000);
            }
            showToast('批量去文字任务完成');
        };

        document.getElementById('export-results-pptx-btn').onclick = () => {
            const results = slots.filter(s => s.resultImg.src.startsWith('data:image'));
            if (results.length === 0) return;
            const pptx = new PptxGenJS();
            pptx.layout = 'LAYOUT_WIDE';
            results.forEach(s => {
                pptx.addSlide().addImage({ data: s.resultImg.src, x: 0, y: 0, w: '100%', h: '100%' });
            });
            pptx.writeFile({ fileName: `${document.getElementById('results-export-name').value}.pptx` });
        };

        function addLog(msg, type='info') {
            const div = document.createElement('div');
            div.className = `log-line ${type}`;
            div.textContent = `[${new Date().toLocaleTimeString()}] ${msg}`;
            pptxLogs.appendChild(div);
            pptxLogs.scrollTop = pptxLogs.scrollHeight;
        }

        document.getElementById('pptx-text-drop').onclick = () => document.getElementById('pptx-text-input').click();
        document.getElementById('pptx-bg-drop').onclick = () => document.getElementById('pptx-bg-input').click();

        document.getElementById('pptx-text-input').onchange = (e) => {
            textPptxFile = e.target.files[0];
            document.getElementById('pptx-text-name').textContent = textPptxFile ? textPptxFile.name : '尚未选择文件';
        };
        document.getElementById('pptx-bg-input').onchange = (e) => {
            bgPptxFile = e.target.files[0];
            document.getElementById('pptx-bg-name').textContent = bgPptxFile ? bgPptxFile.name : '尚未选择文件';
        };

        startMergeBtn.onclick = async () => {
            if (!textPptxFile || !bgPptxFile) return showToast('请先准备好两个 PPTX 文件', 'error');
            startMergeBtn.disabled = true;
            mergeLogContainer.classList.remove('hidden');
            pptxLogs.innerHTML = '';
            addLog('AI 结构重组程序启动...');

            try {
                const textZip = new JSZip();
                const bgZip = new JSZip();
                const textContent = await textZip.loadAsync(textPptxFile);
                const bgContent = await bgZip.loadAsync(bgPptxFile);

                const getSlideNum = (p) => parseInt(p.match(/slide(\d+)\.xml/)[1]);
                const textSlides = Object.keys(textContent.files).filter(p => p.match(/ppt\/slides\/slide\d+\.xml/)).sort((a,b) => getSlideNum(a) - getSlideNum(b));
                const bgSlides = Object.keys(bgContent.files).filter(p => p.match(/ppt\/slides\/slide\d+\.xml/)).sort((a,b) => getSlideNum(a) - getSlideNum(b));

                const parser = new DOMParser();
                const serializer = new XMLSerializer();
                const limit = Math.min(textSlides.length, bgSlides.length);

                for (let i = 0; i < limit; i++) {
                    addLog(`正在融合第 ${i+1} 页的文字图层与视觉背景...`);
                    const tXml = await textContent.file(textSlides[i]).async("string");
                    const bXml = await bgContent.file(bgSlides[i]).async("string");

                    const tDoc = parser.parseFromString(tXml, "application/xml");
                    const bDoc = parser.parseFromString(bXml, "application/xml");

                    const getSpTree = (doc) => {
                        const all = doc.getElementsByTagName("*");
                        for(let el of all) if(el.localName === 'spTree') return el;
                        return null;
                    };

                    const tTree = getSpTree(tDoc);
                    const bTree = getSpTree(bDoc);

                    if (tTree && bTree) {
                        const shapes = Array.from(tTree.childNodes);
                        shapes.forEach(node => {
                            const ln = node.localName || node.nodeName.split(':').pop();
                            if (['sp', 'grpSp', 'graphicFrame', 'pic'].includes(ln)) {
                                bTree.appendChild(bDoc.importNode(node, true));
                            }
                        });
                        bgContent.file(bgSlides[i], serializer.serializeToString(bDoc));
                    }
                }

                mergedBlob = await bgContent.generateAsync({ type: "blob" });
                addLog('融合成功！已重建完整的视觉结构。', 'success');
                downloadMergedBtn.classList.remove('hidden');
                showToast('AI 合并已完成');
            } catch (err) {
                addLog(`程序错误: ${err.message}`, 'error');
                showToast('合并失败', 'error');
            } finally {
                startMergeBtn.disabled = false;
            }
        };

        downloadMergedBtn.onclick = () => {
            if (!mergedBlob) return;
            const a = document.createElement('a');
            a.href = URL.createObjectURL(mergedBlob);
            a.download = `${document.getElementById('merge-export-name').value}.pptx`;
            a.click();
        };

        document.getElementById('master-drop-zone').onclick = () => document.getElementById('master-file-input').click();
        document.getElementById('master-file-input').onchange = (e) => {
            Array.from(e.target.files).forEach(f => {
                const r = new FileReader();
                r.onload = (ev) => createNewSlot(ev.target.result);
                r.readAsDataURL(f);
            });
        };

        document.getElementById('clear-pdf-btn').onclick = () => {
            currentPdfPageUrls = [];
            pdfPagesList.innerHTML = '';
            pdfPreviewContainer.classList.add('hidden');
            pdfControls.classList.add('hidden');
            document.getElementById('pdf-empty-state').classList.remove('hidden');
        };

        window.onload = () => {
            updateGlobalControls();
        };
    </script>
</body>
</html><!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- PDF.js Core -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.min.js"></script>
    <!-- PptxGenJS (PPTX Generation) -->
    <script src="https://cdn.jsdelivr.net/npm/pptxgenjs@3.12.0/dist/pptxgen.bundle.js"></script>
    <!-- JSZip (For PPTX Merging) -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jszip/3.10.1/jszip.min.js"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&family=Noto+Sans+SC:wght@400;700;900&display=swap');

        :root {
            --primary: #2563eb;
            --accent: #7c3aed;
            --success: #10b981;
            --bg-main: #f8fafc;
        }

        body {
            font-family: 'Inter', 'Noto Sans SC', sans-serif;
            background-color: var(--bg-main);
            color: #1e293b;
        }

        .text-size-11 { font-size: 11px !important; }

        .loader {
            border: 2px solid #f3f3f3;
            border-top: 2px solid var(--primary);
            border-radius: 50%;
            width: 16px;
            height: 16px;
            animation: spin 0.8s linear infinite;
        }
        @keyframes spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }

        .pdf-view-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(var(--pdf-page-width, 140px), 1fr));
            gap: 1rem;
        }

        .slots-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(var(--slot-width, 160px), 1fr));
            gap: 1.25rem;
        }

        .custom-scrollbar::-webkit-scrollbar { height: 6px; width: 6px; }
        .custom-scrollbar::-webkit-scrollbar-thumb { background: #cbd5e1; border-radius: 10px; }

        .page-card {
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            border: 2px solid transparent;
            background: white;
        }
        .page-card.para-active {
            border-color: var(--primary);
            box-shadow: 0 0 0 4px rgba(37, 99, 235, 0.1);
        }
        .page-card:hover { transform: translateY(-4px); box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1); }

        .para-badge {
            position: absolute;
            top: 8px;
            right: 8px;
            background: var(--primary);
            color: white;
            padding: 2px 6px;
            border-radius: 9999px;
            font-size: 9px;
            font-weight: 800;
            opacity: 0;
            transition: opacity 0.2s;
            pointer-events: none;
            z-index: 30;
        }
        .para-active .para-badge { opacity: 1; }

        .input-compact {
            border: 1px solid #e2e8f0;
            border-radius: 6px;
            padding: 4px 8px;
            outline: none;
            font-weight: 700;
            font-size: 11px;
            transition: all 0.2s;
        }
        .input-compact:focus { border-color: var(--primary); ring: 2px rgba(37, 99, 235, 0.1); }

        .log-console {
            background: #0f172a;
            color: #10b981;
            font-family: 'ui-monospace', monospace;
            font-size: 11px;
            padding: 12px;
            border-radius: 12px;
            height: 160px;
            overflow-y: auto;
        }
        .log-line { margin-bottom: 2px; border-left: 2px solid transparent; padding-left: 8px; }
        .log-line.info { border-left-color: var(--primary); }
        .log-line.success { border-left-color: var(--success); }

        .glass-panel {
            background: rgba(255, 255, 255, 0.8);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.3);
        }
    </style>
</head>
<body class="min-h-screen pb-12">

    <div class="max-w-[1500px] mx-auto px-6 py-6">
        <!-- Header -->
        <header class="mb-8 flex flex-col md:flex-row justify-between items-end gap-4">
            <div>
                <div class="flex items-center gap-3 mb-1">
                    <div class="bg-blue-600 text-white p-1.5 rounded-lg shadow-lg">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"></svg>
                    </div>
                    <h1 class="text-2xl font-black text-slate-900 tracking-tight italic">同道LAB｜NLM PDF <span class="text-blue-600">PRO V2.1</span></h1>
                </div>
                高级布局还原与视觉去文字系统
            </div>

            <div class="flex items-center gap-4">
                <div class="bg-white px-3 py-1.5 rounded-full shadow-sm border border-slate-200 flex items-center gap-2">
                    <span class="w-2 h-2 bg-emerald-500 rounded-full animate-pulse"></span>
                    <span class="font-bold text-slate-600 uppercase tracking-widest text-[10px]">系统引擎已启动</span>
                </div>
            </div>
        </header>

        <div class="grid grid-cols-1 gap-8">

            <!-- SECTION 1: PDF Analysis -->
            <section class="bg-white rounded-3xl border border-slate-200 shadow-sm overflow-hidden">
                <div class="px-6 py-4 bg-slate-50 border-b border-slate-100 flex items-center justify-between">
                    <div class="flex items-center gap-3">
                        <span class="bg-slate-900 text-white w-6 h-6 rounded-md flex items-center justify-center font-black text-xs">01</span>
                        <h2 class="font-black text-slate-800 tracking-tight">PDF 高精细识别工作区</h2>
                    </div>

                    <div id="pdf-controls" class="hidden flex items-center gap-4">
                        <div class="flex bg-slate-200/50 p-1 rounded-lg">
                            全段落模式
                            取消段落
                        </div>
                        <div class="h-4 w-px bg-slate-200"></div>
                        <div class="flex items-center gap-2">
                            <span class="text-[10px] font-black text-slate-400 uppercase">缩放</span>
                            <input type="range" id="pdf-zoom-range" min="120" max="400" value="160" class="h-1 w-20 bg-slate-200 rounded-lg appearance-none cursor-pointer accent-blue-600">
                        </div>
                        全部导入去文字
                    </div>
                </div>

                <div class="p-6">
                    <div id="pdf-drop-zone" class="border-2 border-dashed border-slate-200 rounded-2xl p-8 text-center cursor-pointer hover:border-blue-400 hover:bg-blue-50/30 transition-all group">
                        <input type="file" id="pdf-file-input" class="hidden" accept="application/pdf">
                        <div id="pdf-empty-state">
                            <div class="mb-3 flex justify-center">
                                <div class="w-12 h-12 bg-blue-100 text-blue-600 rounded-2xl flex items-center justify-center group-hover:scale-110 transition-transform">
                                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"></svg>
                                </div>
                            </div>
                            点击或拖拽 PDF 开始智能识别
                            支持多页批量处理与 NotebookLM 结构优化
                        </div>

                        <div id="pdf-preview-container" class="hidden text-left">
                            <div class="flex flex-wrap items-center justify-between gap-4 mb-6 p-4 bg-slate-50 rounded-xl border border-slate-100">
                                <div class="flex items-center gap-2">
                                    <span id="page-count-tag" class="bg-slate-900 text-white px-2 py-1 rounded font-black text-[10px] tracking-widest">0 页</span>
                                    <input type="text" id="pdf-export-name" value="还原项目" class="input-compact w-40">
                                </div>

                                <div class="flex items-center gap-3">
                                    <div class="flex items-center gap-2 bg-white px-2 py-1.5 rounded-lg border border-slate-200">
                                        <input type="checkbox" id="pdf-ocr-precision-check" class="w-4 h-4 rounded text-blue-600 focus:ring-0">
                                        <label for="pdf-ocr-precision-check" class="font-bold text-slate-600 text-[11px] cursor-pointer">逐行扫描</label>
                                    </div>
                                    <div class="flex items-center gap-2 bg-white px-2 py-1.5 rounded-lg border border-slate-200">
                                        <input type="checkbox" id="pdf-ocr-paragraph-check" class="w-4 h-4 rounded text-blue-600 focus:ring-0">
                                        <label for="pdf-ocr-paragraph-check" class="font-bold text-slate-600 text-[11px] cursor-pointer">全局段落</label>
                                    </div>
                                    <div class="flex items-center gap-2 bg-purple-50 px-2 py-1.5 rounded-lg border border-purple-100">
                                        <input type="checkbox" id="pdf-ocr-notebooklm-check" checked class="w-4 h-4 rounded text-purple-600 focus:ring-0">
                                        <label for="pdf-ocr-notebooklm-check" class="font-black text-purple-700 text-[11px] cursor-pointer">NotebookLM 结构</label>
                                    </div>

                                        <span id="pptx-btn-text">视觉还原 PPTX</span>
                                        <div id="pptx-loader" class="loader !border-white !border-t-transparent hidden"></div>

                                    重置
                                </div>
                            </div>
                            <div id="pdf-pages-list" class="pdf-view-grid custom-scrollbar"></div>
                        </div>
                    </div>
                </div>
            </section>

            <!-- SECTION 2: Image Cleansing -->
            <section class="bg-white rounded-3xl border border-slate-200 shadow-sm overflow-hidden">
                <div class="px-6 py-4 bg-slate-50 border-b border-slate-100 flex items-center justify-between">
                    <div class="flex items-center gap-3">
                        <span class="bg-blue-600 text-white w-6 h-6 rounded-md flex items-center justify-center font-black text-xs">02</span>
                        <h2 class="font-black text-slate-800 tracking-tight">图片背景去文字工作台</h2>
                    </div>

                    <div class="flex items-center gap-4">
                        <div id="result-export-group" class="hidden flex items-center gap-2">
                            <input type="text" id="results-export-name" value="纯净背景" class="input-compact w-32">
                            导出背景 PPTX
                        </div>
                        <div class="flex items-center gap-2">
                            <span class="text-[10px] font-black text-slate-400 uppercase">网格</span>
                            <input type="range" id="slot-zoom-range" min="150" max="400" value="200" class="h-1 w-20 bg-slate-200 rounded-lg appearance-none cursor-pointer accent-blue-600">
                        </div>
                        执行批量去文字
                    </div>
                </div>

                <div class="p-6">
                    <div id="master-drop-zone" class="border-2 border-dashed border-slate-100 rounded-2xl p-6 text-center cursor-pointer bg-slate-50/50 hover:bg-slate-50 transition-all mb-6">
                        <input type="file" id="master-file-input" class="hidden" accept="image/*" multiple>
                        + 导入外部图片进行处理
                    </div>
                    <div id="slots-container" class="slots-grid"></div>
                </div>
            </section>

            <!-- SECTION 3: Magic Merger -->
            <section class="bg-white rounded-3xl border border-slate-200 shadow-sm overflow-hidden">
                <div class="px-6 py-4 bg-slate-50 border-b border-slate-100 flex items-center justify-between">
                    <div class="flex items-center gap-3">
                        <span class="bg-emerald-600 text-white w-6 h-6 rounded-md flex items-center justify-center font-black text-xs">03</span>
                        <h2 class="font-black text-slate-800 tracking-tight">PPTX 内容魔法合并 (重叠还原)</h2>
                    </div>
                    <div class="flex items-center gap-2">
                        <input type="text" id="merge-export-name" value="最终演示文稿" class="input-compact w-40">
                        <span class="font-black text-emerald-600 bg-emerald-50 px-2 py-1 rounded text-[10px] uppercase tracking-wider">智能分层</span>
                    </div>
                </div>

                <div class="p-8">
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-8">
                        <div id="pptx-text-drop" class="border-2 border-dashed border-slate-200 rounded-2xl p-6 text-center cursor-pointer bg-slate-50 hover:border-blue-400 transition-all">
                            <input type="file" id="pptx-text-input" class="hidden" accept=".pptx">
                            <div class="w-10 h-10 bg-white rounded-xl shadow-sm border border-slate-100 flex items-center justify-center mx-auto mb-3">
                                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-blue-500" fill="none" viewBox="0 0 24 24" stroke="currentColor"></svg>
                            </div>
                            1. 文字源文件 (还原出的 PPTX)
                            <span id="pptx-text-name" class="text-slate-400 text-[10px] font-medium mt-2 block italic">尚未选择文件</span>
                        </div>
                        <div id="pptx-bg-drop" class="border-2 border-dashed border-slate-200 rounded-2xl p-6 text-center cursor-pointer bg-slate-50 hover:border-emerald-400 transition-all">
                            <input type="file" id="pptx-bg-input" class="hidden" accept=".pptx">
                            <div class="w-10 h-10 bg-white rounded-xl shadow-sm border border-slate-100 flex items-center justify-center mx-auto mb-3">
                                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-emerald-500" fill="none" viewBox="0 0 24 24" stroke="currentColor"></svg>
                            </div>
                            2. 背景底稿文件 (视觉模板)
                            <span id="pptx-bg-name" class="text-slate-400 text-[10px] font-medium mt-2 block italic">尚未选择文件</span>
                        </div>
                    </div>

                    <div class="flex flex-col items-center">
                        执行 AI 结构合并

                        <div id="merge-log-container" class="w-full mt-8 hidden">
                            <div class="flex items-center justify-between mb-2">
                                <span class="text-[10px] font-black text-slate-400 uppercase italic">处理日志</span>
                                立即下载结果
                            </div>
                            <div id="pptx-logs" class="log-console custom-scrollbar"></div>
                        </div>
                    </div>
                </div>
            </section>
        </div>
    </div>

    <!-- TEMPLATE: Slot Card -->
    <template id="slot-template">
        <div class="slot-card bg-white rounded-2xl p-3 flex flex-col shadow-sm border border-slate-100 group">
            <div class="flex justify-between items-center mb-2">
                <span class="font-black text-blue-600 slot-label text-[10px] italic tracking-tighter">ITEM 00</span>
                ×
            </div>
            <div class="space-y-2 flex-grow">
                <div class="aspect-[4/3] bg-slate-50 rounded-xl overflow-hidden border border-slate-100 relative shadow-inner">
                    <div class="slot-loader absolute inset-0 bg-white/90 hidden flex flex-col items-center justify-center z-20">
                        <div class="loader mb-2 !w-5 !h-5"></div>
                        <span class="font-black text-blue-600 text-[9px] uppercase tracking-widest">去文字处理中...</span>
                    </div>
                    <div class="slot-waiting absolute inset-0 bg-slate-900/10 hidden flex items-center justify-center z-10">
                        <span class="bg-slate-800 text-white text-[9px] font-black px-2 py-1 rounded-full shadow-lg uppercase tracking-tighter">排队中</span>
                    </div>
                </div>
                <div class="aspect-[4/3] bg-slate-100 rounded-xl overflow-hidden border border-dashed border-slate-200 relative flex items-center justify-center group-hover:border-blue-200 transition-all">
                    <div class="placeholder text-slate-300 font-black text-[10px] italic uppercase text-center px-4">处理完成后显示结果</div>
                </div>
            </div>
            <div class="flex gap-2 mt-3">
                去文字

                    <svg xmlns="http://www.w3.org/2000/svg" class="h-3.5 w-3.5" fill="none" viewBox="0 0 24 24" stroke="currentColor"></svg>

            </div>
        </div>
    </template>

    <div id="toast" class="fixed bottom-6 left-1/2 -translate-x-1/2 glass-panel text-slate-900 px-6 py-3 rounded-2xl shadow-2xl opacity-0 transition-all pointer-events-none z-50 font-black text-xs border border-slate-200 flex items-center gap-3">
        <span id="toast-icon"></span>
        <span id="toast-msg"></span>
    </div>

    <script>
        const apiKey = "";
        const MODEL_OCR = "gemini-2.5-flash-preview-09-2025";
        const MODEL_IMAGE = "gemini-2.5-flash-image-preview";

        pdfjsLib.GlobalWorkerOptions.workerSrc = 'https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.worker.min.js';

        const toast = document.getElementById('toast');
        const toastMsg = document.getElementById('toast-msg');
        const pdfPagesList = document.getElementById('pdf-pages-list');
        const pdfPreviewContainer = document.getElementById('pdf-preview-container');
        const pdfControls = document.getElementById('pdf-controls');
        const pdfZoomRange = document.getElementById('pdf-zoom-range');
        const slotsContainer = document.getElementById('slots-container');
        const slotZoomRange = document.getElementById('slot-zoom-range');
        const processAllBtn = document.getElementById('process-all-btn');
        const resultExportGroup = document.getElementById('result-export-group');
        const pptxLogs = document.getElementById('pptx-logs');
        const mergeLogContainer = document.getElementById('merge-log-container');
        const downloadMergedBtn = document.getElementById('download-merged-btn');
        const startMergeBtn = document.getElementById('start-merge-btn');

        let currentPdfPageUrls = [];
        let slots = [];
        let textPptxFile = null;
        let bgPptxFile = null;
        let mergedBlob = null;

        function showToast(msg, type = 'info') {
            toastMsg.textContent = msg;
            toast.style.opacity = '1';
            toast.style.transform = 'translate(-50%, -10px)';

            if(type === 'error') toast.classList.add('border-red-500', 'text-red-600');
            else toast.classList.remove('border-red-500', 'text-red-600');

            setTimeout(() => {
                toast.style.opacity = '0';
                toast.style.transform = 'translate(-50%, 0)';
            }, 3000);
        }

        const wait = (ms) => new Promise(res => setTimeout(res, ms));

        async function fetchWithRetry(url, options, maxRetries = 5) {
            const delays = [1000, 2000, 4000, 8000, 16000];
            for (let i = 0; i < maxRetries; i++) {
                try {
                    const response = await fetch(url, options);
                    if (response.ok) return await response.json();
                    if (response.status === 429) { await wait(delays[i]); continue; }
                    const errorJson = await response.json();
                    throw new Error(errorJson.error?.message || `HTTP ${response.status}`);
                } catch (e) {
                    if (i === maxRetries - 1) throw e;
                    await wait(delays[i]);
                }
            }
        }

        function createNewSlot(imageUrl = null) {
            const index = slots.length;
            const clone = document.getElementById('slot-template').content.cloneNode(true);
            const card = clone.querySelector('.slot-card');
            const data = {
                id: Date.now() + Math.random(),
                el: card,
                originalImg: card.querySelector('.original-img'),
                resultImg: card.querySelector('.result-img'),
                loader: card.querySelector('.slot-loader'),
                waitingOverlay: card.querySelector('.slot-waiting'),
                originalBase64: null
            };

            card.querySelector('.slot-label').textContent = `第 ${String(index + 1).padStart(2, '0')} 页`;
            card.querySelector('.process-btn').onclick = () => processSingleSlot(data);
            card.querySelector('.remove-btn').onclick = () => {
                card.remove();
                slots = slots.filter(s => s.id !== data.id);
                updateGlobalControls();
            };

            if (imageUrl) {
                data.originalBase64 = imageUrl.split(',')[1];
                data.originalImg.src = imageUrl;
                card.querySelector('.placeholder').classList.add('hidden');
            }

            slots.push(data);
            slotsContainer.appendChild(card);
            updateGlobalControls();
            return data;
        }

        function updateGlobalControls() {
            const hasProcessable = slots.some(s => s.originalBase64 && !s.resultImg.src.startsWith('data'));
            const hasResults = slots.some(s => s.resultImg.src.startsWith('data:image'));
            processAllBtn.classList.toggle('hidden', !hasProcessable);
            resultExportGroup.classList.toggle('hidden', !hasResults);
        }

        slotZoomRange.oninput = () => slotsContainer.style.setProperty('--slot-width', `${slotZoomRange.value}px`);
        pdfZoomRange.oninput = () => pdfPagesList.style.setProperty('--pdf-page-width', `${pdfZoomRange.value}px`);

        document.getElementById('pdf-drop-zone').onclick = (e) => {
            if(!e.target.closest('#pdf-preview-container')) document.getElementById('pdf-file-input').click();
        };

        document.getElementById('pdf-file-input').onchange = (e) => {
            const file = e.target.files[0];
            if(file) processPdf(file);
        };

        async function processPdf(file) {
            showToast('正在智能加载 PDF...');
            currentPdfPageUrls = [];
            pdfPagesList.innerHTML = '';
            pdfPreviewContainer.classList.remove('hidden');
            pdfControls.classList.remove('hidden');
            document.getElementById('pdf-empty-state').classList.add('hidden');

            try {
                const arrayBuffer = await file.arrayBuffer();
                const pdf = await pdfjsLib.getDocument({ data: arrayBuffer }).promise;
                document.getElementById('page-count-tag').textContent = `${pdf.numPages} 页`;

                for (let i = 1; i <= pdf.numPages; i++) {
                    const page = await pdf.getPage(i);
                    const viewport = page.getViewport({ scale: 2 });
                    const canvas = document.createElement('canvas');
                    const ctx = canvas.getContext('2d');
                    canvas.height = viewport.height; canvas.width = viewport.width;
                    await page.render({ canvasContext: ctx, viewport }).promise;
                    const dataUrl = canvas.toDataURL('image/png');
                    const pageId = `pdf_p_${i}_${Date.now()}`;

                    const pageData = { id: pageId, url: dataUrl, localParagraphMode: false };
                    currentPdfPageUrls.push(pageData);

                    const div = document.createElement('div');
                    div.className = 'page-card rounded-xl shadow-sm relative group overflow-hidden';
                    div.setAttribute('data-page-id', pageId);
                    div.innerHTML = `
                        <div class="para-badge">段落模式</div>
                        <div class="absolute inset-0 bg-black/40 opacity-0 group-hover:opacity-100 transition-opacity flex flex-col items-center justify-center gap-3">
                            <div class="flex items-center gap-2 bg-white/20 backdrop-blur-md px-3 py-1.5 rounded-full border border-white/30">
                                <input type="checkbox" class="local-para-check w-4 h-4 rounded text-blue-500">
                                <span class="text-white text-[10px] font-black uppercase">段落优化</span>
                            </div>
                            导入去文字区
                        </div>
                    `;

                    const chk = div.querySelector('.local-para-check');
                    chk.onchange = (e) => {
                        pageData.localParagraphMode = e.target.checked;
                        div.classList.toggle('para-active', e.target.checked);
                    };
                    div.querySelector('.add-btn').onclick = () => {
                        createNewSlot(dataUrl);
                        showToast('已加入工作台');
                    };
                    pdfPagesList.appendChild(div);
                }
            } catch (err) { showToast('PDF 识别失败', 'error'); }
        }

        document.getElementById('pdf-to-pptx-btn').onclick = async () => {
            if (currentPdfPageUrls.length === 0) return;
            const btn = document.getElementById('pdf-to-pptx-btn');
            const txt = document.getElementById('pptx-btn-text');
            const ldr = document.getElementById('pptx-loader');
            const projectName = document.getElementById('pdf-export-name').value;

            const precision = document.getElementById('pdf-ocr-precision-check').checked;
            const globalPara = document.getElementById('pdf-ocr-paragraph-check').checked;
            const nlmMode = document.getElementById('pdf-ocr-notebooklm-check').checked;

            btn.disabled = true; ldr.classList.remove('hidden');

            try {
                const pptx = new PptxGenJS();
                pptx.layout = 'LAYOUT_WIDE';

                for (let i = 0; i < currentPdfPageUrls.length; i++) {
                    const page = currentPdfPageUrls[i];
                    txt.textContent = `识别进度 ${i+1}/${currentPdfPageUrls.length}`;
                    const blocks = await callAiOcr(page.url.split(',')[1], precision, globalPara || page.localParagraphMode, nlmMode);

                    const slide = pptx.addSlide();
                    blocks.forEach(b => {
                        let [ymin, xmin, ymax, xmax] = b.box_2d;
                        if (ymax <= 1) { ymin *= 1000; xmin *= 1000; ymax *= 1000; xmax *= 1000; }
                        slide.addText(b.text, {
                            x: `${(xmin/10).toFixed(2)}%`, y: `${(ymin/10).toFixed(2)}%`,
                            w: `${((xmax-xmin)/10).toFixed(2)}%`, h: `${((ymax-ymin)/10).toFixed(2)}%`,
                            fontSize: b.font_size || 11, color: b.color?.replace('#','') || '000000',
                            bold: b.is_bold || false, align: b.align || 'left', valign: 'middle'
                        });
                    });
                    await wait(1800); // Rate limit guard
                }
                pptx.writeFile({ fileName: `${projectName}.pptx` });
                showToast('文字还原 PPTX 已完成下载');
            } catch (e) { showToast(`处理失败: ${e.message}`, 'error'); }
            finally { btn.disabled = false; ldr.classList.add('hidden'); txt.textContent = '视觉还原 PPTX'; }
        };

        async function callAiOcr(base64, precision, paragraph, nlm) {
            let prompt = "识别此图片中的文字。输出 JSON 数组，包含对象：{text, box_2d [ymin, xmin, ymax, xmax], font_size, is_bold, align, color}。坐标使用 0-1000 的标准值。";
            if (nlm) prompt += " 来源：NotebookLM 摘要。识别主标题和双栏布局。如果右下角存在 'NOTEBOOKLM' 水印，请务必精确标出。";
            if (precision) prompt += " 模式：逐行扫描以获得最大密度。";
            if (paragraph) prompt += " 模式：将相关的文本段落归类。";

            const payload = {
                contents: [{ parts: [{ text: prompt }, { inlineData: { mimeType: "image/png", data: base64 } }] }],
                generationConfig: {
                    responseMimeType: "application/json",
                    responseSchema: {
                        type: "ARRAY",
                        items: {
                            type: "OBJECT",
                            properties: {
                                text: { type: "STRING" },
                                box_2d: { type: "ARRAY", items: { type: "NUMBER" } },
                                font_size: { type: "NUMBER" },
                                is_bold: { type: "BOOLEAN" },
                                align: { type: "STRING" },
                                color: { type: "STRING" }
                            },
                            required: ["text", "box_2d"]
                        }
                    }
                }
            };

            const result = await fetchWithRetry(`https://generativelanguage.googleapis.com/v1beta/models/${MODEL_OCR}:generateContent?key=${apiKey}`, {
                method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify(payload)
            });
            const text = result.candidates?.[0]?.content?.parts?.[0]?.text;
            return text ? JSON.parse(text) : [];
        }

        async function processSingleSlot(s) {
            if (!s.originalBase64 || s.resultImg.src.startsWith('data')) return;
            s.loader.classList.remove('hidden');
            try {
                const prompt = "请将此图片重建为干净的背景模板。删除所有文字和前景 UI 元素，用背景纹理自然填充这些区域。保持演示文稿幻灯片的专业风格。";
                const payload = {
                    contents: [{ parts: [{ text: prompt }, { inlineData: { mimeType: "image/png", data: s.originalBase64 } }] }],
                    generationConfig: { responseModalities: ['IMAGE'] }
                };
                const response = await fetchWithRetry(`https://generativelanguage.googleapis.com/v1beta/models/${MODEL_IMAGE}:generateContent?key=${apiKey}`, {
                    method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify(payload)
                });
                const b64 = response.candidates?.[0]?.content?.parts?.find(p => p.inlineData)?.inlineData?.data;
                if (b64) {
                    s.resultImg.src = `data:image/png;base64,${b64}`;
                    s.resultImg.classList.remove('hidden');
                    s.el.querySelector('.placeholder').classList.add('hidden');
                    const dBtn = s.el.querySelector('.download-btn');
                    dBtn.disabled = false;
                    dBtn.onclick = () => {
                        const a = document.createElement('a'); a.href = s.resultImg.src; a.download = `背景图_${Date.now()}.png`; a.click();
                    };
                }
            } catch (e) { showToast('背景处理失败', 'error'); }
            finally { s.loader.classList.add('hidden'); updateGlobalControls(); }
        }

        processAllBtn.onclick = async () => {
            const pending = slots.filter(s => s.originalBase64 && !s.resultImg.src.startsWith('data'));
            showToast(`启动批量去文字 (${pending.length} 张)...`);
            pending.forEach(s => s.waitingOverlay.classList.remove('hidden'));
            for (const s of pending) {
                s.waitingOverlay.classList.add('hidden');
                await processSingleSlot(s);
                await wait(2000);
            }
            showToast('批量去文字任务完成');
        };

        document.getElementById('export-results-pptx-btn').onclick = () => {
            const results = slots.filter(s => s.resultImg.src.startsWith('data:image'));
            if (results.length === 0) return;
            const pptx = new PptxGenJS();
            pptx.layout = 'LAYOUT_WIDE';
            results.forEach(s => {
                pptx.addSlide().addImage({ data: s.resultImg.src, x: 0, y: 0, w: '100%', h: '100%' });
            });
            pptx.writeFile({ fileName: `${document.getElementById('results-export-name').value}.pptx` });
        };

        function addLog(msg, type='info') {
            const div = document.createElement('div');
            div.className = `log-line ${type}`;
            div.textContent = `[${new Date().toLocaleTimeString()}] ${msg}`;
            pptxLogs.appendChild(div);
            pptxLogs.scrollTop = pptxLogs.scrollHeight;
        }

        document.getElementById('pptx-text-drop').onclick = () => document.getElementById('pptx-text-input').click();
        document.getElementById('pptx-bg-drop').onclick = () => document.getElementById('pptx-bg-input').click();

        document.getElementById('pptx-text-input').onchange = (e) => {
            textPptxFile = e.target.files[0];
            document.getElementById('pptx-text-name').textContent = textPptxFile ? textPptxFile.name : '尚未选择文件';
        };
        document.getElementById('pptx-bg-input').onchange = (e) => {
            bgPptxFile = e.target.files[0];
            document.getElementById('pptx-bg-name').textContent = bgPptxFile ? bgPptxFile.name : '尚未选择文件';
        };

        startMergeBtn.onclick = async () => {
            if (!textPptxFile || !bgPptxFile) return showToast('请先准备好两个 PPTX 文件', 'error');
            startMergeBtn.disabled = true;
            mergeLogContainer.classList.remove('hidden');
            pptxLogs.innerHTML = '';
            addLog('AI 结构重组程序启动...');

            try {
                const textZip = new JSZip();
                const bgZip = new JSZip();
                const textContent = await textZip.loadAsync(textPptxFile);
                const bgContent = await bgZip.loadAsync(bgPptxFile);

                const getSlideNum = (p) => parseInt(p.match(/slide(\d+)\.xml/)[1]);
                const textSlides = Object.keys(textContent.files).filter(p => p.match(/ppt\/slides\/slide\d+\.xml/)).sort((a,b) => getSlideNum(a) - getSlideNum(b));
                const bgSlides = Object.keys(bgContent.files).filter(p => p.match(/ppt\/slides\/slide\d+\.xml/)).sort((a,b) => getSlideNum(a) - getSlideNum(b));

                const parser = new DOMParser();
                const serializer = new XMLSerializer();
                const limit = Math.min(textSlides.length, bgSlides.length);

                for (let i = 0; i < limit; i++) {
                    addLog(`正在融合第 ${i+1} 页的文字图层与视觉背景...`);
                    const tXml = await textContent.file(textSlides[i]).async("string");
                    const bXml = await bgContent.file(bgSlides[i]).async("string");

                    const tDoc = parser.parseFromString(tXml, "application/xml");
                    const bDoc = parser.parseFromString(bXml, "application/xml");

                    const getSpTree = (doc) => {
                        const all = doc.getElementsByTagName("*");
                        for(let el of all) if(el.localName === 'spTree') return el;
                        return null;
                    };

                    const tTree = getSpTree(tDoc);
                    const bTree = getSpTree(bDoc);

                    if (tTree && bTree) {
                        const shapes = Array.from(tTree.childNodes);
                        shapes.forEach(node => {
                            const ln = node.localName || node.nodeName.split(':').pop();
                            if (['sp', 'grpSp', 'graphicFrame', 'pic'].includes(ln)) {
                                bTree.appendChild(bDoc.importNode(node, true));
                            }
                        });
                        bgContent.file(bgSlides[i], serializer.serializeToString(bDoc));
                    }
                }

                mergedBlob = await bgContent.generateAsync({ type: "blob" });
                addLog('融合成功！已重建完整的视觉结构。', 'success');
                downloadMergedBtn.classList.remove('hidden');
                showToast('AI 合并已完成');
            } catch (err) {
                addLog(`程序错误: ${err.message}`, 'error');
                showToast('合并失败', 'error');
            } finally {
                startMergeBtn.disabled = false;
            }
        };

        downloadMergedBtn.onclick = () => {
            if (!mergedBlob) return;
            const a = document.createElement('a');
            a.href = URL.createObjectURL(mergedBlob);
            a.download = `${document.getElementById('merge-export-name').value}.pptx`;
            a.click();
        };

        document.getElementById('master-drop-zone').onclick = () => document.getElementById('master-file-input').click();
        document.getElementById('master-file-input').onchange = (e) => {
            Array.from(e.target.files).forEach(f => {
                const r = new FileReader();
                r.onload = (ev) => createNewSlot(ev.target.result);
                r.readAsDataURL(f);
            });
        };

        document.getElementById('clear-pdf-btn').onclick = () => {
            currentPdfPageUrls = [];
            pdfPagesList.innerHTML = '';
            pdfPreviewContainer.classList.add('hidden');
            pdfControls.classList.add('hidden');
            document.getElementById('pdf-empty-state').classList.remove('hidden');
        };

        window.onload = () => {
            updateGlobalControls();
        };
    </script>
</body>
</html>
```

# 图片切分

https://ai.studio/apps/drive/13-IeS6XUr8zmIJr-boBnKyL4Admk0Ejb?fullscreenApplet=true

---
> [!info]- 🧭 导航
> ⬆️ 上级：[AI使用手册](01-AI使用手册.md)
