## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:9c2a76ec050aab94327c6feaf96fc10702e2ceb21ef7a4e3821de9dc5681c6fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2366; amd64
	-	windows version 10.0.14393.4825; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.2366; amd64

```console
$ docker pull caddy@sha256:b7b211aa880cdce8acc7fe0f9f6c683088326ce582343b41796704552a694a40
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2721477226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69f0ccc87258cb337f0e5805011a6910c267211c0e4f0e14676560de9fe132b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 07 Dec 2021 04:56:01 GMT
RUN Install update 1809-amd64
# Wed, 15 Dec 2021 00:45:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Dec 2021 02:25:01 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Dec 2021 02:25:02 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 15 Dec 2021 02:26:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Dec 2021 02:26:04 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Dec 2021 02:26:05 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Dec 2021 02:26:06 GMT
VOLUME [c:/config]
# Wed, 15 Dec 2021 02:26:07 GMT
VOLUME [c:/data]
# Wed, 15 Dec 2021 02:26:08 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 15 Dec 2021 02:26:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Dec 2021 02:26:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Dec 2021 02:26:11 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Dec 2021 02:26:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Dec 2021 02:26:13 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Dec 2021 02:26:13 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Dec 2021 02:26:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Dec 2021 02:26:15 GMT
EXPOSE 80
# Wed, 15 Dec 2021 02:26:16 GMT
EXPOSE 443
# Wed, 15 Dec 2021 02:26:17 GMT
EXPOSE 2019
# Wed, 15 Dec 2021 02:27:05 GMT
RUN caddy version
# Wed, 15 Dec 2021 02:27:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ee7a7ea9cf22f75886179907a41810a992e21f3d0c57cc10d2147ce9237701c`  
		Size: 990.3 MB (990271574 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aabd70b2463e8240ac41c7d726f6fcfc25424b74f20bb5e8642dbb9bc2b789c8`  
		Last Modified: Wed, 15 Dec 2021 01:53:57 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b0cdbf2ad425ad4ae06eff8efd2680687a8b1791a316a065d127675297ad9c`  
		Last Modified: Wed, 15 Dec 2021 02:34:31 GMT  
		Size: 383.6 KB (383570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6530d60da62f6ecb59f232d9909ff47d1451128d25c6552e9f2e14d6882d56c5`  
		Last Modified: Wed, 15 Dec 2021 02:34:30 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14e5873901cb278a3b132ca908a4bf48ddc92873f0a366d120567b69ac13a3b`  
		Last Modified: Wed, 15 Dec 2021 02:34:42 GMT  
		Size: 12.1 MB (12144187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b55cd1b689fe890314e34f4d482472e42e3b0d5b17e4fcef1eee3375dc2f67`  
		Last Modified: Wed, 15 Dec 2021 02:34:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df412fbd68619043dbbf55a3c1c7dec394167e55e270a63c4b637160c4bf5df5`  
		Last Modified: Wed, 15 Dec 2021 02:34:29 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfb51154015c8c11520eb76ab3c76e842b527f7b92ebc8368429988966d1422`  
		Last Modified: Wed, 15 Dec 2021 02:34:28 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d613ebf687a7ef77f3ba9ec17ae99403069ccb1a1164580015d0a7b69c39ccd9`  
		Last Modified: Wed, 15 Dec 2021 02:34:28 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5711fb93c35f0d4b4f85d20d614492bc7d6ead6c5f972e7a24847fd5a30f7ab1`  
		Last Modified: Wed, 15 Dec 2021 02:34:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c01b1d21b0aa7c0381f6ba211b844017575215d9e1c9d1bab3e108d1d483885`  
		Last Modified: Wed, 15 Dec 2021 02:34:27 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40387eab9b48fadefc326d8907ddab250e3bc78bb880d54dea0f0999222ae135`  
		Last Modified: Wed, 15 Dec 2021 02:34:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b73c253a638c310eecfd3ef1a0056ee0044b7e562ea852ee16fbd30a2b33662`  
		Last Modified: Wed, 15 Dec 2021 02:34:26 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07115919ebe6a88fc374988b43b61787b21bb893ff9b274723e2c28083978c3c`  
		Last Modified: Wed, 15 Dec 2021 02:34:25 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98548b3e526d63faf24080c8f42617af31cf8cb65f161e1d86eb9fd9a54c21c`  
		Last Modified: Wed, 15 Dec 2021 02:34:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f9154a626a27bf861a8b5358cf8dd45fdf87ee99e1994cc6e61832dea66e35`  
		Last Modified: Wed, 15 Dec 2021 02:34:25 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be71f4d75607474969688100b105472bd1644e541298a0c47410df71168f0422`  
		Last Modified: Wed, 15 Dec 2021 02:34:25 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da966c586a051463c52b8dd86ab4529f70a08dfc9ef69c70256913811b2eecbd`  
		Last Modified: Wed, 15 Dec 2021 02:34:23 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71f0a688a7aa06a39d1401f9f74318840c34c9fd8e72777a828243129bd0fa1`  
		Last Modified: Wed, 15 Dec 2021 02:34:23 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def47cda5d628c4d5bc839a60f236dce7de8bed41883d7dfa4024b2769fa6177`  
		Last Modified: Wed, 15 Dec 2021 02:34:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e396f6e0539a9e963f0a9b2f67fd27e3c9d0bf9fd8495bd0a3269bce8cd3e07c`  
		Last Modified: Wed, 15 Dec 2021 02:34:23 GMT  
		Size: 321.4 KB (321441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d1151a66b9e88e3a33d7c8dfa9ab785e07d77b44e15930d587cc157ca27d40`  
		Last Modified: Wed, 15 Dec 2021 02:34:23 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.14393.4825; amd64

```console
$ docker pull caddy@sha256:f81dc1250edec4ba0e28c916af19899b9a8cfb67c5a59ad35a0ce1d26936f1a4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6287500240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f00f24f148e71d971d3af93bedbe936f35f200ffa916ec2dfbd069812b3844a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 08 Dec 2021 08:38:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Dec 2021 00:54:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Dec 2021 02:28:30 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Dec 2021 02:28:30 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 15 Dec 2021 02:29:44 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Dec 2021 02:29:45 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Dec 2021 02:29:46 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Dec 2021 02:29:47 GMT
VOLUME [c:/config]
# Wed, 15 Dec 2021 02:29:48 GMT
VOLUME [c:/data]
# Wed, 15 Dec 2021 02:29:49 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 15 Dec 2021 02:29:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Dec 2021 02:29:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Dec 2021 02:29:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Dec 2021 02:29:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Dec 2021 02:29:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Dec 2021 02:29:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Dec 2021 02:29:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Dec 2021 02:29:57 GMT
EXPOSE 80
# Wed, 15 Dec 2021 02:29:58 GMT
EXPOSE 443
# Wed, 15 Dec 2021 02:29:59 GMT
EXPOSE 2019
# Wed, 15 Dec 2021 02:30:45 GMT
RUN caddy version
# Wed, 15 Dec 2021 02:30:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2d026d646213ccf73d9f0584941d108253d62e73df2a74e070776884b7b0242b`  
		Size: 2.2 GB (2204728802 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e473536e08c92a08f92b05dcf009604fd3f0425171a596a8efeeeb5f69746a24`  
		Last Modified: Wed, 15 Dec 2021 01:54:48 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e90c848dd8ea0c0016b244bc9c3447f338a3a7b693d60a5d43252856d973155`  
		Last Modified: Wed, 15 Dec 2021 02:35:05 GMT  
		Size: 340.7 KB (340720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634b6be85b1de96709e8ec7698ececda4e22204337c0cd48df931dc4f65e8868`  
		Last Modified: Wed, 15 Dec 2021 02:35:05 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b492992b322ab5dbb60d4372187aae95f5cba17a2b1fa44615253398535e4413`  
		Last Modified: Wed, 15 Dec 2021 02:35:07 GMT  
		Size: 12.1 MB (12129780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f101f20e8963042f8ef5db7f386f6a101a739a4e7434552d00a03f2a8bf29c9`  
		Last Modified: Wed, 15 Dec 2021 02:35:04 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975bd0787a24dcbb48a7fff974fa4358bf09f60303bf813acb933724b80a6412`  
		Last Modified: Wed, 15 Dec 2021 02:35:03 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf85d0a2b7b82bb506532cdb1543cfffc038be9f0a2bbc88b56d362f066842da`  
		Last Modified: Wed, 15 Dec 2021 02:35:03 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83813d5262cf337d6d111fa93665a94414fc602de755518f5b4924e2dfc51657`  
		Last Modified: Wed, 15 Dec 2021 02:35:02 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a28304e768db104c1c4581980b8b1c28294266d720e12ee2ebf8d3f21afad0`  
		Last Modified: Wed, 15 Dec 2021 02:35:02 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab06335cb4ae08ff9b9f19f11c1992c98d02bd21e6be248903dca4a92bec1600`  
		Last Modified: Wed, 15 Dec 2021 02:35:01 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e179f9bd8c954c5c16f659b65b76e5290ac974328d5a8f5c52450f3ba95d85f`  
		Last Modified: Wed, 15 Dec 2021 02:35:01 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecce875b476bb05e4ad56b779801b169867814e7511700f9d1dab62cce70e09`  
		Last Modified: Wed, 15 Dec 2021 02:35:01 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f421531974af84f1ac3ea2bc58618b115cfc59893d3e2c8c15478a18152fb2cd`  
		Last Modified: Wed, 15 Dec 2021 02:34:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbb0bfc7e8d0868227aad9a4ccca7b2ca72678605e788cfe8cd592dd888003d`  
		Last Modified: Wed, 15 Dec 2021 02:34:59 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c62fa54c3cbb02d0ab21cdfc04da63cea55f4ac1af2b2d63c5b51391536e41`  
		Last Modified: Wed, 15 Dec 2021 02:34:58 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd9f09e272aab6d9ec2cc43bb7c1d52d6058cd600f9b9767ff6b004df3d326a`  
		Last Modified: Wed, 15 Dec 2021 02:34:58 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5633fbaec41b8566ea33b11b433f9db127038e894d6813024bdfc42b76242032`  
		Last Modified: Wed, 15 Dec 2021 02:34:56 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924e9dd54b49abc4341da03a3d72e05216eaed15390a1d337b41899db8ad4121`  
		Last Modified: Wed, 15 Dec 2021 02:34:56 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a7a35938fe952b2ccf20609386a5c76e5513d704c3a893d0d060db759fcecc`  
		Last Modified: Wed, 15 Dec 2021 02:34:56 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44835ce2a87e32ea27c57d44bf7fd4cddfb6449d460f21b7e7602c21585c852d`  
		Last Modified: Wed, 15 Dec 2021 02:34:56 GMT  
		Size: 289.5 KB (289523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1beb77ba2b49f98367f362e4d3254cf3ccc8cc1f4564cce9391cbc86dfc172`  
		Last Modified: Wed, 15 Dec 2021 02:34:56 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
