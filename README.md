# jupyter-remote-via-ssh

## 1. First, connect to the remote server if you haven’t already.

```bash
ssh aiteam@192.168.1.1
```

## 2. Launch a Jupyter session on the remote server.

```bash
jupyter lab --port=9000 --no-browser &
```

## 3. Create an ssh tunnel between a port on our machine and the port our Jupyter session is using on the remote server.
  On our local machine:
  
```bash
ssh -N -f -L 8888:localhost:9000 aiteam@192.168.1.1 
```
