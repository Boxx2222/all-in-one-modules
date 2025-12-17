# all-in-one-modules
All_In_One_6_Modules.sgmodule
#!name=All In One – 6 Modules
#!desc=SoundCloud Go+, YouTube Adblock, OldRoll, PicsArt, Spotify VIP, Locket Gold
#!author=Boxx2222

[Script]

# ===== SoundCloud Go+ =====
soundcloud=type=http-response,pattern=https:\/\/api-mobile\.soundcloud\.com\/configuration\/ios,requires-body=1,script-path=https://raw.githubusercontent.com/Marol62926/MarScrpt/main/soundcloud.js

# ===== YouTube AdBlock =====
youtube=type=http-response,pattern=^https:\/\/youtubei\.googleapis\.com\/youtubei\/v1\/(browse|next|player|search|reel\/reel_watch_sequence|guide|account\/get_setting|get_watch),requires-body=1,binary-body-mode=1,max-size=-1,script-path=https://raw.githubusercontent.com/Maasea/sgmodule/master/Script/Youtube/youtube.response.js

# ===== OldRoll VIP =====
oldroll=type=http-response,pattern=^https?:\/\/buy\.itunes\.apple\.com\/verifyReceipt$,requires-body=1,script-path=https://raw.githubusercontent.com/yqc007/QuantumultX/master/OldRollFVIPCrack.js

# ===== PicsArt Premium =====
picsart=type=http-response,pattern=https:\/\/api\.(picsart|meiease)\.c(n|om)\/users\/show\/me\.json,requires-body=1,max-size=0,script-path=https://raw.githubusercontent.com/NobyDa/Script/master/Surge/JS/PicsArt.js

# ===== Spotify VIP =====
spotify-json=type=http-request,pattern=^https:\/\/(spclient\.wg\.spotify\.com|.*-spclient\.spotify\.com(:443)?)\/(artistview\/v1\/artist|album-entity-view\/v2\/album)\/,script-path=https://raw.githubusercontent.com/app2smile/rules/master/js/spotify-json.js
spotify-proto=type=http-response,pattern=^https:\/\/(spclient\.wg\.spotify\.com|.*-spclient\.spotify\.com(:443)?)\/(bootstrap\/v1\/bootstrap|user-customization-service\/v1\/customize)$,requires-body=1,binary-body-mode=1,max-size=0,script-path=https://raw.githubusercontent.com/app2smile/rules/master/js/spotify-proto.js

# ===== Locket Gold =====
revenuecat=type=http-response,pattern=^https:\/\/api\.revenuecat\.com\/.+\/(receipts$|subscribers\/[^/]+$),script-path=https://raw.githubusercontent.com/DungHoang120401/Nobita/refs/heads/main/Scripts/Locket_Gold.js,requires-body=true,max-size=-1,timeout=60
deleteHeader=type=http-request,pattern=^https:\/\/api\.revenuecat\.com\/.+\/(receipts|subscribers),script-path=https://raw.githubusercontent.com/DungHoang120401/Nobita/refs/heads/main/Scripts/LKG_delete_header.js,timeout=60

[MITM]
hostname = %APPEND% \
api-mobile.soundcloud.com, \
youtubei.googleapis.com,*.googlevideo.com,www.youtube.com,s.youtube.com, \
buy.itunes.apple.com, \
api.picsart.com,api.meiease.com, \
spclient.wg.spotify.com,*spclient.spotify.com, \
api.revenuecat.com