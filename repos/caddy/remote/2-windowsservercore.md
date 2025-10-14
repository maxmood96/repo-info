## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:449a4c5d46c9db58f46b9c3a23dfdb947cd9ad4fb7ec1c9e6b63ba229674f572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `caddy:2-windowsservercore` - windows version 10.0.26100.6899; amd64

```console
$ docker pull caddy@sha256:3d3fb33648d867bdc8c2862cbecc8b31fb1e2fc83e4131befaa5706062d59010
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 GB (3237779321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b193fec8eae40f91efd1fa1f5f4d7b8b33fd346e3d35bfd91d133c7850f25d6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:55:27 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 14 Oct 2025 20:55:28 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 14 Oct 2025 20:55:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 14 Oct 2025 20:55:37 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 14 Oct 2025 20:55:37 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 14 Oct 2025 20:55:38 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Tue, 14 Oct 2025 20:55:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 14 Oct 2025 20:55:39 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 14 Oct 2025 20:55:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 14 Oct 2025 20:55:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 14 Oct 2025 20:55:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 14 Oct 2025 20:55:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 14 Oct 2025 20:55:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 14 Oct 2025 20:55:44 GMT
EXPOSE 80
# Tue, 14 Oct 2025 20:55:44 GMT
EXPOSE 443
# Tue, 14 Oct 2025 20:55:45 GMT
EXPOSE 443/udp
# Tue, 14 Oct 2025 20:55:46 GMT
EXPOSE 2019
# Tue, 14 Oct 2025 20:55:50 GMT
RUN caddy version
# Tue, 14 Oct 2025 20:55:51 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431b021ad59bb881549df3a2d34593558b8b25e5b6fddfbdd088d49ff570b06a`  
		Last Modified: Tue, 14 Oct 2025 20:50:45 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213e81745130409bd0691074d3b2836bad7ce4fa026d6185ae1a406135c68862`  
		Last Modified: Tue, 14 Oct 2025 20:56:11 GMT  
		Size: 366.7 KB (366737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52e742f88d6a48b4949842d0672f992f65e7cd715a89a7edd001af288b605cc`  
		Last Modified: Tue, 14 Oct 2025 20:56:11 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375009b442d93cd55cdf798643d3a76298cfd23f935315f54f004bd45cc4401b`  
		Last Modified: Tue, 14 Oct 2025 20:56:13 GMT  
		Size: 16.6 MB (16568196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f351a0a7f625a4b23b48440de225568e5fe6fd36ddb9c81756455893108f7f23`  
		Last Modified: Tue, 14 Oct 2025 20:56:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b906303cc0ab3b206ac5343bfe62cda861bc1de0365e514a08fffb033c03f7`  
		Last Modified: Tue, 14 Oct 2025 20:56:11 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0c524a1ea8681339fb8ea4a54895f99c6a9723482c968b0b8ee3a4c164bb08`  
		Last Modified: Tue, 14 Oct 2025 20:56:11 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f40299a7e03fad9152578aa2e1879bfe07c86252cef4a72acfc554c81a034c`  
		Last Modified: Tue, 14 Oct 2025 20:56:11 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8b8220afe9b8700768947827d140800b41001a83867b8f3e45cbe509a8da09`  
		Last Modified: Tue, 14 Oct 2025 20:56:11 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b0232f732a848de85311880de44353e998efa51373ca6234aae314a6c62752`  
		Last Modified: Tue, 14 Oct 2025 20:56:11 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b164f4dc228d166a5d4e1c1ce454f9675d6c972a4144a664f36d313098d20606`  
		Last Modified: Tue, 14 Oct 2025 20:56:12 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0d67567eccf55c1158533f87ee9e335a587212531b6cf04b07e43e788279a5`  
		Last Modified: Tue, 14 Oct 2025 20:56:10 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b8af79ab8c60fbc8e4826c6657e292104a7725f58c706cd4458f4ef46d9aab`  
		Last Modified: Tue, 14 Oct 2025 20:56:10 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9411362674e4961fffe4fc521463315e04e99353842697fadd6b6d23bcc8523`  
		Last Modified: Tue, 14 Oct 2025 20:56:10 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f42952f5dcead564f4294ced6fd157a3f10ccfc264a80f7c7b1ed0574cbde4`  
		Last Modified: Tue, 14 Oct 2025 20:56:10 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5756c571a747045882226166bb15bda90a9b9098918a336f7e29cb74830f3b5d`  
		Last Modified: Tue, 14 Oct 2025 20:56:10 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cb20cad1bbe373f903b7ad3d2dc0cc0dce1d8d0cd4633291ce4f4b9efb05b8`  
		Last Modified: Tue, 14 Oct 2025 20:56:10 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5810fb0e9c0a621b963f28628c693edc2a726748645afe5d66da13fe6def6023`  
		Last Modified: Tue, 14 Oct 2025 20:56:10 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3cd9156a28c5414cf778a6790f9994c3ee5d7c3b2376919969bdce96b9ac173`  
		Last Modified: Tue, 14 Oct 2025 20:56:10 GMT  
		Size: 341.5 KB (341497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b543c9308bcf6cb74d9303f3b6cd4904fbb89f76bb56ccefc2f607acb8f5ad89`  
		Last Modified: Tue, 14 Oct 2025 20:56:10 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.20348.4294; amd64

```console
$ docker pull caddy@sha256:8ffdcd060c7bca2b5182de34056ea24a6e4ca4dc52bc69d02dd1f71371527c94
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1506323712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c860029e9e4be4a680867c39dc1b7704c98e5975004afe5e390b1e5afdde8fd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:41:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:53:28 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 14 Oct 2025 20:53:28 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 14 Oct 2025 20:53:37 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 14 Oct 2025 20:53:37 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 14 Oct 2025 20:53:38 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 14 Oct 2025 20:53:38 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Tue, 14 Oct 2025 20:53:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 14 Oct 2025 20:53:39 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 14 Oct 2025 20:53:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 14 Oct 2025 20:53:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 14 Oct 2025 20:53:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 14 Oct 2025 20:53:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 14 Oct 2025 20:53:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 14 Oct 2025 20:53:43 GMT
EXPOSE 80
# Tue, 14 Oct 2025 20:53:44 GMT
EXPOSE 443
# Tue, 14 Oct 2025 20:53:44 GMT
EXPOSE 443/udp
# Tue, 14 Oct 2025 20:53:45 GMT
EXPOSE 2019
# Tue, 14 Oct 2025 20:53:50 GMT
RUN caddy version
# Tue, 14 Oct 2025 20:53:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c73b68129a17f163f24c548f99fac1fa06db5f2df83addedaeeccc104c116fd`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944442d4fa7228ae2f72213ece9c5856e0e07144c4c67b533d6bf974b82130bb`  
		Last Modified: Tue, 14 Oct 2025 20:54:09 GMT  
		Size: 360.4 KB (360369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931dac62e54b188592dc164c0c85e3c851af4cae9f98cb24d9194a32b28dfcb9`  
		Last Modified: Tue, 14 Oct 2025 20:54:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532ce732b24177e7d02bc20cdae96cfc5c2fcafa993b7faf3d4659804d32aae3`  
		Last Modified: Tue, 14 Oct 2025 20:54:10 GMT  
		Size: 16.6 MB (16568804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208a75d0f90591ee1a1b98c56684e3c108ac64bdd27910ce49f6906828e25a3a`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d0d78bed108d4d575590ed89585bbf50ee47ef2128e28c6e6888525379d7ec`  
		Last Modified: Tue, 14 Oct 2025 20:54:09 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9d62e15af93f70a0120a76ff688280a0f26922e2475476bc839ea5860dd35c`  
		Last Modified: Tue, 14 Oct 2025 20:54:09 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91e5a016c80f277af8960cbbe745684becde789f0ea0c77d8eef18144e40151`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65627fbb9732f4b7a1424282c94f426b5ee430e3e32bad43980dad12dde0cd`  
		Last Modified: Tue, 14 Oct 2025 20:54:09 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3c142d1b0d5feb26ea3f65d417f686975c3ec2f48590950878c1a3258c899`  
		Last Modified: Tue, 14 Oct 2025 20:54:09 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc126eb2b4ccd18b17f552b6c2c1edc97d0068b73b72a628246d24413626bd5`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5935984c3d857c1f7fdb1ab04bd59d22e04ad899a12c522235d775582783a3`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a06f791eb1ce34828e0032694bf72acc53e3c2cacc95a6193e846a1293bdfc2`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11c9522644201c2133e3f6e150b8d6dd19c2b3796a5b962c6a8e5b5e768cefb`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a588903917c9ff4e649725da099bc2e0d8bf6ca7fb3f8f36b7605642c2b1d772`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0ea40d67aa66a6eb56827258102feedff5c6a9918965a4340241fd92d04cf3`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f93546e931773eef69740cb6f175bb6c0bacf55ed43701fc243840beda9a81`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ecc941028812c3ef88faa90a87a0021846ccea1b6feeb766e7887849be39e5`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55d9824d28a313143b9dfde65c62fcb5e7e9a99ccf537c11e4293d9ef406926`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 353.2 KB (353164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7372194261cb1b9866efb7908b2117b73e5bad498e307991eda5a1e2be22cccb`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
