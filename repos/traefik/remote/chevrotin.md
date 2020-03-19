## `traefik:chevrotin`

```console
$ docker pull traefik@sha256:c5218f66e8e41c9d5388c9443ba9f88cfb5c28c4d2f3a3e14dab4fdfa2478a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:chevrotin` - linux; amd64

```console
$ docker pull traefik@sha256:a638691e542297b5e9c0e418aac95b3cf73d45177e9682d6bca73149c3c69bab
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24780272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d1e6db5348027b0b036e274331d64662f34d66206a1ceaef0b17851c7f6885`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 23:42:56 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 18 Mar 2020 21:23:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc3/traefik_v2.2.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 18 Mar 2020 21:23:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 18 Mar 2020 21:23:19 GMT
EXPOSE 80
# Wed, 18 Mar 2020 21:23:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Mar 2020 21:23:19 GMT
CMD ["traefik"]
# Wed, 18 Mar 2020 21:23:19 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c141e361698e17a696b4b6bccfed69dc1eb931474405e31a0c907c01f4e272a6`  
		Last Modified: Thu, 06 Feb 2020 23:44:04 GMT  
		Size: 694.2 KB (694182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463bdeb7d88cb685b1d681a3d5c74d95efea6e0977efbe675e5171f92fd80322`  
		Last Modified: Wed, 18 Mar 2020 21:24:05 GMT  
		Size: 21.3 MB (21282765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3468d963bd074dbab9c5b9541fef31413dec4bd0eeb723b9cae6b305eb5033`  
		Last Modified: Wed, 18 Mar 2020 21:24:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:chevrotin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7343ec86cee5b8875dd3b0c8071dd1b4fc683c6a536a2f3f9d3c40053d56476e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23303483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a2346b154cd91daccbc831a27bfb664c31cd40c60e8cc0d6fff964b4ae0ee10`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:49:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 18 Mar 2020 21:49:48 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc3/traefik_v2.2.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 18 Mar 2020 21:49:49 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 18 Mar 2020 21:49:49 GMT
EXPOSE 80
# Wed, 18 Mar 2020 21:49:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Mar 2020 21:49:50 GMT
CMD ["traefik"]
# Wed, 18 Mar 2020 21:49:51 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a045f3facd048d78ccec1317c0b8d3aa5e1b76f175b643f80c704ec2aa89f8`  
		Last Modified: Thu, 06 Feb 2020 22:51:40 GMT  
		Size: 698.0 KB (698013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e333e2bf0f9313ead0c0a88bac6df2ede1c5637d79dbc2865a126509a0f6cb69`  
		Last Modified: Wed, 18 Mar 2020 21:51:57 GMT  
		Size: 20.0 MB (19987540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d1c766dbe760a08e7a18cfe490dc4eaf16ed1342083c6c15e7c659321076e0`  
		Last Modified: Wed, 18 Mar 2020 21:51:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:chevrotin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:c2d5761b1fd800e187c3dbfb3467b91a874280218158abe5de98d4c58c556e8c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23052125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b841b1ba74ace676d602e9044272d28f43fa1f4e481d3899dbf391b5827a9ec4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:44:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 18 Mar 2020 21:40:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc3/traefik_v2.2.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 18 Mar 2020 21:40:42 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 18 Mar 2020 21:40:43 GMT
EXPOSE 80
# Wed, 18 Mar 2020 21:40:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Mar 2020 21:40:44 GMT
CMD ["traefik"]
# Wed, 18 Mar 2020 21:40:45 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5c788179332343fbcbc8b97673406752232ca36894176cc87ece20ee279754`  
		Last Modified: Thu, 06 Feb 2020 22:47:56 GMT  
		Size: 696.0 KB (696043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3867e748ecfa0dd55b07ed8ca560b6e0a28b80a3d17c9cf2378320c2c39a7f`  
		Last Modified: Wed, 18 Mar 2020 21:44:49 GMT  
		Size: 19.6 MB (19632638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d09084103f1ea0bf4671712f5b695db09d0d41cc823b73b3f10772cd214ac7`  
		Last Modified: Wed, 18 Mar 2020 21:44:43 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
