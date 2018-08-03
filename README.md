# AdversaryAttack

In this project, I'm going to try to do an [adversary attack](https://en.wikipedia.org/wiki/Adversarial_machine_learning)
following a [video](https://www.youtube.com/watch?v=JoQx39CoXW8) from Dot CSV channel on Youtube.

For that, I'm going to use Jupyter Notebook using Docker. In this case, there is [an Docker image](http://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html) for that, named `jupyter/tensorflow-notebook`.

Run `~$ docker pull jupyter/tensorflow-notebook` to download Docker image from Docker Hub, and run:

```bash
~$ docker run -p 8888:8888 -v "$PWD":/home/jovyan/work --name adv jupyter/tensorflow-notebook
/usr/local/bin/start-notebook.sh: ignoring /usr/local/bin/start-notebook.d/*

Container must be run with group "root" to update passwd file
Executing the command: jupyter notebook
[I 12:02:53.171 NotebookApp] Writing notebook server cookie secret to /home/jovyan/.local/share/jupyter/runtime/notebook_cookie_secret
[W 12:02:53.497 NotebookApp] WARNING: The notebook server is listening on all IP addresses and not using encryption. This is not recommended.
[I 12:02:53.540 NotebookApp] JupyterLab extension loaded from /opt/conda/lib/python3.6/site-packages/jupyterlab
[I 12:02:53.540 NotebookApp] JupyterLab application directory is /opt/conda/share/jupyter/lab
[I 12:02:53.549 NotebookApp] Serving notebooks from local directory: /home/jovyan
[I 12:02:53.549 NotebookApp] The Jupyter Notebook is running at:
[I 12:02:53.549 NotebookApp] http://(81b5f41757cc or 127.0.0.1):8888/?token=c60ed8fa3c32aacb65a244d1a09b5983b1967d063c4b24bf
[I 12:02:53.549 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
[C 12:02:53.551 NotebookApp]

    Copy/paste this URL into your browser when you connect for the first time,
    to login with a token:
        http://(81b5f41757cc or 127.0.0.1):8888/?token=c60ed8fa3c32aacb65a244d1a09b5983b1967d063c4b24bf
```
