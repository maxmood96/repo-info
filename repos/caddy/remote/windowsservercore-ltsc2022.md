## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:56617392ba81498bb88e4491f2ffa27c5d80f77ce43db19254777899ad7f0418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull caddy@sha256:6e564e7a0425b1363d9fed33204cb9eb3d22ef1094a003ea7b5cfca82cc7d956
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289309502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9fe9826111e075a75bd0b562ceb05d8b866ec3b1ebac075d4439c1ded2b8cf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:30:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:30:32 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 18 Apr 2025 03:30:33 GMT
ENV CADDY_VERSION=v2.9.1
# Fri, 18 Apr 2025 03:30:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 18 Apr 2025 03:30:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 18 Apr 2025 03:30:43 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 18 Apr 2025 03:30:43 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Fri, 18 Apr 2025 03:30:44 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 18 Apr 2025 03:30:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 18 Apr 2025 03:30:45 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 18 Apr 2025 03:30:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 18 Apr 2025 03:30:46 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 18 Apr 2025 03:30:47 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 18 Apr 2025 03:30:48 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 18 Apr 2025 03:30:48 GMT
EXPOSE 80
# Fri, 18 Apr 2025 03:30:49 GMT
EXPOSE 443
# Fri, 18 Apr 2025 03:30:49 GMT
EXPOSE 443/udp
# Fri, 18 Apr 2025 03:30:50 GMT
EXPOSE 2019
# Fri, 18 Apr 2025 03:30:55 GMT
RUN caddy version
# Fri, 18 Apr 2025 03:30:55 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c64ab72795edfb0ea7fae56070eeabae8aac5e8d76f0b44434075011926813e`  
		Last Modified: Fri, 18 Apr 2025 03:31:04 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd20a351eaed36a72519bf80eb163d3bfc147983f41b8e9844944a43307693f9`  
		Last Modified: Fri, 18 Apr 2025 03:31:05 GMT  
		Size: 357.1 KB (357107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de40864ac5c9b93d1e1a212699e6841119e71e1d92ebfad03df09f358ad2042`  
		Last Modified: Fri, 18 Apr 2025 03:31:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4417bc1632b54bfb9e3280bf39a017fe16b20dd08655698bc98f0f2bee576c79`  
		Last Modified: Fri, 18 Apr 2025 03:31:06 GMT  
		Size: 15.0 MB (15008551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4e51de2b7d1a086d0a35048663b6767c8213aece9103ae48e294b0cfcaab86`  
		Last Modified: Fri, 18 Apr 2025 03:31:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cf9167f8fca030d834d2097f043cb0250b8517f59c5501820cdaa4d5cf37a3`  
		Last Modified: Fri, 18 Apr 2025 03:31:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98fe8daff46b925952de1b5fd6e18ee380d40d99c949065ae151f59ac072e956`  
		Last Modified: Fri, 18 Apr 2025 03:31:03 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63725a7413c567bce4a524c49164e9a3e01489b9e20a328dd077d2e4a2f514`  
		Last Modified: Fri, 18 Apr 2025 03:31:03 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09cfd6a3ea5bda6db21ffc1c0b28f1115932f4265079765ca34f48bfe8462176`  
		Last Modified: Fri, 18 Apr 2025 03:31:02 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94d6ace0433d84781717da6ddf1d780962a383a2866f629a720b3870d2d982b`  
		Last Modified: Fri, 18 Apr 2025 03:31:02 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152df2ee72b5451dcf2971e10a86a154765b249574e246ebfd88b1942aba878a`  
		Last Modified: Fri, 18 Apr 2025 03:31:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545d1d912acea6afa7fb039d01a4e78542f6fcc238201117777b2e97d4360df2`  
		Last Modified: Fri, 18 Apr 2025 03:31:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47ea61f9ff05474058bd1466dc756991a5a7fb72448068729933c008544f027`  
		Last Modified: Fri, 18 Apr 2025 03:31:01 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed57e6d1bb5b93dc359b34e025775e9945fce7723e8a5dfb7392608546e9cc44`  
		Last Modified: Fri, 18 Apr 2025 03:31:01 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b13e9cb296f1d74b3386be11e580e168f2ad9a061921883bc9462664d10bff`  
		Last Modified: Fri, 18 Apr 2025 03:31:01 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28e2455c028a4075dd12fbc342d11b999d87c12fb66b515256b287b54d51400`  
		Last Modified: Fri, 18 Apr 2025 03:30:59 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431ab1818b95862632af6c6651cb07ed56b8bb9016864bafa4a2e63e22c0b56e`  
		Last Modified: Fri, 18 Apr 2025 03:30:59 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abfe2475444f153112c04f04300a69eb9edf9280ee15e47b50b503b98d8efa0`  
		Last Modified: Fri, 18 Apr 2025 03:30:59 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48c73da5eec7f179d0e1dae6c2eff576e472bde7a370ab6dd942b5f60738efa`  
		Last Modified: Fri, 18 Apr 2025 03:30:59 GMT  
		Size: 339.1 KB (339111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5711901a370637b62e3f2fc22252cd94574868cf8309e48c83fc3e1c06958f0`  
		Last Modified: Fri, 18 Apr 2025 03:30:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
