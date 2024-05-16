## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:a5b412c8ac820da3d8ce408bc4bcb2fbc19a99c67fd16ff5c2c4ecce76276fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:e2f8b997d964717694810a581f3548bb7c88de368a40ad9de4f8ed414fa2c8bc
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128741780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48489f36ce94641f6ce5703ea4babbd5e2e2ec4dbffc55809b7eb8c1c1508cd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 22:03:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:03:58 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 May 2024 22:04:00 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 22:04:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 May 2024 22:04:09 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 May 2024 22:04:10 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 May 2024 22:04:10 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 15 May 2024 22:04:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 May 2024 22:04:12 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 May 2024 22:04:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 May 2024 22:04:13 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 May 2024 22:04:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 May 2024 22:04:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 May 2024 22:04:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 May 2024 22:04:16 GMT
EXPOSE 80
# Wed, 15 May 2024 22:04:16 GMT
EXPOSE 443
# Wed, 15 May 2024 22:04:17 GMT
EXPOSE 443/udp
# Wed, 15 May 2024 22:04:18 GMT
EXPOSE 2019
# Wed, 15 May 2024 22:04:22 GMT
RUN caddy version
# Wed, 15 May 2024 22:04:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cabe3592a5a508b32120c2f3f50485ce2af3e5b977d817fa71bff28061336aa`  
		Last Modified: Wed, 15 May 2024 22:04:29 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7474cb4a8c303c68700f525e09e3bd29bb30d75dc33c01ea4a44732e7e7423f7`  
		Last Modified: Wed, 15 May 2024 22:04:29 GMT  
		Size: 364.6 KB (364646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6d09183adf4d940c7dac96cc9d75af33bcb47d7d1811a7a296ad60e0d1b1c`  
		Last Modified: Wed, 15 May 2024 22:04:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ce5e1d365ba13fb9103a5020b6644b3ae71e76d5e4d159b2f58914673cf2bf`  
		Last Modified: Wed, 15 May 2024 22:04:31 GMT  
		Size: 15.3 MB (15344884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4aded66dd078b571ebb532e084c4af4f6beb685bd8a5b7524468e97c168f1a5`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37260cc3f9937e208886001176fd42c7113d3d49bdfd01a29d269126dc8538b4`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c851cec2c829abe440fde3ba79f95ec4728dfa01da5cb2b09e817e7581dc6b`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358cdf5957564add30758b73811ebe0f230cea2692cbb624fb5e8c369dcacc32`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b6a2684656992e4dbd6e42d4dd8ee988d00626cd55d362075a3a9243af3b54`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eccb203e5de222a30a89c733e9964e55090c4ff8911cd1ccd005de5e27d7523`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097f79242227f6445dd34eaf655c51b48ce991b72a1ff5589b72787ee42f0fee`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e44fe3122406544397fc58d026c1cbeea8aec0444aaa6d12a759f86d4714c4`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9401e6d173f17fd472a9adf0f3ce231ed4fa53e327b3fbd222c6900a64dc1573`  
		Last Modified: Wed, 15 May 2024 22:04:26 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571e94ebd3fc2965298bc42c3810c16d0f6f6c9743a4b5aea94dc66e91aad8e2`  
		Last Modified: Wed, 15 May 2024 22:04:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484373c77dd756bb7eb292a32b21c4039a936fdd0871ca3bc6c7467fcf29c77f`  
		Last Modified: Wed, 15 May 2024 22:04:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9921976cbc4a4e3222ce034a2dbd34e498f4bc4fc93f52173e5339e8fb9571`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca02ad3a0dd4ff383e5fe8cef81201aa747f513bd724391e69d4272e441fb1c3`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f0fb2e91e46705b26409f246c0bf3647718c5187bb6ffa4c5dafddfc2a2edd`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca09518406089c86c645aa571b37a75799b274b772b04a8fef6703ffbf76ef3b`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 338.9 KB (338919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd845c75155a3609f78ca6b64788a35f72e73fb0c060ee22b4dd7b4be922372f`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.17763.5820; amd64

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
