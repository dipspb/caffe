FROM bvlc/caffe:cpu

EXPOSE 8888

RUN pip install --upgrade pip && \
    pip install jupyter

COPY jupyter_notebook_config.py /

RUN mkdir -p /workspace
WORKDIR /workspace

# ENTRYPOINT ["/bin/bash", "-c"]
CMD ["jupyter", "notebook", "--config=/jupyter_notebook_config.py", "--allow-root"]

