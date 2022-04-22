FROM python
RUN apt-get update && apt-get install -y \
&& apt-get clean
WORKDIR /app
COPY api.py model1.h5 requirement.txt ./
RUN pip install --no-cache-dir -r requirement.txt
CMD uvicorn api:app --host 0.0.0.0 --port 80 --workers 6