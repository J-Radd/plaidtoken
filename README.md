# plaidtoken
td bank klick
const response = await client
  .createLinkToken({3fd388f4ea407242c0eeb2bd92600e63184ce35f
    user: {client_user_id: '5fdf7bd7354a870014623781',
    },
    client_name: 'Svetlana Klick',
    products: ['auth', 'transactions'],
    country_codes: ['CA'],
    language: 'en',
    webhook: 'https://github.com/stripe/scoop-stripe-cli.git',
    account_filters: {
      depository: {
        account_subtypes: ['checking', 'savings'],
      },
    },
  })
{
  "link_token": "link-production-840204-193734",
  "expiration": "2020-03-27T12:56:34.000Z",
  "request_id": "XQVgFigpGHXkb0b"
}((err) => {
    // handle error
  });

const linkToken = response.link_token;
