## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:40c4f77513048ee7e05ee01fb89d360e22b13325c3daaffca57dee62c72b575d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64
	-	windows version 10.0.14393.3930; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.1457; amd64

```console
$ docker pull caddy@sha256:6fdda8066ebb2cfcbb65432af3efad7ecef7f89d4b5a2e0b325692d95ea4e3b9
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2378390339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a3b078a6f6a6627a26f04efe9831b83aa9ce0bbb6249c8b0f92d7a50881c02`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Sep 2020 19:53:27 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 09 Sep 2020 19:54:04 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Sep 2020 19:54:05 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 09 Sep 2020 19:54:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Sep 2020 19:54:36 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Sep 2020 19:54:37 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Sep 2020 19:54:38 GMT
VOLUME [c:/config]
# Wed, 09 Sep 2020 19:54:39 GMT
VOLUME [c:/data]
# Wed, 09 Sep 2020 19:54:40 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 09 Sep 2020 19:54:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Sep 2020 19:54:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Sep 2020 19:54:42 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Sep 2020 19:54:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Sep 2020 19:54:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Sep 2020 19:54:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Sep 2020 19:54:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Sep 2020 19:54:45 GMT
EXPOSE 80
# Wed, 09 Sep 2020 19:54:46 GMT
EXPOSE 443
# Wed, 09 Sep 2020 19:54:46 GMT
EXPOSE 2019
# Wed, 09 Sep 2020 20:25:17 GMT
RUN caddy version
# Wed, 09 Sep 2020 20:25:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c325b871c49357c593876a98f079c074af004dee2cb9cf372880b2cd25fd6a0c`  
		Last Modified: Wed, 09 Sep 2020 20:29:31 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc5eb7f2e0263c6213fc9423cf6eb719de3f7c849643ccdabec913b618f41ad`  
		Last Modified: Wed, 09 Sep 2020 20:29:39 GMT  
		Size: 9.1 MB (9137985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5a77a42e4acde519b57884bb795f3dc263fa0169242832aa756ec95c04dddd`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ef31d9b01fa7c0d2d8b5dc3eb4d389001034b74d7d472cc951df62d115118`  
		Last Modified: Wed, 09 Sep 2020 20:29:48 GMT  
		Size: 17.7 MB (17672633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665a7d301d80ee07b021c74d836eb43352e05ce53a3480b8d9e24d99186bbfbf`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0770a21ef08a40302425e6476fe8c78962bc91e1f2e01ce71d58b44d1eec27ff`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74371eb56f1a9b6b6e10b2915999a33587eecd4cf57dc6442471c378718c1062`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3517d1abc56a70595cf5ae149a9f2843e8fa9eaa2c2f3c9e793cacc8e117dc3`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4bf115547c84fde7026e799220c3a33867058af6f6b469f7f6cad4fb501342`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ba56b6ad310ca4acd04b36bab15c11509edd717eacc8a7a31c575becf2e58c`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8e5887ab35d7d9526248c8ba42cd34560054c2eda04112f03bbb2c7051df82`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced70216aec7f6562500c53e1cb318c4f5fbd754b45dfd4778796eddcc3f44bf`  
		Last Modified: Wed, 09 Sep 2020 20:29:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d064b47540d3a0413e187206009b7420d041bc2abe86a2bdb159421da8a76e63`  
		Last Modified: Wed, 09 Sep 2020 20:29:24 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370539f66a716c49521cd612333716543831af692859d7406721cef7ac87476d`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c29ac445b054afa01e8bd41bdb11ba36d5af91e515aaf7abe5a6a156d838b4`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173743838549e9d6d35bf843fd1d0d578b7ff6f4353e4e14c9b62ac16d750efb`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2116539be5612b7b677cc16f59fd8f7268ad3b1bea415498c4b31c99e1ca4565`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaed27ebe4f3042ae55963898c25ebf1f39d9e362ba02b80ddcefd0f40f3146`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc079d30d61f51e726e25d5f65fad824d0749aefa98e25d25b1562b8785c753`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f7fdcbced701ca09049814e389bdab25b50586d869b3191093f5e9066efcd0`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 285.9 KB (285915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2630294809bc2c1fcd1b1976547723b64c5e7ed91f008f6f7ef23c871474a7fa`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.14393.3930; amd64

