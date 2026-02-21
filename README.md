services:
  - type: web
    name: auto-med-crm
    env: python
    buildCommand: "pip install -r requirements.txt"
    startCommand: "python main.py"
    envVars:
      - key: BOT_TOKEN
        sync: false
      - key: ADMIN_ID
        sync: false
