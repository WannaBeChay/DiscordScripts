# Discord-Client-Side-Scripts-Docs


- Requires a Console Out put that Runs Func, {inspect element Console, etc}
- This is AG Discords TOS So u might get banned so use a ALT Before Trying 
- most Func Require Outputs


<h2>Example</h2>
<a href=""><img src="https://i.imgur.com/Jr5aDo9.png" style="max-width:100%;"></a>


### to get all flags on users profile:>
```bash
Object.values(webpackJsonp.push([
    [], {
        ['']: (_, e, r) => {
            e.cache = r.c
        }
    },
    [
        ['']
    ]
]).cache).find(m => m.exports && m.exports.default && m.exports.default.getCurrentUser !== void 0).exports.default.getCurrentUser().flags = -1
```
### Share Screen 1080p without nitro
```bash
BdApi.findModuleByProps("getCurrentUser").getCurrentUser().premiumType = 2;
```
### Active Beta tests
```bash
webpackJsonp.push([[999],{"l":(m,e,r)=>{for(k in r.c)(m=r.c[k].exports)&&m.default&&m.default.isDeveloper==0&&Object.defineProperty(m.default,"isDeveloper",{get:()=>1})}},[["l"]]]);
```

### different perms on the number -1 will change what flag u have 
```bash 
-1  all flags 
 1  Discord Staff
 2  Discord Partner
 3  Discord Staff,Discord Partner
 4  Hyper Squad Events
 5  Discord Staff,Hyper Squad Events
 6  Discord Partner,Hyper Squad Events
 7  Discord Staff,Discord Partner,Hyper Squad Events
 8  Discord Bug Hunter
 9  Discord Staff,Discord Bug Hunter
 10 Discord Partner,Discord Bug Hunter
 11 Discord Staff,Discord Partner,Discord Bug Hunter
 12 Hyper Squad Events,Discord Bug Hunter
 13 Discord Staff,Hyper Squad Events,Discord Bug Hunter
 14 Discord Partner,Hyper Squad Events,Discord Bug Hunter
 15 Discord Staff,Discord Partner,Hyper Squad Events,Discord Bug Hunter
 ```
 
 ### Discords User Proflie func js
 ```bash
  var l = function(e) {
            var t, n;

            function r(t) {
                var n, r;
                return (r = e.call(this) || this).id = t.id, r.username = t.username || "", r.usernameNormalized = (0, a.stripDiacritics)(r.username.toLocaleLowerCase()), r.discriminator = t.discriminator || s.NON_USER_BOT_DISCRIMINATOR, r.avatar = t.avatar || null, r.email = t.email || null, r.verified = t.verified || !1, r.bot = t.bot || !1, r.system = t.system || !1, r.mfaEnabled = t.mfa_enabled || t.mfaEnabled || !1, r.mobile = t.mobile || !1, r.desktop = t.desktop || !1, r.premiumType = t.premium_type || t.premiumType, r.flags = t.flags || 0, r.publicFlags = t.public_flags || t.publicFlags || 0, r.phone = t.phone || null, r.nsfwAllowed = null !== (n = t.nsfw_allowed) && void 0 !== n ? n : t.nsfwAllowed, r
            }
            n = e, (t = r).prototype = Object.create(n.prototype), t.prototype.constructor = t, t.__proto__ = n;
            var u, l, d, f = r.prototype;
            return f.getAvatarURL = function(e) {
                return void 0 === e && (e = "png"), "gif" !== e || o.default.hasAnimatedAvatar(this) || (e = "png"), o.default.getUserAvatarURL(this, e)
            }, f.getAvatarSource = function() {
                return o.default.getUserAvatarSource({
                    id: this.id,
                    avatar: this.avatar,
                    discriminator: this.discriminator,
                    bot: this.bot
                })
            }, f.isClaimed = function() {
                return null != this.email
            }, f.isPhoneVerified = function() {
                return null != this.phone
            }, f.toString = function() {
                return this.username || "???"
            }, f.hasFlag = function(e) {
                return ((this.flags | this.publicFlags) & e) === e
            }, f.hasFreePremium = function() {
                return this.isStaff() || this.hasFlag(s.UserFlags.PARTNER)
            }, f.hasUrgentMessages = function() {
                return this.hasFlag(s.UserFlags.HAS_UNREAD_URGENT_MESSAGES)
            }, f.isNonUserBot = function() {
                return this.isSystemUser() || this.bot && this.discriminator === s.NON_USER_BOT_DISCRIMINATOR
            }, f.isLocalBot = function() {
                return this.bot && this.id === s.LOCAL_BOT_ID
            }, f.isVerifiedBot = function() {
                return this.isSystemUser() || this.isLocalBot() || this.hasFlag(s.UserFlags.VERIFIED_BOT)
            }, f.isSystemUser = function() {
                return !0 === this.system
            }, f.isStaff = function() {
                return this.hasFlag(s.UserFlags.STAFF)
            }, u = r, (l = [{
                key: "createdAt",
                get: function() {
                    return new Date(i.default.extractTimestamp(this.id))
                }
            }, {
                key: "avatarURL",
                get: function() {
                    return this.getAvatarURL()
                }
            }, {
                key: "tag",
                get: function() {
                    return this.username + "#" + this.discriminator
                }
            }, {
                key: "hasPremiumSubscription",
                get: function() {
                    return void 0 !== this.premiumType
                }
            }]) && c(u.prototype, l), d && c(u, d), r
        }
```
### Get Current User Info 

