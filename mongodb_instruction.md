
# 1️⃣ Install MongoDB with Homebrew (macOS)

First update brew:

```bash
brew update
```

Install MongoDB Community Edition:

```bash
brew tap mongodb/brew
brew install mongodb-community
```

Verify installation:

```bash
mongod --version
```

If you see version info → installed correctly.

---

# 2️⃣ Start MongoDB Server

### Recommended way (as a background service)

```bash
brew services start mongodb-community
```

Check status:

```bash
brew services list
```

If it says `started` → server is running.

---

### Manual start (foreground mode)

If you don’t want it as a service:

```bash
mongod --config /opt/homebrew/etc/mongod.conf
```

⚠️ This will block your terminal.

---

# 3️⃣ Stop MongoDB

If running as service:

```bash
brew services stop mongodb-community
```

If running manually:
Press:

```
CTRL + C
```

---

# 4️⃣ Connect to MongoDB

Open new terminal:

```bash
mongosh
```

If it connects → everything works.

---

# 5️⃣ Where Data Is Stored

Default path (Apple Silicon):

```
/opt/homebrew/var/mongodb
```

Intel Macs:

```
/usr/local/var/mongodb
```
