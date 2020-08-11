# CGM One Monitor API

## Setup

Clone repo

```bash
cd ~  # Go to home
git clone https://github.com/cgm-lab/cgm-one-monitor-api.git ./cgm-one-monitor-api
```

Install `requirements.txt`

```bash
cd cgm-one-monitor-api
pip install -r requirements.txt
```

## Run

```bash
uvicorn app:app --host 0.0.0.0 --port 9999
```

or

```bash
python app.py
```

## Service

- Linux
  - Copy file from `service/cgm-one-monitor-api.service` to `/etc/systemd/system/cgm-one-monitor-api.service`
  - Modify user name
  - ufw firewall `sudo ufw allow proto tcp from 140.118.0.0/16 to any port 9999`
  - <https://askubuntu.com/a/919059>
- Windows
  - Disable `Quick Edit mode` in CMD
  - Copy file from `service/cgm_one_monitor_api.bat` to path `[D|C]:\Users\{User}\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup` or `shell:common startup`
  - <https://stackoverflow.com/questions/21218346/run-batch-file-on-start-up>
