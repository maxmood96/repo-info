## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:719e7a5b787e20985b0cdeec13fd4a3fba6b6c86a9b79341a5aaa6c2a3bab316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:39ca8d38bb88e8ba8d04cd6eeeff4530e4db12daa30aa37e9a0c216a3e2bcfcd
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195917858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d1ee2064b2ba3276dc02e0d45d90e35c36d900905b3034b07989d7ed715418`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:51:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:53:10 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 May 2024 21:53:11 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 21:53:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 May 2024 21:53:41 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 May 2024 21:53:42 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 May 2024 21:53:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 15 May 2024 21:53:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 May 2024 21:53:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 May 2024 21:53:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 May 2024 21:53:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 May 2024 21:53:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 May 2024 21:53:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 May 2024 21:53:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 May 2024 21:53:47 GMT
EXPOSE 80
# Wed, 15 May 2024 21:53:48 GMT
EXPOSE 443
# Wed, 15 May 2024 21:53:48 GMT
EXPOSE 443/udp
# Wed, 15 May 2024 21:53:49 GMT
EXPOSE 2019
# Wed, 15 May 2024 21:54:15 GMT
RUN caddy version
# Wed, 15 May 2024 21:54:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf806c2d672572084312cc8aa494c8cec9af9daeed5057140149ccdd78dfb80`  
		Last Modified: Wed, 15 May 2024 21:54:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b711793313f153495eabe6635f5e8f65dc570d25985f5f6f5ef8c5c0a553b3`  
		Last Modified: Wed, 15 May 2024 21:54:22 GMT  
		Size: 490.6 KB (490620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d512e0e145af2eec1bd2d32a9b70d48703e256b6d9f9d9199a3a7f36a6c9ff`  
		Last Modified: Wed, 15 May 2024 21:54:22 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4f52645186abe39ac028b27c3e9ffdd710c940ddd12cbbf6d0d29065a18491`  
		Last Modified: Wed, 15 May 2024 21:54:23 GMT  
		Size: 15.3 MB (15345743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa23f4c47c349e446197c7316ed9a453a261ab1fdd2c0e3f6d97d0992d65bdef`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc97aa1e7097461ea94ece8afce1dd51ee1513ef285e26743e89614b29a473ed`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576b04f13aae77f986a510a286ba44a00cca8d03b5fffdd0cd881ff59ace8a29`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e02a14a1675118d3895f8691bae0b4c39b9fb31f41a7cee00b3ee9d5d4c6c88`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5029ead0bd0493b4a27aca7d5c7dca9fd26f0cc230fe67e95131782faf30b3c7`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be7a0a749e1ab96c5b49167c6b4740f6dc3bd739e58052f848e479c157bbf16`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36dc01200272cf83484b850657355cb0afd45801fd642b0e293ddd0a66f5bc6e`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff9d61cc398e1efd41ad219b45a7b7954fdca6b77c3641a047a7d3bba2d24ca`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdefed17ab78afabf07e8a0de1c83420d9eb0a05a6a13b1bd7c6e4f42b785ff`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a28a34a28f7595618aa6579263ace412ec6492a68f265fb56920fb0f52e98e`  
		Last Modified: Wed, 15 May 2024 21:54:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e3072da47a79873523ce57465acf158d0f749d150dc2c354873ef27355441a`  
		Last Modified: Wed, 15 May 2024 21:54:19 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709eb7f911c45eec7a80d9be6b73eb9c5b76c363f768c6b678b5e5ec589fb7e0`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0118c06d85763da95dd5181f248564978ab3507b219ffb98f85c7473509bec42`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec0cdeef31f251bce3d39ed741232e9eb28b233af8a7373cf3c706afbfbbab4`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb36f279201594c9a4f90cc70e1669eb98c980e9582e2bb7b53fd70ec5071dda`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 348.0 KB (348008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a72e74ca019379f2a07ba0eaa7e4164da0d80823fab977d9182936d89dcf225`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
