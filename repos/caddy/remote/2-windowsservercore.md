## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:6c6c60e76b33eff11d4a547a3848f59fa339fb31730857d17774168c2972ea40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `caddy:2-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull caddy@sha256:b61ad9da2fadd4591d8824968bc0ce1c49973e69931364e497ea369d170b26bb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279629401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce47f0b935d72310424d53148d916905a1f315f11960967cfaf0ba2bc510780`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:45:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:45:52 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 13 Feb 2025 00:45:53 GMT
ENV CADDY_VERSION=v2.9.1
# Thu, 13 Feb 2025 00:46:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 13 Feb 2025 00:46:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 13 Feb 2025 00:46:02 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 13 Feb 2025 00:46:03 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Thu, 13 Feb 2025 00:46:03 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 13 Feb 2025 00:46:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 13 Feb 2025 00:46:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 13 Feb 2025 00:46:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 13 Feb 2025 00:46:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 13 Feb 2025 00:46:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 13 Feb 2025 00:46:06 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 13 Feb 2025 00:46:06 GMT
EXPOSE 80
# Thu, 13 Feb 2025 00:46:07 GMT
EXPOSE 443
# Thu, 13 Feb 2025 00:46:07 GMT
EXPOSE 443/udp
# Thu, 13 Feb 2025 00:46:08 GMT
EXPOSE 2019
# Thu, 13 Feb 2025 00:46:15 GMT
RUN caddy version
# Thu, 13 Feb 2025 00:46:15 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e41cccbee3b7b19086675e1fecabf5d495113760de54ae6ef3b2774682cf42`  
		Last Modified: Thu, 13 Feb 2025 00:46:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907e0effdcbda7ebdf76a13c2d82684e5efce41ca0c97a5e6b9bcdb908350bd4`  
		Last Modified: Thu, 13 Feb 2025 00:46:25 GMT  
		Size: 380.0 KB (379994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d6bf559f3880a70fda32069c8c89dafa48ba65fc0b5e594c8c25c2123a4b48`  
		Last Modified: Thu, 13 Feb 2025 00:46:25 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8296c0ac971dabe500d7091da17e83c5445e07a19999c62229d95a26dc01ccdb`  
		Last Modified: Thu, 13 Feb 2025 00:46:27 GMT  
		Size: 15.0 MB (15021107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998a23d1eeb52dc745372a404b10b0adb33da8aa31d9d724251f3dfc22cf12fb`  
		Last Modified: Thu, 13 Feb 2025 00:46:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc79e728ff49838c3ed7a5a75915eb92182cf00a3719070e9c6f4f5993c56398`  
		Last Modified: Thu, 13 Feb 2025 00:46:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a212af2c7c6994c05cc9506ab6f506fdbce7e26ba46d3c645906f31c8e7b99`  
		Last Modified: Thu, 13 Feb 2025 00:46:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf155be37ec718e07d2fb6f40b8e1410c475d605afcd14b2b4cb29fff3f7fcc`  
		Last Modified: Thu, 13 Feb 2025 00:46:23 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9e9a946a30b8bc2a868c02d6fdbfedeb7b28e9425648ea18c95a994e909791`  
		Last Modified: Thu, 13 Feb 2025 00:46:23 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10966475d5967c7f03c9835e89451a7bed3f11f808629710cf383dfc5b129d68`  
		Last Modified: Thu, 13 Feb 2025 00:46:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd69b9ea4cb024c88119e048b9f054d013075e41d97962920a489d2cba8087a9`  
		Last Modified: Thu, 13 Feb 2025 00:46:21 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0f6167f97093c9111c3090e56cbc2e5f8745c6d087212a35d92fb928d74bab`  
		Last Modified: Thu, 13 Feb 2025 00:46:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb4f62bf76cdcb8c74817574598da9db4a98b11c8fc8c81e7be7c6cbef52b22`  
		Last Modified: Thu, 13 Feb 2025 00:46:21 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51b2ff2c7c4952d98053c97ac99bca7f12a4b504c35ad035b650cd8d1df353d`  
		Last Modified: Thu, 13 Feb 2025 00:46:21 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93b0d5bdd5a3e6b274e5bccc116b96525cf372e89c5caaf343a214808b1a264`  
		Last Modified: Thu, 13 Feb 2025 00:46:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336b5eda6e8d6160852cfe83c5894481d9c0910bc767d465500b30e809e3c451`  
		Last Modified: Thu, 13 Feb 2025 00:46:19 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f38a4b52d5e1d6ce847270700fa4b8157b620dae2f8679ed49d8f5e181cbef`  
		Last Modified: Thu, 13 Feb 2025 00:46:19 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d71b602e416881d7f3c210b44cdb395befd8f05aab509ac4f59daf7ba5fb9d`  
		Last Modified: Thu, 13 Feb 2025 00:46:19 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce12d149bf7a73a25976c90231722206f0712bff0a7277b612bac3113e44bd3d`  
		Last Modified: Thu, 13 Feb 2025 00:46:19 GMT  
		Size: 348.3 KB (348300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb9cf9d14f3f82df84f1cc6aac34c24104981b501dc734d6d9580eac35e4eaf`  
		Last Modified: Thu, 13 Feb 2025 00:46:19 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull caddy@sha256:bc2c74310d3822c94bee5b60a05f2a2603e1bc5d713342e9564df65b829e5fb8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2152624375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c21cc01a2b6e1af3ed0f5f775e6d596bbb6522ddd9804f362b0230c7c301905`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:39:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:40:17 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 13 Feb 2025 00:40:18 GMT
ENV CADDY_VERSION=v2.9.1
# Thu, 13 Feb 2025 00:40:30 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 13 Feb 2025 00:40:31 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 13 Feb 2025 00:40:31 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 13 Feb 2025 00:40:32 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Thu, 13 Feb 2025 00:40:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 13 Feb 2025 00:40:33 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 13 Feb 2025 00:40:34 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 13 Feb 2025 00:40:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 13 Feb 2025 00:40:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 13 Feb 2025 00:40:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 13 Feb 2025 00:40:36 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 13 Feb 2025 00:40:37 GMT
EXPOSE 80
# Thu, 13 Feb 2025 00:40:38 GMT
EXPOSE 443
# Thu, 13 Feb 2025 00:40:38 GMT
EXPOSE 443/udp
# Thu, 13 Feb 2025 00:40:39 GMT
EXPOSE 2019
# Thu, 13 Feb 2025 00:40:43 GMT
RUN caddy version
# Thu, 13 Feb 2025 00:40:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da71ca3c978efd42e5c7844d85732fce6ee019eee467aac822c734fdce662983`  
		Last Modified: Thu, 13 Feb 2025 00:40:49 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af86a4d6da8deeaf59f769c96324f7e229367777907778e164f026f958e3f3e1`  
		Last Modified: Thu, 13 Feb 2025 00:40:50 GMT  
		Size: 350.7 KB (350711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411f6a2e270a7121d8d17ed30cb596b88c8756acfc0bb44067a348e7cf4322fb`  
		Last Modified: Thu, 13 Feb 2025 00:40:49 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6bffa557db47723ee7935062e0535c86a874864121afd6ada7ee7d29838bd9`  
		Last Modified: Thu, 13 Feb 2025 00:40:51 GMT  
		Size: 15.0 MB (15004171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220cc9ac253b1d1cd442c0ce37279bcc3d8d6aeb3093ab80c83327984a60e8e3`  
		Last Modified: Thu, 13 Feb 2025 00:40:49 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51245cd639bf725fa680c91f6c5ec5fe5266342fc3feda5ceae3717953d0a77a`  
		Last Modified: Thu, 13 Feb 2025 00:40:48 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83422abd41e8a5c458ad70774a46c5ebce307ec0139370f8b899aed0079c7831`  
		Last Modified: Thu, 13 Feb 2025 00:40:48 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8a6eebf28c6625db05b535c2cb1ebe70a3b97fa775ab77783b3eb3899ee303`  
		Last Modified: Thu, 13 Feb 2025 00:40:48 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89747d6377b59b6ea156f3a2444100b32a539c84fe44f6a660521eba36cc7df`  
		Last Modified: Thu, 13 Feb 2025 00:40:48 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe479970f4d7e10609579c5f45c4dd92de3f47304bdf351b04367b28d10bfef7`  
		Last Modified: Thu, 13 Feb 2025 00:40:48 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bd85cbc9a467590ad681c9fa8ec13fc0d1b37bc7d3aef848fde7e2c17a0308`  
		Last Modified: Thu, 13 Feb 2025 00:40:47 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351146b60cdcd553a3affcf859abfe2c74286fb922484acb7bc957dc141cce65`  
		Last Modified: Thu, 13 Feb 2025 00:40:47 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059b6afa03fb9efcd00306804704cb7c42b9718dbb1e11bc3c9dd9006a415a0f`  
		Last Modified: Thu, 13 Feb 2025 00:40:47 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abd6c8cf2abd77050eeb49397379efef5cd8c0e16f013e0bf4cbc616bffee43`  
		Last Modified: Thu, 13 Feb 2025 00:40:47 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf659276e4132838201d9a2e1010b043be70c93418c23a48f69cd1f8dc850389`  
		Last Modified: Thu, 13 Feb 2025 00:40:47 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982bfd32dff5d2093439348de91c94db7a85f0fb79a4e4ca6ed7d7025ce98358`  
		Last Modified: Thu, 13 Feb 2025 00:40:46 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8195f69f90da77d3422d74e79fc2025794f83d684a9214dc8799c19bcaf11abd`  
		Last Modified: Thu, 13 Feb 2025 00:40:46 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493a32384f4efc6e3b6e5254c996e5122702c2937b31f9a3829a4405e6ce63d7`  
		Last Modified: Thu, 13 Feb 2025 00:40:46 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4ab44d66e61f7123dfcfaa261ac137805c9387e4ef076a0b7a82d3dfa30401`  
		Last Modified: Thu, 13 Feb 2025 00:40:46 GMT  
		Size: 338.0 KB (337951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c5bb087eb0f37ce7b74fa90d5cc26271241dd133b7bd7aa39277f782786773`  
		Last Modified: Thu, 13 Feb 2025 00:40:46 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
