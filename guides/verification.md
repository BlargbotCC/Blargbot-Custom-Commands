# Verification Set-up
> **CAUTION!**
> **Still buggy!**
> **USE AT OWN RISH**

{delete} 
{trim;
  {if;!=;{channelid};452692972824428544;
{return}}

{execcc;makecode}
    {dm;{userid};{trim;{execcc;getcodemessagedm}}}
{//;verifies the message, resets after 5 minutes}
{set;~a;{waitmessage;;;{bool;==;{clean;{messagetext}};{clean;{get;~joincode}}};300}}
{apply;delete;{get;~a}}

{//;verifies code}
{void;{set;~userid;{userid}}
      {roleremove;452692932466573332;{get;~userid}}
      {roleadd;452692927743918101;{get;~userid}}
      {execcc;verifyrolesadd}
      {roleremove;452692932466573332;{get;~userid}}
      {roleadd;452692927743918101;{get;~userid}}
      {send;452692979082330115;;
        {embedbuild;
          author.name:{username;{get;~userid}}#{userdiscrim;{get;~userid}};
          author.icon_url:{useravatar;{get;~userid}};
          title:Welcome to {guildname}, {usernick}!;
          description:We hope you enjoy being here, for more information, use `b!bcc help`! in <#452692995389521934>!;
          color:00ff00;
          footer.text:{guildname};
          footer.icon_url:{guildicon};
          timestamp:{time};

        }    
    }
