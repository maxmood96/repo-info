## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:db6a2b0026041bea53769581f8b30e5473c90b9059ab7d6ce3e6e23d3ebdc86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull caddy@sha256:e46f61d8d3a3ac16fb88a9cac634032317e9fb3e0339b963bb66c04343938eb0
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2699400503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d875c2e3b8e5e4449cf18d1496133db5b4b40a2508059729dabee2d3c81f65`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 00:29:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Sep 2021 18:40:24 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Sep 2021 18:40:25 GMT
ENV CADDY_VERSION=v2.4.5
# Wed, 15 Sep 2021 18:41:13 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.5/caddy_2.4.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('794fed88b38bfeb6b3b84d63f0887c4534fc3e94bd31173182b5af80fc7783beb41192bccffdb257a9bdf59541c6822a75fdbe714d65abc3c0cce9c02018eb82')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Sep 2021 18:41:14 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Sep 2021 18:41:15 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Sep 2021 18:41:16 GMT
VOLUME [c:/config]
# Wed, 15 Sep 2021 18:41:16 GMT
VOLUME [c:/data]
# Wed, 15 Sep 2021 18:41:17 GMT
LABEL org.opencontainers.image.version=v2.4.5
# Wed, 15 Sep 2021 18:41:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Sep 2021 18:41:19 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Sep 2021 18:41:20 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Sep 2021 18:41:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Sep 2021 18:41:22 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Sep 2021 18:41:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Sep 2021 18:41:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Sep 2021 18:41:25 GMT
EXPOSE 80
# Wed, 15 Sep 2021 18:41:26 GMT
EXPOSE 443
# Wed, 15 Sep 2021 18:41:27 GMT
EXPOSE 2019
# Wed, 15 Sep 2021 18:42:05 GMT
RUN caddy version
# Wed, 15 Sep 2021 18:42:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92dd43eae724dbe7e9e517c7fded74c5920ae7eb160042055178ceadf1916505`  
		Last Modified: Wed, 15 Sep 2021 01:09:40 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8d532e55ccbd3d074c15b46f36962f3145bb041cbe2b8764fba8c063a22dbe`  
		Last Modified: Wed, 15 Sep 2021 18:48:00 GMT  
		Size: 367.7 KB (367655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63580305fe45b2da5f32bdd27d2d44f99741b3b3b1c490aa30a42c7da0844a03`  
		Last Modified: Wed, 15 Sep 2021 18:47:59 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65256725f4589fdb7edae2dca90bcc6d181289a0635bc32a066d06c4493d5df9`  
		Last Modified: Wed, 15 Sep 2021 18:48:01 GMT  
		Size: 12.0 MB (12011057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e34c53ce33e8e13ecca73b838b34acf823d13259f3715141ab7d9a0adb06247`  
		Last Modified: Wed, 15 Sep 2021 18:47:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc971802df0150f68c16396a8cfa8c04d7a6be8d91af77d9836e07e5e5e6492`  
		Last Modified: Wed, 15 Sep 2021 18:47:58 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053ac14e6903e111098e730f06b6737b2eda6936ef2a96f232ef393c1b249fe3`  
		Last Modified: Wed, 15 Sep 2021 18:47:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2db744928e86bbcdf3686aa68da898f5da3a8a2c397409d2a2770ea5d199bbb`  
		Last Modified: Wed, 15 Sep 2021 18:47:56 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf9bc5e9bfce47b55aeaefce127a3595be1696cb03c9800415944038a2c3d40`  
		Last Modified: Wed, 15 Sep 2021 18:47:56 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb8790d90debfddc7783b7a87fed25be4803a11be01b97f13ce1c43bd807dc8`  
		Last Modified: Wed, 15 Sep 2021 18:47:55 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06336a7a0973bfbdbf99555931ad61b4660b7604c12218804cb2cd0468e224de`  
		Last Modified: Wed, 15 Sep 2021 18:47:55 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c149357bfc3368cab088ac25e38b4259bc07ee3e38cbdaff89712a143ac03d76`  
		Last Modified: Wed, 15 Sep 2021 18:47:54 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15be21b2a9e0b97cd9a0840833095b66ce3b60d5ca2266aae1ef0b3fb547a0b1`  
		Last Modified: Wed, 15 Sep 2021 18:47:53 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689698f074d6df2e1a60812b0a0cf717c52ff2e60a140e5e9ba35514a4b017d6`  
		Last Modified: Wed, 15 Sep 2021 18:47:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055d296dd263ef0a54c018f638069ff10425cd058ffef12f072722e9f1b3489c`  
		Last Modified: Wed, 15 Sep 2021 18:47:53 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1ac5526d2951e0d8922fcd260356b4560788ae6fe1809a908935d0293b9eca`  
		Last Modified: Wed, 15 Sep 2021 18:47:53 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6aa5deb3bb47f2cdd7f32728db4bf23dfd7b385ebb6b62c075d512d8617c9e6`  
		Last Modified: Wed, 15 Sep 2021 18:47:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7012c636d7e863a5d0c70b2a9c6d999690265f77de21cb15ca7124c238551a`  
		Last Modified: Wed, 15 Sep 2021 18:47:50 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb2e995793fd217ba5e66c6487b90c243377778dba5f0712b9e025c3615075c`  
		Last Modified: Wed, 15 Sep 2021 18:47:50 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de91b792d38361997c81440cd92a822e71dc2b3be1e72f2558fa442716db46b4`  
		Last Modified: Wed, 15 Sep 2021 18:47:51 GMT  
		Size: 300.5 KB (300521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387ea232222e69a0afb8b23ff09d95650635f709fe9b6c8f093391c71623b0f1`  
		Last Modified: Wed, 15 Sep 2021 18:47:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
