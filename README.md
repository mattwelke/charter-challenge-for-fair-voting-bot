# charter-challenge-for-fair-voting-bot

A bot that records the amount donated so far for the Charter Challenge for Fair Voting (https://www.charterchallenge.ca/) into a public BigQuery dataset each day.

## Reading data

The data is available in a public dataset that is updated once per day. Example query:

```sql
SELECT
  *
FROM
  `public-datasets-363301.charter_challenge_bot.donation_statuses`
ORDER BY
  date DESC
LIMIT
  1000
```

Any GCP principal authenticated can query this public dataset.

![image](https://user-images.githubusercontent.com/7719209/191647190-3bcb7f7c-ed19-49b9-881a-7e4ebe685864.png)

![image](https://user-images.githubusercontent.com/7719209/191645928-6068d947-c777-41ab-ae94-0d38d3c56110.png)

## Credits

Example used for guidance: https://github.com/apache/openwhisk-runtime-go/tree/master/examples/module-main