---
title: redis
type: cache
---

<!--
     THIS FILE IS AUTOGENERATED!

     To make changes please edit the contents of:
     lib/cache/redis.go
-->


Use a Redis instance as a cache. The expiration can be set to zero or an empty
string in order to set no expiration.


import Tabs from '@theme/Tabs';

<Tabs defaultValue="common" values={[
  { label: 'Common', value: 'common', },
  { label: 'Advanced', value: 'advanced', },
]}>

import TabItem from '@theme/TabItem';

<TabItem value="common">

```yaml
redis:
  url: tcp://localhost:6379
  prefix: ""
  expiration: 24h
```

</TabItem>
<TabItem value="advanced">

```yaml
redis:
  url: tcp://localhost:6379
  prefix: ""
  expiration: 24h
  retries: 3
  retry_period: 500ms
```

</TabItem>
</Tabs>

## Fields

### `url`

`string` The URL of the target Redis server.

### `prefix`

`string` An optional string to prefix item keys with in order to prevent collisions with similar services.

### `expiration`

`string` An optional period after which cached items will expire.

### `retries`

`number` The maximum number of retry attempts to make before abandoning a request.

### `retry_period`

`string` The duration to wait between retry attempts.


