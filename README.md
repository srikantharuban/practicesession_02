# ParaBank Automated Testing with CI/CD Pipeline

This repository contains automated tests for the ParaBank application using Playwright, integrated with a GitHub Actions CI/CD pipeline.

## 🎯 Test Cases

- **TC 001**: Customer Registration - Verify new customer registration functionality
- **TC 002**: User Login - Verify login functionality with valid credentials

## 🚀 CI/CD Pipeline

The GitHub Actions workflow automatically:
- Runs tests on every push to `main` and `develop` branches
- Executes tests on pull requests
- Runs daily at 6 AM UTC for regression testing
- Tests across multiple browsers (Chromium, Firefox, WebKit)
- Generates comprehensive HTML reports
- Uploads test artifacts and screenshots

### Pipeline Features

- **Multi-browser Testing**: Parallel execution across Chromium, Firefox, and WebKit
- **Artifact Storage**: Test reports, screenshots, and results stored for 7-30 days
- **PR Comments**: Automatic test result comments on pull requests
- **Failure Screenshots**: Captures screenshots on test failures for debugging
- **Consolidated Reporting**: Combines results from all browsers into a single report

## 📊 Test Reports

After each pipeline run, you can access:
- **Individual Browser Reports**: Detailed results for each browser
- **Consolidated Report**: Combined overview of all test executions
- **Screenshots**: Visual evidence of test execution and failures
- **Artifacts**: Raw test data and logs

## 🔧 Local Development

### Prerequisites
- Node.js 16+ 
- npm

### Setup
```bash
# Install dependencies
npm install

# Install Playwright browsers
npm run install-browsers

# Run all tests
npm test

# Run tests for specific browser
npm run test:chromium
npm run test:firefox  
npm run test:webkit

# Run tests in headed mode (with browser UI)
npm run test:headed
```

## 🏗️ Pipeline Structure

```
.github/workflows/parabank-tests.yml
├── Setup (Node.js, dependencies)
├── Multi-browser test execution
├── Artifact collection
├── Report generation
└── PR commenting
```

## 📋 Test Environment

- **Target Application**: https://parabank.parasoft.com/parabank
- **Testing Framework**: Playwright
- **Browsers**: Chromium, Firefox, WebKit
- **CI/CD Platform**: GitHub Actions
- **Report Format**: HTML with visual styling

## 🔍 Monitoring

The pipeline provides multiple ways to monitor test execution:

1. **GitHub Actions Tab**: View real-time execution logs
2. **Pull Request Comments**: Automated result summaries
3. **Artifacts Section**: Download detailed reports and screenshots
4. **Email Notifications**: Configured for failures (optional)

## 📈 Metrics Tracked

- Test execution time
- Pass/fail rates per browser
- Historical trend analysis
- Failure screenshots and logs
- Performance benchmarks

## 🛠️ Configuration

Key configuration options in `test.js`:
- Browser selection via `BROWSER` environment variable
- Headless/headed mode via `CI` environment variable  
- Timeout settings
- Screenshot and report paths
- Unique test data generation

## 📝 Contributing

1. Fork the repository
2. Create a feature branch
3. Add/modify test cases
4. Ensure tests pass locally
5. Submit a pull request
6. Review automated test results

The CI/CD pipeline will automatically run your tests and provide feedback on the pull request.
