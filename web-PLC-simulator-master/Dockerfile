FROM ubuntu:latest
RUN apt-get update -y
RUN echo "**** Installing Python and Java****" && \
    apt-get install -y build-essential python3.10 python3.10-dev python3-pip openjdk-17-jdk ant
WORKDIR /app
COPY webUI.py webUI.py
COPY poST2py.jar poST2py.jar
COPY translate.sh translate.sh
COPY startSim.sh startSim.sh
COPY templates/index.html templates/index.html
COPY static/jquery-linenumbers.js static/jquery-linenumbers.js
COPY static/about.png static/about.png
COPY static/clean.png static/clean.png
COPY static/object.png static/object.png
COPY static/open.png static/open.png
COPY static/pause.png static/pause.png
COPY static/pause2.png static/pause2.png
COPY static/run.png static/run.png
COPY static/save.png static/save.png
COPY static/stop.png static/stop.png
COPY static/loadinp.png static/loadinp.png
COPY static/onecycle.png static/onecycle.png
ADD sim sim
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt
EXPOSE 5000

CMD ["python3","-u","webUI.py"]
