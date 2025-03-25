# Ticket Yapp

A Next.js + TypeScript application that uses the Yapp SDK to sell tickets for the "Builders After Party" event. This application is designed to work within the Yodl super dapp iframe.

## Features

- Sell tickets for the "Builders After Party" event at $0.10 USD
- Integrate with the real Yapp SDK for payment processing
- Store purchased tickets in localStorage
- Display QR codes for ticket verification
- View all purchased tickets on a dedicated "My Tickets" page

## Getting Started

### Prerequisites

- Node.js (v14 or newer)
- npm or yarn

### Installation

1. Clone the repository
2. Install dependencies:

```bash
npm install
# or
yarn install
```

### Development

Run the development server:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

### Build for Production

```bash
npm run build
# or
yarn build
```

### Start Production Server

```bash
npm start
# or
yarn start
```

## Technical Details

- Built with Next.js and TypeScript
- Uses the real Yapp SDK (`@yodlpay/yapp-sdk`) for payment processing
- QR code generation with `qrcode.react`
- Responsive design for mobile and desktop
- Tickets are stored in localStorage

## Payment Flow

1. User clicks "Buy Ticket" button
2. A unique memo ID is generated
3. Payment request is created using `createPaymentRequest`
4. Yodl payment flow is launched with `openPayment`
5. Payment status is tracked with `trackPayment`
6. Upon confirmation, ticket is stored in localStorage
7. QR code is displayed with ticket details

## License

MIT