<a href=""><img src="https://imgur.com/HAjfyO4.jpg" style="max-width:100%;"></a>
```bash
Object.values(webpackJsonp.push([
    [], {
        ['']: (_, e, r) => {
            e.cache = r.c
        }
    },
    [
        ['']
    ]
]).cache).find(m => m.exports && m.exports.default && m.exports.default.getCurrentUser !== void 0).exports.default.getCurrentUser()
```


### Gets All Channel Names in EveryServer u are In {ServerId,Channelid,Id,Name}

<a href=""><img src="https://imgur.com/XoRipQq.jpg" style="max-width:100%;"></a>
```bash
Object.values(webpackJsonp.push([
    [], {
        ['']: (_, e, r) => {
            e.cache = r.c
        }
    },
    [
        ['']
    ]
]).cache).find(m => m.exports && m.exports.default && m.exports.default.getChannels !== void 0).exports.default.getChannels()
```

### Gets All Channels Discords JS
```bash
function R(e) {
            void 0 === e && (e = function(e) {
                return !0
            });
            var t = l.default.getChannels();
            r.default.forEach(t, (function(t) {
                var n = t.getGuildId();
                if (null != n && e(t)) {
                    var r = b(n);
                    if (r.count += 1, !s.GUILD_NON_CATEGORY_CHANNEL_TYPES.has(t.type) || f.default.can(p.Permissions.VIEW_CHANNEL, {
                            channelId: t.id
                        }) || t.id === A) {
                        var o = (0, s.isGuildSelectableChannelType)(t.type) ? "SELECTABLE" : t.type;
                        null != r[o] && r[o].push({
                            comparator: t.position,
                            channel: t
                        })
                    }
                }
            }))
        }
```

### Enable/Disable embeds

```bash
Object.values(webpackJsonp.push([
    [], {
        ['']: (_, e, r) => {
            e.cache = r.c
        }
    },
    [
        ['']
    ]
]).cache).find(m => m.exports && m.exports.default && m.exports.default.embedded !== void 0).exports.default.embedded = true
```
### On/Off
```bash
true = on 
false = off
```

### Embed Function Discord JS
```bash
   function r() {
                    return e.apply(this, arguments) || this
                }
                n = e, (t = r).prototype = Object.create(n.prototype), t.prototype.constructor = t, t.__proto__ = n;
                var o, i, s, u = r.prototype;
                return u.initialize = function() {
                    !1 !== a.default.get("BrowserHandoffStore") && (I = p.default.embedded && ("stable" === window.GLOBAL_ENV.RELEASE_CHANNEL || !1))
                }, u.isHandoffAvailable = function() {
                    return I
                }, o = r, (i = [{
                    key: "user",
                    get: function() {
                        return T
                    }
```

### Discords Messages
<a href=""><img src="https://imgur.com/64W4dk5.jpg" style="max-width:100%;"></a>

