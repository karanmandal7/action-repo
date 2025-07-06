📦 Overview
This repository is used to generate GitHub webhook events (Push, Pull Request, Merge) for testing and demonstrating a GitHub Webhook Event Tracker.
It is connected to a separate webhook-repo, which receives and displays these events in real time.
🚀 How to Use

1. Clone the Repo
git clone https://github.com/yourusername/action-repo.git
cd action-repo

2. Generate Events
A. Push Event
Make a change to any file (e.g., edit README.md or create a new file).
Commit and push:
  git add .
  git commit -m "Test push event"
  git push origin main

B. Pull Request Event
Create a new branch:
  git checkout -b feature/test-pr

Make a change (e.g., add pull-test.txt):
  echo "This is a pull request test" > pull-test.txt
  git add pull-test.txt
  git commit -m "Add pull-test.txt for PR test"
  git push origin feature/test-pr

Go to GitHub and open a pull request from feature/test-pr to main.
C. Merge Event
On GitHub, merge the pull request you just created.


🔗 Webhook Connection
This repository is connected to a webhook endpoint (hosted in webhook-repo) via a GitHub webhook.
Webhook URL: (Set by the project owner, usually via ngrok/localtunnel)
Events: Push, Pull Request

📝 Notes
No special code is required in this repo for the webhook to work.
All you need to do is perform normal GitHub actions (push, PR, merge).
The webhook will automatically send event data to the connected backend.

👤 Author
Karan Mandal
