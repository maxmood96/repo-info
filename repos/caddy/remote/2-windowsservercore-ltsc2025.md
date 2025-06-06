## `caddy:2-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:a03dc134d725af61aae1b987d4a8e0e4345cafdd6411a789b97b982be7c63a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `caddy:2-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull caddy@sha256:269572f1c57f2049330683511170b38c7db428b64240bf14b9f417822cde4f19
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3447226990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a96f0d39cd7394fc2f873a81c4a5d4ec492b9cb429f7cf7c377c43bd48da13`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Fri, 06 Jun 2025 17:29:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Jun 2025 17:29:54 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 06 Jun 2025 17:29:55 GMT
ENV CADDY_VERSION=v2.10.0
# Fri, 06 Jun 2025 17:30:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.0/caddy_2.10.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cb97adb2bff5de752e470486ae72d55a6ddcfe4bfa43f09ed849260955df7f61385ac1e2d28fc80458b6910d71fa38d4295bb0689263dcc1743f2050d847c2ad')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 06 Jun 2025 17:30:05 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 06 Jun 2025 17:30:06 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 06 Jun 2025 17:30:07 GMT
LABEL org.opencontainers.image.version=v2.10.0
# Fri, 06 Jun 2025 17:30:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 06 Jun 2025 17:30:08 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 06 Jun 2025 17:30:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 06 Jun 2025 17:30:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 06 Jun 2025 17:30:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 06 Jun 2025 17:30:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 06 Jun 2025 17:30:13 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 06 Jun 2025 17:30:14 GMT
EXPOSE 80
# Fri, 06 Jun 2025 17:30:15 GMT
EXPOSE 443
# Fri, 06 Jun 2025 17:30:16 GMT
EXPOSE 443/udp
# Fri, 06 Jun 2025 17:30:17 GMT
EXPOSE 2019
# Fri, 06 Jun 2025 17:30:22 GMT
RUN caddy version
# Fri, 06 Jun 2025 17:30:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8fd91b29101901de9de308d9f65c6dd0247962ee8c83215f7d24f059d2015c`  
		Last Modified: Fri, 06 Jun 2025 17:34:05 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7140a0579ebeaeb92a4548544e4cc569bb4f7e2f079b1d96b4345b28c0032d4`  
		Last Modified: Fri, 06 Jun 2025 17:34:06 GMT  
		Size: 400.9 KB (400924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816ded71dccdca8a9dcb2bdb9c26858f7c55fe179adfcd7a509bad9ef63bbb31`  
		Last Modified: Fri, 06 Jun 2025 17:34:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ac18e8382a3893fcfaf5ce8c1b3cdb2e25a6071007462bbc18a4733522a045`  
		Last Modified: Fri, 06 Jun 2025 17:34:07 GMT  
		Size: 15.7 MB (15651112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bfd7f02ff2e5522e22b486dc511d51c5c1c8c554bdf9d3af2c80c5d42d1df3`  
		Last Modified: Fri, 06 Jun 2025 17:34:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e3d9f64416740619a4103a72258039de54c15ae615fc00cc341297f44e7d6b`  
		Last Modified: Fri, 06 Jun 2025 17:34:05 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2187bc01e0230f28782eab5c7bbaae03b2d624bb939c6ebdac6f149a8329ec81`  
		Last Modified: Fri, 06 Jun 2025 17:34:06 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5dd5cf35f1b86c28e38c2ec0b54d19f9fb27be4feaf7b54b84ab9441993762`  
		Last Modified: Fri, 06 Jun 2025 17:34:06 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3fea744c2c912a9b73a0f4ddc573babc26db9ba7de114793c3243e69d75245`  
		Last Modified: Fri, 06 Jun 2025 17:34:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4456bcd691e2688ed701ea58ed6537a5673564712d04db52abe95411c61d5867`  
		Last Modified: Fri, 06 Jun 2025 17:34:06 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a448ea1e9b4c24cd8fcd2685f922b4ba794df76cc85350196e86f2268a96b13d`  
		Last Modified: Fri, 06 Jun 2025 17:34:06 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfaff120a296a1d18b3893b373a0bb1124e4ac01bde6a19e52bc94e57b91b8ec`  
		Last Modified: Fri, 06 Jun 2025 17:34:08 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ff158c8b81dd76b841d39dcf3c82e5c556e78df95ac7e6282dc94928bad418`  
		Last Modified: Fri, 06 Jun 2025 17:34:08 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796e66d8e60586e760ee735f42939babe762a657cbccc0bdca8a99af217f3c4b`  
		Last Modified: Fri, 06 Jun 2025 17:34:09 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d0b0e061b50cf8d616286c38d991b2b0dd4471ea516334a8a5e41d06242b1e`  
		Last Modified: Fri, 06 Jun 2025 17:34:09 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a318e0ed45dc6da6df8b3126aaeabf18e61c74680ccd90febbd5453953aa2ed`  
		Last Modified: Fri, 06 Jun 2025 17:33:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc979ef7c956a1efcb8ca6a6977ce529763f3768670022da2833a2ff84019d1`  
		Last Modified: Fri, 06 Jun 2025 17:34:00 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8ee32d59dc3ffb31821b838eeec87062ae0d373bc1bd584cb6eaa411b78e33`  
		Last Modified: Fri, 06 Jun 2025 17:34:00 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3458f64c49adb275d7af6ed2f574a8a52724b9000589ee9241e6b0f43d8328`  
		Last Modified: Fri, 06 Jun 2025 17:34:01 GMT  
		Size: 387.0 KB (386971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f4f63c06bbb9e4a56aa06b919895dc1842e31b878080cc5a9f55e782fb0c64`  
		Last Modified: Fri, 06 Jun 2025 17:34:01 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
