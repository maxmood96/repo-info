## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:af9cf3d243d5c3d4f52d1953a4ec79b766bf0e797857522d94488651ca55d111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull caddy@sha256:9876a5401f4f74850b33c2e82e2a5b728fb51d39691f1b89c624f950cdcbfdba
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2089033307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556eec4497565ce0ef4673708d69457ca1ffb70661d1e64098deea1df1e23af1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 12 May 2026 21:26:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 21:49:44 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 May 2026 21:49:45 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:49:54 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('338f5557a1554677875b79dbc4b10d008781111ad29223811e64217936fa5d58602ddd54724ef1cb1473b7ec07805cf5286d6aa1e810febde7e36daf497d791f')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 May 2026 21:49:54 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 21:49:55 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 21:49:56 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:49:57 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:49:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:49:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:49:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:49:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:50:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:50:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:50:01 GMT
EXPOSE 80
# Tue, 12 May 2026 21:50:01 GMT
EXPOSE 443
# Tue, 12 May 2026 21:50:02 GMT
EXPOSE 443/udp
# Tue, 12 May 2026 21:50:02 GMT
EXPOSE 2019
# Tue, 12 May 2026 21:50:08 GMT
RUN caddy version
# Tue, 12 May 2026 21:50:08 GMT
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
	-	`sha256:5fcf3c0a9f07272631f90dc5bcab0d30239d5784909d8fb968afa1a7ee09591c`  
		Last Modified: Tue, 12 May 2026 21:28:37 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9de0950271e2103c49a4b32082432ca1784f60a2383d12ab543ad8da7e5f094`  
		Last Modified: Tue, 12 May 2026 21:50:18 GMT  
		Size: 514.3 KB (514265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c0346647a1aedb894e70a28050320366328997bad31569ae0d44e94c040816`  
		Last Modified: Tue, 12 May 2026 21:50:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3000c88843822e3dab4b098977b2f77281c5cee0aaaf373af35b554050fb10d9`  
		Last Modified: Tue, 12 May 2026 21:50:21 GMT  
		Size: 17.9 MB (17920167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989bdedc7c742ae41b0c2fe93323a94a07178ed6a05ab7e680f77213d8c76e28`  
		Last Modified: Tue, 12 May 2026 21:50:17 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49745a7e52fae5a0998b2c7b6db2d436347e78ca47720820dc04ad63c8771f79`  
		Last Modified: Tue, 12 May 2026 21:50:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e08df5aa667de9f27c829cb5081f6fdc74c859fc10b236cf80b8e1767240bc`  
		Last Modified: Tue, 12 May 2026 21:50:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b6068e4e7150261982e8c1276c46d0616f1020a86d7827c0fa3ef5f808ff00`  
		Last Modified: Tue, 12 May 2026 21:50:16 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b55f5a1913983906f9a456113dc92acfb4c78400a4f7af2acd9e080b8a1c4a5`  
		Last Modified: Tue, 12 May 2026 21:50:16 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ea0a81eb35dee051b3258611b1cf810a6575c5799f69405a636e11f9485789`  
		Last Modified: Tue, 12 May 2026 21:50:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0039e4d07b82d687993fa49f7c6479225b6f35c586cfcd0f8f925717a767c7d9`  
		Last Modified: Tue, 12 May 2026 21:50:14 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197e123249f2713fcd66fa738c4c948f463c9ae298c550a6c3e4b56f937172fa`  
		Last Modified: Tue, 12 May 2026 21:50:14 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1771c8508ff762a382110d7c525cd0ab4b616ea543f3c413570ed29b392c6027`  
		Last Modified: Tue, 12 May 2026 21:50:14 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eac6737ab8cc10a293811114ac7740900f48f4687d6385adf569718df085afd`  
		Last Modified: Tue, 12 May 2026 21:50:14 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95435b1f420da23e4fb73008839f144ef1dc4048a5ce9f78d91842516da31cdd`  
		Last Modified: Tue, 12 May 2026 21:50:14 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d869f4a4b4fdb4c994d318879abe9505ed26069e7b18b437dc861d38a1f82f46`  
		Last Modified: Tue, 12 May 2026 21:50:12 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8905f5983b3fe46ae24a68c347fdd0a8a86cb7521d83fd9d7410e61897b4dcd`  
		Last Modified: Tue, 12 May 2026 21:50:12 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59aa8457e354cb5bbad51fcd29301506254d2f6516c68e0c84c2b3b90157915`  
		Last Modified: Tue, 12 May 2026 21:50:12 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf59ae7e5fca7ffc430d2985047f3dfe2b56dbd1741c0e7d1ecc4cb3460f42b`  
		Last Modified: Tue, 12 May 2026 21:50:13 GMT  
		Size: 365.2 KB (365163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e442867733c8e89e37ba3a39b947e805e8534b6d68659785722e08c45baf2299`  
		Last Modified: Tue, 12 May 2026 21:50:12 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
