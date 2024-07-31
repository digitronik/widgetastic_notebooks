# Widgetastic Jupyter Notebooks

### Install some requirnments
```
python3 -m venv .env
source .env/bin/activate.fish
pip install -r requirements.txt
```

### Selenium Container
```
podman run -d --expose 4444 --expose 5999 -p 4444:4444 -p 5999:5999 -v $PWD:/wt:Z quay.io/redhatqe/selenium-standalone
```
For vnc access: `vncviewer localhost:5999`
You can access testing page with `file:///wt/test_page.html`
