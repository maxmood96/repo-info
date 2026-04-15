## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:f9118c9ca06f1ae461716a6889a0bd508c16718d56841c9679d1a8fbdb682044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `caddy:2-windowsservercore` - windows version 10.0.26100.32690; amd64

```console
$ docker pull caddy@sha256:2ee305ceeda7058037d4a404f699dffdd0d47d21964fc6ff65d10e15baf2c88a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2148387239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2b43f92b2a4873c53412e5eb3287746053dd45044276535d572d9b30ae111b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:02:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:16:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 14 Apr 2026 21:16:26 GMT
ENV CADDY_VERSION=v2.11.2
# Tue, 14 Apr 2026 21:16:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.2/caddy_2.11.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('77db9ab02b0dbfc3a8b3928e1c88e48f2b328adcdb02affbc49442ce183cc901d1f4d2ce2a5d1dc897a318948133b1f98f209e1cad56b050bb98336c2ffddd04')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 14 Apr 2026 21:16:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 14 Apr 2026 21:16:36 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 14 Apr 2026 21:16:37 GMT
LABEL org.opencontainers.image.version=v2.11.2
# Tue, 14 Apr 2026 21:16:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 14 Apr 2026 21:16:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 14 Apr 2026 21:16:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 14 Apr 2026 21:16:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 14 Apr 2026 21:16:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 14 Apr 2026 21:16:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 14 Apr 2026 21:16:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 14 Apr 2026 21:16:45 GMT
EXPOSE 80
# Tue, 14 Apr 2026 21:16:46 GMT
EXPOSE 443
# Tue, 14 Apr 2026 21:16:48 GMT
EXPOSE 443/udp
# Tue, 14 Apr 2026 21:16:49 GMT
EXPOSE 2019
# Tue, 14 Apr 2026 21:16:54 GMT
RUN caddy version
# Tue, 14 Apr 2026 21:16:55 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6381b6627d94a0354f249ec783cecec3a2f7fe084a83b16b2871e14d271640d2`  
		Last Modified: Tue, 14 Apr 2026 21:03:06 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397e25bc5bdca994921e057bb9ff35a161eac7cd511c793dd73503ea47666c33`  
		Last Modified: Tue, 14 Apr 2026 21:17:04 GMT  
		Size: 358.9 KB (358908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3229bd9f16449ee10207b1ca855615a9dd02d9933c5c7704a4c7f087bac537c1`  
		Last Modified: Tue, 14 Apr 2026 21:17:04 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52662f0889b382a7ccca14599367a28a2e292299cbf01367fa4fddab93fd095`  
		Last Modified: Tue, 14 Apr 2026 21:17:07 GMT  
		Size: 17.7 MB (17672695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e018ad1fe1b75d9b2e8c08d86b1ca882e7c9f0a95474b079a14cca2e02b38986`  
		Last Modified: Tue, 14 Apr 2026 21:17:04 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd32e8fe3295eecc9dd1a486f9982dfe4faad311eaff9e8ff96b613bbcc7684b`  
		Last Modified: Tue, 14 Apr 2026 21:17:02 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ebc2ee56762fc571126a35e7637d9ff6f3d76854ec3533d09f97268bbfd95b3`  
		Last Modified: Tue, 14 Apr 2026 21:17:02 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ae7fe6316b1ecb322630df27ee8b7a18b297e2dbb386179a6f4115e2f00931`  
		Last Modified: Tue, 14 Apr 2026 21:17:02 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbd0cd73795390d0a92c0a6c74762b6af7998cbf58c44b8cf57eb2705274f66`  
		Last Modified: Tue, 14 Apr 2026 21:17:02 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f022d78fbac53222bee4427e90bff2cad69993b59e0c4b215c48822f7bc72e5`  
		Last Modified: Tue, 14 Apr 2026 21:17:02 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f320abd61d8e0f90bdad0f22ab67bb6b340c15a40e2be8e7a6b83ecb65a582b`  
		Last Modified: Tue, 14 Apr 2026 21:17:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb877bffae0de6f77eb6da011580029719c771a87126a89fa84baaf01928153`  
		Last Modified: Tue, 14 Apr 2026 21:17:01 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2dc5ace231634e1833c01d1aa08047025f45f46167e164107ae376dafa227c`  
		Last Modified: Tue, 14 Apr 2026 21:17:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10482279b1ee92970a64ce6a771641031e11fc8abfd36c78c8088d3d78edb23`  
		Last Modified: Tue, 14 Apr 2026 21:17:00 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270bf230a09206a81a72fdbda118ab39560ba709730f04c8180dc388d029e865`  
		Last Modified: Tue, 14 Apr 2026 21:17:00 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b680d1d6f94613e6c7fe4406981f240eb0db5e2f9bfc70bc181508c24c3bf0`  
		Last Modified: Tue, 14 Apr 2026 21:16:59 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de353b5b3e7a6db33fe705562409b09120b0b11110a25dc023e200d882dc5314`  
		Last Modified: Tue, 14 Apr 2026 21:16:59 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714387afcfceaadb924708bfe5cc5b214d414a5341c79f20acfcc95790c9d17a`  
		Last Modified: Tue, 14 Apr 2026 21:16:59 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17289f79660bdb8267e153c9821c6540ee047cd2fb9c665a3e359ab26363438e`  
		Last Modified: Tue, 14 Apr 2026 21:16:59 GMT  
		Size: 347.2 KB (347158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59276903cd726503da75a6fea6543ef3d75b0eb6e4eff110aec891e3cebcaf53`  
		Last Modified: Tue, 14 Apr 2026 21:16:59 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull caddy@sha256:b8df27c06cfdbe2fa4590d2de484278aad4f969b053b9202c91a5072a6b73787
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2088751785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e017579baae316e73869e6a36c53d38e7fbe1e4c0b536c6e356c548f7d9e3723`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:03:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:28:36 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 14 Apr 2026 21:28:37 GMT
ENV CADDY_VERSION=v2.11.2
# Tue, 14 Apr 2026 21:28:48 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.2/caddy_2.11.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('77db9ab02b0dbfc3a8b3928e1c88e48f2b328adcdb02affbc49442ce183cc901d1f4d2ce2a5d1dc897a318948133b1f98f209e1cad56b050bb98336c2ffddd04')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 14 Apr 2026 21:28:49 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 14 Apr 2026 21:28:50 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 14 Apr 2026 21:28:51 GMT
LABEL org.opencontainers.image.version=v2.11.2
# Tue, 14 Apr 2026 21:28:52 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 14 Apr 2026 21:28:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 14 Apr 2026 21:28:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 14 Apr 2026 21:28:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 14 Apr 2026 21:28:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 14 Apr 2026 21:28:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 14 Apr 2026 21:28:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 14 Apr 2026 21:28:57 GMT
EXPOSE 80
# Tue, 14 Apr 2026 21:28:58 GMT
EXPOSE 443
# Tue, 14 Apr 2026 21:29:00 GMT
EXPOSE 443/udp
# Tue, 14 Apr 2026 21:29:00 GMT
EXPOSE 2019
# Tue, 14 Apr 2026 21:29:06 GMT
RUN caddy version
# Tue, 14 Apr 2026 21:29:07 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7859559f7e482ab69f3dddf83b05a23fb97e6c47cc09bb11f9f91ea0b96dbf26`  
		Last Modified: Tue, 14 Apr 2026 21:05:58 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d2bd12f91f97f2185947a6c6616993b9dff74580c85224a5af1d7d96c71cd9`  
		Last Modified: Tue, 14 Apr 2026 21:29:16 GMT  
		Size: 501.5 KB (501474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb54b9bd5755e8e8265a0b7668bbeca0d7ff399477a75b0404682b7a3c7fa8d1`  
		Last Modified: Tue, 14 Apr 2026 21:29:16 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f194135d2550722e1d0b5cdb4f6e37c1bd909280f808b282d49b4af5ae574dad`  
		Last Modified: Tue, 14 Apr 2026 21:29:18 GMT  
		Size: 17.7 MB (17669467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cda0ad7332ed66bf920633ff8248f57fdfbd8a9526aa68a856eab403fa56e9`  
		Last Modified: Tue, 14 Apr 2026 21:29:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791860b8e0f97359a0021293450cf4ac33e732f2d66b1525a543968beb59fd65`  
		Last Modified: Tue, 14 Apr 2026 21:29:14 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6fe46198f0322a89913f7b421d8e8380d40fe26601d7965c0d5e611935c19`  
		Last Modified: Tue, 14 Apr 2026 21:29:14 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7391a402eb516f6f19a3a37d11feacf19bf3efcd7ceebd9af7a1420bbaf454c4`  
		Last Modified: Tue, 14 Apr 2026 21:29:14 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2f73748f041ea7e7a9fb3f0f7591f82957afe40830a5a0791e14e70b4bf06c`  
		Last Modified: Tue, 14 Apr 2026 21:29:14 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08eec5cc013166f15da87d6404c9d4360f7ad9f017d13e5a8d687128b6cd3b0d`  
		Last Modified: Tue, 14 Apr 2026 21:29:14 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def61174716aaa0c6879c3b2eba76348b2ebc16c7d9475981ff5d6005f504325`  
		Last Modified: Tue, 14 Apr 2026 21:29:13 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7506def56d28e15862f644d66a37ca310b2af0e67b40dd9c6fcc595db98aae`  
		Last Modified: Tue, 14 Apr 2026 21:29:12 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29669880bfec5f126f10670df165ea26dde25d0b4a5b413ada63363deeee0c62`  
		Last Modified: Tue, 14 Apr 2026 21:29:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3514521d0494397ad76515629969965baead98a0d17c674804de5f55b7f0bcd6`  
		Last Modified: Tue, 14 Apr 2026 21:29:12 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d95600f6fee4100d97188239dac7eabd1586d0e2adaf937df6ab2a88dacee20`  
		Last Modified: Tue, 14 Apr 2026 21:29:12 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43921159c6d617ff0a0e8aa7187f357153ddf2fc53970d4b37542983bc392d0`  
		Last Modified: Tue, 14 Apr 2026 21:29:11 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549a656bcbd3cb99a7bcee7b3f0d9b6a98976e42fc63a96df98a1d85f215baa4`  
		Last Modified: Tue, 14 Apr 2026 21:29:11 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e971470b949722b894566989b0b0fc2e4ccc9158199c44ef6898c92d35d0ea7a`  
		Last Modified: Tue, 14 Apr 2026 21:29:11 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e247fe332f0242556386843c3436148b806e7fd290c3b07ec7e8622f788b80`  
		Last Modified: Tue, 14 Apr 2026 21:29:11 GMT  
		Size: 347.3 KB (347257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35776271f71d5561051d257aad8ee5adcacca3bd040eb8379b9fb0078f60ee2`  
		Last Modified: Tue, 14 Apr 2026 21:29:11 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
