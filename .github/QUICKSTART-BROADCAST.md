# 🚀 Quick Start Guide: Ecosystem Broadcast System

## Overview

The Ecosystem Broadcast Distribution system allows you to send messages, announcements, and updates from the main `heyns1000/heyns1000` repository to all ecosystem repositories.

## Quick Start

### 1. Manual Broadcast

**Step-by-step:**

1. Go to the **Actions** tab in the `heyns1000/heyns1000` repository
2. Select **"Ecosystem Broadcast Distribution"** workflow
3. Click **"Run workflow"** button
4. Fill in the form:
   ```
   Message Title: Milestone Achievement - Q1 2026
   Message Body: We've successfully integrated all ecosystem repositories!
   Distribution Type: milestone
   Target Repositories: (leave empty for all, or specify: codenest,omnigrid)
   Create Issue: ✓ (checked)
   File to Distribute: (leave empty or specify path)
   ```
5. Click **"Run workflow"**

### 2. What Happens Next

The workflow will:
- ✅ Create tracking issues in each target repository
- ✅ Include your message with proper formatting
- ✅ Add appropriate labels (broadcast, ecosystem, type)
- ✅ Generate a broadcast log in `.github/broadcast-logs/`
- ✅ Create a workflow summary with results

### 3. Automatic Triggers

The workflow also runs automatically when:
- **Milestone is created or closed** → Broadcasts milestone information
- **Release is published** → Broadcasts release notes

## Use Cases

### Announce a New Feature

```yaml
Message Title: New Feature: Cross-Repo Search
Message Body: |
  We're excited to announce cross-repository search functionality!
  
  All ecosystem repositories can now be searched from a single interface.
  Documentation: https://github.com/heyns1000/heyns1000/wiki/search
Distribution Type: announcement
```

### Security Alert

```yaml
Message Title: Security Update Required
Message Body: |
  Critical: Update dependencies immediately
  
  Affected packages:
  - package-x: Update to v2.1.5
  - package-y: Update to v3.0.1
  
  Timeline: 48 hours
Distribution Type: security_alert
Create Issue: true
```

### Documentation Update

```yaml
Message Title: Updated Contributing Guidelines
Message Body: |
  Our contributing guidelines have been updated.
  
  Key changes:
  - New PR template
  - Updated code review process
  - Enhanced testing requirements
  
  Please review: https://github.com/heyns1000/heyns1000/CONTRIBUTING.md
Distribution Type: documentation_update
```

## Target Repositories

By default, broadcasts go to:
- `heyns1000/codenest`
- `heyns1000/omnigrid`
- `heyns1000/baobab-bush-portal`
- `heyns1000/FruitfulPlanetChange`
- `heyns1000/pulse-trade-9s`

You can customize this list in the workflow inputs or edit `.github/ecosystem-config.yml`.

## Monitoring

### View Broadcast History

Check `.github/broadcast-logs/` for historical records:
```bash
ls -la .github/broadcast-logs/
```

### View Workflow Runs

1. Go to **Actions** tab
2. Filter by **"Ecosystem Broadcast Distribution"**
3. Click any run to see detailed logs

### Check Target Repository Issues

Visit any target repository and filter issues by label:
```
label:broadcast label:ecosystem
```

## Best Practices

### ✅ DO

- **Be clear and concise** in your message title
- **Provide context** in the message body
- **Include links** to relevant documentation
- **Specify action items** when needed
- **Use appropriate distribution type** for filtering
- **Test with one repository first** for important broadcasts

### ❌ DON'T

- **Don't spam** - Use broadcasts for important messages only
- **Don't use for repository-specific issues** - Use direct issues instead
- **Don't forget to close broadcast issues** after acknowledgment
- **Don't include sensitive information** - Broadcasts are public

## Troubleshooting

### Issue: Broadcast didn't reach a repository

**Check:**
1. Repository exists and is accessible
2. Repository has issues enabled
3. Workflow logs for specific errors

**Fix:**
- Re-run the workflow
- Verify repository name spelling
- Check GitHub Actions permissions

### Issue: Rate limiting

**Solution:**
- Wait a few minutes and retry
- Reduce number of target repositories
- Contact GitHub support if persistent

### Issue: Permission denied

**Solution:**
- Verify GITHUB_TOKEN has necessary permissions
- Check if target repositories are public
- For private repos, may need a PAT (Personal Access Token)

## Advanced Usage

### Custom Target List

```yaml
Target Repositories: codenest,omnigrid
```

### Distribute a File

```yaml
File to Distribute: .github/templates/ISSUE_TEMPLATE.md
```

### Skip Issue Creation

```yaml
Create Issue: false
```
(Useful for testing or when issues aren't needed)

## Next Steps

- 📖 Read full documentation: [ECOSYSTEM-BROADCAST.md](.github/ECOSYSTEM-BROADCAST.md)
- 📝 View message templates: [broadcast-template.md](.github/templates/broadcast-template.md)
- ⚙️ Configure repositories: [ecosystem-config.yml](.github/ecosystem-config.yml)
- 📊 Review workflow: [ecosystem-broadcast.yml](.github/workflows/ecosystem-broadcast.yml)

## Support

Need help?
- 📋 [Open an issue](https://github.com/heyns1000/heyns1000/issues/new)
- 📚 [Read the docs](.github/ECOSYSTEM-BROADCAST.md)
- 💬 Contact: @heyns1000

---

**🌳 Happy Broadcasting! 🌳**
