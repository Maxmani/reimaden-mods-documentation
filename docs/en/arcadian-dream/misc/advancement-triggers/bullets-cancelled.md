# Bullets Cancelled

Triggers when a player cancels bullets.

ID: `arcadiandream:bullets_cancelled`

### Available extra conditions

Condition  | Type | Default | Description
-------|------|---------|-------------
`amount` | Integer Range | *optional* | The number of bullets that must be cancelled.
`from_extend` | Boolean | *optional*  | Whether the bullets are cancellable with a Bomb or an Extend. Defaults to both.

### Example #1

```json
"criteria": {
    "cancelled_bullets": {
        "conditions": {
            "from_extend": false
        },
        "trigger": "arcadiandream:bullets_cancelled"
    }
}
```

This advancement criterion is met when a player cancels any number of bullets using a Bomb.

### Example #2

```json
"criteria": {
    "cancelled_bullets": {
        "conditions": {
            "amount": {
                "min": 50
            }
        },
        "trigger": "arcadiandream:bullets_cancelled"
    }
}
```

This advancement criterion is met when a player cancels at least 50 bullets using a Bomb or an Extend.