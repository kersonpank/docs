---
sidebar_label: "Docker Easy Install"
title: "Docker Easy Install"
sidebar_position: 1
---


This section provides guidance on setting Woofed CRM Community Easy install self-hosted edition.

1. Create a volume to store your data:
```bash
docker volume create woofedcrm_data
```

2. Run the Woofed CRM container:
```bash
docker run -it --rm --name woofedcrm -p 3001:3001 -v woofedcrm_data:/app/storage douglara/woofedcrm:easy-install-latest
```

🎉 Done! Your Woofed CRM is up and running!

Access it at: http://localhost:3001