## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:1e38bd5242948d952cfdfef0f556ec13f3c3deed3b6cb6d434286c1fa2b7c507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.825; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.825; amd64

```console
$ docker pull caddy@sha256:e1bec125312096b58f79d5b577a0653739b529379193387519e298b23601ac8b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2315502859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa5a325e046244a165d0c7955b04945736acd92975b1cd562404b33793d5beb`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Jul 2022 21:05:32 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/69bb1c539b3ee03fc91271a71653a77ca1e9d131/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/69bb1c539b3ee03fc91271a71653a77ca1e9d131/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 Jul 2022 21:05:33 GMT
ENV CADDY_VERSION=v2.5.1
# Tue, 12 Jul 2022 21:06:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.1/caddy_2.5.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4294796c4bd4bed0c593d83606a5413de30f35f88d624e1b1e5b6cd8672ffbcc7a689d7ce4ef30c1abea0e95eda62220faac15d2a6aca0c3e2b418abe7a74118')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 Jul 2022 21:06:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 Jul 2022 21:06:02 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 Jul 2022 21:06:04 GMT
LABEL org.opencontainers.image.version=v2.5.1
# Tue, 12 Jul 2022 21:06:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 Jul 2022 21:06:05 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 Jul 2022 21:06:06 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 Jul 2022 21:06:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 Jul 2022 21:06:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 Jul 2022 21:06:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 Jul 2022 21:06:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 Jul 2022 21:06:11 GMT
EXPOSE 80
# Tue, 12 Jul 2022 21:06:11 GMT
EXPOSE 443
# Tue, 12 Jul 2022 21:06:12 GMT
EXPOSE 2019
# Tue, 12 Jul 2022 21:06:30 GMT
RUN caddy version
# Tue, 12 Jul 2022 21:06:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b663eff38faad72244f8548731bf581964c01831187244566c697f3bcf94ca`  
		Last Modified: Tue, 12 Jul 2022 21:09:36 GMT  
		Size: 662.2 KB (662249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e468f072008ddbfd7e2528cbb303d2a9d97ffd16de53731d25cdb976086dd5`  
		Last Modified: Tue, 12 Jul 2022 21:09:36 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6b155a7e8806d23e43b6bc343d1b0db43a55a1322020ec019deada3fab35f6`  
		Last Modified: Tue, 12 Jul 2022 21:09:40 GMT  
		Size: 14.2 MB (14245039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8549abe12330bf88674122311a83239cb196d623dedd7ddfd34e94516f45eed4`  
		Last Modified: Tue, 12 Jul 2022 21:09:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce0bbc04a2295bd3e9ed45e9f9515634f6ed3be80abd2e2061d184a2e730892`  
		Last Modified: Tue, 12 Jul 2022 21:09:34 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e474c9f2b15c6b5e6cbcb57b116d43f686815a7e7ad475ece49c330eea3377`  
		Last Modified: Tue, 12 Jul 2022 21:09:34 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460e528a456494d9750219cb82330a2fb454311f86f4b83b0eab6f52a832ed8a`  
		Last Modified: Tue, 12 Jul 2022 21:09:33 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f4578aa914d92629a25fbb501e099295c94db63200d1a9021c2758689c84a1`  
		Last Modified: Tue, 12 Jul 2022 21:09:33 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f74b10adddfd2a771b5a4752cc082a40e30f4cd85e86327fd92148f78ea56`  
		Last Modified: Tue, 12 Jul 2022 21:09:32 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0476848a862539a06b32e1ec82f556135288512c6394ccf7cef952d9040b5d29`  
		Last Modified: Tue, 12 Jul 2022 21:09:31 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0c126d62749fdd37a034b38717997581a9057a3f441b2e30f228f9a57d5275`  
		Last Modified: Tue, 12 Jul 2022 21:09:31 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa39e635a66b534ee7dd3538744dd3f8603a59c4fac9abbf974b226d2624671`  
		Last Modified: Tue, 12 Jul 2022 21:09:32 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7109f8c2f46ce79dc903ac36ee7e16569f2bd6ed24c352137d5e929776c2d80f`  
		Last Modified: Tue, 12 Jul 2022 21:09:31 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e644e88f94ba2df58a3ce7cff64489be1aa5ad1670094b385c6a99caf729d4f`  
		Last Modified: Tue, 12 Jul 2022 21:09:29 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aad12ddd0064eafa56e1acfb3098b5935a51b82f939b3c2721aa47ae249fbe7`  
		Last Modified: Tue, 12 Jul 2022 21:09:29 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8f5e772abab28df039764c06865eadd2334f25365de8c5ae7606768f660b5a`  
		Last Modified: Tue, 12 Jul 2022 21:09:29 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89798db4399cbb2ee3f184326a624db393aa9a56512e8ae1a8ae61b9b8844788`  
		Last Modified: Tue, 12 Jul 2022 21:09:29 GMT  
		Size: 341.6 KB (341589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a993e9151d5c25b74f703ce7fe0ecae20cf1b1601cc65ffca749bf245781af`  
		Last Modified: Tue, 12 Jul 2022 21:09:29 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
