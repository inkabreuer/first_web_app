FROM arm32v7/python:3.6

WORKDIR /first_web_app/first_web_app

# By copying over requirements first, we make sure that Docker will cache
# our installed requirements rather than reinstall them on every build
COPY requirements.txt /first_web_app/first_web_app/requirements.txt
RUN pip install -r requirements.txt

# Now copy in our code, and run it
COPY . /first_web_app/first_web_app
CMD python /first_web_app/first_web_app/manage.py runserver 0.0.0.0:8000
