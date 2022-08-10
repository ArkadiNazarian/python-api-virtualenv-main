# python-api-virtualenv
add py_modules to .gitignore
python -m venv py_modules \
./py_modules/scripts/activate \
python -m pip install --upgrade pip \
pip install wheel \
pip install fastapi uvicorn \
pip install typing \
md server-root \
cd server-root \
md src \
add main.py to src \
```
from fastapi import FastAPI
import uvicorn

app = FastAPI()

@app.get("/echo")
def echo(message):
    return message

if __name__ == "__main__":
    uvicorn.run("main:app", host="localhost", port=8080, reload=True)
```
python src/main.py \
PS C:\Users\user\Desktop\pythonapi-venv\server-root> uvicorn src.main:app --host localhost --port 8080 --reload \ 

if venv ==> ctrl+shift+p ==> select interpreter ==> py_modules/scripts/python.exe
if global env ==>ctrl+shift+p ==> select interpreter ==> program-files