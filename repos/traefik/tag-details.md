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
-	[`traefik:3.0.0-rc1`](#traefik300-rc1)
-	[`traefik:3.0.0-rc1-windowsservercore-1809`](#traefik300-rc1-windowsservercore-1809)
-	[`traefik:3.0.0-rc1-windowsservercore-ltsc2022`](#traefik300-rc1-windowsservercore-ltsc2022)
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
-	[`traefik:v3.0.0-rc1`](#traefikv300-rc1)
-	[`traefik:v3.0.0-rc1-windowsservercore-1809`](#traefikv300-rc1-windowsservercore-1809)
-	[`traefik:v3.0.0-rc1-windowsservercore-ltsc2022`](#traefikv300-rc1-windowsservercore-ltsc2022)
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
$ docker pull traefik@sha256:0168e405ccaaf0876cef130f9e0bf6660bb4a4b541126903e67dddd50e1ed424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:3.0` - linux; amd64

```console
$ docker pull traefik@sha256:a4291860384ab14cf6b14fec90442ea413b0d73e08a1a90ae072d5f87b0a5c5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45215806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7500ba9e0cd2b3b583d5b187cf56519f2978a62e966aef6175617fafed7dd4cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:56:04 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 14 Feb 2024 01:51:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 14 Feb 2024 01:51:21 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 14 Feb 2024 01:51:21 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:51:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 01:51:21 GMT
CMD ["traefik"]
# Wed, 14 Feb 2024 01:51:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:31bd04195f40000b0e1ed3c2ef3a8a0d2f53fd88c276d95cb0b76930303cfb94`  
		Last Modified: Wed, 14 Feb 2024 01:51:42 GMT  
		Size: 41.2 MB (41184549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a5a9477b9d74a0c0333da7227d4a9ab61a40d0120099c5a37dbf91d92bd171`  
		Last Modified: Wed, 14 Feb 2024 01:51:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4faead017690c14f301136a1a98eb1879cf07ad0acc84f86864fd9aa5001eb8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42442406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c237b08566cd841ed92601fb3e908a68e7d6dda1c4aa0f6bd7bf9ddef31773`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:30:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 14 Feb 2024 01:13:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 14 Feb 2024 01:13:52 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 14 Feb 2024 01:13:52 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:13:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 01:13:52 GMT
CMD ["traefik"]
# Wed, 14 Feb 2024 01:13:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:fe3fe7868c1ea143b7df56b2d6b3c6847ddaee96e1fa37bc18a87b3ad36a6c23`  
		Last Modified: Wed, 14 Feb 2024 01:14:11 GMT  
		Size: 38.7 MB (38653255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb42156df07563bc9b31e938379682e1d4b35f6f304406147d149f09391c10d`  
		Last Modified: Wed, 14 Feb 2024 01:14:04 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1c00a020261fd642273c185f9b48745bb1d5003fb2e8bd879907ae273108dbdd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42106293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28adc4dbdab7502b67b1129aa3912439c53aff1ef74573aa4563e8b05c14af81`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:18:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 14 Feb 2024 01:59:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 14 Feb 2024 01:59:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 14 Feb 2024 01:59:22 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:59:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 01:59:22 GMT
CMD ["traefik"]
# Wed, 14 Feb 2024 01:59:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:54440866de0ca0fe3e9e6e7b42590b5411b695f21c4bae155e83410aa5e0b328`  
		Last Modified: Wed, 14 Feb 2024 01:59:40 GMT  
		Size: 38.1 MB (38133003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82aa8f90d259db174923a28ed575665689ba2118c036dfca50bb75b6e1ee988`  
		Last Modified: Wed, 14 Feb 2024 01:59:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; ppc64le

```console
$ docker pull traefik@sha256:7f4dcfc08cd60809966904f0654bfbb685289dc4e47878704f998eb3196b2d97
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40975702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bca94a6548e319d4e308b938921db72ce70d9be20ecee233fa8c3e72cdef3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 00:49:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 14 Feb 2024 01:47:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 14 Feb 2024 01:47:21 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 14 Feb 2024 01:47:22 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:47:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 01:47:24 GMT
CMD ["traefik"]
# Wed, 14 Feb 2024 01:47:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d181bcd9b7ac9d9a7e1e9e6d1c90dd28e0a0f79c68f6078fc500c9a82cc75ac7`  
		Last Modified: Wed, 14 Feb 2024 01:47:51 GMT  
		Size: 37.0 MB (36993826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9716cdbe5ee808f56bce71d706e73d2f4b5526f0a1eea822512b67b2d80a310d`  
		Last Modified: Wed, 14 Feb 2024 01:47:44 GMT  
		Size: 369.0 B  
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
$ docker pull traefik@sha256:66c97ca8fbe5df3c1c0ff6f86bfeec315cbce13effb3ffb8a342e19770cf1826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `traefik:3.0-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull traefik@sha256:b7fc0fdb48d8386ebbe64b9aa205b3806dad93e57a01140a3dd36cfbdca8f832
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2112612791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d5d74e8d49f01a9fd3ee0e8ca207d7736f60a44489ad4ca9efa4a9ee9c7c64`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 01:20:35 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Feb 2024 01:20:36 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:20:37 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Feb 2024 01:20:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:83c985906a307cada02318f1c538b20c702179767bbeb044701f813377b10dea`  
		Last Modified: Wed, 14 Feb 2024 01:22:12 GMT  
		Size: 42.9 MB (42885051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8cc81e75ce72775f5da96e56be1d87f290d904b358ac5ccec00265737d852b`  
		Last Modified: Wed, 14 Feb 2024 01:22:03 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59c39f841dc2a443c02f59ac09c498549c0e61a8f1fb7e1121c7b8f3e753753`  
		Last Modified: Wed, 14 Feb 2024 01:22:03 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d7a270868debd500b8f950e8f2aae55decfd34892fa24b1f5f467dd0e0c485`  
		Last Modified: Wed, 14 Feb 2024 01:22:03 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:f4b0afc615e1ea31719fc20ebc026949317a18b6e34a6e84a0280d596cb38e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `traefik:3.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull traefik@sha256:111fb73808e396a9cc4145690ba8c6bd4ce023946231a8dd1e3e31207de3911d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1943081560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7653e2b60df3ff29290d8eae94b6ceb9a2c50dce37d59ea9c3e71760fbbee30`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 01:19:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Feb 2024 01:19:06 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:19:07 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Feb 2024 01:19:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:ca669fce90e34d80675163908e4c7e7c16e0656a28a5c116b816350295d7ce3b`  
		Last Modified: Wed, 14 Feb 2024 01:21:46 GMT  
		Size: 42.9 MB (42863713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47abd1be3950e078ebf68e63bf3a919a8bcd7bf268416007c513c47a71468c1e`  
		Last Modified: Wed, 14 Feb 2024 01:21:18 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6fcb75827b10780bc35d70b5573f25b66d2703d2777a120def7586adba8ac4`  
		Last Modified: Wed, 14 Feb 2024 01:21:18 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9369421163315ef00dd703434b101bb4c5d8dfb41f99c756d6952ba07dec8102`  
		Last Modified: Wed, 14 Feb 2024 01:21:18 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-rc1`

```console
$ docker pull traefik@sha256:f87f46635d62db3be770a288d9ced2755e37b49b4c142823cd29f16637378794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `traefik:3.0.0-rc1` - linux; amd64

```console
$ docker pull traefik@sha256:a4291860384ab14cf6b14fec90442ea413b0d73e08a1a90ae072d5f87b0a5c5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45215806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7500ba9e0cd2b3b583d5b187cf56519f2978a62e966aef6175617fafed7dd4cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:56:04 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 14 Feb 2024 01:51:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 14 Feb 2024 01:51:21 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 14 Feb 2024 01:51:21 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:51:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 01:51:21 GMT
CMD ["traefik"]
# Wed, 14 Feb 2024 01:51:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:31bd04195f40000b0e1ed3c2ef3a8a0d2f53fd88c276d95cb0b76930303cfb94`  
		Last Modified: Wed, 14 Feb 2024 01:51:42 GMT  
		Size: 41.2 MB (41184549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a5a9477b9d74a0c0333da7227d4a9ab61a40d0120099c5a37dbf91d92bd171`  
		Last Modified: Wed, 14 Feb 2024 01:51:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-rc1` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4faead017690c14f301136a1a98eb1879cf07ad0acc84f86864fd9aa5001eb8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42442406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c237b08566cd841ed92601fb3e908a68e7d6dda1c4aa0f6bd7bf9ddef31773`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:30:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 14 Feb 2024 01:13:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 14 Feb 2024 01:13:52 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 14 Feb 2024 01:13:52 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:13:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 01:13:52 GMT
CMD ["traefik"]
# Wed, 14 Feb 2024 01:13:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:fe3fe7868c1ea143b7df56b2d6b3c6847ddaee96e1fa37bc18a87b3ad36a6c23`  
		Last Modified: Wed, 14 Feb 2024 01:14:11 GMT  
		Size: 38.7 MB (38653255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb42156df07563bc9b31e938379682e1d4b35f6f304406147d149f09391c10d`  
		Last Modified: Wed, 14 Feb 2024 01:14:04 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-rc1` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1c00a020261fd642273c185f9b48745bb1d5003fb2e8bd879907ae273108dbdd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42106293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28adc4dbdab7502b67b1129aa3912439c53aff1ef74573aa4563e8b05c14af81`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:18:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 14 Feb 2024 01:59:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 14 Feb 2024 01:59:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 14 Feb 2024 01:59:22 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:59:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 01:59:22 GMT
CMD ["traefik"]
# Wed, 14 Feb 2024 01:59:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:54440866de0ca0fe3e9e6e7b42590b5411b695f21c4bae155e83410aa5e0b328`  
		Last Modified: Wed, 14 Feb 2024 01:59:40 GMT  
		Size: 38.1 MB (38133003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82aa8f90d259db174923a28ed575665689ba2118c036dfca50bb75b6e1ee988`  
		Last Modified: Wed, 14 Feb 2024 01:59:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-rc1` - linux; ppc64le

```console
$ docker pull traefik@sha256:7f4dcfc08cd60809966904f0654bfbb685289dc4e47878704f998eb3196b2d97
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40975702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bca94a6548e319d4e308b938921db72ce70d9be20ecee233fa8c3e72cdef3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 00:49:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 14 Feb 2024 01:47:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 14 Feb 2024 01:47:21 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 14 Feb 2024 01:47:22 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:47:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 01:47:24 GMT
CMD ["traefik"]
# Wed, 14 Feb 2024 01:47:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d181bcd9b7ac9d9a7e1e9e6d1c90dd28e0a0f79c68f6078fc500c9a82cc75ac7`  
		Last Modified: Wed, 14 Feb 2024 01:47:51 GMT  
		Size: 37.0 MB (36993826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9716cdbe5ee808f56bce71d706e73d2f4b5526f0a1eea822512b67b2d80a310d`  
		Last Modified: Wed, 14 Feb 2024 01:47:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-rc1-windowsservercore-1809`

```console
$ docker pull traefik@sha256:66c97ca8fbe5df3c1c0ff6f86bfeec315cbce13effb3ffb8a342e19770cf1826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `traefik:3.0.0-rc1-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull traefik@sha256:b7fc0fdb48d8386ebbe64b9aa205b3806dad93e57a01140a3dd36cfbdca8f832
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2112612791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d5d74e8d49f01a9fd3ee0e8ca207d7736f60a44489ad4ca9efa4a9ee9c7c64`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 01:20:35 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Feb 2024 01:20:36 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:20:37 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Feb 2024 01:20:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:83c985906a307cada02318f1c538b20c702179767bbeb044701f813377b10dea`  
		Last Modified: Wed, 14 Feb 2024 01:22:12 GMT  
		Size: 42.9 MB (42885051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8cc81e75ce72775f5da96e56be1d87f290d904b358ac5ccec00265737d852b`  
		Last Modified: Wed, 14 Feb 2024 01:22:03 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59c39f841dc2a443c02f59ac09c498549c0e61a8f1fb7e1121c7b8f3e753753`  
		Last Modified: Wed, 14 Feb 2024 01:22:03 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d7a270868debd500b8f950e8f2aae55decfd34892fa24b1f5f467dd0e0c485`  
		Last Modified: Wed, 14 Feb 2024 01:22:03 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-rc1-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:f4b0afc615e1ea31719fc20ebc026949317a18b6e34a6e84a0280d596cb38e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `traefik:3.0.0-rc1-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull traefik@sha256:111fb73808e396a9cc4145690ba8c6bd4ce023946231a8dd1e3e31207de3911d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1943081560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7653e2b60df3ff29290d8eae94b6ceb9a2c50dce37d59ea9c3e71760fbbee30`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 01:19:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Feb 2024 01:19:06 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:19:07 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Feb 2024 01:19:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:ca669fce90e34d80675163908e4c7e7c16e0656a28a5c116b816350295d7ce3b`  
		Last Modified: Wed, 14 Feb 2024 01:21:46 GMT  
		Size: 42.9 MB (42863713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47abd1be3950e078ebf68e63bf3a919a8bcd7bf268416007c513c47a71468c1e`  
		Last Modified: Wed, 14 Feb 2024 01:21:18 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6fcb75827b10780bc35d70b5573f25b66d2703d2777a120def7586adba8ac4`  
		Last Modified: Wed, 14 Feb 2024 01:21:18 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9369421163315ef00dd703434b101bb4c5d8dfb41f99c756d6952ba07dec8102`  
		Last Modified: Wed, 14 Feb 2024 01:21:18 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort`

```console
$ docker pull traefik@sha256:0168e405ccaaf0876cef130f9e0bf6660bb4a4b541126903e67dddd50e1ed424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:beaufort` - linux; amd64

```console
$ docker pull traefik@sha256:a4291860384ab14cf6b14fec90442ea413b0d73e08a1a90ae072d5f87b0a5c5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45215806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7500ba9e0cd2b3b583d5b187cf56519f2978a62e966aef6175617fafed7dd4cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:56:04 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 14 Feb 2024 01:51:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 14 Feb 2024 01:51:21 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 14 Feb 2024 01:51:21 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:51:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 01:51:21 GMT
CMD ["traefik"]
# Wed, 14 Feb 2024 01:51:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:31bd04195f40000b0e1ed3c2ef3a8a0d2f53fd88c276d95cb0b76930303cfb94`  
		Last Modified: Wed, 14 Feb 2024 01:51:42 GMT  
		Size: 41.2 MB (41184549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a5a9477b9d74a0c0333da7227d4a9ab61a40d0120099c5a37dbf91d92bd171`  
		Last Modified: Wed, 14 Feb 2024 01:51:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4faead017690c14f301136a1a98eb1879cf07ad0acc84f86864fd9aa5001eb8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42442406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c237b08566cd841ed92601fb3e908a68e7d6dda1c4aa0f6bd7bf9ddef31773`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:30:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 14 Feb 2024 01:13:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 14 Feb 2024 01:13:52 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 14 Feb 2024 01:13:52 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:13:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 01:13:52 GMT
CMD ["traefik"]
# Wed, 14 Feb 2024 01:13:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:fe3fe7868c1ea143b7df56b2d6b3c6847ddaee96e1fa37bc18a87b3ad36a6c23`  
		Last Modified: Wed, 14 Feb 2024 01:14:11 GMT  
		Size: 38.7 MB (38653255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb42156df07563bc9b31e938379682e1d4b35f6f304406147d149f09391c10d`  
		Last Modified: Wed, 14 Feb 2024 01:14:04 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1c00a020261fd642273c185f9b48745bb1d5003fb2e8bd879907ae273108dbdd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42106293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28adc4dbdab7502b67b1129aa3912439c53aff1ef74573aa4563e8b05c14af81`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:18:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 14 Feb 2024 01:59:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 14 Feb 2024 01:59:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 14 Feb 2024 01:59:22 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:59:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 01:59:22 GMT
CMD ["traefik"]
# Wed, 14 Feb 2024 01:59:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:54440866de0ca0fe3e9e6e7b42590b5411b695f21c4bae155e83410aa5e0b328`  
		Last Modified: Wed, 14 Feb 2024 01:59:40 GMT  
		Size: 38.1 MB (38133003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82aa8f90d259db174923a28ed575665689ba2118c036dfca50bb75b6e1ee988`  
		Last Modified: Wed, 14 Feb 2024 01:59:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; ppc64le

```console
$ docker pull traefik@sha256:7f4dcfc08cd60809966904f0654bfbb685289dc4e47878704f998eb3196b2d97
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40975702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bca94a6548e319d4e308b938921db72ce70d9be20ecee233fa8c3e72cdef3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 00:49:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 14 Feb 2024 01:47:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 14 Feb 2024 01:47:21 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 14 Feb 2024 01:47:22 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:47:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 01:47:24 GMT
CMD ["traefik"]
# Wed, 14 Feb 2024 01:47:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d181bcd9b7ac9d9a7e1e9e6d1c90dd28e0a0f79c68f6078fc500c9a82cc75ac7`  
		Last Modified: Wed, 14 Feb 2024 01:47:51 GMT  
		Size: 37.0 MB (36993826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9716cdbe5ee808f56bce71d706e73d2f4b5526f0a1eea822512b67b2d80a310d`  
		Last Modified: Wed, 14 Feb 2024 01:47:44 GMT  
		Size: 369.0 B  
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
$ docker pull traefik@sha256:66c97ca8fbe5df3c1c0ff6f86bfeec315cbce13effb3ffb8a342e19770cf1826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `traefik:beaufort-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull traefik@sha256:b7fc0fdb48d8386ebbe64b9aa205b3806dad93e57a01140a3dd36cfbdca8f832
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2112612791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d5d74e8d49f01a9fd3ee0e8ca207d7736f60a44489ad4ca9efa4a9ee9c7c64`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 01:20:35 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Feb 2024 01:20:36 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:20:37 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Feb 2024 01:20:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:83c985906a307cada02318f1c538b20c702179767bbeb044701f813377b10dea`  
		Last Modified: Wed, 14 Feb 2024 01:22:12 GMT  
		Size: 42.9 MB (42885051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8cc81e75ce72775f5da96e56be1d87f290d904b358ac5ccec00265737d852b`  
		Last Modified: Wed, 14 Feb 2024 01:22:03 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59c39f841dc2a443c02f59ac09c498549c0e61a8f1fb7e1121c7b8f3e753753`  
		Last Modified: Wed, 14 Feb 2024 01:22:03 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d7a270868debd500b8f950e8f2aae55decfd34892fa24b1f5f467dd0e0c485`  
		Last Modified: Wed, 14 Feb 2024 01:22:03 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:f4b0afc615e1ea31719fc20ebc026949317a18b6e34a6e84a0280d596cb38e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `traefik:beaufort-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull traefik@sha256:111fb73808e396a9cc4145690ba8c6bd4ce023946231a8dd1e3e31207de3911d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1943081560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7653e2b60df3ff29290d8eae94b6ceb9a2c50dce37d59ea9c3e71760fbbee30`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 01:19:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Feb 2024 01:19:06 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:19:07 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Feb 2024 01:19:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:ca669fce90e34d80675163908e4c7e7c16e0656a28a5c116b816350295d7ce3b`  
		Last Modified: Wed, 14 Feb 2024 01:21:46 GMT  
		Size: 42.9 MB (42863713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47abd1be3950e078ebf68e63bf3a919a8bcd7bf268416007c513c47a71468c1e`  
		Last Modified: Wed, 14 Feb 2024 01:21:18 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6fcb75827b10780bc35d70b5573f25b66d2703d2777a120def7586adba8ac4`  
		Last Modified: Wed, 14 Feb 2024 01:21:18 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9369421163315ef00dd703434b101bb4c5d8dfb41f99c756d6952ba07dec8102`  
		Last Modified: Wed, 14 Feb 2024 01:21:18 GMT  
		Size: 1.3 KB (1282 bytes)  
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
$ docker pull traefik@sha256:0168e405ccaaf0876cef130f9e0bf6660bb4a4b541126903e67dddd50e1ed424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:v3.0` - linux; amd64

```console
$ docker pull traefik@sha256:a4291860384ab14cf6b14fec90442ea413b0d73e08a1a90ae072d5f87b0a5c5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45215806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7500ba9e0cd2b3b583d5b187cf56519f2978a62e966aef6175617fafed7dd4cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:56:04 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 14 Feb 2024 01:51:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 14 Feb 2024 01:51:21 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 14 Feb 2024 01:51:21 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:51:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 01:51:21 GMT
CMD ["traefik"]
# Wed, 14 Feb 2024 01:51:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:31bd04195f40000b0e1ed3c2ef3a8a0d2f53fd88c276d95cb0b76930303cfb94`  
		Last Modified: Wed, 14 Feb 2024 01:51:42 GMT  
		Size: 41.2 MB (41184549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a5a9477b9d74a0c0333da7227d4a9ab61a40d0120099c5a37dbf91d92bd171`  
		Last Modified: Wed, 14 Feb 2024 01:51:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4faead017690c14f301136a1a98eb1879cf07ad0acc84f86864fd9aa5001eb8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42442406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c237b08566cd841ed92601fb3e908a68e7d6dda1c4aa0f6bd7bf9ddef31773`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:30:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 14 Feb 2024 01:13:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 14 Feb 2024 01:13:52 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 14 Feb 2024 01:13:52 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:13:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 01:13:52 GMT
CMD ["traefik"]
# Wed, 14 Feb 2024 01:13:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:fe3fe7868c1ea143b7df56b2d6b3c6847ddaee96e1fa37bc18a87b3ad36a6c23`  
		Last Modified: Wed, 14 Feb 2024 01:14:11 GMT  
		Size: 38.7 MB (38653255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb42156df07563bc9b31e938379682e1d4b35f6f304406147d149f09391c10d`  
		Last Modified: Wed, 14 Feb 2024 01:14:04 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1c00a020261fd642273c185f9b48745bb1d5003fb2e8bd879907ae273108dbdd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42106293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28adc4dbdab7502b67b1129aa3912439c53aff1ef74573aa4563e8b05c14af81`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:18:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 14 Feb 2024 01:59:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 14 Feb 2024 01:59:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 14 Feb 2024 01:59:22 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:59:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 01:59:22 GMT
CMD ["traefik"]
# Wed, 14 Feb 2024 01:59:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:54440866de0ca0fe3e9e6e7b42590b5411b695f21c4bae155e83410aa5e0b328`  
		Last Modified: Wed, 14 Feb 2024 01:59:40 GMT  
		Size: 38.1 MB (38133003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82aa8f90d259db174923a28ed575665689ba2118c036dfca50bb75b6e1ee988`  
		Last Modified: Wed, 14 Feb 2024 01:59:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; ppc64le

```console
$ docker pull traefik@sha256:7f4dcfc08cd60809966904f0654bfbb685289dc4e47878704f998eb3196b2d97
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40975702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bca94a6548e319d4e308b938921db72ce70d9be20ecee233fa8c3e72cdef3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 00:49:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 14 Feb 2024 01:47:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 14 Feb 2024 01:47:21 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 14 Feb 2024 01:47:22 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:47:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 01:47:24 GMT
CMD ["traefik"]
# Wed, 14 Feb 2024 01:47:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d181bcd9b7ac9d9a7e1e9e6d1c90dd28e0a0f79c68f6078fc500c9a82cc75ac7`  
		Last Modified: Wed, 14 Feb 2024 01:47:51 GMT  
		Size: 37.0 MB (36993826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9716cdbe5ee808f56bce71d706e73d2f4b5526f0a1eea822512b67b2d80a310d`  
		Last Modified: Wed, 14 Feb 2024 01:47:44 GMT  
		Size: 369.0 B  
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
$ docker pull traefik@sha256:66c97ca8fbe5df3c1c0ff6f86bfeec315cbce13effb3ffb8a342e19770cf1826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `traefik:v3.0-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull traefik@sha256:b7fc0fdb48d8386ebbe64b9aa205b3806dad93e57a01140a3dd36cfbdca8f832
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2112612791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d5d74e8d49f01a9fd3ee0e8ca207d7736f60a44489ad4ca9efa4a9ee9c7c64`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 01:20:35 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Feb 2024 01:20:36 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:20:37 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Feb 2024 01:20:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:83c985906a307cada02318f1c538b20c702179767bbeb044701f813377b10dea`  
		Last Modified: Wed, 14 Feb 2024 01:22:12 GMT  
		Size: 42.9 MB (42885051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8cc81e75ce72775f5da96e56be1d87f290d904b358ac5ccec00265737d852b`  
		Last Modified: Wed, 14 Feb 2024 01:22:03 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59c39f841dc2a443c02f59ac09c498549c0e61a8f1fb7e1121c7b8f3e753753`  
		Last Modified: Wed, 14 Feb 2024 01:22:03 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d7a270868debd500b8f950e8f2aae55decfd34892fa24b1f5f467dd0e0c485`  
		Last Modified: Wed, 14 Feb 2024 01:22:03 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:f4b0afc615e1ea31719fc20ebc026949317a18b6e34a6e84a0280d596cb38e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `traefik:v3.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull traefik@sha256:111fb73808e396a9cc4145690ba8c6bd4ce023946231a8dd1e3e31207de3911d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1943081560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7653e2b60df3ff29290d8eae94b6ceb9a2c50dce37d59ea9c3e71760fbbee30`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 01:19:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Feb 2024 01:19:06 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:19:07 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Feb 2024 01:19:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:ca669fce90e34d80675163908e4c7e7c16e0656a28a5c116b816350295d7ce3b`  
		Last Modified: Wed, 14 Feb 2024 01:21:46 GMT  
		Size: 42.9 MB (42863713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47abd1be3950e078ebf68e63bf3a919a8bcd7bf268416007c513c47a71468c1e`  
		Last Modified: Wed, 14 Feb 2024 01:21:18 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6fcb75827b10780bc35d70b5573f25b66d2703d2777a120def7586adba8ac4`  
		Last Modified: Wed, 14 Feb 2024 01:21:18 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9369421163315ef00dd703434b101bb4c5d8dfb41f99c756d6952ba07dec8102`  
		Last Modified: Wed, 14 Feb 2024 01:21:18 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-rc1`

```console
$ docker pull traefik@sha256:f87f46635d62db3be770a288d9ced2755e37b49b4c142823cd29f16637378794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `traefik:v3.0.0-rc1` - linux; amd64

```console
$ docker pull traefik@sha256:a4291860384ab14cf6b14fec90442ea413b0d73e08a1a90ae072d5f87b0a5c5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45215806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7500ba9e0cd2b3b583d5b187cf56519f2978a62e966aef6175617fafed7dd4cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:56:04 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 14 Feb 2024 01:51:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 14 Feb 2024 01:51:21 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 14 Feb 2024 01:51:21 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:51:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 01:51:21 GMT
CMD ["traefik"]
# Wed, 14 Feb 2024 01:51:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:31bd04195f40000b0e1ed3c2ef3a8a0d2f53fd88c276d95cb0b76930303cfb94`  
		Last Modified: Wed, 14 Feb 2024 01:51:42 GMT  
		Size: 41.2 MB (41184549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a5a9477b9d74a0c0333da7227d4a9ab61a40d0120099c5a37dbf91d92bd171`  
		Last Modified: Wed, 14 Feb 2024 01:51:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-rc1` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4faead017690c14f301136a1a98eb1879cf07ad0acc84f86864fd9aa5001eb8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42442406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c237b08566cd841ed92601fb3e908a68e7d6dda1c4aa0f6bd7bf9ddef31773`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:30:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 14 Feb 2024 01:13:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 14 Feb 2024 01:13:52 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 14 Feb 2024 01:13:52 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:13:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 01:13:52 GMT
CMD ["traefik"]
# Wed, 14 Feb 2024 01:13:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:fe3fe7868c1ea143b7df56b2d6b3c6847ddaee96e1fa37bc18a87b3ad36a6c23`  
		Last Modified: Wed, 14 Feb 2024 01:14:11 GMT  
		Size: 38.7 MB (38653255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb42156df07563bc9b31e938379682e1d4b35f6f304406147d149f09391c10d`  
		Last Modified: Wed, 14 Feb 2024 01:14:04 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-rc1` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1c00a020261fd642273c185f9b48745bb1d5003fb2e8bd879907ae273108dbdd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42106293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28adc4dbdab7502b67b1129aa3912439c53aff1ef74573aa4563e8b05c14af81`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:18:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 14 Feb 2024 01:59:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 14 Feb 2024 01:59:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 14 Feb 2024 01:59:22 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:59:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 01:59:22 GMT
CMD ["traefik"]
# Wed, 14 Feb 2024 01:59:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:54440866de0ca0fe3e9e6e7b42590b5411b695f21c4bae155e83410aa5e0b328`  
		Last Modified: Wed, 14 Feb 2024 01:59:40 GMT  
		Size: 38.1 MB (38133003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82aa8f90d259db174923a28ed575665689ba2118c036dfca50bb75b6e1ee988`  
		Last Modified: Wed, 14 Feb 2024 01:59:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-rc1` - linux; ppc64le

```console
$ docker pull traefik@sha256:7f4dcfc08cd60809966904f0654bfbb685289dc4e47878704f998eb3196b2d97
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40975702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bca94a6548e319d4e308b938921db72ce70d9be20ecee233fa8c3e72cdef3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 00:49:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 14 Feb 2024 01:47:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 14 Feb 2024 01:47:21 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 14 Feb 2024 01:47:22 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:47:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 01:47:24 GMT
CMD ["traefik"]
# Wed, 14 Feb 2024 01:47:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d181bcd9b7ac9d9a7e1e9e6d1c90dd28e0a0f79c68f6078fc500c9a82cc75ac7`  
		Last Modified: Wed, 14 Feb 2024 01:47:51 GMT  
		Size: 37.0 MB (36993826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9716cdbe5ee808f56bce71d706e73d2f4b5526f0a1eea822512b67b2d80a310d`  
		Last Modified: Wed, 14 Feb 2024 01:47:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-rc1-windowsservercore-1809`

```console
$ docker pull traefik@sha256:66c97ca8fbe5df3c1c0ff6f86bfeec315cbce13effb3ffb8a342e19770cf1826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `traefik:v3.0.0-rc1-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull traefik@sha256:b7fc0fdb48d8386ebbe64b9aa205b3806dad93e57a01140a3dd36cfbdca8f832
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2112612791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d5d74e8d49f01a9fd3ee0e8ca207d7736f60a44489ad4ca9efa4a9ee9c7c64`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 01:20:35 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Feb 2024 01:20:36 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:20:37 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Feb 2024 01:20:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:83c985906a307cada02318f1c538b20c702179767bbeb044701f813377b10dea`  
		Last Modified: Wed, 14 Feb 2024 01:22:12 GMT  
		Size: 42.9 MB (42885051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8cc81e75ce72775f5da96e56be1d87f290d904b358ac5ccec00265737d852b`  
		Last Modified: Wed, 14 Feb 2024 01:22:03 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59c39f841dc2a443c02f59ac09c498549c0e61a8f1fb7e1121c7b8f3e753753`  
		Last Modified: Wed, 14 Feb 2024 01:22:03 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d7a270868debd500b8f950e8f2aae55decfd34892fa24b1f5f467dd0e0c485`  
		Last Modified: Wed, 14 Feb 2024 01:22:03 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-rc1-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:f4b0afc615e1ea31719fc20ebc026949317a18b6e34a6e84a0280d596cb38e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `traefik:v3.0.0-rc1-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull traefik@sha256:111fb73808e396a9cc4145690ba8c6bd4ce023946231a8dd1e3e31207de3911d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1943081560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7653e2b60df3ff29290d8eae94b6ceb9a2c50dce37d59ea9c3e71760fbbee30`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 01:19:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Feb 2024 01:19:06 GMT
EXPOSE 80
# Wed, 14 Feb 2024 01:19:07 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Feb 2024 01:19:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:ca669fce90e34d80675163908e4c7e7c16e0656a28a5c116b816350295d7ce3b`  
		Last Modified: Wed, 14 Feb 2024 01:21:46 GMT  
		Size: 42.9 MB (42863713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47abd1be3950e078ebf68e63bf3a919a8bcd7bf268416007c513c47a71468c1e`  
		Last Modified: Wed, 14 Feb 2024 01:21:18 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6fcb75827b10780bc35d70b5573f25b66d2703d2777a120def7586adba8ac4`  
		Last Modified: Wed, 14 Feb 2024 01:21:18 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9369421163315ef00dd703434b101bb4c5d8dfb41f99c756d6952ba07dec8102`  
		Last Modified: Wed, 14 Feb 2024 01:21:18 GMT  
		Size: 1.3 KB (1282 bytes)  
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
