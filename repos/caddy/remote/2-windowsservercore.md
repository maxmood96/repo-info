## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:b3ecc150f34a3c412beb999839613b4f772931edf8edbaadc19b0a8a22fa170d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `caddy:2-windowsservercore` - windows version 10.0.26100.32370; amd64

```console
$ docker pull caddy@sha256:6e7c66c6099d6bc6b5ff906bf6058dd563458ab0007857e97f1e784e2043981f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1982152977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d760c474d4157d97b21a9ee980079e935b92d3ef301e884742c9ce09a3f1aa00`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:51:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 23:01:15 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 10 Feb 2026 23:01:16 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 10 Feb 2026 23:01:23 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 10 Feb 2026 23:01:24 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 10 Feb 2026 23:01:25 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 10 Feb 2026 23:01:25 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Tue, 10 Feb 2026 23:01:26 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 10 Feb 2026 23:01:27 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 10 Feb 2026 23:01:28 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 10 Feb 2026 23:01:28 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 10 Feb 2026 23:01:29 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 10 Feb 2026 23:01:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 10 Feb 2026 23:01:30 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 10 Feb 2026 23:01:30 GMT
EXPOSE 80
# Tue, 10 Feb 2026 23:01:31 GMT
EXPOSE 443
# Tue, 10 Feb 2026 23:01:32 GMT
EXPOSE 443/udp
# Tue, 10 Feb 2026 23:01:32 GMT
EXPOSE 2019
# Tue, 10 Feb 2026 23:01:37 GMT
RUN caddy version
# Tue, 10 Feb 2026 23:01:38 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f3641b48551abf691e707ba76f8b07a225d509249237749ad0c13cbcab89a6`  
		Last Modified: Tue, 10 Feb 2026 22:52:23 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f276061a0e9fd62b5f026c0e8e20432c3c2bed55b1a283749156d4d1a6554fa`  
		Last Modified: Tue, 10 Feb 2026 23:01:47 GMT  
		Size: 391.7 KB (391713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5e15a2289d59d7eca1d6ce05af1d24eee8fa054736c6158129fff6955994b1`  
		Last Modified: Tue, 10 Feb 2026 23:01:47 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cfe98cc5e37fd25c0affc79b51ba982cae3f772287787b68c942b4fa6774b1c`  
		Last Modified: Tue, 10 Feb 2026 23:01:50 GMT  
		Size: 16.6 MB (16603432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979824b982ef69c03807cc87e8a18aad10bd24a1641d9bc1653d483b06549ccf`  
		Last Modified: Tue, 10 Feb 2026 23:01:47 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab9d90cdf8fee003148ca90b1fb97207cdaaeaf6367a1c754fe9c05a39b7d0f`  
		Last Modified: Tue, 10 Feb 2026 23:01:46 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983a0ea0b8e74e83e98e2ce6827eec442564643af8bc41baddffeb2d5c49e079`  
		Last Modified: Tue, 10 Feb 2026 23:01:46 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5e19df1d353e82803821837599cc670b39c65461dade76e4f723e582dbbbb9`  
		Last Modified: Tue, 10 Feb 2026 23:01:46 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc4512c1e5582c86ad4877934fd342dfdc2da294e2bbe6c23179c1b7543306b`  
		Last Modified: Tue, 10 Feb 2026 23:01:45 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3975ec9242bbc052bdb5d57efd0756f45acfcf99094e2805356d46959ed6cbe6`  
		Last Modified: Tue, 10 Feb 2026 23:01:45 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a604552550aaf7489aa0e405ad7aa48c1122509c898547a94a6ca8f0461b6d`  
		Last Modified: Tue, 10 Feb 2026 23:01:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10c6859a9b1be1ccd1f4f75655019335d457f8ce3ba20b1d3cac9590f0db6cf`  
		Last Modified: Tue, 10 Feb 2026 23:01:44 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d940e6676ac8b98f5e03a964e6156d51cea11a5dcceb7f5d1e6fbfc32b88f2c2`  
		Last Modified: Tue, 10 Feb 2026 23:01:44 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ec3a6e40fa5748b341cd6e5d1d2d1766a866b0fad1a1983c7b3904010db56d`  
		Last Modified: Tue, 10 Feb 2026 23:01:44 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e2a8335a8bcd0f09b8881e1aceb0256a1f4ca5cf783ed1f59b3830ac4dfc63`  
		Last Modified: Tue, 10 Feb 2026 23:01:44 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458431ca1f11a4a4821a1f1664937c2030ca380b87fb6f5fbffefd6ca8d7b445`  
		Last Modified: Tue, 10 Feb 2026 23:01:42 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20910b219f8574e2733678cb3c1aa9cff159182d4d5ea6c6389d1c2062748fee`  
		Last Modified: Tue, 10 Feb 2026 23:01:42 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48fae5cf857cd8bbb242ce433c3df4346052140c08697dbf1461654829aabd2f`  
		Last Modified: Tue, 10 Feb 2026 23:01:43 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fafec4cb7000cfd389b9271fa8dcb290d829f68afbbde11c803f8c26840536`  
		Last Modified: Tue, 10 Feb 2026 23:01:42 GMT  
		Size: 375.4 KB (375425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f5cd22343f6e63b3b23bcf0c1877f9b7532439c621b30e43bc13999985be8b`  
		Last Modified: Tue, 10 Feb 2026 23:01:42 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.20348.4773; amd64

```console
$ docker pull caddy@sha256:a3837d693358af45d4af020a98c9ab64bc3d8890cc718b4d71b218ca8a7ed1ab
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1880077650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2080fbc82fecf316257b929e2f540b8338fc2e29dc8f0db452c61bd770358c18`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Tue, 10 Feb 2026 23:14:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 23:14:55 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 10 Feb 2026 23:14:56 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 10 Feb 2026 23:15:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 10 Feb 2026 23:15:08 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 10 Feb 2026 23:15:08 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 10 Feb 2026 23:15:10 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Tue, 10 Feb 2026 23:15:10 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 10 Feb 2026 23:15:11 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 10 Feb 2026 23:15:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 10 Feb 2026 23:15:13 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 10 Feb 2026 23:15:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 10 Feb 2026 23:15:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 10 Feb 2026 23:15:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 10 Feb 2026 23:15:17 GMT
EXPOSE 80
# Tue, 10 Feb 2026 23:15:18 GMT
EXPOSE 443
# Tue, 10 Feb 2026 23:15:18 GMT
EXPOSE 443/udp
# Tue, 10 Feb 2026 23:15:19 GMT
EXPOSE 2019
# Tue, 10 Feb 2026 23:15:26 GMT
RUN caddy version
# Tue, 10 Feb 2026 23:15:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c42f97ad258a14a6dbdcb82f4db240ae770d130ae690da2e4abf30e29919a5`  
		Last Modified: Tue, 10 Feb 2026 23:15:36 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5986a92d2c4741f2d28228dfd7c6283deb455ea86d2277d16fb73c24469e3a0`  
		Last Modified: Tue, 10 Feb 2026 23:15:36 GMT  
		Size: 490.0 KB (490008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffe8601c9aac4730bf36d72767be0c5c461ca36d50bfb8380a36ae220fa964d`  
		Last Modified: Tue, 10 Feb 2026 23:15:36 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cec3a97816b7253b9f0536e61523f608fc9eb09c9a133f2352d36f0a61f5c9`  
		Last Modified: Tue, 10 Feb 2026 23:15:38 GMT  
		Size: 16.6 MB (16564778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8f492e3a72bf1cf6c7a83d87fbb56c36ff7e10b88f13ceda98762c52348c56`  
		Last Modified: Tue, 10 Feb 2026 23:15:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b98fdede264784e07b9b871ad56349fd7a48bdd3f9d86f60cf9d6bd650d859`  
		Last Modified: Tue, 10 Feb 2026 23:15:34 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b55dea49a860842e60026ffb1310e79dabbec2b6249df94e93d8136289f8ef8`  
		Last Modified: Tue, 10 Feb 2026 23:15:34 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650f6d3b28ea2fe1efd0b1d9bde43dc991ac946aad84ccff96d6dd8b5702571b`  
		Last Modified: Tue, 10 Feb 2026 23:15:34 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a04551dc3e2993d1de700b6ad8232cde96a5d6ae10c35f486e40b92da1fe8b`  
		Last Modified: Tue, 10 Feb 2026 23:15:34 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a400410fea1a3a7c70fddc7a2f628361172c51b475c190eb11d1ad25b934294`  
		Last Modified: Tue, 10 Feb 2026 23:15:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e0cc6d534bc45b036852067fc9056ce0509bcb90c81a20a403a84f555b3048`  
		Last Modified: Tue, 10 Feb 2026 23:15:33 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca018aa6e7136f3713a12b83fb8886c6ae355bbbad49ee98329bd3062436822`  
		Last Modified: Tue, 10 Feb 2026 23:15:33 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1047b0c70acde50333d760c4e87b61c55868ac5237207fa7a613adb45053b3c0`  
		Last Modified: Tue, 10 Feb 2026 23:15:32 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e84591cbe17431834bfc10ea86327744d33121c0361e17a9663ff5bc383c92b8`  
		Last Modified: Tue, 10 Feb 2026 23:15:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e6b047f1cb496104ea8b755e7c91d0e112cab0d516c2fa1a117978e0e8bd1c`  
		Last Modified: Tue, 10 Feb 2026 23:15:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d7d061fb740099a287a80e83018e4415a8aafc72a068d2649e1ba8456aaf6d`  
		Last Modified: Tue, 10 Feb 2026 23:15:31 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b9c9ffc4b188fae0c18c88003323717c2e39d96579ad89bb1160b06dac6d9a`  
		Last Modified: Tue, 10 Feb 2026 23:15:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdce7a8989b632d092c616b346647bbf444cfb19f2cd9278aeb477632e2cd672`  
		Last Modified: Tue, 10 Feb 2026 23:15:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b865b67def9a31372e40fda32211a379e86e79ea86c1950799f589b9ebb3706f`  
		Last Modified: Tue, 10 Feb 2026 23:15:31 GMT  
		Size: 343.4 KB (343398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496d68ffbd692e3de604600d4afb7e38c8f40f772e9ffd34e8c8cc57b4dd8f20`  
		Last Modified: Tue, 10 Feb 2026 23:15:31 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
