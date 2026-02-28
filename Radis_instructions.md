# 1️⃣ Install Redis (macOS with Homebrew)

Update brew (optional but safe):

```bash
brew update
```

Install Redis:

```bash
brew install redis
```

Verify installation:

```bash
redis-server --version
```

If version prints → installed correctly.

---

# 2️⃣ Start Redis Server

### ✅ Recommended (run as background service)

```bash
brew services start redis
```

Check status:

```bash
brew services list
```

If it says `started` → Redis is running.

---

### 🔧 Manual Start (foreground mode)

```bash
redis-server
```

This will block your terminal.

Stop it with:

```
CTRL + C
```

---

# 3️⃣ Stop Redis

If running as service:

```bash
brew services stop redis
```

---

# 4️⃣ Test Redis Connection

Open new terminal:

```bash
redis-cli
```

Then type:

```
ping
```

If you see:

```
PONG
```

Redis is working perfectly.

Exit CLI:

```
exit
```

---

# 5️⃣ Where Redis Data Is Stored

Default path (Apple Silicon):

```
/opt/homebrew/var/db/redis
```

Intel Mac:

```
/usr/local/var/db/redis
```
