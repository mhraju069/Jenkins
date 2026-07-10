# Jenkins Installation

## Steps
1. Update package
```bash
sudo apt update
```
2. Install java (If not installed)
```bash
sudo apt install fontconfig openjdk-21-jre
java -version
```
3. Install Jenkins:
```bash
sudo wget -O /etc/apt/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2026.key

echo "deb [signed-by=/etc/apt/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt update

sudo apt install jenkins

```

4. Check status

```bash
sudo systemctl status jenkins

```

5. Start if not started

```bash
sudo systemctl restart jenkins
```

6. Enable on boot

```bash
sudo systemctl enable jenkins
```

7. Access Jenkins
```
http://localhost:8080
```

8. Get Initial Admin Password
```bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```
