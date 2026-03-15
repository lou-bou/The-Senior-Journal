# Messages
A message is the act of one object sending a request to another object to perform an action or provide information.

## Message Types
- Query: Ask an object for information (read). (ask for `diameter` property from `bicycle` object)
- Command: Tell an object to change its state. Generally does not return information. (tell `bicycle` to `set_gear`)

## Message Origins
- Incoming: A message that the object under test receives from another object.
- Outgoing: A message that the object under test sends to another object.
- Self: A message the the object under test sends to itself (private message).

# How to test
1) Incoming + Query: ASSERT result - Test by making assertions about the value they return.
2) Incoming + Command: ASSERT direct public side effects - Test by asserting that they produce the correct direct public side effects.
3) Outgoing + Query: DO NOT TEST. - It's redundant.
4) Outgoing + Command: EXPECT to send - Test by setting expectations (mocking) that the message is sent. Do not test the side effects of the receiving object.
5) Self: DO NOT TEST - They are implementation details. If the public method that calls them is tested, these are covered.

[Source](https://www.youtube.com/watch?v=URSWYvyc42M)
