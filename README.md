Proyecto académico desarrollado para la Electiva de Machine Learning,
Ingeniería de Sistemas — USTA Tunja.

## Descripción
Chatbot conversacional en español basado en RAG (Retrieval-Augmented Generation)
para la organización Latinoamérica Comparte. El sistema responde preguntas sobre
sus programas (Comparte Academia, Liderazgo y Talento) combinando recuperación
semántica con generación de lenguaje natural.

## Stack técnico
- **Embeddings:** paraphrase-multilingual-MiniLM-L12-v2 (Sentence Transformers)
- **Búsqueda semántica:** FAISS (IndexFlatIP, búsqueda por similitud coseno)
- **LLM:** Qwen 2.5 0.5B Instruct (Hugging Face Transformers)
- **Interfaz:** Gradio (chat con historial, intent detectado y score de confianza)

## Características
- Pipeline RAG completo: limpieza de texto → embeddings → FAISS → prompt → generación
- Umbral de confianza configurable con mensaje de fallback
- Corpus con 10 intents y ~80 utterances en español
- Compatible con CPU y GPU (detección automática)
