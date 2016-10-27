## Create, delete table with all access on table prefixed with "stage_"

``` 
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "Stmt1477475892001",
            "Effect": "Allow",
            "Action": [
                "dynamodb:PurchaseReservedCapacityOfferings",
                "dynamodb:List*",
                "dynamodb:Describe*"
            ],
            "Resource": [
                "*"
            ]
        },
        {
            "Sid": "Stmt1477475892000",
            "Effect": "Allow",
            "Action": [
                "dynamodb:BatchGetItem",
                "dynamodb:BatchWriteItem",
                "dynamodb:DeleteItem",
                "dynamodb:GetItem",
                "dynamodb:PutItem",
                "dynamodb:Query",
                "dynamodb:Scan",
                "dynamodb:UpdateTable",
                "dynamodb:CreateTable",
                "dynamodb:UpdateItem"
            ],
            "Resource": [
                "arn:aws:dynamodb:ap-southeast-1:013137792704:table/stage_*"
            ]
        },
        {
            "Sid": "Stmt1477475892002",
            "Effect": "Allow",
            "Action": [
                "dynamodb:GetRecords",
                "dynamodb:GetShardIterator"
            ],
            "Resource": [
                "arn:aws:dynamodb:ap-southeast-1:013137792704:table/stage_*/stream/*"
            ]
        }
    ]
}

```
