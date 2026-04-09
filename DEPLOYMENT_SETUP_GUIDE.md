# 🚀 DEPLOYMENT SETUP GUIDE

Your CI/CD pipeline code has been successfully pushed to GitHub! Now follow these steps to complete the setup:

## ✅ STEP 1: COMPLETED
- [x] Code pushed to GitHub: https://github.com/kavishworks/acb-demo-s-api.git

## 🔧 STEP 2: Configure GitHub Repository Settings

### A. Add Repository Secrets
1. Go to: https://github.com/kavishworks/acb-demo-s-api/settings/secrets/actions
2. Click "New repository secret"
3. Add these secrets:

```
Name: ANYPOINT_USERNAME
Value: [Your Anypoint Platform Username]

Name: ANYPOINT_PASSWORD  
Value: [Your Anypoint Platform Password]
```

### B. Add Repository Variables
1. Go to: https://github.com/kavishworks/acb-demo-s-api/settings/variables/actions
2. Click "New repository variable"
3. Add these variables:

```
Name: APP_NAME_DEV
Value: acb-demo-s-api-dev

Name: ENVIRONMENT_DEV
Value: Development

Name: BUSINESS_GROUP
Value: [Your Business Group ID from Anypoint Platform]

Name: APP_NAME_STAGING
Value: acb-demo-s-api-staging

Name: ENVIRONMENT_STAGING
Value: Staging

Name: APP_NAME_PROD
Value: acb-demo-s-api-prod

Name: ENVIRONMENT_PROD
Value: Production
```

## 🛡️ STEP 3: Create GitHub Environments

### Development Environment
1. Go to: https://github.com/kavishworks/acb-demo-s-api/settings/environments
2. Click "New environment"
3. Name: `development`
4. No protection rules needed (auto-deploy)

### Staging Environment
1. Click "New environment"
2. Name: `staging`
3. Check "Required reviewers" → Add yourself
4. Check "Restrict pushes to protected branches" → Select `main`

### Production Environment
1. Click "New environment"
2. Name: `production`
3. Check "Required reviewers" → Add 2 reviewers (yourself + another person)
4. Check "Restrict pushes to protected branches" → Select `main`
5. Optional: Set "Wait timer" to 5 minutes

## 🔍 STEP 4: Verify Anypoint Platform

### Check Your Environments
1. Login to: https://anypoint.mulesoft.com
2. Go to Runtime Manager
3. Verify these environments exist:
   - Development
   - Staging
   - Production

### Find Your Business Group ID
1. In Anypoint Platform, go to Access Management
2. Click on your organization name
3. Copy the Organization ID (this is your Business Group ID)

## 🧪 STEP 5: Test the Pipeline

### Option A: Trigger CI Pipeline
1. Go to: https://github.com/kavishworks/acb-demo-s-api
2. Edit the README.md file
3. Add a line like: "Pipeline activated on [current date]"
4. Commit directly to main branch

### Option B: Create Pull Request
1. Create a new branch
2. Make a small change
3. Create PR to main branch
4. Merge the PR

## 📊 STEP 6: Monitor Pipeline Execution

1. Go to: https://github.com/kavishworks/acb-demo-s-api/actions
2. Watch the CI pipeline run
3. If CI passes, CD pipeline will start
4. Approve deployments for Staging and Production when prompted

## 🎯 SUCCESS INDICATORS

You'll know it's working when:
- ✅ CI pipeline shows green checkmarks
- ✅ Applications appear in CloudHub 2.0 Runtime Manager
- ✅ Each environment shows "STARTED" status
- ✅ You can access the API endpoints

## 🆘 NEED HELP?

If you encounter issues:
1. Check GitHub Actions logs for error details
2. Verify all secrets and variables are set correctly
3. Ensure Anypoint Platform environments exist
4. Check CloudHub 2.0 permissions

## 📞 QUICK CHECKLIST

- [ ] Added ANYPOINT_USERNAME secret
- [ ] Added ANYPOINT_PASSWORD secret
- [ ] Added all repository variables (6 total)
- [ ] Created development environment
- [ ] Created staging environment (with 1 reviewer)
- [ ] Created production environment (with 2 reviewers)
- [ ] Verified Anypoint Platform environments exist
- [ ] Found and added Business Group ID
- [ ] Triggered first pipeline run
- [ ] Monitored pipeline execution

Once all items are checked, your CI/CD pipeline will be fully operational! 🚀
