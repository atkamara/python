FROM python:3.12

WORKDIR src/usr/app

COPY . .

RUN pip install --upgrade pip

RUN pip install virtualenv \
	&& virtualenv pyenv \
	&& . pyenv/bin/activate

RUN pip install -r requirements.txt --progress-bar off

CMD ['jupyter','notebook','--ip','0.0.0.0']