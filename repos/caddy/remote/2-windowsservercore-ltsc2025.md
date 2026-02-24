## `caddy:2-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:5186c65f58c2517fa5a0bec826d8773a28e6f3a50a728d0b9dff06c0500192d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `caddy:2-windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull caddy@sha256:bdaf10c3768c79c4b3698ef494c0cac0bdd6f11ceda5a52686d5872da60169a4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1983224207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b443dc8398fb5328c8bbcc2d7a0d12a372f745a0894034ba3eed5fb9c06d2d2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Mon, 23 Feb 2026 20:06:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Feb 2026 20:07:05 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 23 Feb 2026 20:07:06 GMT
ENV CADDY_VERSION=v2.11.1
# Mon, 23 Feb 2026 20:07:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.1/caddy_2.11.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('2db57d7f2c5a4ce466449de81702ce86acc3397efaec559f51d76754cca9ba47adcb1c3633fb3cb907949144ee17a418c144e87a2a382801380c961bf80f07e3')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 23 Feb 2026 20:07:18 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 23 Feb 2026 20:07:18 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 23 Feb 2026 20:07:19 GMT
LABEL org.opencontainers.image.version=v2.11.1
# Mon, 23 Feb 2026 20:07:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 23 Feb 2026 20:07:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 23 Feb 2026 20:07:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 23 Feb 2026 20:07:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 23 Feb 2026 20:07:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 23 Feb 2026 20:07:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 23 Feb 2026 20:07:26 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 23 Feb 2026 20:07:27 GMT
EXPOSE 80
# Mon, 23 Feb 2026 20:07:28 GMT
EXPOSE 443
# Mon, 23 Feb 2026 20:07:29 GMT
EXPOSE 443/udp
# Mon, 23 Feb 2026 20:07:30 GMT
EXPOSE 2019
# Mon, 23 Feb 2026 20:07:45 GMT
RUN caddy version
# Mon, 23 Feb 2026 20:07:46 GMT
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
	-	`sha256:4fd4b78df4d169f7144f0ba390c448fb7c1592fa0c097ec1d2cc45f2eedf7a61`  
		Last Modified: Mon, 23 Feb 2026 20:07:55 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882deb7b4312a5cfae424100ad54cea73fbf64e81046d22b33773d795fe2a4ba`  
		Last Modified: Mon, 23 Feb 2026 20:07:56 GMT  
		Size: 394.1 KB (394137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c26a0b2edbddcd7c71c17f3e309319d06234fa0e14b20a311d76d91bd1b741`  
		Last Modified: Mon, 23 Feb 2026 20:07:55 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9573f3624d3253f194b5646faad1b286f8164b3cc8cfdd7732562c0694cff8`  
		Last Modified: Mon, 23 Feb 2026 20:07:57 GMT  
		Size: 17.7 MB (17671917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95ac787187d6040044f232d955e3938f58b21133258fe2ddf94da4521b953e0`  
		Last Modified: Mon, 23 Feb 2026 20:07:55 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162d91d326496d34e229c9bbd8c8cd0fe0a3519bee38b514eb68b1bd8e6b5979`  
		Last Modified: Mon, 23 Feb 2026 20:07:54 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71567ef59b0acc0a79cb66fff5d2de75133cee599583f62bac4ffb693060069`  
		Last Modified: Mon, 23 Feb 2026 20:07:54 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e03a8a2aa7a8b7ec6f08f3f586956d75e30d606d8f87add2d8cba44601030ef`  
		Last Modified: Mon, 23 Feb 2026 20:07:53 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b5a4a8b42df9cdad7df9ed91813b454ea1c4f309acb6d29790b464917c130e`  
		Last Modified: Mon, 23 Feb 2026 20:07:53 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f47546b43b313760761dc7f7b923a266ffe9b949fc724fe3d897614a5fbf49`  
		Last Modified: Mon, 23 Feb 2026 20:07:53 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd864d95333602e149ef2c5e1b3876cc618dfa0ca43e9e1a341a9bd82e087615`  
		Last Modified: Mon, 23 Feb 2026 20:07:52 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048b9814c01376537939e4914fbef47eacf2fbaec0dfdea10aff69ef7feeb9bc`  
		Last Modified: Mon, 23 Feb 2026 20:07:52 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d45755419bf7baf1ab293bf93eec3f6552a1818698776b021a0a3dcdf6e5ff`  
		Last Modified: Mon, 23 Feb 2026 20:07:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e6d165f8c0c063878b556bc1aaccfdd151af9649328607356eb3a04e0cc2f5`  
		Last Modified: Mon, 23 Feb 2026 20:07:52 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1551769ae67ef3da2573b3a0d4f107628ecee35a5f9ec6508a573089e344554`  
		Last Modified: Mon, 23 Feb 2026 20:07:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6a25b8253e7d51d10ee243fc7762cc41bfa72366372b22e55601293787576f`  
		Last Modified: Mon, 23 Feb 2026 20:07:50 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54a533c344da9df3395eff925a191e9974ead14dddbe773fea2000dd684660d`  
		Last Modified: Mon, 23 Feb 2026 20:07:50 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a5f28056b7237b180e86a445284fff777c09a3c8ae027d66db659e4064e5f4`  
		Last Modified: Mon, 23 Feb 2026 20:07:50 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a16bac6128385b05c0010b1a4bbdd6e362f5a5b965e9a9566b675204182d79`  
		Last Modified: Mon, 23 Feb 2026 20:07:50 GMT  
		Size: 375.9 KB (375946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba7dba58447fe97bba11b275f918cabc759191f01f6969ae622c0acd91340c9`  
		Last Modified: Mon, 23 Feb 2026 20:07:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
