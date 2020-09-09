## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:54fc1c11a9a4de45c0e3b30aa2702ac0e55d355cd47e3f7f4fbfdc475bc6c132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.1457; amd64

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
