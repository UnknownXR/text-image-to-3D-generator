# 🧠 Text or Image to 3D Generator using Shap-E

This project uses OpenAI’s **Shap-E** model to generate 3D models (`.obj`, `.stl`) and GIF previews from either a **text prompt** (like `"a shark"`) or a **2D image**.

You can run it interactively on **Google Colab** using a simple **Gradio web interface**.

---

## 🚀 Features

- Input: Text or image
- Output:
  - Rotating 3D GIF preview
  - Downloadable `.obj` and `.stl` files
- Runs on Colab with GPU
- Clean UI with Gradio

---

## 📦 Requirements

All dependencies are listed in `requirements.txt`. Install with:

```bash
pip install -r requirements.txt
```

Or run directly in **Colab**, where everything installs automatically.

---

## 🛠️ Steps to Run

1. Open the Colab notebook (or run locally if you have a GPU)
2. It will:
   - Clone the [Shap-E repository](https://github.com/openai/shap-e)
   - Install required libraries
   - Load pre-trained models
3. Use the Gradio UI to:
   - Enter a text prompt OR upload an image
   - View the 3D GIF
   - Download `.obj` and `.stl` files

---

## 🧠 My Thought Process

- The task was to create a 3D generator from **text or image input**.
- I chose **OpenAI’s Shap-E** because it supports both text-to-3D and image-to-3D directly.
- I tested model loading, GIF rendering, and saving `.obj/.stl` formats using `trimesh`.
- Then I wrapped everything into a Gradio web UI that works smoothly inside Google Colab.
- Main challenges were:
  - Handling model I/O in Colab’s environment
  - Ensuring Gradio could serve files correctly using `allowed_paths`
- The final app is a lightweight demo showing how AI can bridge 2D-to-3D for design, visualization, or printing.

---

## 📂 Example Prompts

- `"a futuristic chair"`
- `"a cactus in a pot"`
- `"a robot dog"`

---

## 📎 Credits

- [OpenAI Shap-E](https://github.com/openai/shap-e)
- [Gradio](https://gradio.app)
- [Trimesh](https://trimsh.org/)

---

✅ Built as part of an internship assignment.
