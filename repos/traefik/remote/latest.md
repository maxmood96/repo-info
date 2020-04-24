## `traefik:latest`

```console
$ docker pull traefik@sha256:f5e013e1ef3b5b5490e352f4db3ea3b3470124d3a5533b816a33f1e4fade2376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:14591144dc8a5dc71dea7ac160683f5578bfbc9cf97aeb042270f843c68e0b17
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24783196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085ead62a4d4b06c34090d14b0f0b516d44777c7b9d71d36f09410f0aef9e5f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 22:23:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 22:23:37 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 22:23:38 GMT
EXPOSE 80
# Wed, 25 Mar 2020 22:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 22:23:38 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 22:23:38 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc367a6045f5900ec7708f21ef9df2d7ad7483e36d85979057667e0b3866bdb6`  
		Last Modified: Wed, 25 Mar 2020 22:24:27 GMT  
		Size: 21.3 MB (21285429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff697159d0030e6aa732f628239bba97a20cfba5cc1c0de77e822a794efedd5c`  
		Last Modified: Wed, 25 Mar 2020 22:24:22 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:c62920492c0306093ceb6f6c68e9d3160f01da9e50ccb3a46def877b8dc10f48
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23307268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fd5cbce915b15d4a61e495965bfe06d53d54d997a57b4e947307ad6ecf5beb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Apr 2020 22:36:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Apr 2020 22:36:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Apr 2020 22:36:41 GMT
EXPOSE 80
# Thu, 23 Apr 2020 22:36:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 22:36:43 GMT
CMD ["traefik"]
# Thu, 23 Apr 2020 22:36:44 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a36cf46e6cb6a8028db7cb68482816e710935254a7d463897840713066cf5ba`  
		Last Modified: Thu, 23 Apr 2020 22:39:24 GMT  
		Size: 698.1 KB (698086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47de4efdca0fea17f0e06d3dbf01b9fb6ddacceb0e536e3346d5dfbc53173b7a`  
		Last Modified: Thu, 23 Apr 2020 22:39:30 GMT  
		Size: 20.0 MB (19988878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75c90c2a0da73caa9c34384ef417269697a38010e34e03bcd43d69ef0889053`  
		Last Modified: Thu, 23 Apr 2020 22:39:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:925cda8f1d4c01d2965b221a2cfee10e56ee7362e7f0e7b5ad6c04327349c437
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23054677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269e148e952b870fb3b3cdbc7dec5f456cb871344571f71f1215f76f2d0a7c83`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 24 Apr 2020 12:14:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 24 Apr 2020 12:14:47 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 24 Apr 2020 12:14:48 GMT
EXPOSE 80
# Fri, 24 Apr 2020 12:14:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Apr 2020 12:14:49 GMT
CMD ["traefik"]
# Fri, 24 Apr 2020 12:14:49 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff968af61b86e34dc2412293ade430f77b7db53f7f4adb925fec30d3ccbb2876`  
		Last Modified: Fri, 24 Apr 2020 12:43:42 GMT  
		Size: 696.1 KB (696058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a36182df057d2b401ac8890611f0b85cee7228d1adba9918e7e7545552a5a4`  
		Last Modified: Fri, 24 Apr 2020 12:43:48 GMT  
		Size: 19.6 MB (19633826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc3d9d954ef8371e3c7e3a8994bd1e5ee69e929f7458ee5c10ddea58cc26382`  
		Last Modified: Fri, 24 Apr 2020 12:43:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
