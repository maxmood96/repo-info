## `traefik:latest`

```console
$ docker pull traefik@sha256:545c32956b8dee9cdc4a4d2119e33960e570a89a93543af3ffb4f539a1252df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:03e2149c3a844ca9543edd2a7a8cd0e4a1a9afb543486ad99e737323eb5c25f2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28384776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52fea93906adbf3a0068165e55c2640a0efa634f983334c78db5f96476df9e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:47:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 18 Dec 2020 07:11:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.6/traefik_v2.3.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 18 Dec 2020 07:11:25 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 18 Dec 2020 07:11:25 GMT
EXPOSE 80
# Fri, 18 Dec 2020 07:11:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Dec 2020 07:11:25 GMT
CMD ["traefik"]
# Fri, 18 Dec 2020 07:11:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d0c2f48fede0de57585b470af3e8e9aa5534db90642859512370fa53ffac21`  
		Last Modified: Thu, 17 Dec 2020 00:48:37 GMT  
		Size: 671.7 KB (671697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce56bf94d075c7497495c1bd7a3736f69d225b246fa78034341e43cffd640afb`  
		Last Modified: Fri, 18 Dec 2020 07:12:04 GMT  
		Size: 24.9 MB (24897848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de49a0677f6c2c9a297b76616fe54ed8ee33a5f14060fc07d679e216b82d930`  
		Last Modified: Fri, 18 Dec 2020 07:11:56 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:866e86d9fed207750fcd6190a8378efdc4cf7378d7473adc7cefd1c47191659b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26482921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d24aa2dc32fc8e97983f070a55ec25388b336c2abd8dc31a1989b6e40c48dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:25:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jan 2021 23:56:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jan 2021 23:56:51 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jan 2021 23:56:52 GMT
EXPOSE 80
# Mon, 11 Jan 2021 23:56:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jan 2021 23:56:54 GMT
CMD ["traefik"]
# Mon, 11 Jan 2021 23:56:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab096bb24791df9de14fbfc840265a32c0d9f7be463db3a782da6095c0e6ad5b`  
		Last Modified: Thu, 17 Dec 2020 00:27:24 GMT  
		Size: 674.9 KB (674902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404789ba4d57d5ebd3b9e346ab72911d9cda4e7f9395248ea5bf3bdd24e42949`  
		Last Modified: Mon, 11 Jan 2021 23:57:59 GMT  
		Size: 23.2 MB (23186881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa14f62f5fc51679fe0d4c53102854dcfec037295c4ede9af9dbb4ecfe545a0`  
		Last Modified: Mon, 11 Jan 2021 23:57:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a514d1067beb769fd25480cba0ffc0bd2aa5f44a004f9d33dc0465c3db9f5c3c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26111594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d24230cfd873ab4443c7220976542b2f075654cae3e8fccbaac8566b2cb4859`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:27:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jan 2021 23:56:48 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jan 2021 23:56:49 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jan 2021 23:56:50 GMT
EXPOSE 80
# Mon, 11 Jan 2021 23:56:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jan 2021 23:56:52 GMT
CMD ["traefik"]
# Mon, 11 Jan 2021 23:56:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278abd308a18c136f69dcabbba1dc64486ebdad665d4a2f4ab14d2826ec08b06`  
		Last Modified: Thu, 17 Dec 2020 00:28:38 GMT  
		Size: 673.2 KB (673246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbb41b44f2a7a3f798996c121379f863b52ffee788ba79ada6d2cbe591a1153`  
		Last Modified: Mon, 11 Jan 2021 23:57:48 GMT  
		Size: 22.7 MB (22712763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892fcc3d290ad4bbced9b6b0286aa15edb6d4b398deda5bb13fa7ce6f4b9013a`  
		Last Modified: Mon, 11 Jan 2021 23:57:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
