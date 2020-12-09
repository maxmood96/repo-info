## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:6f9fa402f617af6a08a77a3d6821621bb5bb0f3b99080d2d9b8d990104a3fb48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull caddy@sha256:b99f350b2de1665d145dad8c93c867427211ed43e1676b25da7c573bf24e97cf
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2416743592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:242dc82d58b3eb28bad3e05fe3004a6da6c5748d32c08be14523fcafd480cbc9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 13:30:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Dec 2020 22:50:42 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Dec 2020 22:50:43 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 09 Dec 2020 22:51:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Dec 2020 22:51:16 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Dec 2020 22:51:17 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Dec 2020 22:51:18 GMT
VOLUME [c:/config]
# Wed, 09 Dec 2020 22:51:18 GMT
VOLUME [c:/data]
# Wed, 09 Dec 2020 22:51:19 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 09 Dec 2020 22:51:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Dec 2020 22:51:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Dec 2020 22:51:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Dec 2020 22:51:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Dec 2020 22:51:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Dec 2020 22:51:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Dec 2020 22:51:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Dec 2020 22:51:25 GMT
EXPOSE 80
# Wed, 09 Dec 2020 22:51:26 GMT
EXPOSE 443
# Wed, 09 Dec 2020 22:51:27 GMT
EXPOSE 2019
# Wed, 09 Dec 2020 22:51:43 GMT
RUN caddy version
# Wed, 09 Dec 2020 22:51:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a4372d14958dc8a7eaaace9e4774e7f1db524da5eb4474b5e46738848a3a61a5`  
		Last Modified: Wed, 09 Dec 2020 13:54:38 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433ced4e59cd32da7d04608be235ec50650c9160c8742a10c9a60ae7294d7f52`  
		Last Modified: Wed, 09 Dec 2020 22:59:41 GMT  
		Size: 9.2 MB (9243267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914209fee7eb59b47ff4c4135d33f98b6b3af4209d114af2f9d0a8f65849d39b`  
		Last Modified: Wed, 09 Dec 2020 22:59:37 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493568bf34f325205007ec539e481c37dd13dd690c9e40e265f5a985393ba1a2`  
		Last Modified: Wed, 09 Dec 2020 22:59:43 GMT  
		Size: 16.3 MB (16325951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee88af8a1f1057877ee81813d03ca89698521e3a410830835be694de9aa3153`  
		Last Modified: Wed, 09 Dec 2020 22:59:37 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9bfb8247c1f8c75fb59ee12dcd363fd2fcae2ac8da5e9fede5617faec7d082c`  
		Last Modified: Wed, 09 Dec 2020 22:59:37 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326e317e6021cafd340d9cb540564d2c79890682efe4baa10fe5bea17847adba`  
		Last Modified: Wed, 09 Dec 2020 22:59:35 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3769dc06e616a825c947d4d1a6c8aa5a427cf792adea55a9dc35672cc76b6d6`  
		Last Modified: Wed, 09 Dec 2020 22:59:34 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8fa4f4d0eb978c7b41fb792c1faf3fc4823a131abc37ca7de8f13f2cb6b56d8`  
		Last Modified: Wed, 09 Dec 2020 22:59:34 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1042475d4dc01a2523d8dae43fd2096a6b87435d2f47f8c3275fcbac6d2453b`  
		Last Modified: Wed, 09 Dec 2020 22:59:34 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f1d1c1053e1fb4775c5939504f7c7554f3c65d033668836428b399f7bd3269`  
		Last Modified: Wed, 09 Dec 2020 22:59:35 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad4951dcfb5db6ad1ce8c0778b1647a8950ced04bd7b2b3051bf2b9df7209a4`  
		Last Modified: Wed, 09 Dec 2020 22:59:32 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21dc0af1dcce3f75d580aaa3f73c92c6bd81249b0e86db979abe8ab511744095`  
		Last Modified: Wed, 09 Dec 2020 22:59:32 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223c49ff4855aff0e5bec5047249790dc3beef9bb99303c7963e0060e19c781e`  
		Last Modified: Wed, 09 Dec 2020 22:59:31 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db82d6aa5350a637ef41ced50f1e2aaab1876acadc50f289261c2b935251abda`  
		Last Modified: Wed, 09 Dec 2020 22:59:31 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ca7f7662411153b8d2e07b4e190fe5f28b55987e6c488eaf407f1b218757db`  
		Last Modified: Wed, 09 Dec 2020 22:59:31 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de08ddd6fa1eec7ccc22299391dd16977f04c771c608d78aac09c2001b65cf36`  
		Last Modified: Wed, 09 Dec 2020 22:59:28 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11252ce2cac0c2d7e62754856c25a1fff65491437f664d589da9d70b608b18c4`  
		Last Modified: Wed, 09 Dec 2020 22:59:28 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159813c0e3aae77d0d2682fc6af3e2efa7204512c729017ee3c3282ba2a0ef30`  
		Last Modified: Wed, 09 Dec 2020 22:59:29 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a54bb1a8f7a905eb1774d7a6343ba5d306106c5dea74d1c9bd6e501cadcc86`  
		Last Modified: Wed, 09 Dec 2020 22:59:29 GMT  
		Size: 279.4 KB (279413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326eaebe45d7e1cadffa1215c3c58ff62541eba9a6209d0140f165099ca8d66b`  
		Last Modified: Wed, 09 Dec 2020 22:59:29 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
