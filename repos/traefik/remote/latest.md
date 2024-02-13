## `traefik:latest`

```console
$ docker pull traefik@sha256:919b100b8c15dfa0bfbf4ef2757bb1b65e35afb14057950c62e2fb3fd1de25b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:00cefa1183ba9d8972b24cca4f53f52cad38599ac01f225d11da004ac907c2db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44766978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0643a799ff035126e2e658c3f68c5e0c2294df52ab11f327a719dc384321a655`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:56:04 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 12 Feb 2024 22:35:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 12 Feb 2024 22:35:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 12 Feb 2024 22:35:58 GMT
EXPOSE 80
# Mon, 12 Feb 2024 22:35:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Feb 2024 22:35:58 GMT
CMD ["traefik"]
# Mon, 12 Feb 2024 22:35:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb44ecee72e822b5008b09918187fdd2017803e9c45293cd4e957e6a57c3814`  
		Last Modified: Sat, 27 Jan 2024 03:56:50 GMT  
		Size: 622.2 KB (622159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79657eb551df635327de56b2aa1843997bb9537815e500179869b5a259ac5f2`  
		Last Modified: Mon, 12 Feb 2024 22:36:18 GMT  
		Size: 40.7 MB (40735721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf6346c712abd00edf7a01385765ac0b0368e61e1a48c5a2e00f9a5e34725ae`  
		Last Modified: Mon, 12 Feb 2024 22:36:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:aeaf52d92e94f315d415f1bb928fceaee2d872bfcad424b52664573af7bbdeaa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42120051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3979f9e439cf5a087e9359ee5e032d9f4123410226c79fb2502f1d68a599454`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:30:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 12 Feb 2024 22:52:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 12 Feb 2024 22:52:53 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 12 Feb 2024 22:52:53 GMT
EXPOSE 80
# Mon, 12 Feb 2024 22:52:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Feb 2024 22:52:54 GMT
CMD ["traefik"]
# Mon, 12 Feb 2024 22:52:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160e025885c4ea1368dd04ecf92b0cc3d3629cbcc04b3ce166fd86dfc1c18dc8`  
		Last Modified: Sat, 27 Jan 2024 09:31:21 GMT  
		Size: 623.4 KB (623387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f302ea65232a84112631bd1219a92d65f0a55507463766c8656d07404cb6a281`  
		Last Modified: Mon, 12 Feb 2024 22:53:18 GMT  
		Size: 38.3 MB (38330900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3d96649d20fe429b99cbfc511040865d12aafc6f0d107bf3892d5f3ad20241`  
		Last Modified: Mon, 12 Feb 2024 22:53:12 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ffcf60c02304b3c0e4a1b9cb7b69a1456481f753d8b3dedbc19537f8d2377e15
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41662653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7364cc326d3f90676ba2650c7561acc23c27d13eafe6aaae869b87941f05502f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:18:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 12 Feb 2024 22:52:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 12 Feb 2024 22:52:30 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 12 Feb 2024 22:52:30 GMT
EXPOSE 80
# Mon, 12 Feb 2024 22:52:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Feb 2024 22:52:30 GMT
CMD ["traefik"]
# Mon, 12 Feb 2024 22:52:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcea9ca6b65b90478531ccf1a61fd544f055615af698f4d0bcd10f79c6d1ae3`  
		Last Modified: Sat, 27 Jan 2024 09:18:55 GMT  
		Size: 625.2 KB (625207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194fdd3d24251898c91d6d080d027a7cb6687b1f6932a4121a09b3bad76dc23b`  
		Last Modified: Mon, 12 Feb 2024 22:53:01 GMT  
		Size: 37.7 MB (37689362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ec410759f14835233a9e67a1ba4fab79c028f898f87ea9fe98a5bf4acc4d36`  
		Last Modified: Mon, 12 Feb 2024 22:52:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:2288dfb2b1598e5f78a8fc195fa6e63ca6583d2dc6aa705195667c924f065d9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43545936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f9f69a2c99970f7beec33266a119e580b233634ce1c93b82c55193b994bb84`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:20:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 12 Feb 2024 23:19:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 12 Feb 2024 23:19:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 12 Feb 2024 23:19:55 GMT
EXPOSE 80
# Mon, 12 Feb 2024 23:19:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Feb 2024 23:19:55 GMT
CMD ["traefik"]
# Mon, 12 Feb 2024 23:19:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf27425c88e5cc0862fced0d047cf74b71578f98896c1a758dee8855f093d79`  
		Last Modified: Sat, 27 Jan 2024 04:23:32 GMT  
		Size: 623.4 KB (623391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3fd5e93fa0b1f81fe2e15f1b973ef18bc797e2253f5b44811d6fa77eda0315`  
		Last Modified: Mon, 12 Feb 2024 23:21:30 GMT  
		Size: 39.7 MB (39679541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87af5bb6339aa046d6d9be943b4b463189ae85db29687c681b99eb95423c0de`  
		Last Modified: Mon, 12 Feb 2024 23:21:24 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