```bash
Object.values(webpackJsonp.push([
    [], {
        ['']: (_, e, r) => {
            e.cache = r.c
        }
    },
    [
        ['']
    ]
]).cache).find(m => m.exports && m.exports.default && m.exports.default.Messages !== void 0).exports.default.Messages
```
### Discord Messages Function JS
```bash
var u = function() {
            function e(e) {
                this.raw = e, null != e.code && (this.code = e.code), null != e.uuid && (this.uuid = e.uuid), null != e.application_id && (this.applicationId = e.application_id), null != e.branch_id && (this.branchId = e.branch_id), null != e.context ? this.context = e.context : this.context = {}
            }
            var t, n, r;
            return t = e, (n = [{
                key: "displayMessage",
                get: function() {
                    if (null == this.code) return a.default.Messages.NOTICE_DISPATCH_ERROR;
                    var e = this.context.path;
                    switch (this.code) {
                        case i.DispatchErrorCodes.DISK_LOW:
                            var t = this.context,
                                n = t.available,
                                r = t.required,
                                s = (0, o.formatSize)(n, {
                                    useKibibytes: !0
                                }),
                                u = (0, o.formatSize)(r, {
                                    useKibibytes: !0
                                });
                            return a.default.Messages.NOTICE_DISPATCH_ERROR_DISK_LOW.format({
                                required: u,
                                available: s
                            });
                        case i.DispatchErrorCodes.POST_INSTALL_FAILED:
                            var c = this.context.name;
                            return a.default.Messages.NOTICE_DISPATCH_ERROR_POST_INSTALL_FAILED.format({
                                name: c
                            });
                        case i.DispatchErrorCodes.FILE_NAME_TOO_LONG:
                            return a.default.Messages.NOTICE_DISPATCH_ERROR_FILE_NAME_TOO_LONG;
                        case i.DispatchErrorCodes.POST_INSTALL_CANCELLED:
                            return a.default.Messages.NOTICE_DISPATCH_ERROR_POST_INSTALL_CANCELLED;
                        case i.DispatchErrorCodes.IO_PERMISSION_DENIED:
                            return a.default.Messages.NOTICE_DISPATCH_ERROR_IO_PERMISSION_DENIED;
                        case i.DispatchErrorCodes.NO_MANIFESTS:
                            return a.default.Messages.NOTICE_DISPATCH_ERROR_NO_MANIFESTS;
                        case i.DispatchErrorCodes.NOT_ENTITLED:
                            return a.default.Messages.NOTICE_DISPATCH_ERROR_NOT_ENTITLED;
                        case i.DispatchErrorCodes.NOT_DIRECTORY:
                        case i.DispatchErrorCodes.DISK_PERMISSION_DENIED:
                            return a.default.Messages.NOTICE_DISPATCH_ERROR_UNWRITABLE.format({
                                path: e
                            });
                        case i.DispatchErrorCodes.INVALID_DRIVE:
                            return a.default.Messages.NOTICE_DISPATCH_ERROR_INVALID_DRIVE.format({
                                path: e
                            });
                        case i.DispatchErrorCodes.APPLICATION_LOCK_FAILED:
                            return a.default.Messages.NOTICE_DISPATCH_APPLICATION_LOCK_FAILED;
                        case i.DispatchErrorCodes.DISK_FULL:
                            return a.default.Messages.NOTICE_DISPATCH_ERROR_DISK_FULL;
                        case i.DispatchErrorCodes.API_ERROR:
                        case i.DispatchErrorCodes.MAX_REQUEST_RETRIES_EXCEEDED:
                            return a.default.Messages.NOTICE_DISPATCH_API_ERROR;
                        default:
                            return a.default.Messages.NOTICE_DISPATCH_ERROR_WITH_CODE.format({
                                code: "" + this.code
                            })
                    }
                }
            }]) && s(t.prototype, n), r && s(t, r), e
        }();
        t.default = u
```

### See Private Channel IDS
<a href=""><img src="https://imgur.com/CoeFqEA.jpg" style="max-width:100%;"></a>

```bash
Object.values(webpackJsonp.push([
    [], {
        ['']: (_, e, r) => {
            e.cache = r.c
        }
    },
    [
        ['']
    ]
]).cache).find(m => m.exports && m.exports.default && m.exports.default.getPrivateChannelIds !== void 0).exports.default.getPrivateChannelIds()
```

### Support ArticleURL 

```bash
Object.values(webpackJsonp.push([
    [], {
        ['']: (_, e, r) => {
            e.cache = r.c
        }
    },
    [
        ['']
    ]
]).cache).find(m => m.exports && m.exports.default && m.exports.default.getArticleURL !== void 0).exports.default.getArticleURL("https://pornhub.com")
```

### Support ArticleURL Function
```bash
t.ActivityCount = B, B.displayName = "ActivityCount";
            var z = function(e) {
                var t = e.className;
                return S(T, {
                    className: t
                }, void 0, S(A, {
                    onClick: function() {
                        return window.open((0, h.getCurrentPlatformDownloadURL)())
                    }
                }, void 0, O.default.Messages.NUF_DOWNLOAD_APP_BUTTON_PLATFORM.format({
                    platform: (0, h.getPlatformReadableName)()
                })), S(x, {
                    className: w.default.downloadButtonSubtext
                }, void 0, O.default.Messages.INCOMPATIBLE_BROWSER.format({
                    supportedBrowserURL: m.default.getArticleURL(b.HelpdeskArticles.SUPPORTED_BROWSERS)
                })))
```


