# Warm Heaven Care Connect

A professional home care management application for Warm Heaven Enterprise Inc.

## Features

- Role-based access control (Admin, House Manager, Supervisor, Nurse, Caregiver)
- Client management system
- Shift scheduling and tracking
- Visit reports and daily task checklists
- Incident reporting and management
- Multi-language support (English, Somali, French)
- Secure authentication and authorization
- Real-time notifications
- Comprehensive analytics dashboard
- Responsive UI with Tailwind CSS
- Push notifications
- Audit logging
- Performance monitoring

## Tech Stack

- Frontend: HTML, Tailwind CSS, JavaScript
- Backend: Supabase (PostgreSQL)
- Authentication: Supabase Auth
- UI Framework: Tailwind CSS
- Icons: FontAwesome
- Charts: Chart.js
- Real-time: Supabase Edge Functions
- Push Notifications: Web Push API

## Performance Optimizations

### Frontend
- Code splitting and lazy loading
- Tree-shaking
- Gzip compression
- Image optimization
- Critical CSS inlining
- Preloading of key assets
- Browser caching headers
- Service Worker for offline support

### Backend
- Database indexes for all frequently queried fields
- Real-time subscriptions optimized
- Edge Functions for serverless operations
- Caching strategies implemented
- Database connection pooling

## Setup

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Configure environment variables:
   ```bash
   cp .env.example .env
   ```
4. Start the development server:
   ```bash
   npm run dev
   ```

## Environment Variables

Create a `.env` file with the following variables:

```
# Supabase
SUPABASE_URL=your_supabase_url
SUPABASE_ANON_KEY=your_supabase_anon_key

# Push Notifications
VITE_PUSH_PUBLIC_KEY=your_push_public_key

# Performance Monitoring
VITE sentry_dsn=your_sentry_dsn

# Analytics
VITE_ANALYTICS_ID=your_analytics_id
```

## Database Schema

The application uses Supabase with the following tables:
- profiles (User profiles and roles)
- clients (Client information and care plans)
- shifts (Shift scheduling and tracking)
- visit_reports (Daily care reports)
- incidents (Incident reporting and tracking)
- intake_forms (Client onboarding forms)
- notifications (Real-time notifications)
- audit_logs (System audit trail)
- performance_metrics (Analytics data)

## Deployment

### Production Build

1. Build the application:
   ```bash
   npm run build
   ```

2. Deploy to your preferred platform:
   - Vercel
   - Netlify
   - GitHub Pages
   - Custom hosting

### Continuous Integration

The application is configured for CI/CD with GitHub Actions:

```yaml
name: Deploy to Production

on:
  push:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: actions/setup-node@v2
        with:
          node-version: '16'
      - run: npm install
      - run: npm run build
      - uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./dist
```

## Security

- All API calls are authenticated
- Role-based access control
- Secure password hashing
- CSRF protection
- XSS prevention
- Regular security audits
- Rate limiting
- IP blocking capabilities

## Monitoring

- Performance monitoring with Sentry
- Error tracking
- User analytics
- Database performance monitoring
- Real-time usage statistics

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, please:
1. Check the documentation
2. Open an issue on GitHub
3. Contact support@warmheaven.com

## Versioning

We use SemVer for versioning. For the versions available, see the tags on this repository.

## Authors

- Your Name - Initial work - [Your GitHub](https://github.com/yourusername)

See also the list of contributors who participated in this project.

## Acknowledgments

- Supabase team for their amazing platform
- Tailwind CSS team for their styling framework
- All contributors who helped test and improve this application
