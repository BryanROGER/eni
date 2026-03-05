FROM python:3.12

WORKDIR /app

ARG HTTP_PROXY=""
ARG HTTPS_PROXY=""

ENV HTTP_PROXY="${HTTP_PROXY}"
ENV HTTPS_PROXY="${HTTPS_PROXY}"

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY . /app/

EXPOSE 8000
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]