### ActionTypes 
<a href=""><img src="https://imgur.com/iy3NQlf.jpg" style="max-width:100%;"></a>
```bash
Object.values(webpackJsonp.push([
    [], {
        ['']: (_, e, r) => {
            e.cache = r.c
        }
    },
    [
        ['']
    ]
]).cache).find(m => m.exports && m.exports && m.exports.ActionTypes !== void 0).exports.ActionTypes
```
### Perms 
<a href=""><img src="https://imgur.com/xrJKtfL.jpg" style="max-width:100%;"></a>

```bash
Object.values(webpackJsonp.push([
    [], {
        ['']: (_, e, r) => {
            e.cache = r.c
        }
    },
    [
        ['']
    ]
]).cache).find(m => m.exports && m.exports && m.exports.Permissions !== void 0).exports.Permissions
```

### RPC COMMANDS 
<a href=""><img src="https://imgur.com/2YcClPC.jpg" style="max-width:100%;"></a>

```bash
Object.values(webpackJsonp.push([
    [], {
        ['']: (_, e, r) => {
            e.cache = r.c
        }
    },
    [
        ['']
    ]
]).cache).find(m => m.exports && m.exports && m.exports.RPCCommands !== void 0).exports.RPCCommands
```
### RPC COMMANDS FUNCTIONS


```bash
var y = (0, r.default)({
            CURRENT_USER_UPDATE: null,
            GUILD_STATUS: null,
            GUILD_CREATE: null,
            CHANNEL_CREATE: null,
            RELATIONSHIP_UPDATE: null,
            VOICE_CHANNEL_SELECT: null,
            VOICE_STATE_CREATE: null,
            VOICE_STATE_DELETE: null,
            VOICE_STATE_UPDATE: null,
            VOICE_SETTINGS_UPDATE: null,
            VOICE_SETTINGS_UPDATE_2: null,
            VOICE_CONNECTION_STATUS: null,
            SPEAKING_START: null,
            SPEAKING_STOP: null,
            GAME_JOIN: null,
            GAME_SPECTATE: null,
            ACTIVITY_JOIN: null,
            ACTIVITY_JOIN_REQUEST: null,
            ACTIVITY_SPECTATE: null,
            ACTIVITY_INVITE: null,
            NOTIFICATION_CREATE: null,
            MESSAGE_CREATE: null,
            MESSAGE_UPDATE: null,
            MESSAGE_DELETE: null,
            LOBBY_DELETE: null,
            LOBBY_UPDATE: null,
            LOBBY_MEMBER_CONNECT: null,
            LOBBY_MEMBER_DISCONNECT: null,
            LOBBY_MEMBER_UPDATE: null,
            LOBBY_MESSAGE: null,
            CAPTURE_SHORTCUT_CHANGE: null,
            OVERLAY: null,
            OVERLAY_UPDATE: null,
            ENTITLEMENT_CREATE: null,
            ENTITLEMENT_DELETE: null,
            USER_ACHIEVEMENT_UPDATE: null,
            READY: null,
            ERROR: null
```
### Has Animated Avatar Check 

```bash
Object.values(webpackJsonp.push([
    [], {
        ['']: (_, e, r) => {
            e.cache = r.c
        }
    },
    [
        ['']
    ]
]).cache).find(m => m.exports && m.exports.default && m.exports.default.hasAnimatedAvatar !== void 0).exports.default.hasAnimatedAvatar()
```

### Has Animated Avatar Check Function 
```bash
function(e, t, r) {
            "use strict";
            Object.defineProperty(t, "__esModule", {
                value: !0
            }), t.getChannelIconURL = function(e, t) {
                switch (e.type) {
                    case l.ChannelTypes.DM:
                        var r = e.recipients.map(n.default.getUser).filter(o.isNotNullish)[0];
                        return null == r ? null : !0 === t && a.default.hasAnimatedAvatar(r) ? r.getAvatarURL("gif") : r.getAvatarURL();
                    case l.ChannelTypes.GROUP_DM:
                        return a.default.getChannelIconURL({
                            id: e.id,
                            icon: e.icon,
                            applicationId: e.getApplicationId()
                        })
```



### Can Use Emojis An 
```bash
Object.values(webpackJsonp.push([
    [], {
        ['']: (_, e, r) => {
            e.cache = r.c
        }
    },
    [
        ['']
    ]
]).cache).find(m => m.exports && m.exports.default && m.exports.default.canUseAnimatedEmojis !== void 0).exports.default.canUseAnimatedEmojis("" + true) + true
```

