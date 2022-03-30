## `traefik:rocamadour`

```console
$ docker pull traefik@sha256:04c961d30ee3cdb45cf600085735a8eb49f0b98a67d5a43a8ddedbe33ec003ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:rocamadour` - linux; amd64

```console
$ docker pull traefik@sha256:e2ea2ac5cf8bfb6a8e41d28915248b01e9df2a86671ec8ef2c41c38fd3285570
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30341606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72463d8000a351a929f93834ecbb65b63e1d5dd2990f9c4b8f7cd28a66acec44`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 11:43:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 29 Mar 2022 11:43:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 29 Mar 2022 11:43:21 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 29 Mar 2022 11:43:21 GMT
EXPOSE 80
# Tue, 29 Mar 2022 11:43:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 11:43:21 GMT
CMD ["traefik"]
# Tue, 29 Mar 2022 11:43:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491249faa733d19d2c4f479860df3563c3f269d08d4c70b53926670b486092d5`  
		Last Modified: Tue, 29 Mar 2022 11:44:20 GMT  
		Size: 666.7 KB (666674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d69831426e507940b8a38e666a9849c8b208c236224b506894ad187a4d8915`  
		Last Modified: Tue, 29 Mar 2022 11:44:44 GMT  
		Size: 26.9 MB (26856210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f4831f8745c18f51d16dcc9683d09cad7a01a8055585cceff89021dc8c0ffb`  
		Last Modified: Tue, 29 Mar 2022 11:44:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:rocamadour` - linux; arm variant v6

```console
$ docker pull traefik@sha256:2a6e91644420e884a47301e5719349eb6a1c6c36d044c7fcfac6789aeb4b0475
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28508633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53d4c7eeb0769e066b9a8fb8fe3463393dc695230d928b19ddc768a90f265ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:46 GMT
ADD file:9670f4f7de6a9b8eb844e418daedd0dbad90009126790eb65e246b29cac5ea47 in / 
# Tue, 29 Mar 2022 00:49:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 13:21:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 29 Mar 2022 20:15:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.3/traefik_v2.6.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 29 Mar 2022 20:15:02 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 29 Mar 2022 20:15:03 GMT
EXPOSE 80
# Tue, 29 Mar 2022 20:15:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 20:15:04 GMT
CMD ["traefik"]
# Tue, 29 Mar 2022 20:15:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:79f5c9df0b90097bae07a9861e9e0e3f52a16b0bfde2793c4e14ad033cfb47f4`  
		Last Modified: Tue, 29 Mar 2022 00:51:45 GMT  
		Size: 2.6 MB (2626017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10449722d0e221d9f2d76fded7a3856b1e5da5de38e926c9dbde9dfeb95c67c8`  
		Last Modified: Tue, 29 Mar 2022 13:24:24 GMT  
		Size: 672.5 KB (672526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b16455b7f19741086604a735e590e982fa72a4f8419eebac2e4b93a6dded9e`  
		Last Modified: Tue, 29 Mar 2022 20:18:07 GMT  
		Size: 25.2 MB (25209721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ea9ec0719c1f9245fcee9072b0a02747793e15bec07885cade6befb6fa13b3`  
		Last Modified: Tue, 29 Mar 2022 20:17:50 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:rocamadour` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:389efd47a88684d6a5de22e08fa8f3b05a51125f6d1cb8529438c02db316da2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27882893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da1b66f3b3f44c03a6fdb670443e82aaecb43bb5f2aa9ed6e6c83e034aed210`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:12 GMT
ADD file:d0894581cf2fb7d7911ecb25bf0368675197db96d762977964ffc3a7ae8c774c in / 
# Tue, 29 Mar 2022 00:40:13 GMT
CMD ["/bin/sh"]
# Wed, 30 Mar 2022 00:36:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 30 Mar 2022 00:36:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.3/traefik_v2.6.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 30 Mar 2022 00:36:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 30 Mar 2022 00:36:46 GMT
EXPOSE 80
# Wed, 30 Mar 2022 00:36:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 00:36:48 GMT
CMD ["traefik"]
# Wed, 30 Mar 2022 00:36:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:810d54c7e01bab9975c1fb485c543715b76de7708166132520dfec0fc32c3754`  
		Last Modified: Tue, 29 Mar 2022 00:41:26 GMT  
		Size: 2.7 MB (2717494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ccccffb928e2a5ee60509b73b86ca0fdb241d4faa4ec3c8a41187a4d4ef811`  
		Last Modified: Wed, 30 Mar 2022 00:38:00 GMT  
		Size: 668.3 KB (668297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b8226739859cfb4b75f678e5763701e8cffe5e9ad74a2b17d9e118c246c511`  
		Last Modified: Wed, 30 Mar 2022 00:38:28 GMT  
		Size: 24.5 MB (24496734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43847c979776e200d78a78854ba08c58b6f0ebb612998f06722862b22292c405`  
		Last Modified: Wed, 30 Mar 2022 00:38:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:rocamadour` - linux; s390x

```console
$ docker pull traefik@sha256:03d2cee4f83e6ef05e4c94f5b961eb15e156ed8d5086eb25a137ac4be04e3208
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29136963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d6c33e80dd21af71cfd1e231279faaf09369e71e425e506f5cea8cc5c82899`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 29 Mar 2022 00:41:39 GMT
ADD file:7966b18580a674f84c4ff21ab8cffb1be1abafba3a0b270522609851441872aa in / 
# Tue, 29 Mar 2022 00:41:39 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:50:19 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 29 Mar 2022 15:50:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 29 Mar 2022 15:50:36 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 29 Mar 2022 15:50:36 GMT
EXPOSE 80
# Tue, 29 Mar 2022 15:50:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 15:50:36 GMT
CMD ["traefik"]
# Tue, 29 Mar 2022 15:50:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91b7491d90d64405ba8401c680bbab3f8f25b600b385adce6abaadf0a4070906`  
		Last Modified: Tue, 29 Mar 2022 00:45:50 GMT  
		Size: 2.6 MB (2604093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c042a90067715ab479af0e9be0eeef7c2fb4a4126ddea8ef7aaff6edecea976f`  
		Last Modified: Tue, 29 Mar 2022 15:51:38 GMT  
		Size: 672.5 KB (672488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39e12984ca0c15a98d3c59812f417a80b7e2ec3eed96f0cc2ae0869e7d60417`  
		Last Modified: Tue, 29 Mar 2022 15:54:40 GMT  
		Size: 25.9 MB (25860014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af006b066061505a13152ee85224bd11190c9488bb846bd8b5546ee9bb6b72b`  
		Last Modified: Tue, 29 Mar 2022 15:54:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
