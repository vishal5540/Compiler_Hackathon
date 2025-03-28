🧠 LLVM-PIM Matrix AI Compiler

An intelligent, web-based compiler for matrix multiplication using a custom Processor-in-Memory (PIM) architecture — with dynamic LLVM IR generation, physical memory mapping, custom ISA encoding, and AI-powered optimization insights.

🚀 Features

    •	🔢 Parameterized Matrix Input – Supports dynamic M × N × P input for A×B = C
    
    •	🛠 LLVM IR Generation – Uses llvmlite to build IR dynamically
    
    •	⚙️ Custom ISA Binary Stream – Translates LLVM IR into 24-bit PIM-compatible instructions.
    
    •	🧠 AI Insights – Suggests loop optimizations, tiling, memory reuse
    
    •	⚡ Energy Prediction (XGBoost) – Estimates energy usage based on instruction pattern
    
    •	📊 Real-time Instruction Graph – Visual chart of LOAD, STORE, MUL, ADD
    
    •	🧭 Physical Memory Mapping – Simulates memory allocation for matrices
    
    •	🌐 Web Interface – Beautiful frontend with dark mode + animations

📁 Project Structure

    Compiler_Hackathon/
    
    ├── server.py                       # Flask web server (backend)
    ├──templates/
      │        └── index.html           # Interactive frontend (with Chart.js + Prism.js)
    ├── ir/
      │   └── llvm_ir_gen.py            # LLVM IR builder (llvmlite)
    ├── backend/
      │   ├── isa_encoder.py            # IR → custom ISA encoder
      │   ├── memory_map.py             # Physical memory allocator
      │   ├── optimizer_ai.py           # Heuristic AI suggestions
      │   ├── energy_predictor.py       # XGBoost-based energy predictor
      │   └── graph_data.py             # Instruction statistics for visualization
    ├── model/
           └── energy_model_advanced.pkl # Pretrained energy prediction model


🔧 Setup & Run

1. Clone & Install

        git clone https://github.com/vishal5540/Compiler_Hackathon.git
        
        cd llvm-pim-compiler
        
        pip install -r requirements.txt

3. Train AI Model

        python train_energy_model.py

4. Start the Compiler Server

        python server.py

5. Open in Browser

        http://localhost:5000

📊 AI Model (XGBoost)

The AI module analyzes the LLVM IR and predicts:

    - Estimated energy usage in mJ
    
    - Optimization strategies (e.g., loop unrolling, memory reuse)
    
    - Instruction bottlenecks

📚 Tech Stack

    •	Python + Flask
    
    •	LLVM IR (via llvmlite)
    
    •	Chart.js + Prism.js + HTML/CSS
    
    •	XGBoost + NumPy + scikit-learn
    
    •	Custom ISA encoder


🧠 Future Ideas

    •	🔁 Loop-based IR (instead of full unrolling)
    
    •	🧮 Visual matrix heatmaps
    
    •	📦 Dockerization for easy deployment
    
    •	📈 Energy-vs-size graphs over time
    
    •	🧑‍🏫 GPT-style code summarization

