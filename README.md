# WeLocal Polls Service

Community polls and voting service for the WeLocal platform, built with Node.js and Express.

## Tech Stack

- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: PostgreSQL
- **Authentication**: JWT (JSON Web Tokens)
- **API Documentation**: Swagger/OpenAPI
- **Testing**: Jest
- **Logging**: Winston
- **Validation**: Joi
- **ORM**: TypeORM
- **File Storage**: AWS S3
- **Search Engine**: Elasticsearch
- **Real-time Communication**: Socket.io
- **Email Service**: SendGrid
- **Analytics**: Google Analytics

## Features

- Poll creation and management
- Multiple choice voting
- Ranked choice voting
- Poll scheduling
- Anonymous voting
- Vote verification
- Real-time results
- Poll analytics
- Community engagement
- Poll categories
- Poll templates
- Result visualization

## Prerequisites

- Node.js (v18 or higher)
- PostgreSQL
- Elasticsearch
- npm or yarn
- AWS S3 bucket
- SendGrid account
- Redis (for real-time features)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-org/welocal-polls-service.git
   cd welocal-polls-service
   ```

2. Install dependencies:
   ```bash
   npm install
   # or
   yarn install
   ```

3. Create environment file:
   ```bash
   cp .env.example .env
   ```

4. Configure environment variables in `.env`:
   ```env
   NODE_ENV=development
   PORT=8087
   DATABASE_URL=postgresql://welocal:welocal123@localhost:5432/welocal
   ELASTICSEARCH_URL=http://localhost:9200
   AWS_ACCESS_KEY_ID=your-aws-access-key
   AWS_SECRET_ACCESS_KEY=your-aws-secret-key
   AWS_REGION=your-aws-region
   AWS_S3_BUCKET=your-s3-bucket
   SENDGRID_API_KEY=your-sendgrid-api-key
   REDIS_URL=redis://localhost:6379
   GOOGLE_ANALYTICS_ID=your-ga-id
   ```

## Running the Service

### Development Mode
```bash
npm run dev
# or
yarn dev
```

### Production Mode
```bash
npm run build
npm start
# or
yarn build
yarn start
```

### Docker
```bash
docker build -t welocal-polls-service .
docker run -p 8087:8087 welocal-polls-service
```

## API Endpoints

### Polls Management
- `GET /api/v1/polls` - Get polls list
- `POST /api/v1/polls` - Create poll
- `GET /api/v1/polls/:id` - Get poll details
- `PUT /api/v1/polls/:id` - Update poll
- `DELETE /api/v1/polls/:id` - Delete poll

### Voting
- `POST /api/v1/polls/:id/vote` - Submit vote
- `GET /api/v1/polls/:id/results` - Get poll results
- `GET /api/v1/polls/:id/status` - Get poll status
- `POST /api/v1/polls/:id/verify` - Verify vote

### Poll Categories
- `GET /api/v1/categories` - Get categories
- `POST /api/v1/categories` - Create category
- `GET /api/v1/categories/:id` - Get category details
- `PUT /api/v1/categories/:id` - Update category
- `DELETE /api/v1/categories/:id` - Delete category

### Poll Templates
- `GET /api/v1/templates` - Get templates
- `POST /api/v1/templates` - Create template
- `GET /api/v1/templates/:id` - Get template details
- `PUT /api/v1/templates/:id` - Update template
- `DELETE /api/v1/templates/:id` - Delete template

### Analytics
- `GET /api/v1/polls/:id/analytics` - Get poll analytics
- `GET /api/v1/polls/:id/analytics/votes` - Get vote analytics
- `GET /api/v1/polls/:id/analytics/engagement` - Get engagement analytics

## API Documentation

API documentation is available at `/api-docs` when running the service.

## Testing

### Unit Tests
```bash
npm run test
# or
yarn test
```

### Integration Tests
```bash
npm run test:integration
# or
yarn test:integration
```

### E2E Tests
```bash
npm run test:e2e
# or
yarn test:e2e
```

## Project Structure

```
src/
├── config/           # Configuration files
├── controllers/      # Route controllers
├── middleware/       # Custom middleware
├── models/          # Database models
├── routes/          # API routes
├── services/        # Business logic
├── utils/           # Utility functions
├── validators/      # Request validation
├── storage/         # File storage handling
├── search/          # Search functionality
├── realtime/        # Real-time updates
├── notifications/   # Email notifications
├── analytics/       # Analytics processing
└── app.js           # Application entry point
```

## Security Features

- JWT token-based authentication
- Rate limiting
- CORS configuration
- Helmet security headers
- Input validation
- SQL injection prevention
- XSS protection
- File upload validation
- Vote verification system
- Anonymous voting support

## Monitoring

The service exposes the following endpoints for monitoring:
- `/health` - Health check
- `/metrics` - Prometheus metrics
- `/status` - Service status

## Logging

Logs are written to:
- Console (development)
- File (production)

Log levels:
- ERROR
- WARN
- INFO
- DEBUG

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

[Your License Here]

## Support

For support, please contact [Your Contact Information] 