# plaidtoken
td bank klick
const response = await client
  .createLinkToken({
    user: {
      client_user_id: '123-test-user-id',
    },
    client_name: 'Plaid Test App',
    products: ['auth', 'transactions'],
    country_codes: ['GB'],
    language: 'en',
    webhook: 'https://sample-web-hook.com',
    account_filters: {
      depository: {
        account_subtypes: ['checking', 'savings'],
      },
    },
  })
  .catch((err) => {
    // handle error
  });

const linkToken = response.link_token;
