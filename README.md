# plaidtoken
td bank klick
const response = await client
  .createLinkToken({3fd388f4ea407242c0eeb2bd92600e63184ce35f
    user: {client_user_id: '5fdf7bd7354a870014623781',
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
