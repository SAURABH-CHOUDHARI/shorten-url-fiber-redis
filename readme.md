# 🚀 Lightning-Fast URL Shortener

## 🔗 Shorten Links Instantly with Redis & Fiber

### 🚀 **Blazing Fast & Efficient**
Built with **Golang**, powered by **Redis**, and running on **Fiber**, this URL shortener ensures high-speed performance and reliability.

### 🎯 **How It Works?**
Make a **POST** request to:
```plaintext
http://ec2-52-66-240-22.ap-south-1.compute.amazonaws.com:3000/api/v1
```
with a JSON payload:
```json
{
  "url": "https://example.com",
  "short": "custom-alias"  // (optional)
}
```

### ⚡ **Key Features**
✅ **Custom Short URLs** – Choose your own alias or let the system generate one.  
✅ **Rate Limiting** – Users can make up to **10 requests per 30 minutes**.  
✅ **Auto-Expiration** – URLs expire after **24 hours** by default.  
✅ **HTTPS Enforcement** – Ensures all URLs are secure.  
✅ **Error Handling** – Prevents abuse and ensures valid links.  

### 📩 **Example Response**
```json
{
  "url": "https://example.com",
  "short": "http://yourdomain.com/custom-alias",
  "expiry": 24,
  "rate_limit": 9,
  "rate_limit_reset": 30
}
```

### 🛠 **Tech Stack**
- **Golang** (Fiber Framework)
- **Redis** (Caching & Rate Limiting)
- **UUID** (Unique Short Codes)
- **Docker** (Deployment)

### 🏗 **Setup & Run Locally**
The project includes a `docker-compose.yml` file for easy setup. Simply run:
```sh
docker-compose up --build
```



