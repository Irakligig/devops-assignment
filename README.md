# DevOps Assignment

## Live Application
🔗 https://devops-assignment.onrender.com

## Pipeline Description
Every push to main triggers GitHub Actions which installs dependencies and runs Jest tests. If tests fail the pipeline stops and nothing is deployed. If tests pass, a deploy hook triggers Render to pull the latest code and restart the server automatically.

## Update Strategy
Rolling Update — Render's default. The new container is built and health-checked before replacing the old one. No downtime on successful deploys. If the new container fails, Render aborts and keeps the old version live.

## Rollback Guide
1. Go to Render dashboard → your service → Events tab
2. Find the last successful deploy
3. Click "Rollback to this deploy"
4. Render immediately redeploys that version
