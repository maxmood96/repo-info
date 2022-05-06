## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:06a63b084f3938d4da5ab1fd9c89832f8233a9d10a56d97685762496667dceac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull caddy@sha256:079298755264aaaf1312eeb016971909d89bc7f5e9ad8467a3d492731e859f62
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2730644260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65586fad6708ae50b8837d623ab4921176163a5dd28346adba6d8cb20a3ce603`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 May 2022 19:16:16 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/69bb1c539b3ee03fc91271a71653a77ca1e9d131/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/69bb1c539b3ee03fc91271a71653a77ca1e9d131/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 06 May 2022 19:16:17 GMT
ENV CADDY_VERSION=v2.5.1
# Fri, 06 May 2022 19:17:23 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.1/caddy_2.5.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4294796c4bd4bed0c593d83606a5413de30f35f88d624e1b1e5b6cd8672ffbcc7a689d7ce4ef30c1abea0e95eda62220faac15d2a6aca0c3e2b418abe7a74118')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 06 May 2022 19:17:24 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 06 May 2022 19:17:25 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 06 May 2022 19:17:26 GMT
LABEL org.opencontainers.image.version=v2.5.1
# Fri, 06 May 2022 19:17:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 06 May 2022 19:17:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 06 May 2022 19:17:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 06 May 2022 19:17:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 06 May 2022 19:17:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 06 May 2022 19:17:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 06 May 2022 19:17:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 06 May 2022 19:17:36 GMT
EXPOSE 80
# Fri, 06 May 2022 19:17:37 GMT
EXPOSE 443
# Fri, 06 May 2022 19:17:38 GMT
EXPOSE 2019
# Fri, 06 May 2022 19:19:00 GMT
RUN caddy version
# Fri, 06 May 2022 19:19:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf363a24c0769528da2882e57e64260d3fafac6d85b772f6ef87c98ab0129dd`  
		Last Modified: Fri, 06 May 2022 19:23:54 GMT  
		Size: 378.6 KB (378584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b8f425b31c579ec70be77ca533aa3acc30f542f2565085f2cef35c72b6ee77`  
		Last Modified: Fri, 06 May 2022 19:23:53 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0929b93a738937ffb835b7d8a3fb7fb81cdf09e3f84fbfb2923f8af2407b3197`  
		Last Modified: Fri, 06 May 2022 19:23:56 GMT  
		Size: 14.0 MB (14015575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b27affce7613f0662eb2b88645278243a109409ad3617971d78b6aebad5acd6`  
		Last Modified: Fri, 06 May 2022 19:23:51 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb689aaa9422c042de7e7fcfa797659d92126be5211626417b985c90e4409da`  
		Last Modified: Fri, 06 May 2022 19:23:51 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d73765c71db98680ada0ac9ebb0c853300ac92ba3b9e283b0814cf50359a7aa`  
		Last Modified: Fri, 06 May 2022 19:23:51 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ec0226891c1d7ef65a9d3e580b5b6db42d6542ad90bae6ca6304e4e94b001e`  
		Last Modified: Fri, 06 May 2022 19:23:51 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7fb7ec178948565e60ed25dc10f3201d3d7af166f34f20f595b9b65c5988ed`  
		Last Modified: Fri, 06 May 2022 19:23:51 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ec932b4dbd2710a4094bda8c984a7aec054abe87f47e6b71a3c55380f6f70b`  
		Last Modified: Fri, 06 May 2022 19:23:49 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016af95ff53e3ba95870f798282b6d2209c414f8d81cbf7588bc88990ff68365`  
		Last Modified: Fri, 06 May 2022 19:23:49 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6650e37988c8fceb532dd0303bc2a0742fd9fe42f1d0cfacfdb9192ba5a3a7a`  
		Last Modified: Fri, 06 May 2022 19:23:49 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ac4935cdc3bd5cbba80081df618e71d96d82b61c1af7066abb00ff191a5392`  
		Last Modified: Fri, 06 May 2022 19:23:49 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59ed2a376532f90a2a4aa720c52e4dab16bc7823c078b67d03b70910ba52d1f`  
		Last Modified: Fri, 06 May 2022 19:23:48 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00933ffb3ed3f11c0248c8cda209a5fd410dea197db357bb6b67421f10c839f0`  
		Last Modified: Fri, 06 May 2022 19:23:46 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e307f5f5a1b551f4c5664063380ab1914436ce882e4eb42e339ee36f536c7394`  
		Last Modified: Fri, 06 May 2022 19:23:46 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b5ab2d1873761befda92fd07127b31797542c94b402bff724356c33c660220`  
		Last Modified: Fri, 06 May 2022 19:23:46 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087ff169acd8f57ca49ff5639af4cbf95665e2e8223be47da85c419d5bac3b9d`  
		Last Modified: Fri, 06 May 2022 19:23:47 GMT  
		Size: 307.3 KB (307317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db87298c711d5e9cac629dd3521fd34ae7b17ca73e9924359024e1354e886003`  
		Last Modified: Fri, 06 May 2022 19:23:46 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
