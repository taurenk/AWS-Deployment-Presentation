# AWS Deployment Options

Quick Commands:

- local: `pipenv run app.py`
- Build Docker contianer:`docker build -t taurenk/flask-example .`
- Run container: `docker run -d -p 5000:5000 taurenk/flask-example`
- Push to Docker Registry: `docker push taurenk/flask-example`

---

## Simple Flask App

Flask - Lightweight python web application framework.

```
from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello_world():
    return 'Flask Dockerized'

if __name__ == '__main__':
    app.run(debug=True,host='0.0.0.0')
```

---

## Deployment Options in AWS

We are production ready... how do we deploy?

- EC2
- ECS -> Fargate or Classic
- K8
- Docker Swarm
- Lambda

---

## EC2

Pros: quick, easy to understand
Cons: mininal alerting, no auto scaling, deploys/updates are tougher, your maintaining a virtual box.

- Launch EC2 Instance
- SSH into box
- Run commands to launch/update

---

## EC2 Cont.

![EC2](https://app.cloudcraft.co/view/59636f85-bd48-4d65-ad39-65ed80c00629?key=zk7NLuMqXFX6mFsTLhm7ww&embed=true)

---

## EC2 Terraform

```
Steps:
- terraform apply
- ssh
- install docker
- pull container
- run container
- done
```

---

## ECS

## Lambda

## EBS
