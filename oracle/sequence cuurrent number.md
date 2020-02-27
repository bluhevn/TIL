How to find out current sequence number
=======================================

### Can not use CURRVAL until use NEXTVAL in same session.

<pre><code>
/* Confirm Current Sequence Number */

SELECT 
        LAST_NUMBER 
FROM 
        USER_SEQUENCES 
WHERE 
        SEQUENCE_NAME = 'SEQUENCE_NAME(UPPER CASE)';
</code></pre>
