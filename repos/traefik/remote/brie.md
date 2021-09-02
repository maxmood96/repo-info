## `traefik:brie`

```console
$ docker pull traefik@sha256:b8802f19de00e344ae5f87d8dde9ff17360a10cf0d5e85949a065de89e69bbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:brie` - linux; amd64

```console
$ docker pull traefik@sha256:68f43dcc76a589f56839c997a50428a50b296b52299c42637d3cc98101252a43
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (29040605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa4d30f224b0690388615733d18d2c22bfe08b96cedde9fbebf588ef1a43160`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 17:28:37 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 02 Sep 2021 17:28:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.2/traefik_v2.5.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 02 Sep 2021 17:28:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 02 Sep 2021 17:28:41 GMT
EXPOSE 80
# Thu, 02 Sep 2021 17:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Sep 2021 17:28:41 GMT
CMD ["traefik"]
# Thu, 02 Sep 2021 17:28:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5295d3cd66d0f8651338b81063a408fcc2c70d810c92e5cb435c467a1939d60`  
		Last Modified: Thu, 02 Sep 2021 17:29:12 GMT  
		Size: 656.4 KB (656356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a668d6573180decf676feb4d8a4a0228c209d5c1ee12dc67f82881a3fe3e6245`  
		Last Modified: Thu, 02 Sep 2021 17:29:16 GMT  
		Size: 25.6 MB (25569436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5147406fd5c8b1a00e8cbbddb8a2b6c3da434268d5bfbc8e0d98cbb70b2df7`  
		Last Modified: Thu, 02 Sep 2021 17:29:11 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:brie` - linux; arm variant v6

```console
$ docker pull traefik@sha256:9c1172f6792773f08678c37f4de551c7a2a1d4d0c034e3412298586d18f88e19
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27284853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9ce4b665be1ef5825b1937974c8cdefc7adaa100553a0e131bef7dd9e67085`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 18:16:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 02 Sep 2021 18:16:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.2/traefik_v2.5.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 02 Sep 2021 18:16:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 02 Sep 2021 18:16:10 GMT
EXPOSE 80
# Thu, 02 Sep 2021 18:16:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Sep 2021 18:16:10 GMT
CMD ["traefik"]
# Thu, 02 Sep 2021 18:16:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac532a93bbc80e8fcf54dcb6ef0229a94aa4f2c94f0e9afec75226cfd91451c`  
		Last Modified: Thu, 02 Sep 2021 18:17:59 GMT  
		Size: 662.0 KB (661991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99aa880db88f752c79e3dd82e0022a16a56928ec2d77eed2755cf821b41b9160`  
		Last Modified: Thu, 02 Sep 2021 18:18:15 GMT  
		Size: 24.0 MB (23995047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63372cda2fd2655b2566608d3b9695c4f8d874102341530d6f240d692b535256`  
		Last Modified: Thu, 02 Sep 2021 18:17:58 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:brie` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:71b500c36ec3c881c73e28772d01a093a4ec6f44820aaf8a6b6f7d5faa6c206c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26697968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6fc50b9732b9564ef38927ead6989eca25b8520dc03fb71ce6229d884206f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 17:46:56 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 02 Sep 2021 17:46:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.2/traefik_v2.5.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 02 Sep 2021 17:46:59 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 02 Sep 2021 17:46:59 GMT
EXPOSE 80
# Thu, 02 Sep 2021 17:46:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Sep 2021 17:46:59 GMT
CMD ["traefik"]
# Thu, 02 Sep 2021 17:47:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55b5f395e28da206554aa30d5732a9b9a134cb909215e47a12301afbb1dba15`  
		Last Modified: Thu, 02 Sep 2021 17:47:55 GMT  
		Size: 658.9 KB (658858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd063daf3161b4aacc7decf9067ae7f44038f1975e9f27f228849742e9a86817`  
		Last Modified: Thu, 02 Sep 2021 17:47:59 GMT  
		Size: 23.3 MB (23326916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352613b664f9fb294d87cbf07347b5a13a2eea70c8e0a63fdba90e986cea9daa`  
		Last Modified: Thu, 02 Sep 2021 17:47:55 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
