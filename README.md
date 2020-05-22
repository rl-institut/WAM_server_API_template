# rli_template
Template repository for creating new projects under the RLI's umbrella

## Get started

Run `sudo docker-compose up -d --build` to run the task queue and the webapp simulaneously.

Run `sudo docker-compose down` to shut the services down

## Develop while services are running

### Using [redis](https://redis.io/documentation)

You have to start redis-server
`service redis-server start`
(to stop it use `service redis-server stop`)
Move to `task_queue` and run `. setup_redis.sh` to start the celery queue with redis a message
 broker.

### Using [RabbitMQ](https://www.rabbitmq.com/getstarted.html)


### Using [flask](https://fastapi.tiangolo.com/)

In another terminal go the the root of the repo and run `python flask_run.py`

Now the flask app is available at `127.0.0.1:5001`

### Using [fastapi](https://fastapi.tiangolo.com/)

In another terminal go the the root of the repo and run `. fastapi_run.sh`

Now the flask app is available at `127.0.0.1:5001`

While docker runs :
https://vsupalov.com/rebuilding-docker-image-development/

RabbitMQ:
https://www.rabbitmq.com/getstarted.html

https://riptutorial.com/flask/example/5831/return-a-json-response-from-flask-api

https://docs.celeryproject.org/en/3.1/getting-started/first-steps-with-celery.html#application

## Docs

To build the docs simply go to the `docs` folder

    cd docs

Install the requirements

    pip install -r docs_requirements.txt

and run

    make html

The output will then be located in `docs/_build/html` and can be opened with your favorite browser

## Code linting

In this template, 3 possible linters are proposed:
- flake8 only sends warnings and error about linting (PEP8)
- pylint sends warnings and error about linting (PEP8) and also allows warning about imports order
- black sends warning but can also fix the files for you

You can perfectly use the 3 of them or subset, at your preference. Don't forget to edit `.travis.yml` if you want to desactivate the automatic testing of some linters!
