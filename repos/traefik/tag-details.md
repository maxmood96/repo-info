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
-	[`traefik:3.0.0-rc3`](#traefik300-rc3)
-	[`traefik:3.0.0-rc3-windowsservercore-1809`](#traefik300-rc3-windowsservercore-1809)
-	[`traefik:3.0.0-rc3-windowsservercore-ltsc2022`](#traefik300-rc3-windowsservercore-ltsc2022)
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
-	[`traefik:v3.0.0-rc3`](#traefikv300-rc3)
-	[`traefik:v3.0.0-rc3-windowsservercore-1809`](#traefikv300-rc3-windowsservercore-1809)
-	[`traefik:v3.0.0-rc3-windowsservercore-ltsc2022`](#traefikv300-rc3-windowsservercore-ltsc2022)
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
$ docker pull traefik@sha256:2aac8ebfad3ba904b4d3526df665da626873047f67c5342e1ed998989c43ea8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `traefik:2.11-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull traefik@sha256:bbe0a7db1135c5aa48369a4eda314906864f78383e7b1fe09431f98ee6ccd234
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167341162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f811c8f069782b8d45e62475a89a201832c48402d8133e1515c291182b26a502`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:25:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:25:48 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:25:49 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:25:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95ac7200a8e3a2c0ba493c179bc071869284c2508fd9bb2fe002278f0afcb18`  
		Last Modified: Wed, 13 Mar 2024 04:27:37 GMT  
		Size: 42.2 MB (42235535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd691174aab3bf358c4e8c04e2289a6417f9a218daef3f6b340becc6b0d3db0`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2031e082f306cfde918d303ec4b3c6b20fe28fa4e98bc75bdf94e6a16c3fc9`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34956f4ae2a88ec16d6fc2161f4cf70d3f9a56e0fba9bec37bbadc0f11d1ef64`  
		Last Modified: Wed, 13 Mar 2024 04:27:27 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:21d300d8d72db35e94fd885be7873e66fdf9a50407378145a1e8c5df0ae6f1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:698b27fe2f1a7d910141455723932f32b8c7cb729830eb791a0b9bb9e1dfc37b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1999700334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac748ff26ef4b15d8858f826b681d177e9546e01c1809c76064e4595ef8f622`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:24:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:24:05 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:24:06 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:24:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3defa6c0936d429cc07a43d4c41e98fe9a563b22d6d47c2d4e8b26bb91fd09`  
		Last Modified: Wed, 13 Mar 2024 04:27:11 GMT  
		Size: 42.2 MB (42235665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90320aa66285218bea75d45b7a0ce6306af06d7590d55538d05bb2d86f92f8d`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff82c34f3abc3e251df983c86355fbe950801d6de486bdf2b7bc3ab052e92cce`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bffafb756604dddb7d508523e6b558dbb9907799b21e53718fda2e27125f2af`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1424 bytes)  
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
$ docker pull traefik@sha256:2aac8ebfad3ba904b4d3526df665da626873047f67c5342e1ed998989c43ea8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `traefik:2.11.0-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull traefik@sha256:bbe0a7db1135c5aa48369a4eda314906864f78383e7b1fe09431f98ee6ccd234
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167341162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f811c8f069782b8d45e62475a89a201832c48402d8133e1515c291182b26a502`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:25:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:25:48 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:25:49 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:25:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95ac7200a8e3a2c0ba493c179bc071869284c2508fd9bb2fe002278f0afcb18`  
		Last Modified: Wed, 13 Mar 2024 04:27:37 GMT  
		Size: 42.2 MB (42235535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd691174aab3bf358c4e8c04e2289a6417f9a218daef3f6b340becc6b0d3db0`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2031e082f306cfde918d303ec4b3c6b20fe28fa4e98bc75bdf94e6a16c3fc9`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34956f4ae2a88ec16d6fc2161f4cf70d3f9a56e0fba9bec37bbadc0f11d1ef64`  
		Last Modified: Wed, 13 Mar 2024 04:27:27 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.0-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:21d300d8d72db35e94fd885be7873e66fdf9a50407378145a1e8c5df0ae6f1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:2.11.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:698b27fe2f1a7d910141455723932f32b8c7cb729830eb791a0b9bb9e1dfc37b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1999700334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac748ff26ef4b15d8858f826b681d177e9546e01c1809c76064e4595ef8f622`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:24:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:24:05 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:24:06 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:24:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3defa6c0936d429cc07a43d4c41e98fe9a563b22d6d47c2d4e8b26bb91fd09`  
		Last Modified: Wed, 13 Mar 2024 04:27:11 GMT  
		Size: 42.2 MB (42235665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90320aa66285218bea75d45b7a0ce6306af06d7590d55538d05bb2d86f92f8d`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff82c34f3abc3e251df983c86355fbe950801d6de486bdf2b7bc3ab052e92cce`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bffafb756604dddb7d508523e6b558dbb9907799b21e53718fda2e27125f2af`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0`

```console
$ docker pull traefik@sha256:b94eeadd5a798e34f715a97bf2dc10e43295a2bd76a4a7f719c8ba985eac47b8
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
$ docker pull traefik@sha256:b8daf47c228a785540ac1793e5a55cd426b9be9ae5463a3329ca628bc64d4578
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45170558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ce85d3f6b67315d6426844f91fb73d28aaf7f26847f7e195dcc320a697da68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:56:04 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 12 Mar 2024 18:06:36 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc2/traefik_v3.0.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 12 Mar 2024 18:06:36 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 12 Mar 2024 18:06:36 GMT
EXPOSE 80
# Tue, 12 Mar 2024 18:06:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 18:06:36 GMT
CMD ["traefik"]
# Tue, 12 Mar 2024 18:06:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:64ee46bb1b004ebf92efe7749a0743fc8f514645f6f550314050725042359d52`  
		Last Modified: Tue, 12 Mar 2024 18:06:58 GMT  
		Size: 41.1 MB (41139302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58fad920bf0963d9b14c2cbb626abec9c5ff58c24d8e1241310e9a13c735ba04`  
		Last Modified: Tue, 12 Mar 2024 18:06:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1a35e26afe4dc019235a3191cdd828fccfed5b616f3277b2ac1191160ce2e16e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42392623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ed8c341d285d363e4b6eb788570336afcf80b26197f01d40c3ddc0c3ed3e21`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:30:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 12 Mar 2024 16:50:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc2/traefik_v3.0.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 12 Mar 2024 16:50:47 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 12 Mar 2024 16:50:48 GMT
EXPOSE 80
# Tue, 12 Mar 2024 16:50:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 16:50:48 GMT
CMD ["traefik"]
# Tue, 12 Mar 2024 16:50:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d07f64a25aa704ff93d5f78f6896c27e8270cb0091d433c753ac0a8d184c09b8`  
		Last Modified: Tue, 12 Mar 2024 16:51:09 GMT  
		Size: 38.6 MB (38603472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900a4af0b0c446a15b957e6b3308fe45b57de59aa4962de4540c21e05c401674`  
		Last Modified: Tue, 12 Mar 2024 16:51:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:c8393a10852c5aff2d6d25a2fb26d02b6ab0f43c2c2ac81fae5614490df3bc40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42046075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edd35743be8eb62efff73a37302e5b471369d54fa77a69c74d15c043f9aba7b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:18:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 12 Mar 2024 19:22:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc2/traefik_v3.0.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 12 Mar 2024 19:22:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 12 Mar 2024 19:22:22 GMT
EXPOSE 80
# Tue, 12 Mar 2024 19:22:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 19:22:22 GMT
CMD ["traefik"]
# Tue, 12 Mar 2024 19:22:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:b397dcabfef180431b2890cb8fc1dc2011e6005fcc71e797c9cfe2f0dc6efced`  
		Last Modified: Tue, 12 Mar 2024 19:22:40 GMT  
		Size: 38.1 MB (38072785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96978b1f871033c585618174426cad2bb9cf85191e83709741c1f5aed1c9e6c1`  
		Last Modified: Tue, 12 Mar 2024 19:22:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; ppc64le

```console
$ docker pull traefik@sha256:5df2a7a48bbc7bc8b9102d1be19ed7739db46a811c7c17632a4e0e1556913d31
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40911753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703f4c4e50756136ce84a3d6ce131ef01d217d7d9841d00f1667291dbe06c44f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 00:49:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Mar 2024 19:26:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Mar 2024 19:26:53 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Mar 2024 19:26:53 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:26:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Mar 2024 19:26:54 GMT
CMD ["traefik"]
# Wed, 13 Mar 2024 19:26:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:e84276c557c55d0b763d852100a27cf507630a42743be661153455e374884705`  
		Last Modified: Wed, 13 Mar 2024 19:27:19 GMT  
		Size: 36.9 MB (36929877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbd405b5f66d9a4da08abf8b723fadb8e19e062ca8f136c78b09f51d12abd0f`  
		Last Modified: Wed, 13 Mar 2024 19:27:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; s390x

```console
$ docker pull traefik@sha256:069b8c8e84b489b522d633e91bdd51cc5ceef29f9ea33ed92e23f4112a455dd3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43799571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10f04a6fc7f8f19251aafefd7499ccd4baea178c072109b316c2235f76cdcf3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:20:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 12 Mar 2024 19:58:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc2/traefik_v3.0.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 12 Mar 2024 19:58:11 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 12 Mar 2024 19:58:11 GMT
EXPOSE 80
# Tue, 12 Mar 2024 19:58:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 19:58:12 GMT
CMD ["traefik"]
# Tue, 12 Mar 2024 19:58:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a4c37ece4642190957bf3c90cb4653b444dc6bd1347473d2fb8a4425b6aa1189`  
		Last Modified: Tue, 12 Mar 2024 20:00:45 GMT  
		Size: 39.9 MB (39933177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06929efbab357dee048e08143eba49fb99551615e3c19b70b1b296eca94ed60`  
		Last Modified: Tue, 12 Mar 2024 20:00:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:8cd933505291271393e38dee7c95ad038c39aaad0a7e2f98e504fb1874effeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `traefik:3.0-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull traefik@sha256:1765dfc7a5bd9874ae38acda9135d4051f862f147f7c74b2f1a5adf5e4b7e453
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167946232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ae201a76bc79c7366a245a122af50968181c082a2565a45d9271d0d33ece1b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 19:19:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 19:19:02 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:19:03 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 19:19:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0715f5907ace3ad301acdf493973e89a9b672116bac6afd2749e9ce4a44a8eb`  
		Last Modified: Wed, 13 Mar 2024 19:20:36 GMT  
		Size: 42.8 MB (42840623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4dae33104c82d0189cfd84d69f2eb1837501f5fa16fdc3ca5e2a5e8fb99253`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78ea15fee491549e4e912349cd2e5c59f95685186ab429b8245903ef3c8f436`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d5bf92c0a782bf09a681c092db045e7fd92ff41b97e6edef7c93db76378f68`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:73e2c44013cf3dfa5f84a7b2243eac5c8dce9167463c4efb67cbe9a7a42e37ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:3.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:ae569feeca4b45ed9255c22a65efb91c846f28365423687f193aa44c0e655102
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2000292492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0731b3bf072fcc8a146ae5c4ab1935bbc470841c7378a91a35649beace00a22`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 19:16:26 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 19:16:27 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:16:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 19:16:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8dcc153faf25844163e5b2f08f18f94ab93dcaaab8919038821ffde2a49021`  
		Last Modified: Wed, 13 Mar 2024 19:20:07 GMT  
		Size: 42.8 MB (42827825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27d87838d656d80f32043c43304582529474e4fb8bcc682a3d0cf5c3699f30f`  
		Last Modified: Wed, 13 Mar 2024 19:19:57 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfdad8e3579fee6ea282c79f652abbf970849ca89071214d8027e16525fa3fa`  
		Last Modified: Wed, 13 Mar 2024 19:19:58 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7429cd8653cca61b37ad619d4aa4a2e5fe763b829cf968d0be23b2f9612bed`  
		Last Modified: Wed, 13 Mar 2024 19:19:57 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-rc3`

```console
$ docker pull traefik@sha256:eefd1b77c77149cbd42f3ee5992d1469b6f7a9fb56b1d233c11320f88b75f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; ppc64le

### `traefik:3.0.0-rc3` - linux; ppc64le

```console
$ docker pull traefik@sha256:5df2a7a48bbc7bc8b9102d1be19ed7739db46a811c7c17632a4e0e1556913d31
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40911753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703f4c4e50756136ce84a3d6ce131ef01d217d7d9841d00f1667291dbe06c44f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 00:49:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Mar 2024 19:26:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Mar 2024 19:26:53 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Mar 2024 19:26:53 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:26:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Mar 2024 19:26:54 GMT
CMD ["traefik"]
# Wed, 13 Mar 2024 19:26:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:e84276c557c55d0b763d852100a27cf507630a42743be661153455e374884705`  
		Last Modified: Wed, 13 Mar 2024 19:27:19 GMT  
		Size: 36.9 MB (36929877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbd405b5f66d9a4da08abf8b723fadb8e19e062ca8f136c78b09f51d12abd0f`  
		Last Modified: Wed, 13 Mar 2024 19:27:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-rc3-windowsservercore-1809`

```console
$ docker pull traefik@sha256:8cd933505291271393e38dee7c95ad038c39aaad0a7e2f98e504fb1874effeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `traefik:3.0.0-rc3-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull traefik@sha256:1765dfc7a5bd9874ae38acda9135d4051f862f147f7c74b2f1a5adf5e4b7e453
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167946232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ae201a76bc79c7366a245a122af50968181c082a2565a45d9271d0d33ece1b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 19:19:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 19:19:02 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:19:03 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 19:19:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0715f5907ace3ad301acdf493973e89a9b672116bac6afd2749e9ce4a44a8eb`  
		Last Modified: Wed, 13 Mar 2024 19:20:36 GMT  
		Size: 42.8 MB (42840623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4dae33104c82d0189cfd84d69f2eb1837501f5fa16fdc3ca5e2a5e8fb99253`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78ea15fee491549e4e912349cd2e5c59f95685186ab429b8245903ef3c8f436`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d5bf92c0a782bf09a681c092db045e7fd92ff41b97e6edef7c93db76378f68`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-rc3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:73e2c44013cf3dfa5f84a7b2243eac5c8dce9167463c4efb67cbe9a7a42e37ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:3.0.0-rc3-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:ae569feeca4b45ed9255c22a65efb91c846f28365423687f193aa44c0e655102
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2000292492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0731b3bf072fcc8a146ae5c4ab1935bbc470841c7378a91a35649beace00a22`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 19:16:26 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 19:16:27 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:16:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 19:16:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8dcc153faf25844163e5b2f08f18f94ab93dcaaab8919038821ffde2a49021`  
		Last Modified: Wed, 13 Mar 2024 19:20:07 GMT  
		Size: 42.8 MB (42827825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27d87838d656d80f32043c43304582529474e4fb8bcc682a3d0cf5c3699f30f`  
		Last Modified: Wed, 13 Mar 2024 19:19:57 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfdad8e3579fee6ea282c79f652abbf970849ca89071214d8027e16525fa3fa`  
		Last Modified: Wed, 13 Mar 2024 19:19:58 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7429cd8653cca61b37ad619d4aa4a2e5fe763b829cf968d0be23b2f9612bed`  
		Last Modified: Wed, 13 Mar 2024 19:19:57 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort`

```console
$ docker pull traefik@sha256:b94eeadd5a798e34f715a97bf2dc10e43295a2bd76a4a7f719c8ba985eac47b8
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
$ docker pull traefik@sha256:b8daf47c228a785540ac1793e5a55cd426b9be9ae5463a3329ca628bc64d4578
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45170558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ce85d3f6b67315d6426844f91fb73d28aaf7f26847f7e195dcc320a697da68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:56:04 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 12 Mar 2024 18:06:36 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc2/traefik_v3.0.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 12 Mar 2024 18:06:36 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 12 Mar 2024 18:06:36 GMT
EXPOSE 80
# Tue, 12 Mar 2024 18:06:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 18:06:36 GMT
CMD ["traefik"]
# Tue, 12 Mar 2024 18:06:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:64ee46bb1b004ebf92efe7749a0743fc8f514645f6f550314050725042359d52`  
		Last Modified: Tue, 12 Mar 2024 18:06:58 GMT  
		Size: 41.1 MB (41139302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58fad920bf0963d9b14c2cbb626abec9c5ff58c24d8e1241310e9a13c735ba04`  
		Last Modified: Tue, 12 Mar 2024 18:06:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1a35e26afe4dc019235a3191cdd828fccfed5b616f3277b2ac1191160ce2e16e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42392623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ed8c341d285d363e4b6eb788570336afcf80b26197f01d40c3ddc0c3ed3e21`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:30:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 12 Mar 2024 16:50:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc2/traefik_v3.0.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 12 Mar 2024 16:50:47 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 12 Mar 2024 16:50:48 GMT
EXPOSE 80
# Tue, 12 Mar 2024 16:50:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 16:50:48 GMT
CMD ["traefik"]
# Tue, 12 Mar 2024 16:50:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d07f64a25aa704ff93d5f78f6896c27e8270cb0091d433c753ac0a8d184c09b8`  
		Last Modified: Tue, 12 Mar 2024 16:51:09 GMT  
		Size: 38.6 MB (38603472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900a4af0b0c446a15b957e6b3308fe45b57de59aa4962de4540c21e05c401674`  
		Last Modified: Tue, 12 Mar 2024 16:51:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:c8393a10852c5aff2d6d25a2fb26d02b6ab0f43c2c2ac81fae5614490df3bc40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42046075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edd35743be8eb62efff73a37302e5b471369d54fa77a69c74d15c043f9aba7b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:18:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 12 Mar 2024 19:22:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc2/traefik_v3.0.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 12 Mar 2024 19:22:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 12 Mar 2024 19:22:22 GMT
EXPOSE 80
# Tue, 12 Mar 2024 19:22:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 19:22:22 GMT
CMD ["traefik"]
# Tue, 12 Mar 2024 19:22:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:b397dcabfef180431b2890cb8fc1dc2011e6005fcc71e797c9cfe2f0dc6efced`  
		Last Modified: Tue, 12 Mar 2024 19:22:40 GMT  
		Size: 38.1 MB (38072785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96978b1f871033c585618174426cad2bb9cf85191e83709741c1f5aed1c9e6c1`  
		Last Modified: Tue, 12 Mar 2024 19:22:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; ppc64le

```console
$ docker pull traefik@sha256:5df2a7a48bbc7bc8b9102d1be19ed7739db46a811c7c17632a4e0e1556913d31
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40911753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703f4c4e50756136ce84a3d6ce131ef01d217d7d9841d00f1667291dbe06c44f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 00:49:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Mar 2024 19:26:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Mar 2024 19:26:53 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Mar 2024 19:26:53 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:26:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Mar 2024 19:26:54 GMT
CMD ["traefik"]
# Wed, 13 Mar 2024 19:26:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:e84276c557c55d0b763d852100a27cf507630a42743be661153455e374884705`  
		Last Modified: Wed, 13 Mar 2024 19:27:19 GMT  
		Size: 36.9 MB (36929877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbd405b5f66d9a4da08abf8b723fadb8e19e062ca8f136c78b09f51d12abd0f`  
		Last Modified: Wed, 13 Mar 2024 19:27:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; s390x

```console
$ docker pull traefik@sha256:069b8c8e84b489b522d633e91bdd51cc5ceef29f9ea33ed92e23f4112a455dd3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43799571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10f04a6fc7f8f19251aafefd7499ccd4baea178c072109b316c2235f76cdcf3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:20:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 12 Mar 2024 19:58:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc2/traefik_v3.0.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 12 Mar 2024 19:58:11 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 12 Mar 2024 19:58:11 GMT
EXPOSE 80
# Tue, 12 Mar 2024 19:58:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 19:58:12 GMT
CMD ["traefik"]
# Tue, 12 Mar 2024 19:58:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a4c37ece4642190957bf3c90cb4653b444dc6bd1347473d2fb8a4425b6aa1189`  
		Last Modified: Tue, 12 Mar 2024 20:00:45 GMT  
		Size: 39.9 MB (39933177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06929efbab357dee048e08143eba49fb99551615e3c19b70b1b296eca94ed60`  
		Last Modified: Tue, 12 Mar 2024 20:00:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort-windowsservercore-1809`

```console
$ docker pull traefik@sha256:8cd933505291271393e38dee7c95ad038c39aaad0a7e2f98e504fb1874effeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `traefik:beaufort-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull traefik@sha256:1765dfc7a5bd9874ae38acda9135d4051f862f147f7c74b2f1a5adf5e4b7e453
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167946232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ae201a76bc79c7366a245a122af50968181c082a2565a45d9271d0d33ece1b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 19:19:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 19:19:02 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:19:03 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 19:19:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0715f5907ace3ad301acdf493973e89a9b672116bac6afd2749e9ce4a44a8eb`  
		Last Modified: Wed, 13 Mar 2024 19:20:36 GMT  
		Size: 42.8 MB (42840623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4dae33104c82d0189cfd84d69f2eb1837501f5fa16fdc3ca5e2a5e8fb99253`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78ea15fee491549e4e912349cd2e5c59f95685186ab429b8245903ef3c8f436`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d5bf92c0a782bf09a681c092db045e7fd92ff41b97e6edef7c93db76378f68`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:73e2c44013cf3dfa5f84a7b2243eac5c8dce9167463c4efb67cbe9a7a42e37ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:beaufort-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:ae569feeca4b45ed9255c22a65efb91c846f28365423687f193aa44c0e655102
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2000292492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0731b3bf072fcc8a146ae5c4ab1935bbc470841c7378a91a35649beace00a22`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 19:16:26 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 19:16:27 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:16:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 19:16:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8dcc153faf25844163e5b2f08f18f94ab93dcaaab8919038821ffde2a49021`  
		Last Modified: Wed, 13 Mar 2024 19:20:07 GMT  
		Size: 42.8 MB (42827825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27d87838d656d80f32043c43304582529474e4fb8bcc682a3d0cf5c3699f30f`  
		Last Modified: Wed, 13 Mar 2024 19:19:57 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfdad8e3579fee6ea282c79f652abbf970849ca89071214d8027e16525fa3fa`  
		Last Modified: Wed, 13 Mar 2024 19:19:58 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7429cd8653cca61b37ad619d4aa4a2e5fe763b829cf968d0be23b2f9612bed`  
		Last Modified: Wed, 13 Mar 2024 19:19:57 GMT  
		Size: 1.4 KB (1423 bytes)  
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
$ docker pull traefik@sha256:2aac8ebfad3ba904b4d3526df665da626873047f67c5342e1ed998989c43ea8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `traefik:mimolette-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull traefik@sha256:bbe0a7db1135c5aa48369a4eda314906864f78383e7b1fe09431f98ee6ccd234
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167341162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f811c8f069782b8d45e62475a89a201832c48402d8133e1515c291182b26a502`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:25:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:25:48 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:25:49 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:25:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95ac7200a8e3a2c0ba493c179bc071869284c2508fd9bb2fe002278f0afcb18`  
		Last Modified: Wed, 13 Mar 2024 04:27:37 GMT  
		Size: 42.2 MB (42235535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd691174aab3bf358c4e8c04e2289a6417f9a218daef3f6b340becc6b0d3db0`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2031e082f306cfde918d303ec4b3c6b20fe28fa4e98bc75bdf94e6a16c3fc9`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34956f4ae2a88ec16d6fc2161f4cf70d3f9a56e0fba9bec37bbadc0f11d1ef64`  
		Last Modified: Wed, 13 Mar 2024 04:27:27 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:21d300d8d72db35e94fd885be7873e66fdf9a50407378145a1e8c5df0ae6f1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:698b27fe2f1a7d910141455723932f32b8c7cb729830eb791a0b9bb9e1dfc37b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1999700334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac748ff26ef4b15d8858f826b681d177e9546e01c1809c76064e4595ef8f622`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:24:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:24:05 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:24:06 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:24:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3defa6c0936d429cc07a43d4c41e98fe9a563b22d6d47c2d4e8b26bb91fd09`  
		Last Modified: Wed, 13 Mar 2024 04:27:11 GMT  
		Size: 42.2 MB (42235665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90320aa66285218bea75d45b7a0ce6306af06d7590d55538d05bb2d86f92f8d`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff82c34f3abc3e251df983c86355fbe950801d6de486bdf2b7bc3ab052e92cce`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bffafb756604dddb7d508523e6b558dbb9907799b21e53718fda2e27125f2af`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1424 bytes)  
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
$ docker pull traefik@sha256:2aac8ebfad3ba904b4d3526df665da626873047f67c5342e1ed998989c43ea8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `traefik:v2.11-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull traefik@sha256:bbe0a7db1135c5aa48369a4eda314906864f78383e7b1fe09431f98ee6ccd234
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167341162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f811c8f069782b8d45e62475a89a201832c48402d8133e1515c291182b26a502`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:25:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:25:48 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:25:49 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:25:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95ac7200a8e3a2c0ba493c179bc071869284c2508fd9bb2fe002278f0afcb18`  
		Last Modified: Wed, 13 Mar 2024 04:27:37 GMT  
		Size: 42.2 MB (42235535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd691174aab3bf358c4e8c04e2289a6417f9a218daef3f6b340becc6b0d3db0`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2031e082f306cfde918d303ec4b3c6b20fe28fa4e98bc75bdf94e6a16c3fc9`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34956f4ae2a88ec16d6fc2161f4cf70d3f9a56e0fba9bec37bbadc0f11d1ef64`  
		Last Modified: Wed, 13 Mar 2024 04:27:27 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:21d300d8d72db35e94fd885be7873e66fdf9a50407378145a1e8c5df0ae6f1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:698b27fe2f1a7d910141455723932f32b8c7cb729830eb791a0b9bb9e1dfc37b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1999700334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac748ff26ef4b15d8858f826b681d177e9546e01c1809c76064e4595ef8f622`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:24:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:24:05 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:24:06 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:24:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3defa6c0936d429cc07a43d4c41e98fe9a563b22d6d47c2d4e8b26bb91fd09`  
		Last Modified: Wed, 13 Mar 2024 04:27:11 GMT  
		Size: 42.2 MB (42235665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90320aa66285218bea75d45b7a0ce6306af06d7590d55538d05bb2d86f92f8d`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff82c34f3abc3e251df983c86355fbe950801d6de486bdf2b7bc3ab052e92cce`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bffafb756604dddb7d508523e6b558dbb9907799b21e53718fda2e27125f2af`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1424 bytes)  
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
$ docker pull traefik@sha256:2aac8ebfad3ba904b4d3526df665da626873047f67c5342e1ed998989c43ea8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `traefik:v2.11.0-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull traefik@sha256:bbe0a7db1135c5aa48369a4eda314906864f78383e7b1fe09431f98ee6ccd234
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167341162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f811c8f069782b8d45e62475a89a201832c48402d8133e1515c291182b26a502`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:25:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:25:48 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:25:49 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:25:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95ac7200a8e3a2c0ba493c179bc071869284c2508fd9bb2fe002278f0afcb18`  
		Last Modified: Wed, 13 Mar 2024 04:27:37 GMT  
		Size: 42.2 MB (42235535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd691174aab3bf358c4e8c04e2289a6417f9a218daef3f6b340becc6b0d3db0`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2031e082f306cfde918d303ec4b3c6b20fe28fa4e98bc75bdf94e6a16c3fc9`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34956f4ae2a88ec16d6fc2161f4cf70d3f9a56e0fba9bec37bbadc0f11d1ef64`  
		Last Modified: Wed, 13 Mar 2024 04:27:27 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.0-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:21d300d8d72db35e94fd885be7873e66fdf9a50407378145a1e8c5df0ae6f1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:v2.11.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:698b27fe2f1a7d910141455723932f32b8c7cb729830eb791a0b9bb9e1dfc37b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1999700334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac748ff26ef4b15d8858f826b681d177e9546e01c1809c76064e4595ef8f622`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:24:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:24:05 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:24:06 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:24:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3defa6c0936d429cc07a43d4c41e98fe9a563b22d6d47c2d4e8b26bb91fd09`  
		Last Modified: Wed, 13 Mar 2024 04:27:11 GMT  
		Size: 42.2 MB (42235665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90320aa66285218bea75d45b7a0ce6306af06d7590d55538d05bb2d86f92f8d`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff82c34f3abc3e251df983c86355fbe950801d6de486bdf2b7bc3ab052e92cce`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bffafb756604dddb7d508523e6b558dbb9907799b21e53718fda2e27125f2af`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0`

```console
$ docker pull traefik@sha256:b94eeadd5a798e34f715a97bf2dc10e43295a2bd76a4a7f719c8ba985eac47b8
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
$ docker pull traefik@sha256:b8daf47c228a785540ac1793e5a55cd426b9be9ae5463a3329ca628bc64d4578
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45170558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ce85d3f6b67315d6426844f91fb73d28aaf7f26847f7e195dcc320a697da68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:56:04 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 12 Mar 2024 18:06:36 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc2/traefik_v3.0.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 12 Mar 2024 18:06:36 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 12 Mar 2024 18:06:36 GMT
EXPOSE 80
# Tue, 12 Mar 2024 18:06:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 18:06:36 GMT
CMD ["traefik"]
# Tue, 12 Mar 2024 18:06:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:64ee46bb1b004ebf92efe7749a0743fc8f514645f6f550314050725042359d52`  
		Last Modified: Tue, 12 Mar 2024 18:06:58 GMT  
		Size: 41.1 MB (41139302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58fad920bf0963d9b14c2cbb626abec9c5ff58c24d8e1241310e9a13c735ba04`  
		Last Modified: Tue, 12 Mar 2024 18:06:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1a35e26afe4dc019235a3191cdd828fccfed5b616f3277b2ac1191160ce2e16e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42392623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ed8c341d285d363e4b6eb788570336afcf80b26197f01d40c3ddc0c3ed3e21`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:30:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 12 Mar 2024 16:50:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc2/traefik_v3.0.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 12 Mar 2024 16:50:47 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 12 Mar 2024 16:50:48 GMT
EXPOSE 80
# Tue, 12 Mar 2024 16:50:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 16:50:48 GMT
CMD ["traefik"]
# Tue, 12 Mar 2024 16:50:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d07f64a25aa704ff93d5f78f6896c27e8270cb0091d433c753ac0a8d184c09b8`  
		Last Modified: Tue, 12 Mar 2024 16:51:09 GMT  
		Size: 38.6 MB (38603472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900a4af0b0c446a15b957e6b3308fe45b57de59aa4962de4540c21e05c401674`  
		Last Modified: Tue, 12 Mar 2024 16:51:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:c8393a10852c5aff2d6d25a2fb26d02b6ab0f43c2c2ac81fae5614490df3bc40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42046075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edd35743be8eb62efff73a37302e5b471369d54fa77a69c74d15c043f9aba7b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:18:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 12 Mar 2024 19:22:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc2/traefik_v3.0.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 12 Mar 2024 19:22:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 12 Mar 2024 19:22:22 GMT
EXPOSE 80
# Tue, 12 Mar 2024 19:22:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 19:22:22 GMT
CMD ["traefik"]
# Tue, 12 Mar 2024 19:22:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:b397dcabfef180431b2890cb8fc1dc2011e6005fcc71e797c9cfe2f0dc6efced`  
		Last Modified: Tue, 12 Mar 2024 19:22:40 GMT  
		Size: 38.1 MB (38072785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96978b1f871033c585618174426cad2bb9cf85191e83709741c1f5aed1c9e6c1`  
		Last Modified: Tue, 12 Mar 2024 19:22:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; ppc64le

```console
$ docker pull traefik@sha256:5df2a7a48bbc7bc8b9102d1be19ed7739db46a811c7c17632a4e0e1556913d31
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40911753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703f4c4e50756136ce84a3d6ce131ef01d217d7d9841d00f1667291dbe06c44f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 00:49:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Mar 2024 19:26:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Mar 2024 19:26:53 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Mar 2024 19:26:53 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:26:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Mar 2024 19:26:54 GMT
CMD ["traefik"]
# Wed, 13 Mar 2024 19:26:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:e84276c557c55d0b763d852100a27cf507630a42743be661153455e374884705`  
		Last Modified: Wed, 13 Mar 2024 19:27:19 GMT  
		Size: 36.9 MB (36929877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbd405b5f66d9a4da08abf8b723fadb8e19e062ca8f136c78b09f51d12abd0f`  
		Last Modified: Wed, 13 Mar 2024 19:27:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; s390x

```console
$ docker pull traefik@sha256:069b8c8e84b489b522d633e91bdd51cc5ceef29f9ea33ed92e23f4112a455dd3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43799571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10f04a6fc7f8f19251aafefd7499ccd4baea178c072109b316c2235f76cdcf3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:20:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 12 Mar 2024 19:58:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc2/traefik_v3.0.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 12 Mar 2024 19:58:11 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 12 Mar 2024 19:58:11 GMT
EXPOSE 80
# Tue, 12 Mar 2024 19:58:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 19:58:12 GMT
CMD ["traefik"]
# Tue, 12 Mar 2024 19:58:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a4c37ece4642190957bf3c90cb4653b444dc6bd1347473d2fb8a4425b6aa1189`  
		Last Modified: Tue, 12 Mar 2024 20:00:45 GMT  
		Size: 39.9 MB (39933177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06929efbab357dee048e08143eba49fb99551615e3c19b70b1b296eca94ed60`  
		Last Modified: Tue, 12 Mar 2024 20:00:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:8cd933505291271393e38dee7c95ad038c39aaad0a7e2f98e504fb1874effeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `traefik:v3.0-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull traefik@sha256:1765dfc7a5bd9874ae38acda9135d4051f862f147f7c74b2f1a5adf5e4b7e453
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167946232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ae201a76bc79c7366a245a122af50968181c082a2565a45d9271d0d33ece1b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 19:19:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 19:19:02 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:19:03 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 19:19:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0715f5907ace3ad301acdf493973e89a9b672116bac6afd2749e9ce4a44a8eb`  
		Last Modified: Wed, 13 Mar 2024 19:20:36 GMT  
		Size: 42.8 MB (42840623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4dae33104c82d0189cfd84d69f2eb1837501f5fa16fdc3ca5e2a5e8fb99253`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78ea15fee491549e4e912349cd2e5c59f95685186ab429b8245903ef3c8f436`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d5bf92c0a782bf09a681c092db045e7fd92ff41b97e6edef7c93db76378f68`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:73e2c44013cf3dfa5f84a7b2243eac5c8dce9167463c4efb67cbe9a7a42e37ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:v3.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:ae569feeca4b45ed9255c22a65efb91c846f28365423687f193aa44c0e655102
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2000292492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0731b3bf072fcc8a146ae5c4ab1935bbc470841c7378a91a35649beace00a22`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 19:16:26 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 19:16:27 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:16:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 19:16:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8dcc153faf25844163e5b2f08f18f94ab93dcaaab8919038821ffde2a49021`  
		Last Modified: Wed, 13 Mar 2024 19:20:07 GMT  
		Size: 42.8 MB (42827825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27d87838d656d80f32043c43304582529474e4fb8bcc682a3d0cf5c3699f30f`  
		Last Modified: Wed, 13 Mar 2024 19:19:57 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfdad8e3579fee6ea282c79f652abbf970849ca89071214d8027e16525fa3fa`  
		Last Modified: Wed, 13 Mar 2024 19:19:58 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7429cd8653cca61b37ad619d4aa4a2e5fe763b829cf968d0be23b2f9612bed`  
		Last Modified: Wed, 13 Mar 2024 19:19:57 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-rc3`

```console
$ docker pull traefik@sha256:eefd1b77c77149cbd42f3ee5992d1469b6f7a9fb56b1d233c11320f88b75f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; ppc64le

### `traefik:v3.0.0-rc3` - linux; ppc64le

```console
$ docker pull traefik@sha256:5df2a7a48bbc7bc8b9102d1be19ed7739db46a811c7c17632a4e0e1556913d31
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40911753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703f4c4e50756136ce84a3d6ce131ef01d217d7d9841d00f1667291dbe06c44f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 00:49:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Mar 2024 19:26:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Mar 2024 19:26:53 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Mar 2024 19:26:53 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:26:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Mar 2024 19:26:54 GMT
CMD ["traefik"]
# Wed, 13 Mar 2024 19:26:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:e84276c557c55d0b763d852100a27cf507630a42743be661153455e374884705`  
		Last Modified: Wed, 13 Mar 2024 19:27:19 GMT  
		Size: 36.9 MB (36929877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbd405b5f66d9a4da08abf8b723fadb8e19e062ca8f136c78b09f51d12abd0f`  
		Last Modified: Wed, 13 Mar 2024 19:27:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-rc3-windowsservercore-1809`

```console
$ docker pull traefik@sha256:8cd933505291271393e38dee7c95ad038c39aaad0a7e2f98e504fb1874effeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `traefik:v3.0.0-rc3-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull traefik@sha256:1765dfc7a5bd9874ae38acda9135d4051f862f147f7c74b2f1a5adf5e4b7e453
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167946232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ae201a76bc79c7366a245a122af50968181c082a2565a45d9271d0d33ece1b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 19:19:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 19:19:02 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:19:03 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 19:19:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0715f5907ace3ad301acdf493973e89a9b672116bac6afd2749e9ce4a44a8eb`  
		Last Modified: Wed, 13 Mar 2024 19:20:36 GMT  
		Size: 42.8 MB (42840623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4dae33104c82d0189cfd84d69f2eb1837501f5fa16fdc3ca5e2a5e8fb99253`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78ea15fee491549e4e912349cd2e5c59f95685186ab429b8245903ef3c8f436`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d5bf92c0a782bf09a681c092db045e7fd92ff41b97e6edef7c93db76378f68`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-rc3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:73e2c44013cf3dfa5f84a7b2243eac5c8dce9167463c4efb67cbe9a7a42e37ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:v3.0.0-rc3-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:ae569feeca4b45ed9255c22a65efb91c846f28365423687f193aa44c0e655102
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2000292492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0731b3bf072fcc8a146ae5c4ab1935bbc470841c7378a91a35649beace00a22`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 19:16:26 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 19:16:27 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:16:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 19:16:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8dcc153faf25844163e5b2f08f18f94ab93dcaaab8919038821ffde2a49021`  
		Last Modified: Wed, 13 Mar 2024 19:20:07 GMT  
		Size: 42.8 MB (42827825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27d87838d656d80f32043c43304582529474e4fb8bcc682a3d0cf5c3699f30f`  
		Last Modified: Wed, 13 Mar 2024 19:19:57 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfdad8e3579fee6ea282c79f652abbf970849ca89071214d8027e16525fa3fa`  
		Last Modified: Wed, 13 Mar 2024 19:19:58 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7429cd8653cca61b37ad619d4aa4a2e5fe763b829cf968d0be23b2f9612bed`  
		Last Modified: Wed, 13 Mar 2024 19:19:57 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:2aac8ebfad3ba904b4d3526df665da626873047f67c5342e1ed998989c43ea8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull traefik@sha256:bbe0a7db1135c5aa48369a4eda314906864f78383e7b1fe09431f98ee6ccd234
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167341162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f811c8f069782b8d45e62475a89a201832c48402d8133e1515c291182b26a502`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:25:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:25:48 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:25:49 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:25:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95ac7200a8e3a2c0ba493c179bc071869284c2508fd9bb2fe002278f0afcb18`  
		Last Modified: Wed, 13 Mar 2024 04:27:37 GMT  
		Size: 42.2 MB (42235535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd691174aab3bf358c4e8c04e2289a6417f9a218daef3f6b340becc6b0d3db0`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2031e082f306cfde918d303ec4b3c6b20fe28fa4e98bc75bdf94e6a16c3fc9`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34956f4ae2a88ec16d6fc2161f4cf70d3f9a56e0fba9bec37bbadc0f11d1ef64`  
		Last Modified: Wed, 13 Mar 2024 04:27:27 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:21d300d8d72db35e94fd885be7873e66fdf9a50407378145a1e8c5df0ae6f1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:698b27fe2f1a7d910141455723932f32b8c7cb729830eb791a0b9bb9e1dfc37b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1999700334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac748ff26ef4b15d8858f826b681d177e9546e01c1809c76064e4595ef8f622`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:24:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:24:05 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:24:06 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:24:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3defa6c0936d429cc07a43d4c41e98fe9a563b22d6d47c2d4e8b26bb91fd09`  
		Last Modified: Wed, 13 Mar 2024 04:27:11 GMT  
		Size: 42.2 MB (42235665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90320aa66285218bea75d45b7a0ce6306af06d7590d55538d05bb2d86f92f8d`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff82c34f3abc3e251df983c86355fbe950801d6de486bdf2b7bc3ab052e92cce`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bffafb756604dddb7d508523e6b558dbb9907799b21e53718fda2e27125f2af`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
