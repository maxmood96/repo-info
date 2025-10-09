## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:1603006139680a0662d08ce063b15cb2949c2dcec05e8b43a1d555c7ed80f802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull caddy@sha256:3432ae806f193fdae814d3ddeb65c9946855c98976a1e2e1f5d9f75d93bf2d6f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2299444310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c31c8b4860be0760ba065dd8f7fd442eebf48693c4c0ecfef5fa982ebe513c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:53:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 22:00:58 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Sep 2025 22:00:59 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 10 Sep 2025 22:01:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Sep 2025 22:01:07 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Sep 2025 22:01:07 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Sep 2025 22:01:08 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Wed, 10 Sep 2025 22:01:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Sep 2025 22:01:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Sep 2025 22:01:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Sep 2025 22:01:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Sep 2025 22:01:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Sep 2025 22:01:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Sep 2025 22:01:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Sep 2025 22:01:12 GMT
EXPOSE 80
# Wed, 10 Sep 2025 22:01:13 GMT
EXPOSE 443
# Wed, 10 Sep 2025 22:01:13 GMT
EXPOSE 443/udp
# Wed, 10 Sep 2025 22:01:14 GMT
EXPOSE 2019
# Wed, 10 Sep 2025 22:01:18 GMT
RUN caddy version
# Wed, 10 Sep 2025 22:01:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Thu, 09 Oct 2025 10:32:05 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4099e040dab5364d73cd9952f3875b25d8740bc20dceb8e13860f7abbec96c`  
		Last Modified: Wed, 10 Sep 2025 21:54:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2b24e8d99c7e7c2b590a29ae1e5627f01d9a6438476321b10bdb82dc912aeb`  
		Last Modified: Wed, 10 Sep 2025 22:01:45 GMT  
		Size: 364.8 KB (364771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82917233b2ec0cc7033079eb2180a7cdc94fc9435dc2b23b2566e7e4e23d1b27`  
		Last Modified: Wed, 10 Sep 2025 22:01:45 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3905b88445f49f3ad485117989c7906c298a7f29eda7d9e91b0ed619f33b41b6`  
		Last Modified: Wed, 10 Sep 2025 22:01:46 GMT  
		Size: 16.6 MB (16569681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4b118a4e68fde4a8e6e7c3ea5909bfd7fc7d5d0db5ef6f3fb0cc4e5c2080da`  
		Last Modified: Wed, 10 Sep 2025 22:01:45 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f01adc8b5dbab3d5189b79586665dc303937c30c18c4fecad0ad8fd77900003`  
		Last Modified: Wed, 10 Sep 2025 22:01:45 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8f2d03bbbaa777b7d3fd18a245c8a85ec96d9f19084aa4a1e39b6d913bf07c`  
		Last Modified: Wed, 10 Sep 2025 22:01:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f00f78ce9743a4362997455907d90965b7e1d6eda585dcc10fdf0605a326b3`  
		Last Modified: Wed, 10 Sep 2025 22:01:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a20693c9337b17cde11cd4a7be58d3bd86ed547d4d03909d4855c815876f1d`  
		Last Modified: Wed, 10 Sep 2025 22:01:45 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247f46e9784dd9ce9d0e2e81d0124c86b857c9fcc03a24185a520e1fb246cbb6`  
		Last Modified: Wed, 10 Sep 2025 22:01:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127b115b4b0b6930fa69dc398e7e85839d00bf5e8648ca7c9a24ecd4af29efba`  
		Last Modified: Wed, 10 Sep 2025 22:01:45 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db369826bb358b14a9ae8a83429978a5e38a189376d3a8a1f00ebeb4656a2e0`  
		Last Modified: Wed, 10 Sep 2025 22:01:45 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5f9a9b80b3d16bacdbdec1f868a38d3e9049407bb1fda239c8afc6e22674be`  
		Last Modified: Wed, 10 Sep 2025 22:01:45 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52bb7925bfc506743710743e500aeda3eb29172ef49db25106a6c1966607faa`  
		Last Modified: Wed, 10 Sep 2025 22:01:45 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45a9df085ab14518759560d59053800a9d1022003306b75055764d523cf88f3`  
		Last Modified: Wed, 10 Sep 2025 22:01:45 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1b9250b94d60637384459d17b0211993c6665e2ba437b3e4f3b6b338789ba8`  
		Last Modified: Wed, 10 Sep 2025 22:01:45 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35f230158ace9f18200ce0918ec6abacb9b759b73580f6761bc4b5db7e4437f`  
		Last Modified: Wed, 10 Sep 2025 22:01:45 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fab236324b6f64a9960253bb90167d7a218d97a940746ba0c6d19f016cb5b78`  
		Last Modified: Wed, 10 Sep 2025 22:01:46 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de77ead9c814da62ede28eb9cab0cfa5ba54718b85a2fffc728b4bec5b14471b`  
		Last Modified: Wed, 10 Sep 2025 22:01:46 GMT  
		Size: 342.6 KB (342566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2c769d234b2078621b72211db758a8a17ac55bd2a59d0a89902b387569ae6a`  
		Last Modified: Wed, 10 Sep 2025 22:01:46 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
