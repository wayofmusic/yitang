---
title: LIVE34 的作业，用AI写程序
node_token: SpHZwzxiaiW4kOk6mjBcxbFfnhd
source: https://www.feishu.cn/wiki/SpHZwzxiaiW4kOk6mjBcxbFfnhd
space: 一堂学习
obj_type: docx
synced: 2026-09-26 02:05
course_line: AI能力线
stage: AI业务落地
train: AI业务落地
form: 作业/练习
audience: 全员
series: AI俱乐部周三LIVE
---
# LIVE34 的作业，用AI写程序

## 先说自己的背景

学过一些BASIC C 机器语言这类， 基本上就是大学自动化专业的一些基础，想什么JAVA python没怎么深入接触 属于语法不会，逻辑略懂的选手……

## 先开搞

先用cursor ，之前被安利装了一个，直接就写我的想法，先看他吐的东西如何

我的提示词，cursor里面按ctrl+L可以弹出来。

### 提示词：

（cursor可以耗免费羊毛目前，30天试用 有邮箱就可以）

### 代码是：

文件名：

main.py

内容：
import sys

import os

from PyQt6.QtWidgets import (QApplication, QMainWindow, QPushButton,

                           QVBoxLayout, QWidget, QFileDialog, QTextEdit,

                           QProgressBar, QLabel, QComboBox)

from PyQt6.QtCore import QThread, pyqtSignal

import whisper

class TranscriptionWorker(QThread):

    progress = pyqtSignal(int)

    finished = pyqtSignal(str)

    def \_\_init\_\_(self, audio_files, model_name):

        super().\_\_init\_\_()

        self.audio_files = audio_files

        self.model_name = model_name

    def run(self):

        model = whisper.load_model(self.model_name)

        results = []

        for i, file in enumerate(self.audio_files):

            try:

                result = model.transcribe(file)

                results.append(f"文件: {os.path.basename(file)}\n{result['text']}\n\n")

                self.progress.emit(int((i + 1) / len(self.audio_files) \* 100))

            except Exception as e:

                results.append(f"文件: {os.path.basename(file)}\n转换错误: {str(e)}\n\n")

        self.finished.emit("".join(results))

class WhisperGUI(QMainWindow):

    def \_\_init\_\_(self):

        super().\_\_init\_\_()

        self.setWindowTitle("Whisper 批量语音转文字")

        self.setGeometry(100, 100, 800, 600)

        \# 主布局

        main_widget = QWidget()

        self.setCentralWidget(main_widget)

        layout = QVBoxLayout()

        main_widget.setLayout(layout)

        \# 模型选择

        self.model_combo = QComboBox()

        self.model_combo.addItems(['tiny', 'base', 'small', 'medium', 'large'])

        layout.addWidget(QLabel("选择模型:"))

        layout.addWidget(self.model_combo)

        \# 选择文件按钮

        self.select_button = QPushButton("选择音频文件")

        self.select_button.clicked.connect(self.select_files)

        layout.addWidget(self.select_button)

        \# 进度条

        self.progress_bar = QProgressBar()

        layout.addWidget(self.progress_bar)

        \# 结果显示区域

        self.result_text = QTextEdit()

        layout.addWidget(self.result_text)

        self.audio_files = []

    def select_files(self):

        files, \_ = QFileDialog.getOpenFileNames(

            self,

            "选择音频文件",

            "",

            "Audio Files (\*.mp3 \*.wav \*.m4a)"

        )

        if files:

            self.audio_files = files

            self.result_text.setText(f"已选择 {len(files)} 个文件，准备转换...")

            self.start_transcription()

    def start_transcription(self):

        self.worker = TranscriptionWorker(self.audio_files, self.model_combo.currentText())

        self.worker.progress.connect(self.update_progress)

        self.worker.finished.connect(self.show_results)

        self.worker.start()

        self.select_button.setEnabled(False)

    def update_progress(self, value):

        self.progress_bar.setValue(value)

    def show_results(self, text):

        self.result_text.setText(text)

        self.select_button.setEnabled(True)

if **name** == '\_\_main\_\_':

    app = QApplication(sys.argv)

    window = WhisperGUI()

    window.show()

    sys.exit(app.exec())

### 放到python里面去运行下看看效果，

1 下载一个python 环境，

下载python https://www.python.org/downloads/

下载稳定版本，https://www.python.org/ftp/python/3.13.0/python-3.13.0-amd64.exe

等download下来，安装好\~

2 复制进去，先试一下 看看啥反馈。

---
> [!info]- 🧭 导航
> ⬆️ 上级：[AI落地Live34·抖音业务探索+AI辅助编程入门](29-AI落地Live34·抖音业务探索+AI辅助编程入门.md)

---

<details>
<summary>原文配图上的文字（3 条，图片本身未随文提供）</summary>

**提示词**

- 在VS Code中使用Python语言开发的代码界面。左侧是代码编辑区域，显示了TranscriptionWorker、WhisperGUI等类的代码，涉及音频文件处理、模型加载、转录等功能。右侧是聊天窗口，显示了与AI助手的对话内容，如询问是否可以使用PyQt6来创建界面、使用whisper进行语音转写等。图片

**放到python里面去运行下看看效果**

- 是Python 3.13.0版本的Windows发布页面。左侧为Stable Releases部分，列出Python 3.13.0 - Oct. 7, 2024及Python 3.12.7 - Oct. 1, 2024两个版本，分别有64-bit和32-bit的Windows installer、Windows embeddable package（64-bit、32-bit、ARM64）等下载选
- 「正在接收数据...」 「隐藏详情」

</details>
