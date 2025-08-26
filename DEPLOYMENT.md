# Deployment Guide

This guide will help you deploy your Cyber Hacking Breaches Prediction application to various platforms.

## 🚀 Local Development

### Prerequisites
- Python 3.9+
- MySQL Server
- Git

### Quick Start
```bash
# Clone the repository
git clone https://github.com/yourusername/cyber-hacking-prediction.git
cd cyber-hacking-prediction

# Install dependencies
pip install -r requirements.txt

# Set up database
mysql -u root -p < db.sql

# Run the application
python app.py
```

## ☁️ Cloud Deployment Options

### 1. Heroku Deployment

#### Prerequisites
- Heroku account
- Heroku CLI installed

#### Steps
```bash
# Login to Heroku
heroku login

# Create a new Heroku app
heroku create your-app-name

# Add MySQL addon (ClearDB)
heroku addons:create cleardb:ignite

# Get database URL
heroku config:get CLEARDB_DATABASE_URL

# Update app.py with the new database URL
# Set environment variables
heroku config:set FLASK_ENV=production

# Deploy
git add .
git commit -m "Deploy to Heroku"
git push heroku main

# Open the app
heroku open
```

### 2. Railway Deployment

#### Prerequisites
- Railway account
- GitHub repository

#### Steps
1. Go to [Railway.app](https://railway.app)
2. Connect your GitHub account
3. Create a new project
4. Select your repository
5. Add MySQL service
6. Deploy automatically

### 3. Render Deployment

#### Prerequisites
- Render account
- GitHub repository

#### Steps
1. Go to [Render.com](https://render.com)
2. Connect your GitHub account
3. Create a new Web Service
4. Select your repository
5. Add MySQL database service
6. Deploy

### 4. DigitalOcean App Platform

#### Prerequisites
- DigitalOcean account
- GitHub repository

#### Steps
1. Go to [DigitalOcean App Platform](https://www.digitalocean.com/products/app-platform)
2. Connect your GitHub account
3. Create a new app
4. Select your repository
5. Add MySQL database
6. Deploy

## 🐳 Docker Deployment

### Local Docker
```bash
# Build and run with Docker Compose
docker-compose up --build

# Or build and run manually
docker build -t cyber-hacking-app .
docker run -p 5000:5000 cyber-hacking-app
```

### Docker Hub
```bash
# Build image
docker build -t yourusername/cyber-hacking-app .

# Push to Docker Hub
docker push yourusername/cyber-hacking-app

# Pull and run on any machine
docker pull yourusername/cyber-hacking-app
docker run -p 5000:5000 yourusername/cyber-hacking-app
```

## 🌐 Production Considerations

### Environment Variables
```bash
# Set these in production
export FLASK_ENV=production
export FLASK_DEBUG=False
export MYSQL_HOST=your-db-host
export MYSQL_USER=your-db-user
export MYSQL_PASSWORD=your-db-password
export MYSQL_DATABASE=cyber1
```

### Security
- Use HTTPS in production
- Set strong database passwords
- Enable firewall rules
- Regular security updates

### Performance
- Use a production WSGI server (Gunicorn, uWSGI)
- Enable database connection pooling
- Implement caching (Redis)
- Use CDN for static files

## 📊 Monitoring

### Health Checks
```python
@app.route('/health')
def health_check():
    return {'status': 'healthy', 'timestamp': datetime.now().isoformat()}
```

### Logging
```python
import logging
logging.basicConfig(level=logging.INFO)
logger = logging.getLogger(__name__)
```

## 🔧 Troubleshooting

### Common Issues
1. **Database Connection Failed**
   - Check database credentials
   - Verify database is running
   - Check firewall settings

2. **Port Already in Use**
   - Change port in app.py
   - Kill existing process
   - Use different port

3. **Dependencies Missing**
   - Run `pip install -r requirements.txt`
   - Check Python version compatibility
   - Install system dependencies

### Support
- Check GitHub Issues
- Review logs
- Contact maintainers

## 📈 Scaling

### Horizontal Scaling
- Use load balancer
- Multiple application instances
- Database replication

### Vertical Scaling
- Increase server resources
- Optimize database queries
- Implement caching

---

For more detailed deployment instructions, refer to the platform-specific documentation.
