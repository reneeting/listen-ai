FROM python:3.13-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 8501

CMD ["streamlit", "run", "app.py", "--server.port", "8501"]

# FROM python:3.13-slim
# WORKDIR /app
# # 故意將 COPY . . 放到 pip install 之前
# COPY . . 
# RUN pip install --no-cache-dir -r requirements.txt
# EXPOSE 8501
# CMD ["streamlit", "run", "app.py", "--server.port", "8501"]