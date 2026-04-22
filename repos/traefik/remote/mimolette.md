## `traefik:mimolette`

```console
$ docker pull traefik@sha256:b4d78b12a81f3d854979c6b0f99ff00827fcff11b01746217d691e7c54a60db3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:mimolette` - linux; amd64

```console
$ docker pull traefik@sha256:22360aded1cfd4a807dfd50c3bd8da9de6bca24f2f073fb30cec8939c8a7990c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51200741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a20f44e2294e1f4430bcf6fcd7032f0914cf07d26dae3e2b2a487e41a6d41fab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 17:38:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 22 Apr 2026 17:38:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.43/traefik_v2.11.43_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 22 Apr 2026 17:38:47 GMT
COPY entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 17:38:47 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 17:38:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 17:38:47 GMT
CMD ["traefik"]
# Wed, 22 Apr 2026 17:38:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.43 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e94ffdb9ea58492fe2756f7d28ff0d1334a3aa13a3792537a0f4c7baf4f18b`  
		Last Modified: Wed, 22 Apr 2026 17:39:10 GMT  
		Size: 455.7 KB (455657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85cbadb0f6c0fcbb54d5a32ab663d7bc80afa9ee8c77caa7f2563c62d432115f`  
		Last Modified: Wed, 22 Apr 2026 17:39:11 GMT  
		Size: 46.9 MB (46880526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bf35446a3679d132a3fac91f9a2cff7683c678a9f0245f6b3c19f0efec52f3`  
		Last Modified: Wed, 22 Apr 2026 17:39:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:20e3e5cf194584602596cf888d8a9080e3085f30e70f87aa7c549c15ec150f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26da138020660f7c9655f373ff4bfd28cb01ee59c64784d5f425109820b9a5a0`

```dockerfile
```

-	Layers:
	-	`sha256:23d36558a6e1a06a2765e0a3d4a630f6f5701c86613c8281fd056935a35e7e08`  
		Last Modified: Wed, 22 Apr 2026 17:39:10 GMT  
		Size: 853.0 KB (853005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:962b12c391958f1951525531e783be62b752462bebca886cd04dc3c2cd4e255a`  
		Last Modified: Wed, 22 Apr 2026 17:39:10 GMT  
		Size: 12.6 KB (12610 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:a8a2e4e685341c143d9239cace7b7d1ebf78c05a55a98338dd0def8315c35961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46913252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c619d1d06d90ae0c9d0637b02f04db36090d00ff30f121b3c5403578320aa9d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 17:37:32 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 22 Apr 2026 17:37:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.43/traefik_v2.11.43_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 22 Apr 2026 17:37:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 17:37:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 17:37:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 17:37:55 GMT
CMD ["traefik"]
# Wed, 22 Apr 2026 17:37:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.43 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22733e9b782bed0a545f8955760b4174c55fa47aa4d8e54388e03494e2d1eac9`  
		Last Modified: Wed, 22 Apr 2026 17:37:43 GMT  
		Size: 456.5 KB (456522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153c035658fee4bce532fce3639f0058232f5504fea329668826d402326d5c3f`  
		Last Modified: Wed, 22 Apr 2026 17:38:04 GMT  
		Size: 42.9 MB (42884498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f91341c8375407d57b8c28ca92503431b4cf3d6ebb1cd412a2bb08cb2e80afe`  
		Last Modified: Wed, 22 Apr 2026 17:38:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:36cafc33a9804d6898a725b5dd976e363206c554756ec191e63deb178dbd0ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 KB (12512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8254434d10d66dbe3cb9a0bcd9178b41978c5cd9956db13507c66b77a5e349f3`

```dockerfile
```

-	Layers:
	-	`sha256:3df688666f46316e77e22c33becd4eb5546e0486a40b4e712b0a7cb090f6e12a`  
		Last Modified: Wed, 22 Apr 2026 17:38:03 GMT  
		Size: 12.5 KB (12512 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:b6df290bc3db373c28b16bf26e4365f4113ca5eacac7fcb0bbfa106015dd7ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46820540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3912cae0cae5e0aa3e347b277a870ae4b9fb593bc04e5d386896599f46609c55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 17:38:24 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 22 Apr 2026 17:38:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.43/traefik_v2.11.43_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 22 Apr 2026 17:38:27 GMT
COPY entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 17:38:27 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 17:38:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 17:38:27 GMT
CMD ["traefik"]
# Wed, 22 Apr 2026 17:38:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.43 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6521cf741fc73eb4c349ba80f62c442a46afbb57c2a48baaa59102bfd3695f`  
		Last Modified: Wed, 22 Apr 2026 17:38:51 GMT  
		Size: 457.9 KB (457922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8a63f66c9df0f08280b58a03d3567882a5871d110b40f726dca12b2c0ba606`  
		Last Modified: Wed, 22 Apr 2026 17:38:53 GMT  
		Size: 42.2 MB (42162379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cc6fdc5e403a1b48e2ec9a0d5295190ca51526d091b3ef39d54f4c648ecb8b`  
		Last Modified: Wed, 22 Apr 2026 17:38:51 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:c6ebfece32e70312e76bc40d4457f6e490009cc1941cb27df18433b6664d4b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.2 KB (865212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97061e357cc06d061ab3eb9f705838a3c2293d6f86e4044bc5d740a78681147`

```dockerfile
```

-	Layers:
	-	`sha256:6b5b4541aeb55437a61f332ed377e3c2ee4dc96484a8789678be07aaa8445df2`  
		Last Modified: Wed, 22 Apr 2026 17:38:51 GMT  
		Size: 852.4 KB (852447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2bdd52d896f7057743ff8a9bd21ae929f6924b22bd1a1774c6cf640f4d39f7b`  
		Last Modified: Wed, 22 Apr 2026 17:38:51 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:3d0715211e9ec25edb169fcf0c879d92405e660dcce60f66f40fd9e0f9a5a907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45385362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc922dfafe0b6d364422650b7dd48b7c60967ad89f4d368756d7de07eea5e9ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:08:00 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 15 Apr 2026 21:09:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.42/traefik_v2.11.42_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 15 Apr 2026 21:09:08 GMT
COPY entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:09:08 GMT
EXPOSE map[80/tcp:{}]
# Wed, 15 Apr 2026 21:09:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 21:09:08 GMT
CMD ["traefik"]
# Wed, 15 Apr 2026 21:09:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.42 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ce53e29a62df07c200ac0d7cc718585a7031556056c94626ccbb010496ad7d`  
		Last Modified: Wed, 15 Apr 2026 21:08:51 GMT  
		Size: 458.3 KB (458325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4b8d9b31c3243f749f349eee1fb7d0ebf78ee9e6f2d2935ec4978adc92f72f`  
		Last Modified: Wed, 15 Apr 2026 21:09:54 GMT  
		Size: 41.1 MB (41095738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d40e8b70821d440111ce771bc95c5b76ed70eaef86918508fc9aeecfde8a9a`  
		Last Modified: Wed, 15 Apr 2026 21:09:53 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:d31a5f2c2b2924319537032faf354a687c3fecdc307c7c36e00b7ab86614fcc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.1 KB (865080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c60d05871c7289a3d5bfe75c646359a38e457972c35a507284957657eb556e5`

```dockerfile
```

-	Layers:
	-	`sha256:806b0e4a63458b881d94dddb904bee3bbf2af7ba0d2a9996eec555033b88151e`  
		Last Modified: Wed, 15 Apr 2026 21:09:53 GMT  
		Size: 852.4 KB (852406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb101f2a774c2dc09dcb6c092823f33a41c2724467f873389804fb49506d467`  
		Last Modified: Wed, 15 Apr 2026 21:09:53 GMT  
		Size: 12.7 KB (12674 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:811dd25bf268abaeb75c81623962e35fb5ea7cc8afd38926ce6d748e53fa6cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49516390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e63328dafa907728721f3cde55a95521747e98e8915464f704f561439f8d08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:20:27 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 16 Apr 2026 16:32:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.42/traefik_v2.11.42_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 16 Apr 2026 16:32:43 GMT
COPY entrypoint.sh / # buildkit
# Thu, 16 Apr 2026 16:32:43 GMT
EXPOSE map[80/tcp:{}]
# Thu, 16 Apr 2026 16:32:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2026 16:32:43 GMT
CMD ["traefik"]
# Thu, 16 Apr 2026 16:32:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.42 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981583f7aacfec3a6d84364895133cc9cba1bc1df0a68220b2ebf6c7c74b60af`  
		Last Modified: Thu, 16 Apr 2026 16:25:55 GMT  
		Size: 456.0 KB (456004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b1a00b91fdad025e3d59a3758a7f27658df8f8c54b31cf5e8a322a80a727bd`  
		Last Modified: Thu, 16 Apr 2026 16:38:49 GMT  
		Size: 45.5 MB (45472354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975d463abd622a270cecfa6824873adf19c9f260889ba93f502b05cb42bc751a`  
		Last Modified: Thu, 16 Apr 2026 16:38:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:de9fb247e82fa223b27a583f5d140a7c296a39d508ef348d79ca89742076203d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.1 KB (865075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea84a90d29dcc3427849abeed8b695c012d46e24b7869b43ad6e97172ea1a910`

```dockerfile
```

-	Layers:
	-	`sha256:4d197b08074cae06750d71f7889acc31cb34f22707873076418e9361e1360d9b`  
		Last Modified: Thu, 16 Apr 2026 16:38:42 GMT  
		Size: 852.4 KB (852402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c970977d508450da33e4b0d67bb0966d417ef4337f669a9b4c6771c357e1640a`  
		Last Modified: Thu, 16 Apr 2026 16:38:42 GMT  
		Size: 12.7 KB (12673 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:49f991092b568ccb16b1f06e3f31bd9c55a1e1d642f75bb6395da4c50970c435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49524110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b659c44a4f71e10aa6a6761bfc5e9e0e833b43e8906b65e5993ae0f13dbf3d5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:41:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 22 Apr 2026 17:36:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.43/traefik_v2.11.43_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 22 Apr 2026 17:36:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 17:36:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 17:36:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 17:36:13 GMT
CMD ["traefik"]
# Wed, 22 Apr 2026 17:36:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.43 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935dd66668d2f6e060f9d991a73aee8127a53466085251bae64e750e36112cdc`  
		Last Modified: Wed, 15 Apr 2026 20:42:42 GMT  
		Size: 456.7 KB (456660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece6aa21834cf9185a0afc6cef44c79aab2c8da2e7694d3cb3ecd5a685a6ab9a`  
		Last Modified: Wed, 22 Apr 2026 17:37:07 GMT  
		Size: 45.3 MB (45340549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256fa1d6ccc534363be5b3b1af425c424686f5b5bd74efa24135a0ec6a23dd18`  
		Last Modified: Wed, 22 Apr 2026 17:37:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:225b764f0afdc1e8a8114560241c3286f748235c391e92bdf996871618929046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.0 KB (864960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8555eb3bfc2f10161cd5b3ed7ae908eccceb9edc29ca32d45bded19bf2ae871`

```dockerfile
```

-	Layers:
	-	`sha256:689254fd3b61789a0e60d1c3becb26f2a5b06db484363bc8bb390941d7b53620`  
		Last Modified: Wed, 22 Apr 2026 17:37:06 GMT  
		Size: 852.4 KB (852350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70db69694dd53e9a3d8d1464fe5981f3b00c778cabaf7a5168ab77ed0bba7214`  
		Last Modified: Wed, 22 Apr 2026 17:37:06 GMT  
		Size: 12.6 KB (12610 bytes)  
		MIME: application/vnd.in-toto+json
