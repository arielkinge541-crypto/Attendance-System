# Attendance System — Real-time attendance system with facial recognition check-in, dashboard, and member enrollment.

Demo only: sample roster, all face processing runs in the browser on-device, no face data is saved or sent anywhere. Open `index.html` in a browser to use it.

## Links (live)

- GitHub repo: https://github.com/arielkinge541-crypto/Attendance-System
- GitHub Pages: https://arielkinge541-crypto.github.io/Attendance-System/
- Dashboard (direct): https://arielkinge541-crypto.github.io/Attendance-System/attendance-system-mockup.html

## Run it as a website on your own server (Docker)

```bash
docker compose up -d --build
# open http://YOUR-SERVER:8080/
```

## Py AutoDeploy — auto-deploy on every push

On the server, inside the cloned repo folder:

```bash
# One-time deploy (pull + rebuild + restart)
python3 deploy.py

# Watch mode — checks for new pushes every 60s and redeploys by itself
python3 deploy.py --watch

# Webhook mode — GitLab/GitHub calls this on push (instant deploy)
python3 deploy.py --webhook --port 9000
# then set the repo webhook to http://YOUR-SERVER:9000/deploy
```

## GitLab

`.gitlab-ci.yml` is included: on every push to the default branch it builds
the Docker image, publishes the site to GitLab Pages (free link), and — if you
set the `DEPLOY_WEBHOOK_URL` variable in GitLab Settings > CI/CD > Variables —
tells your server to auto-deploy via Py AutoDeploy.
