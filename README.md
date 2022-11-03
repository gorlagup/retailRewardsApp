# retailRewardsApp

Rest end Point URl:
POST: http://localhost:8282/RetailRewards/api/rewards

Sample Request:
{
    "timePeriod": 3,
    "transactions": [
        {
            "amount": "120",
            "transactionDate": "2022-09-02",
            "customerid": "1111"
        },
        {
            "amount": "150",
            "transactionDate": "2022-10-02",
            "customerid": "1111"
        },
        {
            "amount": "160",
            "transactionDate": "2022-11-02",
            "customerid": "1111"
        },
        {
            "amount": "120",
            "transactionDate": "2022-09-02",
            "customerid": "2222"
        }
    ]
}

Sample Response:
[
    {
        "customerName": "Albert",
        "rewardsPerMonth": [
            {
                "month": "OCTOBER",
                "rewards": 150
            },
            {
                "month": "SEPTEMBER",
                "rewards": 90
            },
            {
                "month": "NOVEMBER",
                "rewards": 170
            }
        ],
        "totalRewardsEarned": 410
    },
    {
        "customerName": "Thomson",
        "rewardsPerMonth": [
            {
                "month": "SEPTEMBER",
                "rewards": 90
            }
        ],
        "totalRewardsEarned": 90
    }
]