```console
$ docker pull caddy@sha256:c399072135a67ae1bf41ddf60b732de7e9d1513000021162c25f1a1471c07f95
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5772293185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb680f013a85014fccf399ba08c16d449ca381f1a5154276bc2b49470ac8f942`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 01 Sep 2020 19:14:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 08 Sep 2020 19:31:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Sep 2020 20:25:23 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 09 Sep 2020 20:26:37 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Sep 2020 20:26:38 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 09 Sep 2020 20:28:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Sep 2020 20:28:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Sep 2020 20:28:02 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Sep 2020 20:28:03 GMT
VOLUME [c:/config]
# Wed, 09 Sep 2020 20:28:04 GMT
VOLUME [c:/data]
# Wed, 09 Sep 2020 20:28:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 09 Sep 2020 20:28:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Sep 2020 20:28:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Sep 2020 20:28:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Sep 2020 20:28:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Sep 2020 20:28:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Sep 2020 20:28:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Sep 2020 20:28:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Sep 2020 20:28:11 GMT
EXPOSE 80
# Wed, 09 Sep 2020 20:28:12 GMT
EXPOSE 443
# Wed, 09 Sep 2020 20:28:12 GMT
EXPOSE 2019
# Wed, 09 Sep 2020 20:28:52 GMT
RUN caddy version
# Wed, 09 Sep 2020 20:28:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bc202b498d589027cc702b23cf959b8842907508b3465b9d6ff739c9668e5134`  
		Size: 1.7 GB (1669268544 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f6f82df7cca9113965bd35d2921a651250266aa7a3a9df6a0a42e8c005f1333`  
		Last Modified: Tue, 08 Sep 2020 19:53:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a449faf0a811f283e675b95675b755ed5caeaf09c377b034b4730f6451aa51`  
		Last Modified: Wed, 09 Sep 2020 20:30:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3226e2cab68073e9c97dacb0b90ecf5fec0142f1690d3ce6268fbe7236afc5`  
		Last Modified: Wed, 09 Sep 2020 20:30:24 GMT  
		Size: 9.9 MB (9897398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761d232ac4fd149d90e5347a5bd38a319bfb55a301c1a111b6503356911322b8`  
		Last Modified: Wed, 09 Sep 2020 20:30:13 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c767daadf962c116a6b9c0a3515446a8b285066125527c4222daf121a40a2ad7`  
		Last Modified: Wed, 09 Sep 2020 20:30:18 GMT  
		Size: 22.9 MB (22872196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b987d95380ab88f45603aaaed62a622130e9e3fdfaf920f4f75bce40bae1a635`  
		Last Modified: Wed, 09 Sep 2020 20:30:12 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d802d13151eefdd188af28474ad33dc2a1c63c9403c1ed769da6d40b0e54a806`  
		Last Modified: Wed, 09 Sep 2020 20:30:12 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26007a9ef743163079afd033ec88dc054a50a1691ceb86abf06c3027fb4e5960`  
		Last Modified: Wed, 09 Sep 2020 20:30:10 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42df9545735b7e2fd0e54384a7d867cb94d15f421965a72064960cd7b8884700`  
		Last Modified: Wed, 09 Sep 2020 20:30:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91bd9d5351e7b6f497b9506e976a1e9a722f4c1e3a99e8a476e1a7bda5fd3f4`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fdc70bbab6bb9610494fc861f433042c460157a65717802379ddf4da12e81e`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b663a9f158ac2229e071d383cec9f621fd28f6b0652215f5b4b4450b58dc68a1`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a243df49719e70d6a15b261449414bc069ffdd04a552563e129e402e3cc129`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2d8f5da7ba33566df13bc15bfa47c970f50f27d4a373e0ad2085ff6435ffb4`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05d556209c77456fc89bd1484059081409259c5946aa6fc367179ceaca4674d`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1f5c7e3672363102592a251895dd3aebe3b1ffb623b0b03712525571abf474`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1deca8290b7668c1e16e216ed2040490186e8013ee60f992ab46347e92ccfde5`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713887e22bbfa9481da702fba31404d11d79a9952c0ba63e8db952c7ab063b6d`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087dd32d3c1a6a7665699ccc8a08848a94b90c86b352804c29de30be754c7508`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0202c220609d5cf8ed133c56b31a32168cf749346cdd1453edc215f62cd09a8f`  
		Last Modified: Wed, 09 Sep 2020 20:30:05 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0823fb990936970db69fcf021f5cf762bcf64bf24669f09449c6f578ddd6f2`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 247.5 KB (247496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab51024f33e212313a4c9be7fb692bf2a599f8b8095c80c62127268d4ce704d3`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
