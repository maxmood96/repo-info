## `traefik:latest`

```console
$ docker pull traefik@sha256:24773b7a8cf711c695957a076d550b5988bad343bf6e274ade55921ad8601841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:454062c529ab5beacb6fa42ea6da7dd9e9291ead3933211efd23146f9c8e3885
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48568396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae37360e39889a0d6c857dc724fc61f63409cd7d861c5abcfbd38e3411a765e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:57:04 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 23 Jul 2024 00:57:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.0/traefik_v3.1.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 23 Jul 2024 00:57:08 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 23 Jul 2024 00:57:08 GMT
EXPOSE 80
# Tue, 23 Jul 2024 00:57:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Jul 2024 00:57:09 GMT
CMD ["traefik"]
# Tue, 23 Jul 2024 00:57:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a322cd301f5b19d2620b7fcd176a2effb9583283af4cecc6806840780af6bb`  
		Last Modified: Tue, 23 Jul 2024 00:57:29 GMT  
		Size: 461.7 KB (461694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5857c2ee221f33cf852e30657784d8508c4aa3b58dc6baaf3f9aad3535ac60c6`  
		Last Modified: Tue, 23 Jul 2024 00:57:35 GMT  
		Size: 44.5 MB (44483441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38aa6d9846bfac6affb4e55e787dedda54d2ab89a63d10582c6b6c071ebd269`  
		Last Modified: Tue, 23 Jul 2024 00:57:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ef6f0d43c705e065f67bd506581ecb457e29a93b6e658bde073599a6fa6e1d3f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45376308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f1fe4bab8d82cce411629209e7774f71d391cf0e448fa65dd8a624945b03bef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:17:49 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 23 Jul 2024 01:17:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.0/traefik_v3.1.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 23 Jul 2024 01:17:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 23 Jul 2024 01:17:55 GMT
EXPOSE 80
# Tue, 23 Jul 2024 01:17:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Jul 2024 01:17:56 GMT
CMD ["traefik"]
# Tue, 23 Jul 2024 01:17:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a5f0c935c6c1eda4844d2b7ba995975a7190e47c1f1117040693822316aed6`  
		Last Modified: Tue, 23 Jul 2024 01:18:13 GMT  
		Size: 462.5 KB (462465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4c5ed7f7842ac19bf3b681b2b2f3a65d67f2ed3f24a631558bb5ec26f79f83`  
		Last Modified: Tue, 23 Jul 2024 01:18:19 GMT  
		Size: 41.5 MB (41548286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782978943359f2ba0fd7cac993f76b0efb8f0934453a52063c5d2e937eb21e4f`  
		Last Modified: Tue, 23 Jul 2024 01:18:12 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:59c13b667e6c56c36f5c66cc1dc43e7c2f5f0aee901f5be6b0e83bf08d60a6ed
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45760358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf7e5c4bf9f263a3505c57bfaed543c7021faf3fb99f4dbc37de8e13d57ee80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:47:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 23 Jul 2024 02:47:38 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.0/traefik_v3.1.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 23 Jul 2024 02:47:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 23 Jul 2024 02:47:39 GMT
EXPOSE 80
# Tue, 23 Jul 2024 02:47:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Jul 2024 02:47:39 GMT
CMD ["traefik"]
# Tue, 23 Jul 2024 02:47:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53df005727c4531718692629248a4acf9fcca84ebd56edab34cfb7439e3157c2`  
		Last Modified: Tue, 23 Jul 2024 02:47:56 GMT  
		Size: 463.7 KB (463747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0be67410fba90f49a0ed043b739c0789cc4dcdfd5c26dee5df293733eda4ee`  
		Last Modified: Tue, 23 Jul 2024 02:48:01 GMT  
		Size: 41.2 MB (41209309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa1a6a20bb95f4458699b628690cad73dc122f58455aa4feac738045c80a2ab`  
		Last Modified: Tue, 23 Jul 2024 02:47:56 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:38a099e913edcd2d1c97cf2cf7b39a31b97066eb8c06747abe5ba9a90740f946
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43796858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79cb8f76a5df02af3cc5d809f3a33c61cd0e38558675e276bc59ab298a177b64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:51:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 22 Jul 2024 23:51:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.0/traefik_v3.1.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 22 Jul 2024 23:51:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 22 Jul 2024 23:51:19 GMT
EXPOSE 80
# Mon, 22 Jul 2024 23:51:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 23:51:20 GMT
CMD ["traefik"]
# Mon, 22 Jul 2024 23:51:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66cc9c65616ee56352d34607b25bfd7ca70586365891d701497eee11fd6b917f`  
		Last Modified: Mon, 22 Jul 2024 23:51:47 GMT  
		Size: 464.1 KB (464125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aff83b1bbf8f7b99e9fc0b25f3509dba1d98d7e7cdc8ae0c10f3e0c9dba21fd`  
		Last Modified: Mon, 22 Jul 2024 23:51:54 GMT  
		Size: 39.8 MB (39760810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c221f0f22bdddda483b15a00d59b968c0cc838fd0cf08de6250624832486e3`  
		Last Modified: Mon, 22 Jul 2024 23:51:47 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:4b7263a5887cec40a8af7e47d1145fc61c02d125e23d886b365f40afd2e85472
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46629147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23ce94b85b105dc70869e3cc0885456d05719ee465a2e3a51ea4fb64d67ab6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 22 Jul 2024 22:21:00 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 22 Jul 2024 22:21:00 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 12:44:46 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 23 Jul 2024 12:45:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.0/traefik_v3.1.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 23 Jul 2024 12:45:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 23 Jul 2024 12:45:41 GMT
EXPOSE 80
# Tue, 23 Jul 2024 12:45:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Jul 2024 12:45:42 GMT
CMD ["traefik"]
# Tue, 23 Jul 2024 12:45:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3220e9e4f206b6ef30443855a7d18341eb7e8a6c5825f79355c757a1f65b3d`  
		Last Modified: Tue, 23 Jul 2024 12:48:05 GMT  
		Size: 462.4 KB (462409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366b4161b433cadc1f50c889ffd35d84651e0687fb15ff0dead5fa0415498ba1`  
		Last Modified: Tue, 23 Jul 2024 12:48:49 GMT  
		Size: 42.8 MB (42795696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6296186fd45d68a195238e26a27c93a1988e16f7bd6a76f3949f4cb53ed443ba`  
		Last Modified: Tue, 23 Jul 2024 12:48:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:11d8f6dc1b6d3cc9bd8408ccaa763dd41f0e965eba4cc7cbb101ece5295ba03a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46905158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4635e8d965f7b4b69a4656d3490bcf5d77cd424cd72a0b41124cdca63996fdbc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:04:30 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 23 Jul 2024 01:04:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.0/traefik_v3.1.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 23 Jul 2024 01:04:37 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 23 Jul 2024 01:04:37 GMT
EXPOSE 80
# Tue, 23 Jul 2024 01:04:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Jul 2024 01:04:38 GMT
CMD ["traefik"]
# Tue, 23 Jul 2024 01:04:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581abf80513b43cb8d51b8bcffc8fd390bdc8913788754fc844bcd330bc5cc79`  
		Last Modified: Tue, 23 Jul 2024 01:05:06 GMT  
		Size: 462.6 KB (462636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189347360e98e26a6710070f70693bb69ac3142fb056d393f644568b7deccdf7`  
		Last Modified: Tue, 23 Jul 2024 01:05:13 GMT  
		Size: 43.0 MB (42981087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7450f418dfbbc5bc29457eb8ee9a842d10e3fb17e4c70dbe9b681f92b91d30`  
		Last Modified: Tue, 23 Jul 2024 01:05:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
