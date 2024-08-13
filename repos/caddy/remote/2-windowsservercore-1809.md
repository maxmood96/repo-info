## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:1e91918f6579d3e8d7f98049c0c8478c64cb82ee1370e452c5e82d8b89fd2296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull caddy@sha256:9dd7282988c710649158bb6a3740b912a3ac0959876b4158bec95f09c17ffcb2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261400894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f372d0ba80da106acc9febe45ec90f07e429812103e18a64f3c31ff1e8a9577`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:27:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Aug 2024 20:28:47 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 13 Aug 2024 20:28:48 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 13 Aug 2024 20:29:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 13 Aug 2024 20:29:12 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 13 Aug 2024 20:29:13 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 13 Aug 2024 20:29:14 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Tue, 13 Aug 2024 20:29:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 13 Aug 2024 20:29:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 13 Aug 2024 20:29:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 13 Aug 2024 20:29:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 13 Aug 2024 20:29:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 13 Aug 2024 20:29:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 13 Aug 2024 20:29:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 13 Aug 2024 20:29:20 GMT
EXPOSE 80
# Tue, 13 Aug 2024 20:29:20 GMT
EXPOSE 443
# Tue, 13 Aug 2024 20:29:21 GMT
EXPOSE 443/udp
# Tue, 13 Aug 2024 20:29:21 GMT
EXPOSE 2019
# Tue, 13 Aug 2024 20:29:40 GMT
RUN caddy version
# Tue, 13 Aug 2024 20:29:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c43266bc4f0220a4b62c568aa5d637423601e92361d71cc5519de9a6fa2a59`  
		Last Modified: Tue, 13 Aug 2024 20:29:53 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f767d2b6e33ca2d9e64905ffe71117a96ab6425a8326241efea61fc9bbc82222`  
		Last Modified: Tue, 13 Aug 2024 20:29:52 GMT  
		Size: 527.9 KB (527863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6551cb57be2c89047839b6a1ecc7b1b86cc0f67ed8da89121ddbab23faa59f`  
		Last Modified: Tue, 13 Aug 2024 20:29:52 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3beb6aeb8d16bcb711886f2aa83cdec533b0a4894cb2bfbf403fac6808ba63c`  
		Last Modified: Tue, 13 Aug 2024 20:29:54 GMT  
		Size: 15.3 MB (15295206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9005ecd32014094b84de1a345859f8d3292d53dfab71e520014d300b076c0e3`  
		Last Modified: Tue, 13 Aug 2024 20:29:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ffda87ff771d371a3849d50cb4014a6621d118a8436ff04307760fc8c1718d`  
		Last Modified: Tue, 13 Aug 2024 20:29:51 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7124754f79a69f222e319f4ced1f9606ac7692358897b1ae76c6808faec3c5e6`  
		Last Modified: Tue, 13 Aug 2024 20:29:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5200f76c1f29dc61341848efcbeffafe85b8c529ff849bdc92448600eb5124eb`  
		Last Modified: Tue, 13 Aug 2024 20:29:50 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8967723c83a4fef106b1be9f2a64b04b4c1b47a7736c20c63dcb338bc6532a`  
		Last Modified: Tue, 13 Aug 2024 20:29:50 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e3df4fc252bc176183c81c6f500d7fbee24ca12f73f5f41436960d3a08dbb0`  
		Last Modified: Tue, 13 Aug 2024 20:29:50 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16d1c3c06cfbafa5029e57615e7533078e2879459ecadf59cd434ed1a4ccdb1`  
		Last Modified: Tue, 13 Aug 2024 20:29:49 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bd720a4fde6622c986fb286e09af013b3fe34dd34381a9c245faf055cfe93e`  
		Last Modified: Tue, 13 Aug 2024 20:29:48 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b50fd5747d01e5325da459cf7239fb3f365f2fa1eb256018c025f4171ca7cd2`  
		Last Modified: Tue, 13 Aug 2024 20:29:48 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9787aedf5acb61421aa57815671a56656cb8f11e304d518c2e7a17050b95af52`  
		Last Modified: Tue, 13 Aug 2024 20:29:48 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579770aad0ad2871496f8df81c369dbebb5e2aeb1e03c7f49a767eccc9a82d11`  
		Last Modified: Tue, 13 Aug 2024 20:29:48 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802edbbdeae1d639993fc80750b031b1ef3f7142fec2d20934aa4ae09f2230ee`  
		Last Modified: Tue, 13 Aug 2024 20:29:46 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2ac61e99d9dcb39453c19ff032b426611c4a93579f3f6888e96fe82b4c90ee`  
		Last Modified: Tue, 13 Aug 2024 20:29:46 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2d7cc43bae536b4afe6fbf9216472ab253ef86239884faa08e5fd9d9b6b28a`  
		Last Modified: Tue, 13 Aug 2024 20:29:46 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a90bb9020f8d8380bf4e0b1aa683d36971e28e0f7b3250b3e496c2a66b0d64`  
		Last Modified: Tue, 13 Aug 2024 20:29:46 GMT  
		Size: 352.3 KB (352252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624b78ba6d81aec0016619970afb9fc3ec7f810b823b5201c6699b77dfa1a961`  
		Last Modified: Tue, 13 Aug 2024 20:29:46 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
