# MySQL misc notes

## Disable foreign keys during DELETE

```
SET FOREIGN_KEY_CHECKS = 0;
 
DELETE ...

SET FOREIGN_KEY_CHECKS = 1;
```
