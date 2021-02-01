## 00 Create Base Docker Image
Execute at root of project directory:
```
time docker build 00_base_setup -t base:example_setup
```
### Notes
- This command takes several minutes to complete
- `time` included at start of command to track execution time

## 01 Build Project Docker Image
Execute at root of project directory:
```
docker build . -t example_setup:latest
```

### Notes
- Using `latest` as default tag
- Can specify other tags for different local builds

## 02 Run Project
Execute at root of project directory:
```
docker run -p 8899:8888 -v $PWD:/project example_setup:latest
```
### Opening Jupyter
1. In browser, navigate to `localhost:8899`
2. A password prompt will appear. In the Terminal, you will see some links that include `token=<long string>`. Copy this token and enter it as the password.
3. You can now execute code, running notebooks in Python or R!

### Notes
- Local host port is set to `8899`. Can be changed if desired. Docker-level port (right of the colon) must be set to `8888` according to Dockerfile.
- Connects local instance of project as a volume to the docker image. Anything you do while running, will update your local files.

