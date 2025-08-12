## 📁 SmartCamRT – Real-Time Smart Camera Inference Optimizer

**SmartCamRT** is a real-time object detection and performance optimization engine designed for edge devices. It enables developers to easily deploy, monitor, and optimize AI models using various inference runtimes such as ONNX Runtime, TensorRT, TensorFlow Lite, and ExecuTorch. The system supports runtime switching, model compression, performance logging, and deployment to real edge platforms like Raspberry Pi or Android.

---

### 📦 Project Structure
```
smartcamrt/
├── core/
│   ├── inference/
│   │   ├── onnx_runtime.py
│   │   ├── tensorrt.py
│   │   ├── tflite.py
│   │   └── executorch.py
│   ├── models/
│   │   ├── yolov5_utils.py
│   │   └── transformer_utils.py
│   ├── optimization/
│   │   ├── quantization.py
│   │   ├── pruning.py
│   │   └── runtime_switcher.py
│   ├── monitoring/
│   │   └── logger.py
│   ├── deploy/
│   │   ├── deploy_rpi.md
│   │   └── deploy_android.md
├── assets/
│   └── sample_outputs.png
├── README.md
├── requirements.txt
└── learn_and_replicate/
    ├── milestone_checklist.md
    ├── milestone_01_onnx_runtime/
    ├── milestone_02_tensor_rt_tflite/
    ├── milestone_03_performance_logger/
    ├── milestone_04_optimizer_logic/
    ├── milestone_05_cpp_inference/
    ├── milestone_06_sequence_models/
    ├── milestone_07_executorch/
    ├── milestone_08_compression/
    └── milestone_09_edge_deployment/
```

---

### 🛠 Key Features and Tech Stack
- Plug-and-play runtime support: ONNX Runtime, TensorRT, TFLite, ExecuTorch
- Runtime selection and switching based on device load
- Quantization and pruning for model compression
- Performance profiling: latency, memory, CPU/GPU usage
- Deployable to Raspberry Pi and Android devices
- Python 3.12 with [`uv`](https://docs.astral.sh/uv/) for virtual env and dependency management
- PyTorch for training/export and model compression
- psutil, py3nvml for system monitoring
- pre-commit for code linting and hygiene

---

### 🚀 Use Cases
- Optimizing AI-powered cameras and embedded vision systems
- Benchmarking model performance across runtimes
- Researching DNN workload characteristics on edge
- Building robust real-time inference pipelines

---

### ✅ Getting Started

Create `.env` file from existing `.env.example` file. Update values in `.env`
```bash
cp .env.example .env
```

Set up a dedicated virtual environment to run the service
```bash
# install uv if you haven't already - https://docs.astral.sh/uv/getting-started/installation/
# curl -LsSf https://astral.sh/uv/install.sh | sh # macOS/Linux
# powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex" # Windows

uv python install 3.12

uv sync --extra dev
```

Activate the environment to run commands without the `uv run` prefix
```bash
source .venv/bin/activate
# .\.venv\Scripts\activate.ps1 # Windows
```

install `pre-commit` git hook scripts
```bash
pre-commit install
```

Run your first inference:
```bash
python smartcamrt/core/inference/onnx_runtime.py
```

---

### 🧠 Project Summary & Insights
For key results, benchmarks, and reflections on how this system was built and optimized, see the [Capstone Summary](./capstone_summary.md).

---

### 📘 Want to Learn and Build This Yourself?
Follow [`learn_and_replicate/`](./learn_and_replicate/), which contains:
- A milestone checklist
- Modular code-by-code progression
- Replicable steps to build this full system from scratch

Perfect for those who want to learn edge AI optimization hands-on.

---

### 📃 License
MIT License – Free to use, fork, and extend.
