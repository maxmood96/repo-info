## `traefik:latest`

```console
$ docker pull traefik@sha256:851f46de27b52db5f345c9405cec2b09bf611edf73dd8a499f5d6d04e5ab390f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:d1317cf3bd8e5016db5f48bfc227d0e0c1d9308cf3bf7c8bc6a2e0c8e084e5ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39614731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3019f7419217f4bca7942871abea2a289dc4b55ce05eece966740497dddd4c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Tue, 21 Mar 2023 20:20:09 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 21 Mar 2023 20:20:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.9/traefik_v2.9.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 21 Mar 2023 20:20:12 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 21 Mar 2023 20:20:12 GMT
EXPOSE 80
# Tue, 21 Mar 2023 20:20:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Mar 2023 20:20:13 GMT
CMD ["traefik"]
# Tue, 21 Mar 2023 20:20:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ae84fc17309bb4699abd282faa21aee64a99f3df7bb0d6aa950911f29b7add`  
		Last Modified: Tue, 21 Mar 2023 20:20:33 GMT  
		Size: 622.9 KB (622941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a996fe26bc3c22f7e278385b1c7862a3b602c0b0d9160434f3b3289da92aeaf`  
		Last Modified: Tue, 21 Mar 2023 20:20:38 GMT  
		Size: 35.6 MB (35616976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc083908edbac98ae426bbdcdce3368ddd2b0fe34e0189d87e80ce54072b344`  
		Last Modified: Tue, 21 Mar 2023 20:20:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:b45f882e5a6c1229a285aa460569aa45c487c878ff713c9d038d012a9ea7cf74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36629054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a42eaf1d53da78868c01e06a4c4b2fa9dde5d9aa210460f2948fb6f13f1781b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:51 GMT
ADD file:141468a99f598ddb90dbb73978d10c0f00d01ece185e157ac33a0a1414d45944 in / 
# Mon, 13 Mar 2023 16:12:51 GMT
CMD ["/bin/sh"]
# Tue, 14 Mar 2023 01:31:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Mar 2023 01:31:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.8/traefik_v2.9.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Mar 2023 01:31:35 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Mar 2023 01:31:35 GMT
EXPOSE 80
# Tue, 14 Mar 2023 01:31:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Mar 2023 01:31:36 GMT
CMD ["traefik"]
# Tue, 14 Mar 2023 01:31:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ed6cbaa656dcebfe8d252792a339ccf10dddd695875f07c9636d59a5baf85f3f`  
		Last Modified: Fri, 10 Feb 2023 20:50:51 GMT  
		Size: 2.6 MB (2633649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937713bf36e8ddb19f4d3861767039861708c7cc2a83e388aa80b6981bd0dc3a`  
		Last Modified: Tue, 14 Mar 2023 01:32:58 GMT  
		Size: 666.5 KB (666511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930bc1d14d49fdac439a68245e1142963cd97f387ff68c5eb42604d4fc03e324`  
		Last Modified: Tue, 14 Mar 2023 01:33:29 GMT  
		Size: 33.3 MB (33328526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331609b39766af505ef55a69602b8ceac4018a6aca9937efac165e7296ba860c`  
		Last Modified: Tue, 14 Mar 2023 01:33:22 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4f9029190d2211977970c56ebfa5fd21c1b32b7de344665fb0c1c3848055460e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36496410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbec9db2728fd3471e17d2dce1e771b59922d56183f86fb28b17559c86e77844`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Tue, 21 Mar 2023 20:34:30 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 21 Mar 2023 20:34:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.9/traefik_v2.9.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 21 Mar 2023 20:34:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 21 Mar 2023 20:34:34 GMT
EXPOSE 80
# Tue, 21 Mar 2023 20:34:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Mar 2023 20:34:34 GMT
CMD ["traefik"]
# Tue, 21 Mar 2023 20:34:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38fa8056026d2f43828b73e0ab328da2596a91223ac4c6ae73fef33ff33a318`  
		Last Modified: Tue, 21 Mar 2023 20:34:50 GMT  
		Size: 624.9 KB (624926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7de9d521520dc972618c023825b448a2304fb9c7130162d42f08d8256dac98`  
		Last Modified: Tue, 21 Mar 2023 20:34:54 GMT  
		Size: 32.6 MB (32609156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0653653cea54a5782ad23bc418616e571bb4e3467e36f548b8c9bda1ad1ea35f`  
		Last Modified: Tue, 21 Mar 2023 20:34:50 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:718bfa461a2e7c988a388097592ab729d273379f189c84604029de176ffa4dd3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38328113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c152252c9dc771f96eff694ef25b9e238e775ceee71d8caaa7540650029080`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:25 GMT
ADD file:03b2fb4d732a294329449ff55c5d84f7d2735e6510985718979469994f3a607b in / 
# Fri, 10 Feb 2023 21:41:26 GMT
CMD ["/bin/sh"]
# Tue, 21 Mar 2023 20:16:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 21 Mar 2023 20:16:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.9/traefik_v2.9.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 21 Mar 2023 20:16:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 21 Mar 2023 20:16:22 GMT
EXPOSE 80
# Tue, 21 Mar 2023 20:16:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Mar 2023 20:16:22 GMT
CMD ["traefik"]
# Tue, 21 Mar 2023 20:16:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:24c4f8de3549a39c64b0edc2cfa68769b373f35138d0f13725100160bb32d4e2`  
		Last Modified: Fri, 10 Feb 2023 21:42:16 GMT  
		Size: 3.2 MB (3175116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e50c9632bc9309a5c497a3fd5ada6e4337f762cde8e36db671131d5cf6cad6`  
		Last Modified: Tue, 21 Mar 2023 20:16:38 GMT  
		Size: 623.2 KB (623240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2943ab9186254c13754cb13940ad5d9fdd3f4e4e8a99cec6cca5f2d4b38c53ec`  
		Last Modified: Tue, 21 Mar 2023 20:16:43 GMT  
		Size: 34.5 MB (34529390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d40c3f37ccf57e3b0eec4caeb849ac768830c55b2d53889c84bc070ebbbe126`  
		Last Modified: Tue, 21 Mar 2023 20:16:38 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
