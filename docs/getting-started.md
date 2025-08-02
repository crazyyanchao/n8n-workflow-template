# Quick Start Guide

## What is n8n?

[n8n](https://n8n.io/) is a powerful workflow automation platform that allows you to connect different applications and services through a visual interface.

## Installing n8n

### Method 1: Docker (Recommended)

```bash
docker run -it --rm \
  --name n8n \
  -p 5678:5678 \
  -v ~/.n8n:/home/node/.n8n \
  n8nio/n8n
```

### Method 2: npm

```bash
npm install n8n -g
n8n
```

### Method 3: npx

```bash
npx n8n
```

## Importing Workflows

1. After starting n8n, visit `http://localhost:5678`
2. Click "Workflows" in the left menu
3. Click the "Import from file" button
4. Select workflow files from the project (such as `workflows/page-by-page tushare data fetching.json`)

## Configuring Credentials

### Tushare API Configuration

1. Visit [Tushare Pro](https://tushare.pro/) to register an account
2. Get your API Token
3. In n8n:
   - Go to the "Credentials" page
   - Click "Add Credential"
   - Select "Tushare API"
   - Enter your Token

## Running Workflows

1. After importing a workflow, click on the workflow name to enter the edit page
2. Ensure all credentials are properly configured
3. Click the "Execute Workflow" button in the top right corner
4. View the execution results and output

## Frequently Asked Questions

### Q: What should I do if workflow execution fails?
A: Check the following points:
- Whether API credentials are correctly configured
- Whether network connection is normal
- Whether API call frequency exceeds limits

### Q: How to modify workflows?
A: In the n8n editor, you can:
- Add new nodes
- Modify parameters of existing nodes
- Reconnect nodes
- Save changes

### Q: How to export workflows?
A: On the workflow edit page, click the "Export" button in the top right corner to download the workflow file.

## Next Steps

- View [Workflow Documentation](../README.md#workflow-description) for detailed functionality
- Explore examples in the [examples](../examples/) directory
- Read the [API Documentation](https://docs.n8n.io/) to learn more features 
