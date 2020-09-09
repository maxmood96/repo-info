## `traefik:latest`

```console
$ docker pull traefik@sha256:ea0aa8832bfd08369166baecd40b35fc58979df8f5dc5182e4e63ee6adbe66db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:a06428212b155cb688e7088609ffad20f0cf3e8e568c12af376234a92df9755a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25387047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f965f5a1fff83fd0c440bb12a20f14e40f0ad33f1dc6d4f57736751ded8c5f87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 09 Sep 2020 00:18:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.11/traefik_v2.2.11_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 09 Sep 2020 00:18:16 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 09 Sep 2020 00:18:16 GMT
EXPOSE 80
# Wed, 09 Sep 2020 00:18:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Sep 2020 00:18:16 GMT
CMD ["traefik"]
# Wed, 09 Sep 2020 00:18:16 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.11 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16506d32a25436b458a7f443ec1ca0d096d99d3479523c92c247856fc6148c0`  
		Last Modified: Fri, 24 Apr 2020 17:34:15 GMT  
		Size: 694.1 KB (694148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605303653d66773f0f99bd0e0a5bacb4168587f3037055222390ef7f1d352c0d`  
		Last Modified: Wed, 09 Sep 2020 00:18:53 GMT  
		Size: 21.9 MB (21879215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9005a35b171f9ed8c81d7393d795238fe6f017643450c1332fcfe68e04b4057`  
		Last Modified: Wed, 09 Sep 2020 00:18:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ff08c0c0c396097cf33925b84457515dd3afb3880f42f43ba5a452eec31e8669
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23864455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cd6c4b89864191ea1a0a1c7ed0416be946b081bb23a7dc66bc995af8d9a3dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 08 Sep 2020 21:56:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.11/traefik_v2.2.11_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 08 Sep 2020 21:56:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 08 Sep 2020 21:57:10 GMT
EXPOSE 80
# Tue, 08 Sep 2020 21:57:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Sep 2020 21:57:27 GMT
CMD ["traefik"]
# Tue, 08 Sep 2020 21:57:37 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.11 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:9e128f074fb2c219af4c56468908163db26b20bb819992a79fa962b6993b1bfd`  
		Last Modified: Tue, 08 Sep 2020 21:58:37 GMT  
		Size: 20.5 MB (20546064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eee7de7981c07a8c4e5c6e3814f264f96e1f9d9f3ec17d051ec3e971ed2edc7`  
		Last Modified: Tue, 08 Sep 2020 21:58:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ac8c7ffd65cdc79828dac2e7406ff0cbc71e1cf303d6b877766fc3adb18e628c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23623325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f35bc39f6a35e7247e6b5221747e52bd9ff05bf0a6ccc4661460e04d8a37dd5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 08 Sep 2020 23:07:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.11/traefik_v2.2.11_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 08 Sep 2020 23:07:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 08 Sep 2020 23:07:28 GMT
EXPOSE 80
# Tue, 08 Sep 2020 23:07:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Sep 2020 23:07:29 GMT
CMD ["traefik"]
# Tue, 08 Sep 2020 23:07:30 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.11 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:145e4e79b07b1aedc42c224a5e63f58a3b97555f95c9e8243c23e19ec5c4750e`  
		Last Modified: Tue, 08 Sep 2020 23:08:28 GMT  
		Size: 20.2 MB (20202475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e2827e7526e42443553490a290001495bfd8a6b3215e8a8fef9e174325f8da`  
		Last Modified: Tue, 08 Sep 2020 23:08:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
