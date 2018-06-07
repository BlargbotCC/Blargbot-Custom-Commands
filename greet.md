# Greet Setup
```
b!greet {if;==;{userisbot};false;
{quiet;{send;452692972824428544;Welcome to {guildname}, {usermention}! Please use `b!getcode` to receive your verification code! 
(You must have your DMs enabled to receive the code from blargbot!)}}
{quiet;{roleadd;452692932466573332;{userid}}}
;
{//;this next part is the bot autorole}
{quiet;{roleadd;452692928377126914;{userid}}}
}
```
