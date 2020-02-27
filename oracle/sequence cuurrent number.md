How to find out current sequence number
=======================================

### Can not use CURRVAL until use NEXTVAL in same session.

<pre><code>
/* 현재 시퀀스 값 확인 */

SELECT 
        LAST_NUMBER 
FROM 
        USER_SEQUENCES 
WHERE 
        SEQUENCE_NAME = '시퀀스명(대문자)';
</code></pre>