### Can Use Emojis Everywhere
```bash
Object.values(webpackJsonp.push([
    [], {
        ['']: (_, e, r) => {
            e.cache = r.c
        }
    },
    [
        ['']
    ]
]).cache).find(m => m.exports && m.exports.default && m.exports.default.canUseEmojisEverywhere !== void 0).exports.default.canUseEmojisEverywhere()
```
### Can Use Emojis EveryWhere Function
```bash
var d = u({
                sanitizeEmojiName: function(e) {
                    for (e = e.replace(a.EMOJI_RE, "").slice(0, a.EMOJI_MAX_LENGTH); e.length < 2;) e += "_";
                    return e
                },
                getURL: function(e) {
                    return ""
                },
                filterUnsupportedEmojis: function(e) {
                    return e
                }
            }, n(1690).default, {
                isEmojiFiltered: function(e, s) {
                    var n = i.default.getCurrentUser();
                    if (!e.guildId) return !1;
                    if (null == s || !(0, r.isGuildTextChannelType)(s.type)) return !1;
                    var o = e.guildId === s.getGuildId(),
                        f = t.default.can(a.Permissions.USE_EXTERNAL_EMOJIS, n, s);
                    return !o && !f
                },
                isEmojiDisabled: function(e, s, n) {
                    void 0 === n && (n = !0);
                    var f = i.default.getCurrentUser();
                    if (!e.guildId) return !1;
                    if (e.animated && !o.default.canUseAnimatedEmojis(f)) return !0;
                    if (!e.available) return !0;
                    if (null != s && (0, r.isGuildTextChannelType)(s.type)) {
                        var u = e.guildId === s.getGuildId(),
                            d = t.default.can(a.Permissions.USE_EXTERNAL_EMOJIS, f, s),
                            _ = e.managed || o.default.canUseEmojisEverywhere(f);
                        return !u && !(!u && d && _)
                    }
                    return !o.default.canUseEmojisEverywhere(f) && !(e.managed && n)
                },
                isInternalEmojiForGuildId: function(e, s) {
                    return null == e.guildId || s === e.guildId
                }
            });
```


### Get Status
<a href=""><img src="https://imgur.com/mCVaVmA.jpg" style="max-width:100%;"></a>

```bash
Object.values(webpackJsonp.push([
    [], {
        ['']: (_, e, r) => {
            e.cache = r.c
        }
    },
    [
        ['']
    ]
]).cache).find(m => m.exports && m.exports.default && m.exports.default.getStatus !== void 0).exports.default.getStatus()
```

### Get Status Function 


```bash
  function I() {
                var e = f.default.getId();
                c[e] = u.default.getStatus(), v[e] = u.default.getActivities()
```


### getOnlineFriendCount 
```bash
Object.values(webpackJsonp.push([
    [], {
        ['']: (_, e, r) => {
            e.cache = r.c
        }
    },
    [
        ['']
    ]
]).cache).find(m => m.exports && m.exports.default && m.exports.default.getOnlineFriendCount !== void 0).exports.default.getOnlineFriendCount()
```

### Get Online Friend Count Function 
```bash
i.getOnlineFriendCount = function() {
                    return y.size
```


### Get All Users IDS 
<a href=""><img src="https://imgur.com/4ZV4AuF.jpg" style="max-width:100%;"></a>


```bash
Object.values(webpackJsonp.push([
    [], {
        ['']: (_, e, r) => {
            e.cache = r.c
        }
    },
    [
        ['']
    ]
]).cache).find(m => m.exports && m.exports.default && m.exports.default.getUserIds !== void 0).exports.default.getUserIds()
```

### Get All Users Function
```bash
 i.getUserIds = function() {
                    return Object.keys(v)
```



### Get State
```bash
Object.values(webpackJsonp.push([
    [], {
        ['']: (_, e, r) => {
            e.cache = r.c
        }
    },
    [
        ['']
    ]
]).cache).find(m => m.exports && m.exports.default && m.exports.default.getState !== void 0).exports.default.getState()
```
### Get State Function
```bash
i.getState = function() {
                    return {
                        presencesForGuilds: m,
                        statuses: c,
                        activities: v,
                        activityMetadata: h,
                        onlineFriends: y,
                        clientStatuses: l
                    }
```


### Get Accounts
<a href=""><img src="https://imgur.com/OU7C8mm.jpg" style="max-width:100%;"></a>


```bash
Object.values(webpackJsonp.push([
    [], {
        ['']: (_, e, r) => {
            e.cache = r.c
        }
    },
    [
        ['']
    ]
]).cache).find(m => m.exports && m.exports.default && m.exports.default.getAccounts !== void 0).exports.default.getAccounts()
```
