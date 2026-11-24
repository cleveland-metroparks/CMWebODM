# WebODM Local Customizations

## jQuery Upgrade

Date: 2026-11-24

Reason:
- BitSight / security finding identified jQuery 1.11.2.

Changes:
- Upgraded jQuery from 1.11.2 to 3.7.1.
- Updated app/templates/app/base.html.
- Updated jest.config.js.
- Added jquery-3.7.1.min.js.

Verification:
- jQuery.fn.jquery returns 3.7.1.
- WebODM UI loads and functions normally.

---

## Build Notes (Windows VM)

Environment:
- Windows VM
- Docker Desktop
- WSL Ubuntu

Known Issues:
- Git checkout converted Linux files to CRLF.
- Dockerfile and shell scripts required LF line endings.

Commands used:

dos2unix webodm.sh
dos2unix Dockerfile
dos2unix nodeodm/cleanup.sh

Build:

./webodm.sh rebuild

Startup:

docker compose \
  -f docker-compose.yml \
  -f docker-compose.nodeodx.yml \
  up -d

---

## NodeODX

Configuration:

docker-compose.nodeodx.yml

Status:
- NodeODX restored after rebuild.
- Port 3000 no longer externally exposed.

Expected:

3000/tcp

Not:

0.0.0.0:3000->3000/tcp
