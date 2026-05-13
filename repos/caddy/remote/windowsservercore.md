## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:dd9caa282070e337fd66f329142021eb128ed437389f477540685dd67af617ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `caddy:windowsservercore` - windows version 10.0.26100.32690; amd64

```console
$ docker pull caddy@sha256:528df65834b097e07699437b741f4a87309527896ead10f906b7b74bbd084398
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2148703162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426f9237e7b75f1d275758c956dc5c46c33f82ca6b1c8e9f6f08e9974520e232`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 12 May 2026 21:26:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 21:49:50 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 May 2026 21:49:51 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:49:59 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('338f5557a1554677875b79dbc4b10d008781111ad29223811e64217936fa5d58602ddd54724ef1cb1473b7ec07805cf5286d6aa1e810febde7e36daf497d791f')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 May 2026 21:49:59 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 21:50:00 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 21:50:01 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:50:02 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:50:02 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:50:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:50:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:50:04 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:50:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:50:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:50:06 GMT
EXPOSE 80
# Tue, 12 May 2026 21:50:06 GMT
EXPOSE 443
# Tue, 12 May 2026 21:50:07 GMT
EXPOSE 443/udp
# Tue, 12 May 2026 21:50:08 GMT
EXPOSE 2019
# Tue, 12 May 2026 21:50:13 GMT
RUN caddy version
# Tue, 12 May 2026 21:50:13 GMT
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
	-	`sha256:53780a0be316cb5b2d6420aaa41e0fe9076e300d16c8962aa16655e112ebb41c`  
		Last Modified: Tue, 12 May 2026 21:27:40 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82711d79d0af3d5c7b89a16b52786dd329612bc19d4bd6f1aa5e1535d7c77b0f`  
		Last Modified: Tue, 12 May 2026 21:50:23 GMT  
		Size: 387.6 KB (387585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c3b5b5764cdd520485581ade13984fd8f9eb2eeee01e5016be243c0d381d62`  
		Last Modified: Tue, 12 May 2026 21:50:23 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06ea13d8fca217e66a56e0616c910935bd4e0571a2773d585e0d37044bbdbdc`  
		Last Modified: Tue, 12 May 2026 21:50:25 GMT  
		Size: 17.9 MB (17933377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c9bc212e968dd43e8b39baf995948d1f890e7a73378182f54491d35de93f57`  
		Last Modified: Tue, 12 May 2026 21:50:23 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5d3acfda3f3e021c7e16b8c3bb1222ff3205de62a014c0b672cfa206afc6d6`  
		Last Modified: Tue, 12 May 2026 21:50:21 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe751d37a100a071268c797880af34ddfafa5b79543449051eb39fc4eb1bf84`  
		Last Modified: Tue, 12 May 2026 21:50:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995b477388fa66c179daca7cee83bc04baf3b0399cd8c256a0069e0def4563b5`  
		Last Modified: Tue, 12 May 2026 21:50:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a26fef51278acf85e4c3fc298ff6114f94ea2e17a54d1c6d8722eaae8d4f14`  
		Last Modified: Tue, 12 May 2026 21:50:21 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41fb6eff192b0c14e6de74d0acecc9c61c114e5c7f21ff184e49741267c0dd8`  
		Last Modified: Tue, 12 May 2026 21:50:21 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5745b1feb9bdb6a46ccb0fb78285fff2cf9436d81640aca3c16ca74c2721d4`  
		Last Modified: Tue, 12 May 2026 21:50:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18448eca2c9162b11749797e4bfa28421065638a7bb716f81818acd1e200d11`  
		Last Modified: Tue, 12 May 2026 21:50:19 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8f93ba385cb5d11047d166a16a0b24e057c12f44ab8995007398e0f8757bf5`  
		Last Modified: Tue, 12 May 2026 21:50:19 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dadf8b984224f14437f1287ad414140a49e65e714664145a3cf8ddc6b96f73b`  
		Last Modified: Tue, 12 May 2026 21:50:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d14400322ea948f0c1351a68919be83f51c886160906fbd2fbd77b91ee84e1b`  
		Last Modified: Tue, 12 May 2026 21:50:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5906713bf1eea0daf6ea6d203bdc3b74986a249a31ed6fa019ba0b8ceddfd77`  
		Last Modified: Tue, 12 May 2026 21:50:18 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e03658dd80b8f3cbe58da624d05d27b3d70ef7bd9564a06a7d1a9160d0b322`  
		Last Modified: Tue, 12 May 2026 21:50:18 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117847fdb0dea3cf92d2e31bf1664f9f938cbf66d110d5292ab4b3d996f049a8`  
		Last Modified: Tue, 12 May 2026 21:50:18 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f00dd169ff59481667c83ee77147f404caef6763d8c8a9419742c817c18fdd`  
		Last Modified: Tue, 12 May 2026 21:50:18 GMT  
		Size: 373.9 KB (373850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c5d8d6dd43699581dc662c62cb551dc974f635db2fa6ea6fe5b4c13e4a5ad9`  
		Last Modified: Tue, 12 May 2026 21:50:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.20348.5020; amd64

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
