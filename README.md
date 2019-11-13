# Secret Data Validation

## About

[Enigma](https://enigma.co/) is a secure computation protocol, where “secret nodes” perform computations over encrypted data. Enigma brings privacy to any kind of computation - not just transactions - helping to improve the adoption and usability of decentralized technologies.

This application uses enigma's secret contracts to create secure a "data validation" module that enables users to encrypt data and check their encrypted data set against another user’s encrypted data set 

## Key Features:

This solution enables User A to upload a small dataset (email, phone number), 
and also enables a second user to submit their own dataset (with the same fields).

Then, the secret contract compares the two data sets. If they are equivalent, the secret contract sends an encrypted affirmation of this to User B, who has now verified their data set against user A.

If they are not equivalent, the user receives a false response.

## Install

### 1. Start Discovery Network

In a separate terminal:
```bash
npm i -g @enigmampc/discovery-cli
npm install
discovery start
```
### 2. Deploy Contracts
```bash
discovery compile
discovery migrate
```
### 3. Start dApp
```bash
cd client
npm install
npm start
```

## Using dApp

1. Navigate browser to https://localhost:3000/
2. Wait for Enigma to load.
3. Select address.
4. Fill in the phone and email fields.
5. Click 'Submit'.
6. Go to step 2.

## Test Contracts

From the root of your project:
```bash
discovery test
```
