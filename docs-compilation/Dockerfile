FROM python:alpine

# Install dependencies
RUN pip install mkdocs && \
    pip install mkdocs-material


RUN mkdir /mkdocs

# Copy Host docs to container 
COPY ./src /mkdocs/

# Set current directory to mkdocs
WORKDIR /mkdocs

# Build doc
RUN mkdocs build


# docker run --name docscompiler_container
# docker run --name docscompiler_container docscompiler
# docker container cp docscompiler_container:/mkdocs/site ./
# docker container rm -f docscompiler_container
