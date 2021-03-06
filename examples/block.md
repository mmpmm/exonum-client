# Block verification

An example of block verification:

```javascript
const data = {
  block: {
    height: '4',
    prev_hash: '2e933eba2887a1d9bb38c396577be23db58ea5f414761f6dda939d660b323140',
    proposer_id: 0,
    schema_version: 0,
    state_hash: 'da5ae8362137d3e4acae0917e30388959b6d2a91760d25bb5eca832b449550ce',
    tx_count: 1,
    tx_hash: '759de4b2df16488e1c13c20cb9a356487204abcedd97177f2fe773c187beb29e'
  },
  precommits: [
    {
      body: {
        block_hash: '1a1b6bf4c9f7543809e1011b1d5e4ad0b76eab14924d8ff00ba1a79f0466ce6b',
        height: '4',
        propose_hash: '878165361bb6b207ca75cac83e2817b34564a9b5115128b21f4f89f729d60769',
        round: 4,
        time: {
          nanos: 804000000,
          secs: '1486720350'
        },
        validator: 0
      },
      message_id: 4,
      protocol_version: 0,
      service_id: 0,
      signature: 'f69f1cd9bd8dfd822a923f427556842b2cb194b75fc437248a6260f218e0d188911c1ef4616db3edcda78176d8d56273417439a1824a90e5df16775edb8dd608'
    },
    {
      body: {
        block_hash: '1a1b6bf4c9f7543809e1011b1d5e4ad0b76eab14924d8ff00ba1a79f0466ce6b',
        height: '4',
        propose_hash: '878165361bb6b207ca75cac83e2817b34564a9b5115128b21f4f89f729d60769',
        round: 4,
        time: {
          nanos: 804000000,
          secs: '1486720350'
        },
        validator: 1
      },
      message_id: 4,
      protocol_version: 0,
      service_id: 0,
      signature: '0660b18a35e6e9ee2a9f9447a2362a1e498314843aa8ddb838a81112dd2b290ff54cdd089a1877a82c3505b7376dc91e7e0d0f9a1150064ce1199a12845d560b'
    },
    {
      body: {
        block_hash: '1a1b6bf4c9f7543809e1011b1d5e4ad0b76eab14924d8ff00ba1a79f0466ce6b',
        height: '4',
        propose_hash: '878165361bb6b207ca75cac83e2817b34564a9b5115128b21f4f89f729d60769',
        round: 4,
        time: {
          nanos: 804000000,
          secs: '1486720350'
        },
        validator: 2
      },
      message_id: 4,
      protocol_version: 0,
      service_id: 0,
      signature: '02e26fac66f7e6fd9013f34832d53f7bbf928bd5824900594f8a247d4f4ec5f84c77420dd2bb98ebbf0910e48539d3abd9b57be70f15ca5ceccb85a92d41270a'
    }
  ]
}
const validators = [
  '0b513ad9b4924015ca0902ed079044d3ac5dbec2306f06948c10da8eb6e39f2d',
  '91a28a0b74381593a4d9469579208926afc8ad82c8839b7644359b9eba9a4b3a',
  '5c9c6df261c9cb840475776aaefcd944b405328fab28f9b3a95ef40490d3de84',
  '66cd608b928b88e50e0efeaa33faf1c43cefe07294b0b87e9fe0aba6a3cf7633'
]
const networkId = 0

Exonum.verifyBlock(data, validators, networkId) // true
```
