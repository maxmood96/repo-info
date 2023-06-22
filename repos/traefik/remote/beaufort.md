## `traefik:beaufort`

```console
$ docker pull traefik@sha256:1d566a321843959d0d36eff27fb63a198bf5cd1880b0cd6c3775942ae963708f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:beaufort` - linux; amd64

```console
$ docker pull traefik@sha256:e5d4d00b48c51509c5b7fe051688e3d5254ae32459d822b04e845721f18f01b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42335491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60a5464b41e9a0fa02ad5c08069c9d61c3820b69ddb7539cda1ffbe66c36034`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 21 Jun 2023 00:26:12 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 22 Jun 2023 20:20:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 22 Jun 2023 20:20:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 22 Jun 2023 20:20:11 GMT
EXPOSE 80
# Thu, 22 Jun 2023 20:20:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jun 2023 20:20:11 GMT
CMD ["traefik"]
# Thu, 22 Jun 2023 20:20:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a9b499d7ae3ed84aef77186cbd2b1ae5418ddc653e721702ec1a35fa324a3`  
		Last Modified: Wed, 21 Jun 2023 00:26:31 GMT  
		Size: 622.2 KB (622241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8de7a217c34522d58e5296d7481baf74ca19f272f764c99614230fdfb6614d8`  
		Last Modified: Thu, 22 Jun 2023 20:20:30 GMT  
		Size: 38.3 MB (38315002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7429dc1ef43cddca6161c8b5989c8407cf8a2d9d8ffc38382d61b27cf27a3a69`  
		Last Modified: Thu, 22 Jun 2023 20:20:24 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm variant v6

```console
$ docker pull traefik@sha256:22f66eedf9ec04ff456795e91a8519a5e04f6110094f14e62df80ec6dba61f44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39833301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f3db4da9d6930a282aebd30a573f36d02e72a0c516e64bb475780cde5ba07ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:20 GMT
ADD file:4213782693bf27a9a6de23bc924ef0c4fb6b2d56010fc07b25f81edeba83b0d4 in / 
# Wed, 14 Jun 2023 18:49:20 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 22:49:44 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 22 Jun 2023 19:49:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 22 Jun 2023 19:49:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 22 Jun 2023 19:49:46 GMT
EXPOSE 80
# Thu, 22 Jun 2023 19:49:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jun 2023 19:49:46 GMT
CMD ["traefik"]
# Thu, 22 Jun 2023 19:49:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7836be94d3024e2042069c1095caba0b391f70c4b3d34a0475a503239d73dfba`  
		Last Modified: Wed, 14 Jun 2023 18:49:46 GMT  
		Size: 3.1 MB (3143353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be273dc11f4147c3910cbabccdb1e28523a1cb24f3f849c4c36c5a2ce46bd092`  
		Last Modified: Tue, 20 Jun 2023 22:50:03 GMT  
		Size: 622.7 KB (622687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07840166c34a2e12ef402033be29e8bb7524516da54ee6db2f3e5185ff495986`  
		Last Modified: Thu, 22 Jun 2023 19:50:04 GMT  
		Size: 36.1 MB (36066893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d892833f57673fca586bfc451c221c347befdfc63a587bf4360e09dac3a4487d`  
		Last Modified: Thu, 22 Jun 2023 19:49:58 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:70a1b62539b384a09d98e22bea5212f0120150377a85a599839d35897a55ef3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37406948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe5414a44cb1b3f5ada2c4d4477d9bb6c73103354707edb71a0adfb2138efb4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:10 GMT
ADD file:2b463f242cb7bf946452bb4781838348ecbe80da144fbab09f51d7e050dc68f3 in / 
# Wed, 14 Jun 2023 20:49:11 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 07:10:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 15 Jun 2023 07:10:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 15 Jun 2023 07:10:05 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 15 Jun 2023 07:10:05 GMT
EXPOSE 80
# Thu, 15 Jun 2023 07:10:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jun 2023 07:10:06 GMT
CMD ["traefik"]
# Thu, 15 Jun 2023 07:10:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a147224bf413aeffbbfcdcb5104d35c647256a5c32083f4d8134f09a4e74ddeb`  
		Last Modified: Wed, 14 Jun 2023 20:49:52 GMT  
		Size: 2.7 MB (2720801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d273c78104fe60b8d6b0a1d68c0b259293bd972e3ff515bc403a8bfbff6d88a9`  
		Last Modified: Thu, 15 Jun 2023 07:10:24 GMT  
		Size: 662.3 KB (662262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be3d50287a2f7fba1e120466ee42285469a74914da1378df40803a29c6245f3`  
		Last Modified: Thu, 15 Jun 2023 07:10:28 GMT  
		Size: 34.0 MB (34023516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452eba291077ce9af0d14edf868a5522679b04016d43f8a2e05b194d2618d210`  
		Last Modified: Thu, 15 Jun 2023 07:10:24 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; s390x

```console
$ docker pull traefik@sha256:9524d85b440d108c8641a51639b18fe27525d764a76327bfe2056ccf1f53f742
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40949702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5245200a97de3f0132729144c7ad3ec05bff569700b534486980a5d5139f063e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 22:49:13 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 22 Jun 2023 19:43:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 22 Jun 2023 19:43:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 22 Jun 2023 19:43:18 GMT
EXPOSE 80
# Thu, 22 Jun 2023 19:43:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jun 2023 19:43:19 GMT
CMD ["traefik"]
# Thu, 22 Jun 2023 19:43:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6fdd3c34275458c3ea0a8688ec24b8c7698ce5a31715673ae57aa8dd5b0844`  
		Last Modified: Tue, 20 Jun 2023 22:49:39 GMT  
		Size: 622.8 KB (622821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf960d6667a0be4844e96e2d1289b0e0220f968f717a8deaa46a4b97a2fe84ad`  
		Last Modified: Thu, 22 Jun 2023 19:43:56 GMT  
		Size: 37.1 MB (37113016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ec02b13b7d2100602de0b81f0e2f099162042d9fd9e2eddacc5f7c75313ded`  
		Last Modified: Thu, 22 Jun 2023 19:43:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
