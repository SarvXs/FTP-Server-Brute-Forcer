# FTP-Server-Brute-Forcer
This Python script is designed to perform a brute-force attack on an FTP server to discover valid login credentials. The script uses asynchronous operations to maximize the efficiency of the attack by trying multiple passwords concurrently.

---


✨ Features

- ⚡ Asynchronous Execution: Uses `asyncio` and `aioftp` to handle multiple login attempts concurrently
- 📊 Concurrency Control: Limits the number of simultaneous attempts to prevent overloading the target server
- 🧰 Customizable Parameters: Configure target, port, username, and wordlist as needed

---

 📦 Requirements

- Python 3.7+
- Required packages:

```bash
pip install aioftp termcolor
````

---

 🚀 Usage

```bash
python ftp-brute-forcer.py <target> -u <username> -w <wordlist> [-p <port>]
```

 🔧 Arguments

| Argument           | Description                                     |
| ------------------ | ----------------------------------------------- |
| `<target>`         | IP address or hostname of the target FTP server |
| `-u`, `--username` | Username to brute-force                         |
| `-w`, `--wordlist` | Path to password wordlist                       |
| `-p`, `--port`     | (Optional) FTP port (default is `21`)           |

---

 💡 Example

```bash
python ftp-brute-forcer.py 192.168.1.10 -u admin -w passwords.txt -p 21
```

---

 ⚙️ How It Works

1. **Input Parsing**: Gathers target, port, username, and wordlist from CLI arguments
2. **Wordlist Reading**: Loads all passwords from the given file
3. **Asynchronous Bruteforcing**: Attempts each login asynchronously for speed
4. **Concurrency Control**: Prevents overwhelming the server
5. **Result Handling**: Outputs credentials if successful or a failure message if not

---

 🎯 Output

✅ Success:

```
[21] [ftp] host: 192.168.1.10 login: admin password: password123
```

❌ Failure:

```
[-] Failed to find the correct password.
```

---

 ⚠️ Important Notes

* **Ethical Use Only**: This tool is strictly for educational and authorized penetration testing purposes.
* **Get Permission**: Use only on systems where you have **explicit written permission**.

---

 📝 License

This project is licensed under the **MIT License**.
See the [LICENSE](LICENSE) file for full details.

---

 👤 Author

Created by [Sarvesvaraan (SarvXs)](https://github.com/SarvXs)
📫 [k.s.sarvesvaraan@gmail.com](mailto:k.s.sarvesvaraan@gmail.com)
🔗 [LinkedIn](https://www.linkedin.com/in/sarvesvaraan-k-s-a06a76251)

---

