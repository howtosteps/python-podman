# Create Image

We will use `podman build` command to build the images using `DockerFile`

```
PS C:\Users\aniru\workspace\github\python-podman> podman build -t helloworld-python -f .\DockerFile
STEP 1/6: FROM python:3
Resolved "python" as an alias (/etc/containers/registries.conf.d/000-shortnames.conf)
Trying to pull docker.io/library/python:3...
Getting image source signatures
Copying blob sha256:fa1d4c8d85a4e064e50cea74d4aa848dc5fc275aef223fcc1f21fbdb1b5dd182
Copying blob sha256:81283a9569ad5e90773f038daedd0d565810ca5935eec8f53b8bcb6a199030d6
Copying blob sha256:32de3c850997ce03b6ff4ae8fb00b34b9d7d7f9a35bfcdb8538e22cc7b77c29d
Copying blob sha256:60b38700e7fb2cdfac79b15e4c1691a80fe6b4101c7b7fea66b9e7cd64d961cf
Copying blob sha256:c796299bbbddc7aeada9539a4e7874a75fa2b6ff421f8d5ad40f227b40ab4d86
Copying blob sha256:0f67f32c26d393a2580062f2cebfde80cc4c5a5e264bbb7a32569c6c7551c1c2
Copying blob sha256:1922a20932d42b7e6dbcad420d9f77ac92bc9eed4a36497944b06abf15dc771e
Copying blob sha256:47dd72d73dba61b8cd9fcd0d657feba4ff458a3022f5e435e631af31ca63f58b
Copying blob sha256:25f882f6cd8bb7a08d03f58c8e0ea475c5cb0059801f44fdfb0dd8468075c4d8
Copying config sha256:75cc8d87cc34bdb26dfcbe6c9e4483d9b483761510b5069852f52bd8431b8012
Writing manifest to image destination
Storing signatures
STEP 2/6: ADD helloworld.py /
--> dd6bf7aa01b
STEP 3/6: RUN pip install flask
Collecting flask
  Downloading Flask-2.2.2-py3-none-any.whl (101 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 101.5/101.5 kB 1.7 MB/s eta 0:00:00
Collecting Werkzeug>=2.2.2
  Downloading Werkzeug-2.2.2-py3-none-any.whl (232 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 232.7/232.7 kB 5.0 MB/s eta 0:00:00
Collecting Jinja2>=3.0
  Downloading Jinja2-3.1.2-py3-none-any.whl (133 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 133.1/133.1 kB 8.8 MB/s eta 0:00:00
Collecting itsdangerous>=2.0
  Downloading itsdangerous-2.1.2-py3-none-any.whl (15 kB)
Collecting click>=8.0
  Downloading click-8.1.3-py3-none-any.whl (96 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 96.6/96.6 kB 9.4 MB/s eta 0:00:00
Collecting MarkupSafe>=2.0
  Downloading MarkupSafe-2.1.1.tar.gz (18 kB)
  Preparing metadata (setup.py): started
  Preparing metadata (setup.py): finished with status 'done'
Building wheels for collected packages: MarkupSafe
  Building wheel for MarkupSafe (setup.py): started
  Building wheel for MarkupSafe (setup.py): finished with status 'done'
  Created wheel for MarkupSafe: filename=MarkupSafe-2.1.1-cp311-cp311-linux_x86_64.whl size=27478 sha256=134d2c399c38a556640a79249b0fec5ac8818ff4e00a7459a2e2aeaf66402147
  Stored in directory: /root/.cache/pip/wheels/96/ee/62/407c247ad088bcb67b530ba3ac1479058c58a651bd6bf09a1f
Successfully built MarkupSafe
Installing collected packages: MarkupSafe, itsdangerous, click, Werkzeug, Jinja2, flask
Successfully installed Jinja2-3.1.2 MarkupSafe-2.1.1 Werkzeug-2.2.2 click-8.1.3 flask-2.2.2 itsdangerous-2.1.2
WARNING: Running pip as the 'root' user can result in broken permissions and conflicting behaviour with the system package manager. It is recommended to use a virtual environment instead: https://pip.pypa.io/warnings/venv
--> 5bee9c9fb08
STEP 4/6: RUN pip install flask_restful
C
```

### Check image status
```
PS C:\Users\aniru\workspace\github\python-podman> podman images
REPOSITORY                             TAG         IMAGE ID      CREATED         SIZE
localhost/helloworld-python            latest      aa9bb579340e  11 seconds ago  978 MB
docker.io/library/python               3           75cc8d87cc34  2 weeks ago     954 MB
registry.access.redhat.com/ubi8-micro  latest      655e3818c6df  2 months ago    28.5 MB
```