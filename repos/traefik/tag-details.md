<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2.11`](#traefik211)
-	[`traefik:2.11-windowsservercore-1809`](#traefik211-windowsservercore-1809)
-	[`traefik:2.11-windowsservercore-ltsc2022`](#traefik211-windowsservercore-ltsc2022)
-	[`traefik:2.11.0`](#traefik2110)
-	[`traefik:2.11.0-windowsservercore-1809`](#traefik2110-windowsservercore-1809)
-	[`traefik:2.11.0-windowsservercore-ltsc2022`](#traefik2110-windowsservercore-ltsc2022)
-	[`traefik:3.0`](#traefik30)
-	[`traefik:3.0-windowsservercore-1809`](#traefik30-windowsservercore-1809)
-	[`traefik:3.0-windowsservercore-ltsc2022`](#traefik30-windowsservercore-ltsc2022)
-	[`traefik:3.0.0-beta5`](#traefik300-beta5)
-	[`traefik:3.0.0-beta5-windowsservercore-1809`](#traefik300-beta5-windowsservercore-1809)
-	[`traefik:3.0.0-beta5-windowsservercore-ltsc2022`](#traefik300-beta5-windowsservercore-ltsc2022)
-	[`traefik:beaufort`](#traefikbeaufort)
-	[`traefik:beaufort-windowsservercore-1809`](#traefikbeaufort-windowsservercore-1809)
-	[`traefik:beaufort-windowsservercore-ltsc2022`](#traefikbeaufort-windowsservercore-ltsc2022)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:mimolette`](#traefikmimolette)
-	[`traefik:mimolette-windowsservercore-1809`](#traefikmimolette-windowsservercore-1809)
-	[`traefik:mimolette-windowsservercore-ltsc2022`](#traefikmimolette-windowsservercore-ltsc2022)
-	[`traefik:v2.11`](#traefikv211)
-	[`traefik:v2.11-windowsservercore-1809`](#traefikv211-windowsservercore-1809)
-	[`traefik:v2.11-windowsservercore-ltsc2022`](#traefikv211-windowsservercore-ltsc2022)
-	[`traefik:v2.11.0`](#traefikv2110)
-	[`traefik:v2.11.0-windowsservercore-1809`](#traefikv2110-windowsservercore-1809)
-	[`traefik:v2.11.0-windowsservercore-ltsc2022`](#traefikv2110-windowsservercore-ltsc2022)
-	[`traefik:v3.0`](#traefikv30)
-	[`traefik:v3.0-windowsservercore-1809`](#traefikv30-windowsservercore-1809)
-	[`traefik:v3.0-windowsservercore-ltsc2022`](#traefikv30-windowsservercore-ltsc2022)
-	[`traefik:v3.0.0-beta5`](#traefikv300-beta5)
-	[`traefik:v3.0.0-beta5-windowsservercore-1809`](#traefikv300-beta5-windowsservercore-1809)
-	[`traefik:v3.0.0-beta5-windowsservercore-ltsc2022`](#traefikv300-beta5-windowsservercore-ltsc2022)
-	[`traefik:windowsservercore-1809`](#traefikwindowsservercore-1809)
-	[`traefik:windowsservercore-ltsc2022`](#traefikwindowsservercore-ltsc2022)

## `traefik:2.11`

```console
$ docker pull traefik@sha256:4be302e188b5be7637a3404033e8088c005059fd29e05b7ff04a403fac3d13ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:2.11` - linux; amd64

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

### `traefik:2.11` - linux; arm variant v6

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

### `traefik:2.11` - linux; arm64 variant v8

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

### `traefik:2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:a8f1545bdb1bb1a4433ef368846cf6461bcc7ef388c650b86bbc465bb2caf636
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40633824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7443e5aaf5d064276dd06a0496c831fc5268d17ddafca5b65461d882ae9da7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 00:49:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 13 Feb 2024 00:49:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 13 Feb 2024 00:49:43 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 13 Feb 2024 00:49:44 GMT
EXPOSE 80
# Tue, 13 Feb 2024 00:49:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 00:49:44 GMT
CMD ["traefik"]
# Tue, 13 Feb 2024 00:49:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925e55686869481cec5013bfadef6029068b862a623c351094616c335d8c5bcd`  
		Last Modified: Tue, 13 Feb 2024 00:50:00 GMT  
		Size: 623.2 KB (623154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7d1cfe7233426807a8e2f31e0b60c914effe76b40c293fc8d58e1de7f718b5`  
		Last Modified: Tue, 13 Feb 2024 00:50:06 GMT  
		Size: 36.7 MB (36651948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb48c7f4c6e411ddfad004f4158d98523a13d588ec355c926ae14d65bb76c02a`  
		Last Modified: Tue, 13 Feb 2024 00:49:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.11` - linux; s390x

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

## `traefik:2.11-windowsservercore-1809`

```console
$ docker pull traefik@sha256:f7a50aee3fdde8ae5aded88d0fd58aa317935ca72713ed0242bd7809a52ca570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `traefik:2.11-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull traefik@sha256:11af0932b812b0e766efaccb987c14ed57124d9a27d21f3f5a8a288c38b2bcb2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2111970705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c58c6f589458150087243450e772d2f48ee302060a0f2643320c385f090ed1`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Feb 2024 23:20:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 12 Feb 2024 23:20:08 GMT
EXPOSE 80
# Mon, 12 Feb 2024 23:20:09 GMT
ENTRYPOINT ["/traefik"]
# Mon, 12 Feb 2024 23:20:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8ac948dab7d4d3a44ab44e27a80115467b2f5fba68a58b377fef3e920bc5eb`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e3e182650f59b900de51ded3bfee4017bab649d21de3f8341d68e7f796aee9`  
		Last Modified: Mon, 12 Feb 2024 23:21:25 GMT  
		Size: 42.2 MB (42242650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423e3dfa116da7e393dd48909dd95ea29060058784705fe4f1c9f6604693da09`  
		Last Modified: Mon, 12 Feb 2024 23:21:16 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8afe44f0fa3239edbc49d366a7f03f1d76be21abfddc9db48f31b6348890ae`  
		Last Modified: Mon, 12 Feb 2024 23:21:16 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8f8c0f5fba9a08bf883b01678de16eeff3672d6dad6182f8bef0eb23331a60`  
		Last Modified: Mon, 12 Feb 2024 23:21:16 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8d6492e1e69eb6e597e2cde516711cb939eb3c1129348a26d521f91b2bb224c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull traefik@sha256:1680177046cc5ecb21fde7f8eec02a9b595da8f359c716cd82105e9d4ec205ea
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1942451131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21e0a8f8d21d9a7823d1efde30bf8a1456a52ea4bafa820e321d8cd13fb9c0c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Feb 2024 23:18:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 12 Feb 2024 23:18:25 GMT
EXPOSE 80
# Mon, 12 Feb 2024 23:18:26 GMT
ENTRYPOINT ["/traefik"]
# Mon, 12 Feb 2024 23:18:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddb0a528ee25f289459dfa0d84bac9a14b9127f771882f0b60425ffaab79933`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2b12c1d6e1dcf9104a5f56288334de87014cf49a113618ecb6eaf9f1d105c0`  
		Last Modified: Mon, 12 Feb 2024 23:20:58 GMT  
		Size: 42.2 MB (42232942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599fa3d7f5a1ac976cf218211ca963ce0208743ffbae93fc61e6f85ce7d61897`  
		Last Modified: Mon, 12 Feb 2024 23:20:48 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83394d5b11d0a0cfe86232947a0d42f0263549aaa4e8bae4d3b24659b6a8f0e`  
		Last Modified: Mon, 12 Feb 2024 23:20:47 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9ddee79f9f3d5a6e240d718947993b13695b4b956f8408788174e2e5aebb13`  
		Last Modified: Mon, 12 Feb 2024 23:20:48 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.0`

```console
$ docker pull traefik@sha256:4be302e188b5be7637a3404033e8088c005059fd29e05b7ff04a403fac3d13ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:2.11.0` - linux; amd64

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

### `traefik:2.11.0` - linux; arm variant v6

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

### `traefik:2.11.0` - linux; arm64 variant v8

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

### `traefik:2.11.0` - linux; ppc64le

```console
$ docker pull traefik@sha256:a8f1545bdb1bb1a4433ef368846cf6461bcc7ef388c650b86bbc465bb2caf636
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40633824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7443e5aaf5d064276dd06a0496c831fc5268d17ddafca5b65461d882ae9da7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 00:49:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 13 Feb 2024 00:49:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 13 Feb 2024 00:49:43 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 13 Feb 2024 00:49:44 GMT
EXPOSE 80
# Tue, 13 Feb 2024 00:49:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 00:49:44 GMT
CMD ["traefik"]
# Tue, 13 Feb 2024 00:49:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925e55686869481cec5013bfadef6029068b862a623c351094616c335d8c5bcd`  
		Last Modified: Tue, 13 Feb 2024 00:50:00 GMT  
		Size: 623.2 KB (623154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7d1cfe7233426807a8e2f31e0b60c914effe76b40c293fc8d58e1de7f718b5`  
		Last Modified: Tue, 13 Feb 2024 00:50:06 GMT  
		Size: 36.7 MB (36651948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb48c7f4c6e411ddfad004f4158d98523a13d588ec355c926ae14d65bb76c02a`  
		Last Modified: Tue, 13 Feb 2024 00:49:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.11.0` - linux; s390x

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

## `traefik:2.11.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:f7a50aee3fdde8ae5aded88d0fd58aa317935ca72713ed0242bd7809a52ca570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `traefik:2.11.0-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull traefik@sha256:11af0932b812b0e766efaccb987c14ed57124d9a27d21f3f5a8a288c38b2bcb2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2111970705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c58c6f589458150087243450e772d2f48ee302060a0f2643320c385f090ed1`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Feb 2024 23:20:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 12 Feb 2024 23:20:08 GMT
EXPOSE 80
# Mon, 12 Feb 2024 23:20:09 GMT
ENTRYPOINT ["/traefik"]
# Mon, 12 Feb 2024 23:20:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8ac948dab7d4d3a44ab44e27a80115467b2f5fba68a58b377fef3e920bc5eb`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e3e182650f59b900de51ded3bfee4017bab649d21de3f8341d68e7f796aee9`  
		Last Modified: Mon, 12 Feb 2024 23:21:25 GMT  
		Size: 42.2 MB (42242650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423e3dfa116da7e393dd48909dd95ea29060058784705fe4f1c9f6604693da09`  
		Last Modified: Mon, 12 Feb 2024 23:21:16 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8afe44f0fa3239edbc49d366a7f03f1d76be21abfddc9db48f31b6348890ae`  
		Last Modified: Mon, 12 Feb 2024 23:21:16 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8f8c0f5fba9a08bf883b01678de16eeff3672d6dad6182f8bef0eb23331a60`  
		Last Modified: Mon, 12 Feb 2024 23:21:16 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.0-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8d6492e1e69eb6e597e2cde516711cb939eb3c1129348a26d521f91b2bb224c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `traefik:2.11.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull traefik@sha256:1680177046cc5ecb21fde7f8eec02a9b595da8f359c716cd82105e9d4ec205ea
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1942451131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21e0a8f8d21d9a7823d1efde30bf8a1456a52ea4bafa820e321d8cd13fb9c0c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Feb 2024 23:18:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 12 Feb 2024 23:18:25 GMT
EXPOSE 80
# Mon, 12 Feb 2024 23:18:26 GMT
ENTRYPOINT ["/traefik"]
# Mon, 12 Feb 2024 23:18:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddb0a528ee25f289459dfa0d84bac9a14b9127f771882f0b60425ffaab79933`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2b12c1d6e1dcf9104a5f56288334de87014cf49a113618ecb6eaf9f1d105c0`  
		Last Modified: Mon, 12 Feb 2024 23:20:58 GMT  
		Size: 42.2 MB (42232942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599fa3d7f5a1ac976cf218211ca963ce0208743ffbae93fc61e6f85ce7d61897`  
		Last Modified: Mon, 12 Feb 2024 23:20:48 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83394d5b11d0a0cfe86232947a0d42f0263549aaa4e8bae4d3b24659b6a8f0e`  
		Last Modified: Mon, 12 Feb 2024 23:20:47 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9ddee79f9f3d5a6e240d718947993b13695b4b956f8408788174e2e5aebb13`  
		Last Modified: Mon, 12 Feb 2024 23:20:48 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0`

```console
$ docker pull traefik@sha256:81a73de0d19b6d61eb1f1e413d48835fe3c412f5ed3d9750dc3dab5c93519445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:3.0` - linux; amd64

```console
$ docker pull traefik@sha256:961c403e0663bec37efeaf1ead73eba9f2239ec078e8f3b9ab3766792e30b045
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44345773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6dc1a90d15dea9a0e5374c2006dff2618614d657b9e12d7cd3e4d6b84f02f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:55:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 27 Jan 2024 03:55:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 27 Jan 2024 03:55:59 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 27 Jan 2024 03:55:59 GMT
EXPOSE 80
# Sat, 27 Jan 2024 03:55:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:55:59 GMT
CMD ["traefik"]
# Sat, 27 Jan 2024 03:56:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987f790ee1434532d04fff8e0ff09f57d177ab515cdad8c0c3797d839f186a98`  
		Last Modified: Sat, 27 Jan 2024 03:56:31 GMT  
		Size: 622.8 KB (622798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c7ee2ab615563dcd9c77124f242f64520830ea09f7d2959e3e6beac42be540`  
		Last Modified: Sat, 27 Jan 2024 03:56:37 GMT  
		Size: 40.3 MB (40320065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2458ede9a225d84ce3b67646c51d2ed5856d8ccd5cad6699ae799fd8c4f8cd7`  
		Last Modified: Sat, 27 Jan 2024 03:56:31 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; arm variant v6

```console
$ docker pull traefik@sha256:af860a1868760cb06d86ce5fdb2d58de1ff91d170fe4463bdae23284245c80d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41867658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7db22bf0dacfe86ebff59713181fcd74d5d790a40478b5b614f30d9d3b9d95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:30:23 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 27 Jan 2024 09:30:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 27 Jan 2024 09:30:28 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 27 Jan 2024 09:30:29 GMT
EXPOSE 80
# Sat, 27 Jan 2024 09:30:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 09:30:29 GMT
CMD ["traefik"]
# Sat, 27 Jan 2024 09:30:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982de14def5b39cd26b9b8095345186dd246994b7be1bacf68fe810cf91b5c23`  
		Last Modified: Sat, 27 Jan 2024 09:31:00 GMT  
		Size: 623.2 KB (623196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f50cbdd950c3cac5a5ceb8ce0c09db1946dae3ed2a84888fe79e54f600fb464`  
		Last Modified: Sat, 27 Jan 2024 09:31:06 GMT  
		Size: 38.1 MB (38097034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2a36c4a8f6aca2e9235956d4601348e823fad16211b6381642ab8a60be4931`  
		Last Modified: Sat, 27 Jan 2024 09:30:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1a77ba6edfb6d1840bf931fc6606f1ef7f0ae4633eab030ded9b1eead051e28b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41269360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbaf9024ae8bdf537fdbb3faa4c2f6a8da7f499cb143ef32dc248ec47982f879`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:18:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 27 Jan 2024 09:18:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 27 Jan 2024 09:18:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 27 Jan 2024 09:18:10 GMT
EXPOSE 80
# Sat, 27 Jan 2024 09:18:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 09:18:10 GMT
CMD ["traefik"]
# Sat, 27 Jan 2024 09:18:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce888d1547525f7b13a7ebe582acbbf32204c342e18951b58b916087c88b4845`  
		Last Modified: Sat, 27 Jan 2024 09:18:37 GMT  
		Size: 625.1 KB (625057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886c5c7807cd7c4adfa8eec0080bf85774eeeae29bcfe3183f54f14ac52b30e3`  
		Last Modified: Sat, 27 Jan 2024 09:18:41 GMT  
		Size: 37.3 MB (37310574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5889fd36e1d40b740b76199b5027ff5cfbb211ef2f84d6b66ea9033680ea948c`  
		Last Modified: Sat, 27 Jan 2024 09:18:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; s390x

```console
$ docker pull traefik@sha256:f4e3b280fc13dc77f8d2cd719a4aaf5704f8c5e25f6c8d71ba2486bf791e826a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43097120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb2097c50b8e2f7fd81df1941d759374e1bfdb9c9a1f126c1bb2d3d5f0399f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:19:00 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 27 Jan 2024 04:19:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 27 Jan 2024 04:19:08 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 27 Jan 2024 04:19:09 GMT
EXPOSE 80
# Sat, 27 Jan 2024 04:19:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 04:19:09 GMT
CMD ["traefik"]
# Sat, 27 Jan 2024 04:19:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a8e27c29b7fbf4c31ac7c82b3365eca2436fa8dafa39d1b1e168d59122e8fb`  
		Last Modified: Sat, 27 Jan 2024 04:23:16 GMT  
		Size: 623.3 KB (623315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875f71b4d746606d64debc55adac979ebdcefe5a915cfc7e20e4ef8f7b535b9b`  
		Last Modified: Sat, 27 Jan 2024 04:23:22 GMT  
		Size: 39.3 MB (39255907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be081a497ca8dde0d3a277da18c62573fc002048c92f05b85916e95011faff9`  
		Last Modified: Sat, 27 Jan 2024 04:23:16 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7944d1f076a9bf9e011a18195fe94c09182ad20323889522f4be294cf6655fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `traefik:3.0-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull traefik@sha256:15bf0b1a96f1b47d7f8a3928652132d404b5bed226db4539ec838754f7f9f163
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2111553847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ce7c49f8a45aaf425200aa14d97c486e6634df0366a75b3de886310f596760`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 02:56:46 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Jan 2024 02:56:47 GMT
EXPOSE 80
# Thu, 11 Jan 2024 02:56:48 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Jan 2024 02:56:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8ac948dab7d4d3a44ab44e27a80115467b2f5fba68a58b377fef3e920bc5eb`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49eb407301b5f508eb7606a90cf89bd0a401890f635297ab6e6485757c1f4d27`  
		Last Modified: Thu, 11 Jan 2024 03:02:25 GMT  
		Size: 41.8 MB (41826107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fdc65ad253940c7733bfe5b1c14f88383310d5abc8ce7e814d074828c9f2c6`  
		Last Modified: Thu, 11 Jan 2024 03:02:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20260907bb69491a01d8371b08dbcb108fa09fed8512fc8f80336993ca327fee`  
		Last Modified: Thu, 11 Jan 2024 03:02:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57039062e8bd897795195c64f2f55927819e379db2efa832a09be6f9952e37d`  
		Last Modified: Thu, 11 Jan 2024 03:02:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:0084d4bb9d9b219532a0c7a49fd1438552a0689ae3c72d164e98cf248656d731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `traefik:3.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull traefik@sha256:4d4b9dfbd3f20864adb35cdfcd62f2ca4e516ec1fa96c31d050ed32c00459241
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1942021057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebbbdfd3595247cbe68a2b6ad81bfafb420be2d9c6a1f160f3983b12062f999`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 02:55:28 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Jan 2024 02:55:29 GMT
EXPOSE 80
# Thu, 11 Jan 2024 02:55:30 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Jan 2024 02:55:31 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddb0a528ee25f289459dfa0d84bac9a14b9127f771882f0b60425ffaab79933`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e15c3c989998bebef01e6f171e9fb5b99f55348a3879ed15b6daabff0aafb3`  
		Last Modified: Thu, 11 Jan 2024 03:02:00 GMT  
		Size: 41.8 MB (41803194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7c5c08c03f3a3058bd365dd03f1ca2060bbdf3565509f2ba85ef99d94048f1`  
		Last Modified: Thu, 11 Jan 2024 03:01:50 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a307677f611cfb82606d5fa26ca3281533fbbc379b98c4097015b614ab2d7d`  
		Last Modified: Thu, 11 Jan 2024 03:01:50 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fad3662942fc37b68b55707e5f6535567f16dd002fc3a19f491db73b04e7c3b`  
		Last Modified: Thu, 11 Jan 2024 03:01:50 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-beta5`

```console
$ docker pull traefik@sha256:81a73de0d19b6d61eb1f1e413d48835fe3c412f5ed3d9750dc3dab5c93519445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:3.0.0-beta5` - linux; amd64

```console
$ docker pull traefik@sha256:961c403e0663bec37efeaf1ead73eba9f2239ec078e8f3b9ab3766792e30b045
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44345773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6dc1a90d15dea9a0e5374c2006dff2618614d657b9e12d7cd3e4d6b84f02f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:55:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 27 Jan 2024 03:55:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 27 Jan 2024 03:55:59 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 27 Jan 2024 03:55:59 GMT
EXPOSE 80
# Sat, 27 Jan 2024 03:55:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:55:59 GMT
CMD ["traefik"]
# Sat, 27 Jan 2024 03:56:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987f790ee1434532d04fff8e0ff09f57d177ab515cdad8c0c3797d839f186a98`  
		Last Modified: Sat, 27 Jan 2024 03:56:31 GMT  
		Size: 622.8 KB (622798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c7ee2ab615563dcd9c77124f242f64520830ea09f7d2959e3e6beac42be540`  
		Last Modified: Sat, 27 Jan 2024 03:56:37 GMT  
		Size: 40.3 MB (40320065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2458ede9a225d84ce3b67646c51d2ed5856d8ccd5cad6699ae799fd8c4f8cd7`  
		Last Modified: Sat, 27 Jan 2024 03:56:31 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-beta5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:af860a1868760cb06d86ce5fdb2d58de1ff91d170fe4463bdae23284245c80d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41867658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7db22bf0dacfe86ebff59713181fcd74d5d790a40478b5b614f30d9d3b9d95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:30:23 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 27 Jan 2024 09:30:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 27 Jan 2024 09:30:28 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 27 Jan 2024 09:30:29 GMT
EXPOSE 80
# Sat, 27 Jan 2024 09:30:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 09:30:29 GMT
CMD ["traefik"]
# Sat, 27 Jan 2024 09:30:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982de14def5b39cd26b9b8095345186dd246994b7be1bacf68fe810cf91b5c23`  
		Last Modified: Sat, 27 Jan 2024 09:31:00 GMT  
		Size: 623.2 KB (623196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f50cbdd950c3cac5a5ceb8ce0c09db1946dae3ed2a84888fe79e54f600fb464`  
		Last Modified: Sat, 27 Jan 2024 09:31:06 GMT  
		Size: 38.1 MB (38097034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2a36c4a8f6aca2e9235956d4601348e823fad16211b6381642ab8a60be4931`  
		Last Modified: Sat, 27 Jan 2024 09:30:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-beta5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1a77ba6edfb6d1840bf931fc6606f1ef7f0ae4633eab030ded9b1eead051e28b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41269360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbaf9024ae8bdf537fdbb3faa4c2f6a8da7f499cb143ef32dc248ec47982f879`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:18:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 27 Jan 2024 09:18:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 27 Jan 2024 09:18:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 27 Jan 2024 09:18:10 GMT
EXPOSE 80
# Sat, 27 Jan 2024 09:18:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 09:18:10 GMT
CMD ["traefik"]
# Sat, 27 Jan 2024 09:18:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce888d1547525f7b13a7ebe582acbbf32204c342e18951b58b916087c88b4845`  
		Last Modified: Sat, 27 Jan 2024 09:18:37 GMT  
		Size: 625.1 KB (625057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886c5c7807cd7c4adfa8eec0080bf85774eeeae29bcfe3183f54f14ac52b30e3`  
		Last Modified: Sat, 27 Jan 2024 09:18:41 GMT  
		Size: 37.3 MB (37310574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5889fd36e1d40b740b76199b5027ff5cfbb211ef2f84d6b66ea9033680ea948c`  
		Last Modified: Sat, 27 Jan 2024 09:18:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-beta5` - linux; s390x

```console
$ docker pull traefik@sha256:f4e3b280fc13dc77f8d2cd719a4aaf5704f8c5e25f6c8d71ba2486bf791e826a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43097120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb2097c50b8e2f7fd81df1941d759374e1bfdb9c9a1f126c1bb2d3d5f0399f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:19:00 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 27 Jan 2024 04:19:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 27 Jan 2024 04:19:08 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 27 Jan 2024 04:19:09 GMT
EXPOSE 80
# Sat, 27 Jan 2024 04:19:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 04:19:09 GMT
CMD ["traefik"]
# Sat, 27 Jan 2024 04:19:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a8e27c29b7fbf4c31ac7c82b3365eca2436fa8dafa39d1b1e168d59122e8fb`  
		Last Modified: Sat, 27 Jan 2024 04:23:16 GMT  
		Size: 623.3 KB (623315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875f71b4d746606d64debc55adac979ebdcefe5a915cfc7e20e4ef8f7b535b9b`  
		Last Modified: Sat, 27 Jan 2024 04:23:22 GMT  
		Size: 39.3 MB (39255907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be081a497ca8dde0d3a277da18c62573fc002048c92f05b85916e95011faff9`  
		Last Modified: Sat, 27 Jan 2024 04:23:16 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-beta5-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7944d1f076a9bf9e011a18195fe94c09182ad20323889522f4be294cf6655fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `traefik:3.0.0-beta5-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull traefik@sha256:15bf0b1a96f1b47d7f8a3928652132d404b5bed226db4539ec838754f7f9f163
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2111553847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ce7c49f8a45aaf425200aa14d97c486e6634df0366a75b3de886310f596760`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 02:56:46 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Jan 2024 02:56:47 GMT
EXPOSE 80
# Thu, 11 Jan 2024 02:56:48 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Jan 2024 02:56:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8ac948dab7d4d3a44ab44e27a80115467b2f5fba68a58b377fef3e920bc5eb`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49eb407301b5f508eb7606a90cf89bd0a401890f635297ab6e6485757c1f4d27`  
		Last Modified: Thu, 11 Jan 2024 03:02:25 GMT  
		Size: 41.8 MB (41826107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fdc65ad253940c7733bfe5b1c14f88383310d5abc8ce7e814d074828c9f2c6`  
		Last Modified: Thu, 11 Jan 2024 03:02:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20260907bb69491a01d8371b08dbcb108fa09fed8512fc8f80336993ca327fee`  
		Last Modified: Thu, 11 Jan 2024 03:02:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57039062e8bd897795195c64f2f55927819e379db2efa832a09be6f9952e37d`  
		Last Modified: Thu, 11 Jan 2024 03:02:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-beta5-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:0084d4bb9d9b219532a0c7a49fd1438552a0689ae3c72d164e98cf248656d731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `traefik:3.0.0-beta5-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull traefik@sha256:4d4b9dfbd3f20864adb35cdfcd62f2ca4e516ec1fa96c31d050ed32c00459241
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1942021057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebbbdfd3595247cbe68a2b6ad81bfafb420be2d9c6a1f160f3983b12062f999`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 02:55:28 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Jan 2024 02:55:29 GMT
EXPOSE 80
# Thu, 11 Jan 2024 02:55:30 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Jan 2024 02:55:31 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddb0a528ee25f289459dfa0d84bac9a14b9127f771882f0b60425ffaab79933`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e15c3c989998bebef01e6f171e9fb5b99f55348a3879ed15b6daabff0aafb3`  
		Last Modified: Thu, 11 Jan 2024 03:02:00 GMT  
		Size: 41.8 MB (41803194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7c5c08c03f3a3058bd365dd03f1ca2060bbdf3565509f2ba85ef99d94048f1`  
		Last Modified: Thu, 11 Jan 2024 03:01:50 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a307677f611cfb82606d5fa26ca3281533fbbc379b98c4097015b614ab2d7d`  
		Last Modified: Thu, 11 Jan 2024 03:01:50 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fad3662942fc37b68b55707e5f6535567f16dd002fc3a19f491db73b04e7c3b`  
		Last Modified: Thu, 11 Jan 2024 03:01:50 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort`

```console
$ docker pull traefik@sha256:81a73de0d19b6d61eb1f1e413d48835fe3c412f5ed3d9750dc3dab5c93519445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:beaufort` - linux; amd64

```console
$ docker pull traefik@sha256:961c403e0663bec37efeaf1ead73eba9f2239ec078e8f3b9ab3766792e30b045
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44345773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6dc1a90d15dea9a0e5374c2006dff2618614d657b9e12d7cd3e4d6b84f02f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:55:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 27 Jan 2024 03:55:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 27 Jan 2024 03:55:59 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 27 Jan 2024 03:55:59 GMT
EXPOSE 80
# Sat, 27 Jan 2024 03:55:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:55:59 GMT
CMD ["traefik"]
# Sat, 27 Jan 2024 03:56:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987f790ee1434532d04fff8e0ff09f57d177ab515cdad8c0c3797d839f186a98`  
		Last Modified: Sat, 27 Jan 2024 03:56:31 GMT  
		Size: 622.8 KB (622798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c7ee2ab615563dcd9c77124f242f64520830ea09f7d2959e3e6beac42be540`  
		Last Modified: Sat, 27 Jan 2024 03:56:37 GMT  
		Size: 40.3 MB (40320065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2458ede9a225d84ce3b67646c51d2ed5856d8ccd5cad6699ae799fd8c4f8cd7`  
		Last Modified: Sat, 27 Jan 2024 03:56:31 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm variant v6

```console
$ docker pull traefik@sha256:af860a1868760cb06d86ce5fdb2d58de1ff91d170fe4463bdae23284245c80d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41867658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7db22bf0dacfe86ebff59713181fcd74d5d790a40478b5b614f30d9d3b9d95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:30:23 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 27 Jan 2024 09:30:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 27 Jan 2024 09:30:28 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 27 Jan 2024 09:30:29 GMT
EXPOSE 80
# Sat, 27 Jan 2024 09:30:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 09:30:29 GMT
CMD ["traefik"]
# Sat, 27 Jan 2024 09:30:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982de14def5b39cd26b9b8095345186dd246994b7be1bacf68fe810cf91b5c23`  
		Last Modified: Sat, 27 Jan 2024 09:31:00 GMT  
		Size: 623.2 KB (623196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f50cbdd950c3cac5a5ceb8ce0c09db1946dae3ed2a84888fe79e54f600fb464`  
		Last Modified: Sat, 27 Jan 2024 09:31:06 GMT  
		Size: 38.1 MB (38097034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2a36c4a8f6aca2e9235956d4601348e823fad16211b6381642ab8a60be4931`  
		Last Modified: Sat, 27 Jan 2024 09:30:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1a77ba6edfb6d1840bf931fc6606f1ef7f0ae4633eab030ded9b1eead051e28b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41269360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbaf9024ae8bdf537fdbb3faa4c2f6a8da7f499cb143ef32dc248ec47982f879`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:18:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 27 Jan 2024 09:18:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 27 Jan 2024 09:18:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 27 Jan 2024 09:18:10 GMT
EXPOSE 80
# Sat, 27 Jan 2024 09:18:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 09:18:10 GMT
CMD ["traefik"]
# Sat, 27 Jan 2024 09:18:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce888d1547525f7b13a7ebe582acbbf32204c342e18951b58b916087c88b4845`  
		Last Modified: Sat, 27 Jan 2024 09:18:37 GMT  
		Size: 625.1 KB (625057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886c5c7807cd7c4adfa8eec0080bf85774eeeae29bcfe3183f54f14ac52b30e3`  
		Last Modified: Sat, 27 Jan 2024 09:18:41 GMT  
		Size: 37.3 MB (37310574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5889fd36e1d40b740b76199b5027ff5cfbb211ef2f84d6b66ea9033680ea948c`  
		Last Modified: Sat, 27 Jan 2024 09:18:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; s390x

```console
$ docker pull traefik@sha256:f4e3b280fc13dc77f8d2cd719a4aaf5704f8c5e25f6c8d71ba2486bf791e826a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43097120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb2097c50b8e2f7fd81df1941d759374e1bfdb9c9a1f126c1bb2d3d5f0399f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:19:00 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 27 Jan 2024 04:19:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 27 Jan 2024 04:19:08 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 27 Jan 2024 04:19:09 GMT
EXPOSE 80
# Sat, 27 Jan 2024 04:19:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 04:19:09 GMT
CMD ["traefik"]
# Sat, 27 Jan 2024 04:19:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a8e27c29b7fbf4c31ac7c82b3365eca2436fa8dafa39d1b1e168d59122e8fb`  
		Last Modified: Sat, 27 Jan 2024 04:23:16 GMT  
		Size: 623.3 KB (623315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875f71b4d746606d64debc55adac979ebdcefe5a915cfc7e20e4ef8f7b535b9b`  
		Last Modified: Sat, 27 Jan 2024 04:23:22 GMT  
		Size: 39.3 MB (39255907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be081a497ca8dde0d3a277da18c62573fc002048c92f05b85916e95011faff9`  
		Last Modified: Sat, 27 Jan 2024 04:23:16 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7944d1f076a9bf9e011a18195fe94c09182ad20323889522f4be294cf6655fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `traefik:beaufort-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull traefik@sha256:15bf0b1a96f1b47d7f8a3928652132d404b5bed226db4539ec838754f7f9f163
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2111553847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ce7c49f8a45aaf425200aa14d97c486e6634df0366a75b3de886310f596760`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 02:56:46 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Jan 2024 02:56:47 GMT
EXPOSE 80
# Thu, 11 Jan 2024 02:56:48 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Jan 2024 02:56:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8ac948dab7d4d3a44ab44e27a80115467b2f5fba68a58b377fef3e920bc5eb`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49eb407301b5f508eb7606a90cf89bd0a401890f635297ab6e6485757c1f4d27`  
		Last Modified: Thu, 11 Jan 2024 03:02:25 GMT  
		Size: 41.8 MB (41826107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fdc65ad253940c7733bfe5b1c14f88383310d5abc8ce7e814d074828c9f2c6`  
		Last Modified: Thu, 11 Jan 2024 03:02:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20260907bb69491a01d8371b08dbcb108fa09fed8512fc8f80336993ca327fee`  
		Last Modified: Thu, 11 Jan 2024 03:02:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57039062e8bd897795195c64f2f55927819e379db2efa832a09be6f9952e37d`  
		Last Modified: Thu, 11 Jan 2024 03:02:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:0084d4bb9d9b219532a0c7a49fd1438552a0689ae3c72d164e98cf248656d731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `traefik:beaufort-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull traefik@sha256:4d4b9dfbd3f20864adb35cdfcd62f2ca4e516ec1fa96c31d050ed32c00459241
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1942021057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebbbdfd3595247cbe68a2b6ad81bfafb420be2d9c6a1f160f3983b12062f999`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 02:55:28 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Jan 2024 02:55:29 GMT
EXPOSE 80
# Thu, 11 Jan 2024 02:55:30 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Jan 2024 02:55:31 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddb0a528ee25f289459dfa0d84bac9a14b9127f771882f0b60425ffaab79933`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e15c3c989998bebef01e6f171e9fb5b99f55348a3879ed15b6daabff0aafb3`  
		Last Modified: Thu, 11 Jan 2024 03:02:00 GMT  
		Size: 41.8 MB (41803194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7c5c08c03f3a3058bd365dd03f1ca2060bbdf3565509f2ba85ef99d94048f1`  
		Last Modified: Thu, 11 Jan 2024 03:01:50 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a307677f611cfb82606d5fa26ca3281533fbbc379b98c4097015b614ab2d7d`  
		Last Modified: Thu, 11 Jan 2024 03:01:50 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fad3662942fc37b68b55707e5f6535567f16dd002fc3a19f491db73b04e7c3b`  
		Last Modified: Thu, 11 Jan 2024 03:01:50 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:4be302e188b5be7637a3404033e8088c005059fd29e05b7ff04a403fac3d13ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
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

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:a8f1545bdb1bb1a4433ef368846cf6461bcc7ef388c650b86bbc465bb2caf636
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40633824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7443e5aaf5d064276dd06a0496c831fc5268d17ddafca5b65461d882ae9da7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 00:49:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 13 Feb 2024 00:49:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 13 Feb 2024 00:49:43 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 13 Feb 2024 00:49:44 GMT
EXPOSE 80
# Tue, 13 Feb 2024 00:49:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 00:49:44 GMT
CMD ["traefik"]
# Tue, 13 Feb 2024 00:49:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925e55686869481cec5013bfadef6029068b862a623c351094616c335d8c5bcd`  
		Last Modified: Tue, 13 Feb 2024 00:50:00 GMT  
		Size: 623.2 KB (623154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7d1cfe7233426807a8e2f31e0b60c914effe76b40c293fc8d58e1de7f718b5`  
		Last Modified: Tue, 13 Feb 2024 00:50:06 GMT  
		Size: 36.7 MB (36651948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb48c7f4c6e411ddfad004f4158d98523a13d588ec355c926ae14d65bb76c02a`  
		Last Modified: Tue, 13 Feb 2024 00:49:59 GMT  
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

## `traefik:mimolette`

```console
$ docker pull traefik@sha256:4be302e188b5be7637a3404033e8088c005059fd29e05b7ff04a403fac3d13ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:mimolette` - linux; amd64

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

### `traefik:mimolette` - linux; arm variant v6

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

### `traefik:mimolette` - linux; arm64 variant v8

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

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:a8f1545bdb1bb1a4433ef368846cf6461bcc7ef388c650b86bbc465bb2caf636
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40633824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7443e5aaf5d064276dd06a0496c831fc5268d17ddafca5b65461d882ae9da7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 00:49:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 13 Feb 2024 00:49:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 13 Feb 2024 00:49:43 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 13 Feb 2024 00:49:44 GMT
EXPOSE 80
# Tue, 13 Feb 2024 00:49:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 00:49:44 GMT
CMD ["traefik"]
# Tue, 13 Feb 2024 00:49:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925e55686869481cec5013bfadef6029068b862a623c351094616c335d8c5bcd`  
		Last Modified: Tue, 13 Feb 2024 00:50:00 GMT  
		Size: 623.2 KB (623154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7d1cfe7233426807a8e2f31e0b60c914effe76b40c293fc8d58e1de7f718b5`  
		Last Modified: Tue, 13 Feb 2024 00:50:06 GMT  
		Size: 36.7 MB (36651948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb48c7f4c6e411ddfad004f4158d98523a13d588ec355c926ae14d65bb76c02a`  
		Last Modified: Tue, 13 Feb 2024 00:49:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; s390x

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

## `traefik:mimolette-windowsservercore-1809`

```console
$ docker pull traefik@sha256:f7a50aee3fdde8ae5aded88d0fd58aa317935ca72713ed0242bd7809a52ca570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `traefik:mimolette-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull traefik@sha256:11af0932b812b0e766efaccb987c14ed57124d9a27d21f3f5a8a288c38b2bcb2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2111970705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c58c6f589458150087243450e772d2f48ee302060a0f2643320c385f090ed1`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Feb 2024 23:20:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 12 Feb 2024 23:20:08 GMT
EXPOSE 80
# Mon, 12 Feb 2024 23:20:09 GMT
ENTRYPOINT ["/traefik"]
# Mon, 12 Feb 2024 23:20:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8ac948dab7d4d3a44ab44e27a80115467b2f5fba68a58b377fef3e920bc5eb`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e3e182650f59b900de51ded3bfee4017bab649d21de3f8341d68e7f796aee9`  
		Last Modified: Mon, 12 Feb 2024 23:21:25 GMT  
		Size: 42.2 MB (42242650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423e3dfa116da7e393dd48909dd95ea29060058784705fe4f1c9f6604693da09`  
		Last Modified: Mon, 12 Feb 2024 23:21:16 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8afe44f0fa3239edbc49d366a7f03f1d76be21abfddc9db48f31b6348890ae`  
		Last Modified: Mon, 12 Feb 2024 23:21:16 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8f8c0f5fba9a08bf883b01678de16eeff3672d6dad6182f8bef0eb23331a60`  
		Last Modified: Mon, 12 Feb 2024 23:21:16 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8d6492e1e69eb6e597e2cde516711cb939eb3c1129348a26d521f91b2bb224c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull traefik@sha256:1680177046cc5ecb21fde7f8eec02a9b595da8f359c716cd82105e9d4ec205ea
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1942451131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21e0a8f8d21d9a7823d1efde30bf8a1456a52ea4bafa820e321d8cd13fb9c0c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Feb 2024 23:18:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 12 Feb 2024 23:18:25 GMT
EXPOSE 80
# Mon, 12 Feb 2024 23:18:26 GMT
ENTRYPOINT ["/traefik"]
# Mon, 12 Feb 2024 23:18:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddb0a528ee25f289459dfa0d84bac9a14b9127f771882f0b60425ffaab79933`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2b12c1d6e1dcf9104a5f56288334de87014cf49a113618ecb6eaf9f1d105c0`  
		Last Modified: Mon, 12 Feb 2024 23:20:58 GMT  
		Size: 42.2 MB (42232942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599fa3d7f5a1ac976cf218211ca963ce0208743ffbae93fc61e6f85ce7d61897`  
		Last Modified: Mon, 12 Feb 2024 23:20:48 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83394d5b11d0a0cfe86232947a0d42f0263549aaa4e8bae4d3b24659b6a8f0e`  
		Last Modified: Mon, 12 Feb 2024 23:20:47 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9ddee79f9f3d5a6e240d718947993b13695b4b956f8408788174e2e5aebb13`  
		Last Modified: Mon, 12 Feb 2024 23:20:48 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:4be302e188b5be7637a3404033e8088c005059fd29e05b7ff04a403fac3d13ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:v2.11` - linux; amd64

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

### `traefik:v2.11` - linux; arm variant v6

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

### `traefik:v2.11` - linux; arm64 variant v8

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

### `traefik:v2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:a8f1545bdb1bb1a4433ef368846cf6461bcc7ef388c650b86bbc465bb2caf636
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40633824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7443e5aaf5d064276dd06a0496c831fc5268d17ddafca5b65461d882ae9da7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 00:49:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 13 Feb 2024 00:49:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 13 Feb 2024 00:49:43 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 13 Feb 2024 00:49:44 GMT
EXPOSE 80
# Tue, 13 Feb 2024 00:49:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 00:49:44 GMT
CMD ["traefik"]
# Tue, 13 Feb 2024 00:49:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925e55686869481cec5013bfadef6029068b862a623c351094616c335d8c5bcd`  
		Last Modified: Tue, 13 Feb 2024 00:50:00 GMT  
		Size: 623.2 KB (623154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7d1cfe7233426807a8e2f31e0b60c914effe76b40c293fc8d58e1de7f718b5`  
		Last Modified: Tue, 13 Feb 2024 00:50:06 GMT  
		Size: 36.7 MB (36651948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb48c7f4c6e411ddfad004f4158d98523a13d588ec355c926ae14d65bb76c02a`  
		Last Modified: Tue, 13 Feb 2024 00:49:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.11` - linux; s390x

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

## `traefik:v2.11-windowsservercore-1809`

```console
$ docker pull traefik@sha256:f7a50aee3fdde8ae5aded88d0fd58aa317935ca72713ed0242bd7809a52ca570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `traefik:v2.11-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull traefik@sha256:11af0932b812b0e766efaccb987c14ed57124d9a27d21f3f5a8a288c38b2bcb2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2111970705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c58c6f589458150087243450e772d2f48ee302060a0f2643320c385f090ed1`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Feb 2024 23:20:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 12 Feb 2024 23:20:08 GMT
EXPOSE 80
# Mon, 12 Feb 2024 23:20:09 GMT
ENTRYPOINT ["/traefik"]
# Mon, 12 Feb 2024 23:20:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8ac948dab7d4d3a44ab44e27a80115467b2f5fba68a58b377fef3e920bc5eb`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e3e182650f59b900de51ded3bfee4017bab649d21de3f8341d68e7f796aee9`  
		Last Modified: Mon, 12 Feb 2024 23:21:25 GMT  
		Size: 42.2 MB (42242650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423e3dfa116da7e393dd48909dd95ea29060058784705fe4f1c9f6604693da09`  
		Last Modified: Mon, 12 Feb 2024 23:21:16 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8afe44f0fa3239edbc49d366a7f03f1d76be21abfddc9db48f31b6348890ae`  
		Last Modified: Mon, 12 Feb 2024 23:21:16 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8f8c0f5fba9a08bf883b01678de16eeff3672d6dad6182f8bef0eb23331a60`  
		Last Modified: Mon, 12 Feb 2024 23:21:16 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8d6492e1e69eb6e597e2cde516711cb939eb3c1129348a26d521f91b2bb224c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull traefik@sha256:1680177046cc5ecb21fde7f8eec02a9b595da8f359c716cd82105e9d4ec205ea
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1942451131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21e0a8f8d21d9a7823d1efde30bf8a1456a52ea4bafa820e321d8cd13fb9c0c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Feb 2024 23:18:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 12 Feb 2024 23:18:25 GMT
EXPOSE 80
# Mon, 12 Feb 2024 23:18:26 GMT
ENTRYPOINT ["/traefik"]
# Mon, 12 Feb 2024 23:18:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddb0a528ee25f289459dfa0d84bac9a14b9127f771882f0b60425ffaab79933`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2b12c1d6e1dcf9104a5f56288334de87014cf49a113618ecb6eaf9f1d105c0`  
		Last Modified: Mon, 12 Feb 2024 23:20:58 GMT  
		Size: 42.2 MB (42232942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599fa3d7f5a1ac976cf218211ca963ce0208743ffbae93fc61e6f85ce7d61897`  
		Last Modified: Mon, 12 Feb 2024 23:20:48 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83394d5b11d0a0cfe86232947a0d42f0263549aaa4e8bae4d3b24659b6a8f0e`  
		Last Modified: Mon, 12 Feb 2024 23:20:47 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9ddee79f9f3d5a6e240d718947993b13695b4b956f8408788174e2e5aebb13`  
		Last Modified: Mon, 12 Feb 2024 23:20:48 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.0`

```console
$ docker pull traefik@sha256:4be302e188b5be7637a3404033e8088c005059fd29e05b7ff04a403fac3d13ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:v2.11.0` - linux; amd64

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

### `traefik:v2.11.0` - linux; arm variant v6

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

### `traefik:v2.11.0` - linux; arm64 variant v8

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

### `traefik:v2.11.0` - linux; ppc64le

```console
$ docker pull traefik@sha256:a8f1545bdb1bb1a4433ef368846cf6461bcc7ef388c650b86bbc465bb2caf636
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40633824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7443e5aaf5d064276dd06a0496c831fc5268d17ddafca5b65461d882ae9da7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 00:49:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 13 Feb 2024 00:49:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 13 Feb 2024 00:49:43 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 13 Feb 2024 00:49:44 GMT
EXPOSE 80
# Tue, 13 Feb 2024 00:49:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 00:49:44 GMT
CMD ["traefik"]
# Tue, 13 Feb 2024 00:49:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925e55686869481cec5013bfadef6029068b862a623c351094616c335d8c5bcd`  
		Last Modified: Tue, 13 Feb 2024 00:50:00 GMT  
		Size: 623.2 KB (623154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7d1cfe7233426807a8e2f31e0b60c914effe76b40c293fc8d58e1de7f718b5`  
		Last Modified: Tue, 13 Feb 2024 00:50:06 GMT  
		Size: 36.7 MB (36651948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb48c7f4c6e411ddfad004f4158d98523a13d588ec355c926ae14d65bb76c02a`  
		Last Modified: Tue, 13 Feb 2024 00:49:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.11.0` - linux; s390x

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

## `traefik:v2.11.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:f7a50aee3fdde8ae5aded88d0fd58aa317935ca72713ed0242bd7809a52ca570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `traefik:v2.11.0-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull traefik@sha256:11af0932b812b0e766efaccb987c14ed57124d9a27d21f3f5a8a288c38b2bcb2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2111970705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c58c6f589458150087243450e772d2f48ee302060a0f2643320c385f090ed1`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Feb 2024 23:20:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 12 Feb 2024 23:20:08 GMT
EXPOSE 80
# Mon, 12 Feb 2024 23:20:09 GMT
ENTRYPOINT ["/traefik"]
# Mon, 12 Feb 2024 23:20:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8ac948dab7d4d3a44ab44e27a80115467b2f5fba68a58b377fef3e920bc5eb`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e3e182650f59b900de51ded3bfee4017bab649d21de3f8341d68e7f796aee9`  
		Last Modified: Mon, 12 Feb 2024 23:21:25 GMT  
		Size: 42.2 MB (42242650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423e3dfa116da7e393dd48909dd95ea29060058784705fe4f1c9f6604693da09`  
		Last Modified: Mon, 12 Feb 2024 23:21:16 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8afe44f0fa3239edbc49d366a7f03f1d76be21abfddc9db48f31b6348890ae`  
		Last Modified: Mon, 12 Feb 2024 23:21:16 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8f8c0f5fba9a08bf883b01678de16eeff3672d6dad6182f8bef0eb23331a60`  
		Last Modified: Mon, 12 Feb 2024 23:21:16 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.0-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8d6492e1e69eb6e597e2cde516711cb939eb3c1129348a26d521f91b2bb224c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `traefik:v2.11.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull traefik@sha256:1680177046cc5ecb21fde7f8eec02a9b595da8f359c716cd82105e9d4ec205ea
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1942451131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21e0a8f8d21d9a7823d1efde30bf8a1456a52ea4bafa820e321d8cd13fb9c0c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Feb 2024 23:18:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 12 Feb 2024 23:18:25 GMT
EXPOSE 80
# Mon, 12 Feb 2024 23:18:26 GMT
ENTRYPOINT ["/traefik"]
# Mon, 12 Feb 2024 23:18:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddb0a528ee25f289459dfa0d84bac9a14b9127f771882f0b60425ffaab79933`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2b12c1d6e1dcf9104a5f56288334de87014cf49a113618ecb6eaf9f1d105c0`  
		Last Modified: Mon, 12 Feb 2024 23:20:58 GMT  
		Size: 42.2 MB (42232942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599fa3d7f5a1ac976cf218211ca963ce0208743ffbae93fc61e6f85ce7d61897`  
		Last Modified: Mon, 12 Feb 2024 23:20:48 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83394d5b11d0a0cfe86232947a0d42f0263549aaa4e8bae4d3b24659b6a8f0e`  
		Last Modified: Mon, 12 Feb 2024 23:20:47 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9ddee79f9f3d5a6e240d718947993b13695b4b956f8408788174e2e5aebb13`  
		Last Modified: Mon, 12 Feb 2024 23:20:48 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0`

```console
$ docker pull traefik@sha256:81a73de0d19b6d61eb1f1e413d48835fe3c412f5ed3d9750dc3dab5c93519445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v3.0` - linux; amd64

```console
$ docker pull traefik@sha256:961c403e0663bec37efeaf1ead73eba9f2239ec078e8f3b9ab3766792e30b045
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44345773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6dc1a90d15dea9a0e5374c2006dff2618614d657b9e12d7cd3e4d6b84f02f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:55:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 27 Jan 2024 03:55:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 27 Jan 2024 03:55:59 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 27 Jan 2024 03:55:59 GMT
EXPOSE 80
# Sat, 27 Jan 2024 03:55:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:55:59 GMT
CMD ["traefik"]
# Sat, 27 Jan 2024 03:56:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987f790ee1434532d04fff8e0ff09f57d177ab515cdad8c0c3797d839f186a98`  
		Last Modified: Sat, 27 Jan 2024 03:56:31 GMT  
		Size: 622.8 KB (622798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c7ee2ab615563dcd9c77124f242f64520830ea09f7d2959e3e6beac42be540`  
		Last Modified: Sat, 27 Jan 2024 03:56:37 GMT  
		Size: 40.3 MB (40320065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2458ede9a225d84ce3b67646c51d2ed5856d8ccd5cad6699ae799fd8c4f8cd7`  
		Last Modified: Sat, 27 Jan 2024 03:56:31 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; arm variant v6

```console
$ docker pull traefik@sha256:af860a1868760cb06d86ce5fdb2d58de1ff91d170fe4463bdae23284245c80d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41867658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7db22bf0dacfe86ebff59713181fcd74d5d790a40478b5b614f30d9d3b9d95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:30:23 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 27 Jan 2024 09:30:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 27 Jan 2024 09:30:28 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 27 Jan 2024 09:30:29 GMT
EXPOSE 80
# Sat, 27 Jan 2024 09:30:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 09:30:29 GMT
CMD ["traefik"]
# Sat, 27 Jan 2024 09:30:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982de14def5b39cd26b9b8095345186dd246994b7be1bacf68fe810cf91b5c23`  
		Last Modified: Sat, 27 Jan 2024 09:31:00 GMT  
		Size: 623.2 KB (623196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f50cbdd950c3cac5a5ceb8ce0c09db1946dae3ed2a84888fe79e54f600fb464`  
		Last Modified: Sat, 27 Jan 2024 09:31:06 GMT  
		Size: 38.1 MB (38097034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2a36c4a8f6aca2e9235956d4601348e823fad16211b6381642ab8a60be4931`  
		Last Modified: Sat, 27 Jan 2024 09:30:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1a77ba6edfb6d1840bf931fc6606f1ef7f0ae4633eab030ded9b1eead051e28b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41269360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbaf9024ae8bdf537fdbb3faa4c2f6a8da7f499cb143ef32dc248ec47982f879`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:18:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 27 Jan 2024 09:18:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 27 Jan 2024 09:18:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 27 Jan 2024 09:18:10 GMT
EXPOSE 80
# Sat, 27 Jan 2024 09:18:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 09:18:10 GMT
CMD ["traefik"]
# Sat, 27 Jan 2024 09:18:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce888d1547525f7b13a7ebe582acbbf32204c342e18951b58b916087c88b4845`  
		Last Modified: Sat, 27 Jan 2024 09:18:37 GMT  
		Size: 625.1 KB (625057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886c5c7807cd7c4adfa8eec0080bf85774eeeae29bcfe3183f54f14ac52b30e3`  
		Last Modified: Sat, 27 Jan 2024 09:18:41 GMT  
		Size: 37.3 MB (37310574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5889fd36e1d40b740b76199b5027ff5cfbb211ef2f84d6b66ea9033680ea948c`  
		Last Modified: Sat, 27 Jan 2024 09:18:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; s390x

```console
$ docker pull traefik@sha256:f4e3b280fc13dc77f8d2cd719a4aaf5704f8c5e25f6c8d71ba2486bf791e826a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43097120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb2097c50b8e2f7fd81df1941d759374e1bfdb9c9a1f126c1bb2d3d5f0399f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:19:00 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 27 Jan 2024 04:19:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 27 Jan 2024 04:19:08 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 27 Jan 2024 04:19:09 GMT
EXPOSE 80
# Sat, 27 Jan 2024 04:19:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 04:19:09 GMT
CMD ["traefik"]
# Sat, 27 Jan 2024 04:19:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a8e27c29b7fbf4c31ac7c82b3365eca2436fa8dafa39d1b1e168d59122e8fb`  
		Last Modified: Sat, 27 Jan 2024 04:23:16 GMT  
		Size: 623.3 KB (623315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875f71b4d746606d64debc55adac979ebdcefe5a915cfc7e20e4ef8f7b535b9b`  
		Last Modified: Sat, 27 Jan 2024 04:23:22 GMT  
		Size: 39.3 MB (39255907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be081a497ca8dde0d3a277da18c62573fc002048c92f05b85916e95011faff9`  
		Last Modified: Sat, 27 Jan 2024 04:23:16 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7944d1f076a9bf9e011a18195fe94c09182ad20323889522f4be294cf6655fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `traefik:v3.0-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull traefik@sha256:15bf0b1a96f1b47d7f8a3928652132d404b5bed226db4539ec838754f7f9f163
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2111553847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ce7c49f8a45aaf425200aa14d97c486e6634df0366a75b3de886310f596760`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 02:56:46 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Jan 2024 02:56:47 GMT
EXPOSE 80
# Thu, 11 Jan 2024 02:56:48 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Jan 2024 02:56:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8ac948dab7d4d3a44ab44e27a80115467b2f5fba68a58b377fef3e920bc5eb`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49eb407301b5f508eb7606a90cf89bd0a401890f635297ab6e6485757c1f4d27`  
		Last Modified: Thu, 11 Jan 2024 03:02:25 GMT  
		Size: 41.8 MB (41826107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fdc65ad253940c7733bfe5b1c14f88383310d5abc8ce7e814d074828c9f2c6`  
		Last Modified: Thu, 11 Jan 2024 03:02:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20260907bb69491a01d8371b08dbcb108fa09fed8512fc8f80336993ca327fee`  
		Last Modified: Thu, 11 Jan 2024 03:02:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57039062e8bd897795195c64f2f55927819e379db2efa832a09be6f9952e37d`  
		Last Modified: Thu, 11 Jan 2024 03:02:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:0084d4bb9d9b219532a0c7a49fd1438552a0689ae3c72d164e98cf248656d731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `traefik:v3.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull traefik@sha256:4d4b9dfbd3f20864adb35cdfcd62f2ca4e516ec1fa96c31d050ed32c00459241
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1942021057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebbbdfd3595247cbe68a2b6ad81bfafb420be2d9c6a1f160f3983b12062f999`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 02:55:28 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Jan 2024 02:55:29 GMT
EXPOSE 80
# Thu, 11 Jan 2024 02:55:30 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Jan 2024 02:55:31 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddb0a528ee25f289459dfa0d84bac9a14b9127f771882f0b60425ffaab79933`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e15c3c989998bebef01e6f171e9fb5b99f55348a3879ed15b6daabff0aafb3`  
		Last Modified: Thu, 11 Jan 2024 03:02:00 GMT  
		Size: 41.8 MB (41803194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7c5c08c03f3a3058bd365dd03f1ca2060bbdf3565509f2ba85ef99d94048f1`  
		Last Modified: Thu, 11 Jan 2024 03:01:50 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a307677f611cfb82606d5fa26ca3281533fbbc379b98c4097015b614ab2d7d`  
		Last Modified: Thu, 11 Jan 2024 03:01:50 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fad3662942fc37b68b55707e5f6535567f16dd002fc3a19f491db73b04e7c3b`  
		Last Modified: Thu, 11 Jan 2024 03:01:50 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-beta5`

```console
$ docker pull traefik@sha256:81a73de0d19b6d61eb1f1e413d48835fe3c412f5ed3d9750dc3dab5c93519445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v3.0.0-beta5` - linux; amd64

```console
$ docker pull traefik@sha256:961c403e0663bec37efeaf1ead73eba9f2239ec078e8f3b9ab3766792e30b045
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44345773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6dc1a90d15dea9a0e5374c2006dff2618614d657b9e12d7cd3e4d6b84f02f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:55:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 27 Jan 2024 03:55:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 27 Jan 2024 03:55:59 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 27 Jan 2024 03:55:59 GMT
EXPOSE 80
# Sat, 27 Jan 2024 03:55:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:55:59 GMT
CMD ["traefik"]
# Sat, 27 Jan 2024 03:56:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987f790ee1434532d04fff8e0ff09f57d177ab515cdad8c0c3797d839f186a98`  
		Last Modified: Sat, 27 Jan 2024 03:56:31 GMT  
		Size: 622.8 KB (622798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c7ee2ab615563dcd9c77124f242f64520830ea09f7d2959e3e6beac42be540`  
		Last Modified: Sat, 27 Jan 2024 03:56:37 GMT  
		Size: 40.3 MB (40320065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2458ede9a225d84ce3b67646c51d2ed5856d8ccd5cad6699ae799fd8c4f8cd7`  
		Last Modified: Sat, 27 Jan 2024 03:56:31 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-beta5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:af860a1868760cb06d86ce5fdb2d58de1ff91d170fe4463bdae23284245c80d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41867658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7db22bf0dacfe86ebff59713181fcd74d5d790a40478b5b614f30d9d3b9d95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:30:23 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 27 Jan 2024 09:30:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 27 Jan 2024 09:30:28 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 27 Jan 2024 09:30:29 GMT
EXPOSE 80
# Sat, 27 Jan 2024 09:30:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 09:30:29 GMT
CMD ["traefik"]
# Sat, 27 Jan 2024 09:30:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982de14def5b39cd26b9b8095345186dd246994b7be1bacf68fe810cf91b5c23`  
		Last Modified: Sat, 27 Jan 2024 09:31:00 GMT  
		Size: 623.2 KB (623196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f50cbdd950c3cac5a5ceb8ce0c09db1946dae3ed2a84888fe79e54f600fb464`  
		Last Modified: Sat, 27 Jan 2024 09:31:06 GMT  
		Size: 38.1 MB (38097034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2a36c4a8f6aca2e9235956d4601348e823fad16211b6381642ab8a60be4931`  
		Last Modified: Sat, 27 Jan 2024 09:30:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-beta5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1a77ba6edfb6d1840bf931fc6606f1ef7f0ae4633eab030ded9b1eead051e28b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41269360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbaf9024ae8bdf537fdbb3faa4c2f6a8da7f499cb143ef32dc248ec47982f879`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:18:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 27 Jan 2024 09:18:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 27 Jan 2024 09:18:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 27 Jan 2024 09:18:10 GMT
EXPOSE 80
# Sat, 27 Jan 2024 09:18:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 09:18:10 GMT
CMD ["traefik"]
# Sat, 27 Jan 2024 09:18:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce888d1547525f7b13a7ebe582acbbf32204c342e18951b58b916087c88b4845`  
		Last Modified: Sat, 27 Jan 2024 09:18:37 GMT  
		Size: 625.1 KB (625057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886c5c7807cd7c4adfa8eec0080bf85774eeeae29bcfe3183f54f14ac52b30e3`  
		Last Modified: Sat, 27 Jan 2024 09:18:41 GMT  
		Size: 37.3 MB (37310574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5889fd36e1d40b740b76199b5027ff5cfbb211ef2f84d6b66ea9033680ea948c`  
		Last Modified: Sat, 27 Jan 2024 09:18:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-beta5` - linux; s390x

```console
$ docker pull traefik@sha256:f4e3b280fc13dc77f8d2cd719a4aaf5704f8c5e25f6c8d71ba2486bf791e826a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43097120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb2097c50b8e2f7fd81df1941d759374e1bfdb9c9a1f126c1bb2d3d5f0399f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:19:00 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 27 Jan 2024 04:19:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 27 Jan 2024 04:19:08 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 27 Jan 2024 04:19:09 GMT
EXPOSE 80
# Sat, 27 Jan 2024 04:19:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 04:19:09 GMT
CMD ["traefik"]
# Sat, 27 Jan 2024 04:19:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a8e27c29b7fbf4c31ac7c82b3365eca2436fa8dafa39d1b1e168d59122e8fb`  
		Last Modified: Sat, 27 Jan 2024 04:23:16 GMT  
		Size: 623.3 KB (623315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875f71b4d746606d64debc55adac979ebdcefe5a915cfc7e20e4ef8f7b535b9b`  
		Last Modified: Sat, 27 Jan 2024 04:23:22 GMT  
		Size: 39.3 MB (39255907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be081a497ca8dde0d3a277da18c62573fc002048c92f05b85916e95011faff9`  
		Last Modified: Sat, 27 Jan 2024 04:23:16 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-beta5-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7944d1f076a9bf9e011a18195fe94c09182ad20323889522f4be294cf6655fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `traefik:v3.0.0-beta5-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull traefik@sha256:15bf0b1a96f1b47d7f8a3928652132d404b5bed226db4539ec838754f7f9f163
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2111553847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ce7c49f8a45aaf425200aa14d97c486e6634df0366a75b3de886310f596760`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 02:56:46 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Jan 2024 02:56:47 GMT
EXPOSE 80
# Thu, 11 Jan 2024 02:56:48 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Jan 2024 02:56:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8ac948dab7d4d3a44ab44e27a80115467b2f5fba68a58b377fef3e920bc5eb`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49eb407301b5f508eb7606a90cf89bd0a401890f635297ab6e6485757c1f4d27`  
		Last Modified: Thu, 11 Jan 2024 03:02:25 GMT  
		Size: 41.8 MB (41826107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fdc65ad253940c7733bfe5b1c14f88383310d5abc8ce7e814d074828c9f2c6`  
		Last Modified: Thu, 11 Jan 2024 03:02:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20260907bb69491a01d8371b08dbcb108fa09fed8512fc8f80336993ca327fee`  
		Last Modified: Thu, 11 Jan 2024 03:02:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57039062e8bd897795195c64f2f55927819e379db2efa832a09be6f9952e37d`  
		Last Modified: Thu, 11 Jan 2024 03:02:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-beta5-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:0084d4bb9d9b219532a0c7a49fd1438552a0689ae3c72d164e98cf248656d731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `traefik:v3.0.0-beta5-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull traefik@sha256:4d4b9dfbd3f20864adb35cdfcd62f2ca4e516ec1fa96c31d050ed32c00459241
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1942021057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebbbdfd3595247cbe68a2b6ad81bfafb420be2d9c6a1f160f3983b12062f999`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 02:55:28 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Jan 2024 02:55:29 GMT
EXPOSE 80
# Thu, 11 Jan 2024 02:55:30 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Jan 2024 02:55:31 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddb0a528ee25f289459dfa0d84bac9a14b9127f771882f0b60425ffaab79933`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e15c3c989998bebef01e6f171e9fb5b99f55348a3879ed15b6daabff0aafb3`  
		Last Modified: Thu, 11 Jan 2024 03:02:00 GMT  
		Size: 41.8 MB (41803194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7c5c08c03f3a3058bd365dd03f1ca2060bbdf3565509f2ba85ef99d94048f1`  
		Last Modified: Thu, 11 Jan 2024 03:01:50 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a307677f611cfb82606d5fa26ca3281533fbbc379b98c4097015b614ab2d7d`  
		Last Modified: Thu, 11 Jan 2024 03:01:50 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fad3662942fc37b68b55707e5f6535567f16dd002fc3a19f491db73b04e7c3b`  
		Last Modified: Thu, 11 Jan 2024 03:01:50 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:f7a50aee3fdde8ae5aded88d0fd58aa317935ca72713ed0242bd7809a52ca570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull traefik@sha256:11af0932b812b0e766efaccb987c14ed57124d9a27d21f3f5a8a288c38b2bcb2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2111970705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c58c6f589458150087243450e772d2f48ee302060a0f2643320c385f090ed1`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Feb 2024 23:20:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 12 Feb 2024 23:20:08 GMT
EXPOSE 80
# Mon, 12 Feb 2024 23:20:09 GMT
ENTRYPOINT ["/traefik"]
# Mon, 12 Feb 2024 23:20:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8ac948dab7d4d3a44ab44e27a80115467b2f5fba68a58b377fef3e920bc5eb`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e3e182650f59b900de51ded3bfee4017bab649d21de3f8341d68e7f796aee9`  
		Last Modified: Mon, 12 Feb 2024 23:21:25 GMT  
		Size: 42.2 MB (42242650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423e3dfa116da7e393dd48909dd95ea29060058784705fe4f1c9f6604693da09`  
		Last Modified: Mon, 12 Feb 2024 23:21:16 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8afe44f0fa3239edbc49d366a7f03f1d76be21abfddc9db48f31b6348890ae`  
		Last Modified: Mon, 12 Feb 2024 23:21:16 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8f8c0f5fba9a08bf883b01678de16eeff3672d6dad6182f8bef0eb23331a60`  
		Last Modified: Mon, 12 Feb 2024 23:21:16 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8d6492e1e69eb6e597e2cde516711cb939eb3c1129348a26d521f91b2bb224c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull traefik@sha256:1680177046cc5ecb21fde7f8eec02a9b595da8f359c716cd82105e9d4ec205ea
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1942451131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21e0a8f8d21d9a7823d1efde30bf8a1456a52ea4bafa820e321d8cd13fb9c0c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Feb 2024 23:18:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 12 Feb 2024 23:18:25 GMT
EXPOSE 80
# Mon, 12 Feb 2024 23:18:26 GMT
ENTRYPOINT ["/traefik"]
# Mon, 12 Feb 2024 23:18:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddb0a528ee25f289459dfa0d84bac9a14b9127f771882f0b60425ffaab79933`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2b12c1d6e1dcf9104a5f56288334de87014cf49a113618ecb6eaf9f1d105c0`  
		Last Modified: Mon, 12 Feb 2024 23:20:58 GMT  
		Size: 42.2 MB (42232942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599fa3d7f5a1ac976cf218211ca963ce0208743ffbae93fc61e6f85ce7d61897`  
		Last Modified: Mon, 12 Feb 2024 23:20:48 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83394d5b11d0a0cfe86232947a0d42f0263549aaa4e8bae4d3b24659b6a8f0e`  
		Last Modified: Mon, 12 Feb 2024 23:20:47 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9ddee79f9f3d5a6e240d718947993b13695b4b956f8408788174e2e5aebb13`  
		Last Modified: Mon, 12 Feb 2024 23:20:48 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
