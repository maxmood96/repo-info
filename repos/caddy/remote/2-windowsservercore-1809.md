## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:778cca090d5b4b748ee599fe57de9e6858bdeec56fb25f3d2fb06ea84876655a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull caddy@sha256:39a2bc3e8c37cb9cb637b81e79b51f1037f0e2abf55542054a2a0209c72b87c9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2026756150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35e275391e47b0c5fe768f372c6f0e4d2497da4ce395939d22c7275adc2b23a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:10:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:10:50 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 14 Nov 2024 20:10:51 GMT
ENV CADDY_VERSION=v2.8.4
# Thu, 14 Nov 2024 20:11:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 14 Nov 2024 20:11:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 14 Nov 2024 20:11:03 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 14 Nov 2024 20:11:03 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Thu, 14 Nov 2024 20:11:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 14 Nov 2024 20:11:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 14 Nov 2024 20:11:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 14 Nov 2024 20:11:06 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 14 Nov 2024 20:11:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 14 Nov 2024 20:11:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 14 Nov 2024 20:11:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 14 Nov 2024 20:11:08 GMT
EXPOSE 80
# Thu, 14 Nov 2024 20:11:09 GMT
EXPOSE 443
# Thu, 14 Nov 2024 20:11:10 GMT
EXPOSE 443/udp
# Thu, 14 Nov 2024 20:11:10 GMT
EXPOSE 2019
# Thu, 14 Nov 2024 20:11:14 GMT
RUN caddy version
# Thu, 14 Nov 2024 20:11:15 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb0f9f279ee9e7dd1365fd78330c7f3e78668607db2f238bee9607c40e6b24f`  
		Last Modified: Thu, 14 Nov 2024 20:11:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbaf8c2e8a44f71136f5c66c22624c9543d4af41ac7be0238e228ab14fd9418c`  
		Last Modified: Thu, 14 Nov 2024 20:11:25 GMT  
		Size: 491.4 KB (491387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c5617394a40d535165100722748023ccfa9c50966827839dba3d79bd9386f9`  
		Last Modified: Thu, 14 Nov 2024 20:11:24 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab8ed8a220d91302109bf6cbe4478f85e70ee56dec4c114d3f0ccf2d2dd5639`  
		Last Modified: Thu, 14 Nov 2024 20:11:26 GMT  
		Size: 15.3 MB (15250636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2d12426710e24ec694b91c686d2273d2a88d8b1326900efda20365d651bf28`  
		Last Modified: Thu, 14 Nov 2024 20:11:24 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4427fc6af43ffa5fd46154602de3a0ea215d52368ec9d3f06027ddfae0b6288`  
		Last Modified: Thu, 14 Nov 2024 20:11:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d17443d29347edbef2ee392a3ce34d3b2fff5a09ff22b14602f779f181d39c2`  
		Last Modified: Thu, 14 Nov 2024 20:11:23 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b40c761961919d175cfdbeb4d8a901472d1dcb809762cf41a2b078592a4299a`  
		Last Modified: Thu, 14 Nov 2024 20:11:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8808cbb63e5ecb63ddb38377aeb0c2bf9bc521afe25814833e516c27bc3d8e`  
		Last Modified: Thu, 14 Nov 2024 20:11:23 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c93089649ed47d5d717f1813413e28fadcb898514ebc2a88ceb851e6eedb4e`  
		Last Modified: Thu, 14 Nov 2024 20:11:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47c68fa4ead40db718d35e072d2b4a6abfdf114464a95dfbc162cac91cfcd33`  
		Last Modified: Thu, 14 Nov 2024 20:11:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190ae22380e2f8754a0d04305c2127afe3a1be175c0baa3883a544263ce5aef6`  
		Last Modified: Thu, 14 Nov 2024 20:11:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20134d1cb360692962b6ded6cb2df50a99078a8c2ba2897f64b745fa2074113`  
		Last Modified: Thu, 14 Nov 2024 20:11:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4cb77b4efeaf64d4f76aa0d699af96f412852b1fa01fc0ec7042b5b33894e26`  
		Last Modified: Thu, 14 Nov 2024 20:11:21 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd582b3bd22ac486cc83a125931b393b99ba51d26ad05cddf98b55a6adb151d`  
		Last Modified: Thu, 14 Nov 2024 20:11:21 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42a302e81f30ac657fbe24b5d6f1a9e65798dd8cf3f56f6a16a7b6219a5ae3b`  
		Last Modified: Thu, 14 Nov 2024 20:11:19 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edfedaf12dd13fd3d1574fb8aa8e7c9e9185ba2e43a9cb12c2b5a2a9bf09f20`  
		Last Modified: Thu, 14 Nov 2024 20:11:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02476dc02ade8429d71e3aa13029a1e232f12773616163792de770088fd5bef6`  
		Last Modified: Thu, 14 Nov 2024 20:11:19 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884bfa3fbd4101904cf32a683dc64a3e55ebec5c11c569387c605338c2d79459`  
		Last Modified: Thu, 14 Nov 2024 20:11:19 GMT  
		Size: 338.3 KB (338268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc16207501aa7c5836f0d1565d664fa399810398b687311fa844251896b780b`  
		Last Modified: Thu, 14 Nov 2024 20:11:19 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
