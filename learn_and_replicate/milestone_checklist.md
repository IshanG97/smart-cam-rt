📘 SmartCamRT – Milestone Learning Checklist

This checklist guides you through building SmartCamRT from scratch. Each milestone builds on the last, helping you learn AI runtime environments, model compression, and edge deployment.

⸻

🧠 Context for LLMs / Assistants

📌 Project Description

I’m building a real-time AI inference engine called SmartCamRT that runs optimized DNN models (e.g., YOLOv5, LSTM, BERT) on edge devices using different runtimes like ONNX Runtime, TensorRT, TFLite, and ExecuTorch. It supports runtime switching, model compression, performance logging, and deployment to Raspberry Pi/Android. I’m following a milestone-based plan to gradually build and optimize each component.

🗂 Repo Layout

My project has a core/ folder for production-ready modules and a learn_and_replicate/ folder for my step-by-step development process. Each milestone builds one part of the final system (e.g., runtime wrapper, logger, optimizer, edge deployment).

🧾 Prompt Template

I’m following a milestone-based plan stored in milestone_checklist.md. Here’s the checklist: [paste it]. I’m currently working on milestone X. Can you help me with [describe your task]?

⸻

✅ Milestone 1: Run DNN Model with ONNX Runtime
	•	Convert YOLOv5 from PyTorch to ONNX.
	•	Load and run ONNX model on webcam frames using ONNX Runtime (Python).
	•	Measure inference latency per frame.
	•	Save results/logs to CSV or file.

⸻

✅ Milestone 2: Add TensorRT and TensorFlow Lite Support
	•	Convert ONNX to TensorRT engine using trtexec or API.
	•	Convert model to TFLite using TensorFlow converter.
	•	Implement runtime switch between ONNX, TensorRT, and TFLite in Python.
	•	Benchmark all runtimes on the same input.

⸻

✅ Milestone 3: Build Performance Logger
	•	Log CPU/memory usage using psutil.
	•	Log GPU usage using py3nvml or NVIDIA tools.
	•	Track per-frame latency, CPU, and memory usage.
	•	Plot performance trends with matplotlib or show CLI summary.

⸻

✅ Milestone 4: Real-Time Optimizer Logic
	•	Monitor system load (CPU/GPU).
	•	Automatically switch to lighter models/runtimes under load.
	•	Integrate fallback to YOLOv5n or similar.
	•	Stress test with simultaneous inferences.

⸻

✅ Milestone 5: C++ Inference Path
	•	Load and run model with ONNX Runtime or TensorRT C++ API.
	•	Recreate inference loop and logger in C++.
	•	Measure and compare C++ vs Python performance.
	•	Optional: Add multithreading for throughput.

⸻

✅ Milestone 6: LSTM and Transformer Models
	•	Run inference using an LSTM-based model (e.g., sentiment analysis).
	•	Run a transformer model (e.g., DistilBERT or Whisper).
	•	Compare performance of CNN, LSTM, and Transformer models.
	•	Log latency, memory, and differences in runtime behavior.

⸻

✅ Milestone 7: Integrate ExecuTorch
	•	Export a lightweight model with torch.export for ExecuTorch.
	•	Deploy or simulate on an ExecuTorch-compatible environment (e.g., Android).
	•	Run inference and measure performance.
	•	Compare ExecuTorch with other runtimes.

⸻

✅ Milestone 8: Model Compression for Edge
	•	Apply post-training quantization (ONNX/PyTorch/TFLite).
	•	Experiment with quantization-aware training if accuracy drops.
	•	Apply pruning using torch.nn.utils.prune.
	•	Compare size, speed, and accuracy before and after compression.
	•	Optional: Perform knowledge distillation from a large to small model.

⸻

✅ Milestone 9: Deploy to Edge Device
	•	Deploy ONNX/TFLite model to Raspberry Pi (Option A).
	•	Deploy PyTorch/ExecuTorch model to Android (Option B).
	•	Measure on-device latency and resource usage.
	•	Document deployment constraints and performance.

⸻

🏁 Bonus: Final Capstone Summary
	•	Write a report summarizing:
	•	Runtime and model comparisons
	•	Optimization and compression results
	•	Edge deployment insights
	•	Visuals: charts, tables, logs
	•	Move production-ready code to smartcamrt/core/
	•	Clean up experiment code in learn_and_replicate/
	•	Refer to [`capstone_summary_template.md`](./capstone_summary_template.md) for guidance

⸻

You now have a portfolio-ready, production-quality edge AI optimizer.

Happy building! 🚀