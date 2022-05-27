Missing error messages in require statements: There are many places where require statements are correctly followed by their error messages, clarifying what was the triggered exception. However, there are places where require statements are not followed by the corresponding error messages. If any of those require statements were to fail the checked condition, the transaction
would revert silently without an informative error message.

    Recommendation: Consider including specific and informative error messages in all require statements.

    OpenZeppelin's Audit of GEB Protocol