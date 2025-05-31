FROM nvidia/cuda:12.3.2-cudnn9-runtime-ubuntu22.04
WORKDIR /root
RUN apt-get update -y && apt-get --no-install-recommends -y install python3-pip && rm -rf /var/lib/apt/lists/*
COPY infer.py jfk.flac ./
RUN pip3 install --no-cache-dir faster-whisper
CMD ["python3", "infer.py"]
