## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:563746fc8452b4f4de6224f120719f0bb9e80760bbf5854b73112b37e6f42770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull caddy@sha256:91c85a2b76228a9458ea61f978ade7e1566097ba95d59754591e931486a24872
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2686743989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:222c5ce9e438eb8f55831fd01ca5450509a2703aebfc3bc5aa7d7a1c0d97d837`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Jul 2022 21:02:39 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/69bb1c539b3ee03fc91271a71653a77ca1e9d131/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/69bb1c539b3ee03fc91271a71653a77ca1e9d131/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 Jul 2022 21:02:40 GMT
ENV CADDY_VERSION=v2.5.1
# Tue, 12 Jul 2022 21:03:47 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.1/caddy_2.5.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4294796c4bd4bed0c593d83606a5413de30f35f88d624e1b1e5b6cd8672ffbcc7a689d7ce4ef30c1abea0e95eda62220faac15d2a6aca0c3e2b418abe7a74118')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 Jul 2022 21:03:49 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 Jul 2022 21:03:49 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 Jul 2022 21:03:50 GMT
LABEL org.opencontainers.image.version=v2.5.1
# Tue, 12 Jul 2022 21:03:51 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 Jul 2022 21:03:52 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 Jul 2022 21:03:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 Jul 2022 21:03:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 Jul 2022 21:03:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 Jul 2022 21:03:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 Jul 2022 21:03:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 Jul 2022 21:03:58 GMT
EXPOSE 80
# Tue, 12 Jul 2022 21:03:59 GMT
EXPOSE 443
# Tue, 12 Jul 2022 21:03:59 GMT
EXPOSE 2019
# Tue, 12 Jul 2022 21:04:51 GMT
RUN caddy version
# Tue, 12 Jul 2022 21:04:51 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bef76419737006aed31e08290249d329a05ed10a4c4566bd669fae88218c88`  
		Last Modified: Tue, 12 Jul 2022 21:09:11 GMT  
		Size: 363.6 KB (363596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef8a8019fd762ae153c43f714fd21304f41d4908f7f956851d9d66885dfb0d1`  
		Last Modified: Tue, 12 Jul 2022 21:09:11 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7925f76cd18c89331c24bdb8542da766976ab51df5ea41336f7b78e07c4ca51e`  
		Last Modified: Tue, 12 Jul 2022 21:09:14 GMT  
		Size: 14.0 MB (14006151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f30315a526566e46f779eee3590fa94b3c132b660bd24fc13a2c5310b7a737b`  
		Last Modified: Tue, 12 Jul 2022 21:09:10 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643fc454cea2d0487926ddacffbfd78b6fc1f492fdf25615c4ae3b1c57a71369`  
		Last Modified: Tue, 12 Jul 2022 21:09:09 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c3cc1deec0c8645ddca64580321bee7fa6158dcc74476e7d19c191e19e993b`  
		Last Modified: Tue, 12 Jul 2022 21:09:09 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9114e4c82654bee43572ba6ebba1a1505b85c736ed6622c5f44dd06d45ee662e`  
		Last Modified: Tue, 12 Jul 2022 21:09:08 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1348aeddc8f2b0ee779ddf91fec9a083e46ba5237229eff9bed3f60c7d8a220`  
		Last Modified: Tue, 12 Jul 2022 21:09:08 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c317434d68eba3b8958926f02459decf49b4c25cb42dccaaefa2e824d786470d`  
		Last Modified: Tue, 12 Jul 2022 21:09:07 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2e91eb168bc71fe2eae9fb71f808958fc8b3ae0394c958e61ab78713a188a4`  
		Last Modified: Tue, 12 Jul 2022 21:09:06 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858f0b575a4e4e56bf791a93922498dd50591dca0219d3181a997e1c99e4c5f9`  
		Last Modified: Tue, 12 Jul 2022 21:09:06 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138fa86d9d5d32d6f96333fa809ac1fe75e57bb56bb07d7c73ba5f394ce8e26a`  
		Last Modified: Tue, 12 Jul 2022 21:09:06 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a8b341825d420901361dae5bec1374ed25ab67028eca6ea729a154a3c33fe3`  
		Last Modified: Tue, 12 Jul 2022 21:09:06 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a54a8a51c9ea29dc6e29da8fbacc21c6cf4f68bc5c8502a9fc65412b02e6bd3`  
		Last Modified: Tue, 12 Jul 2022 21:09:04 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef25d5c05081d158cea0702e1bb922c641ec629beb8b84bd6036b9d76f973e6`  
		Last Modified: Tue, 12 Jul 2022 21:09:04 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa2d3ec3911fb5e9e031c2479ad631ca55d9fd2bdecd49a69be5be3081f0fac`  
		Last Modified: Tue, 12 Jul 2022 21:09:04 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5278a61248829326a1c17e8c139d74d29633667fe552974ea4d7d1ae399cf24`  
		Last Modified: Tue, 12 Jul 2022 21:09:04 GMT  
		Size: 308.2 KB (308156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328045049d150e0cc57cda42c28ab079d6c50d51a3c51141f4d77d3d60d8adb0`  
		Last Modified: Tue, 12 Jul 2022 21:09:04 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
