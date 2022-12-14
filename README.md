This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.tsx`. The page auto-updates as you edit the file.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/api-routes/introduction) instead of React pages.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Environment Setup

- Install jq: https://stedolan.github.io/jq/
- Install sam: https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/install-sam-cli.html
- Install docker

## Deployment Steps

Make sure docker is running. Fill in values in _parameters.json_.

1. Run `make build_image ImageTag=$(uuidgen)`
2. Run `make deploy_image ImageTag=[from step 1]`
3. Run `make deploy_fargate ImageTag=[from step 1]`
