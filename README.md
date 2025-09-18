# Generador de mensajes de asistencia (Gemini)

Qué es
- Notebook que genera mensajes de RR. HH. para ausencias usando Google Gemini.
- La API key está ofuscada en el notebook para ejecutar sin .env (solo uso académico).

Requisitos
- Python 3.10+
- VS Code con extensiones Python y Jupyter (o Jupyter Notebook/Lab)
- Internet

Instalación
1) Clonar
```
git clone https://github.com/MatiasBoek/Proyecto_Clase_IA.git
cd Proyecto_Clase_IA
```
2) Entorno e instalación
- Windows:
```
py -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```
- macOS/Linux:
```
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Ejecución
1) Abrir el .ipynb en VS Code/Jupyter
2) Seleccionar el kernel del entorno (.venv)
3) Run All
Deberías ver: prueba “OK” de la API y un mensaje generado.

Reemplazar la API key (opcional)
- El notebook usa ENC_KEY (key ofuscada). Para cambiarla:
1) Genera cadena codificada (en una celda aparte, no la subas):
```
def encode_key(plain: str) -> str:
    import zlib, base64
    return base64.b64encode(zlib.compress(plain.encode())).decode()
print(encode_key("TU_API_KEY_REAL"))
```
2) Copia el resultado en la variable ENC_KEY del notebook.
3) Ejecuta de nuevo.

Problemas comunes
- No encuentra google-generativeai:
```
pip install -U google-generativeai
```
- 401/UNAUTHENTICATED: la key es inválida/revocada → vuelve a ofuscar una nueva key.
- 404/MODEL_NOT_FOUND: cambia el modelo a "gemini-1.5-flash-002".

Estructura
- Notebook principal: nombre_del_notebook.ipynb
- requirements.txt
- README.md

Notas de seguridad
- La ofuscación solo oculta; no protege. Usa una key con límites y revócala tras la evaluación.
