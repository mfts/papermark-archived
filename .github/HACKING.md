# Developer Guide

## Attribution

This document is heavily inspired by Shoutify's [Hacking.md](https://github.com/TechSquidTV/Shoutify/blob/main/.github/HACKING.md). Thank you Kyle. 

## Repository Setup

### 1. Fork and clone the repository

1. Visit the [Papermark repository](https://github.com/mfts/papermark) and click the [Fork](https://github.com/mfts/papermark/fork) button in the top right corner.
2. Clone your forked repository to your local machine.

```shell
git clone git@github.com:<YOUR-USER>/papermark.git
cd papermark
```

### 2. Install npm dependencies

```shell
npm install
```

### 3. Copy the `.env.example` file to `.env`

```shell
cp .env.example .env
```

### 4. Configure the variables in `.env`

| Variable | Value |
|---|---|
| NEXTAUTH_SECRET | a random string |
| ACCESS_KEY | < AWS IAM Access Key > |
| SECRET_KEY  | < AWS IAM Secret Key > |
| REGION | < AWS S3 bucket region > |
| S3_BUCKET_NAME | < AWS S3 bucket name > |
| EMAIL_SERVER | < SMTP server string > |
| EMAIL_FROM | < Default sender email address > |

### 5. Initialize the database

```shell
npx prisma db push
```

### 6. Run the dev server

```shell
npm run dev
```

### 7. Open the app in your browser

Visit [http://localhost:3000](http://localhost:3000) in your browser.

## Contributing

You are now ready to develop! Congratulations on getting Papermark up and running!

Next Steps:

- Read the [Contributing Guide](./CONTRIBUTING.md)
- Read the [Code of Conduct](./CODE_OF_CONDUCT.md)
