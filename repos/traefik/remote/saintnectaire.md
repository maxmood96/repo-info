## `traefik:saintnectaire`

```console
$ docker pull traefik@sha256:8a826738d0f6a52156c242c7c703edee618aba4cb8ec75ad76d5270592fd01e7
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

### `traefik:saintnectaire` - linux; amd64

```console
$ docker pull traefik@sha256:48ac39e4fce1f251e36958e283856137f9390b94e2aaee1a2937e3c0f507e313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52155205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0aaa08e850f1e91024ead7220b05cf3b6abb1b891662d618af6b2b90faa384`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 20 Dec 2024 11:05:54 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 20 Dec 2024 11:05:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.0-rc2/traefik_v3.3.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 20 Dec 2024 11:05:54 GMT
COPY entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 11:05:54 GMT
EXPOSE map[80/tcp:{}]
# Fri, 20 Dec 2024 11:05:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 11:05:54 GMT
CMD ["traefik"]
# Fri, 20 Dec 2024 11:05:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d703ef24357d1ab084c3e8a5d2acf32029d93128c9341b4228b6d94a8f42a5b`  
		Last Modified: Fri, 20 Dec 2024 21:35:24 GMT  
		Size: 461.8 KB (461799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71e55f584fa9c8e66170f8aa5091516d7c9905657b30a2ad670ae2990322739`  
		Last Modified: Fri, 20 Dec 2024 21:35:26 GMT  
		Size: 48.0 MB (48048593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdb80cf23335d5c83849d89e4742fc2ab15fb79ed36c40b9bdfe1a8e8e89d7b`  
		Last Modified: Fri, 20 Dec 2024 21:35:24 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:052ce4f3f5b4385c2936a00f9de018d48e550256e434e1ab13109b2be783b50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **836.3 KB (836333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad96a4582dc482cb1d3add072e1f4f3d647cd4090385214280e6a5494502fda0`

```dockerfile
```

-	Layers:
	-	`sha256:63ea66d63380c325d47e16618293619f6c8680eefa1db9b7ccd18f603a889f38`  
		Last Modified: Fri, 20 Dec 2024 21:35:24 GMT  
		Size: 824.9 KB (824946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e8fe02f6692074388fe92412a141bf7b3fc60504059c57973e27e517be464a`  
		Last Modified: Fri, 20 Dec 2024 21:35:24 GMT  
		Size: 11.4 KB (11387 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:saintnectaire` - linux; arm variant v6

```console
$ docker pull traefik@sha256:bc2031e1a696060c50bdf9fd46604726991c1a3854b1841066b7d8fbba35a715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48767027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad70f3cae7b4ac858779fc0a058d6d08193cd7aa448d1e46d4c6289279f4d410`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 20 Dec 2024 11:05:54 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 20 Dec 2024 11:05:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.0-rc2/traefik_v3.3.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 20 Dec 2024 11:05:54 GMT
COPY entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 11:05:54 GMT
EXPOSE map[80/tcp:{}]
# Fri, 20 Dec 2024 11:05:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 11:05:54 GMT
CMD ["traefik"]
# Fri, 20 Dec 2024 11:05:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92901f08881e2db31f763999740c8205a808d7b994dc4c764e09e6b7bce069fc`  
		Last Modified: Tue, 10 Dec 2024 23:08:43 GMT  
		Size: 463.0 KB (462956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca022f64d529d17c4d1ed115c58ed37b3f5e728ddc8cfe351a52d3aaac95989`  
		Last Modified: Fri, 20 Dec 2024 22:57:33 GMT  
		Size: 44.9 MB (44936520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562c83ce0f9a417e6ad14e6ad08b90995ccd08c478e04ec39305fadb5e205605`  
		Last Modified: Fri, 20 Dec 2024 22:57:32 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:14312118d61ba21d3d622329e1d18e5678d220763968c49d4143b437a951b9f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 KB (11253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499ae135e9ab790d351bd85b0d3797b71ce087217795b311c9a012729caf69be`

```dockerfile
```

-	Layers:
	-	`sha256:a0ca0b7ae74b7c8bab16a6ad8ef2b3e0bb1fc45fc78957d9f03096a908195f55`  
		Last Modified: Fri, 20 Dec 2024 22:57:32 GMT  
		Size: 11.3 KB (11253 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:saintnectaire` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:34e558df65203879b2832fa5b47cc4185b19317495e2ec16e307df3b33b50101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48998188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00303c8c585f2a4a19eba888f11ab1a4badc483ed16bf5ec487cd632c213a02c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 20 Dec 2024 11:05:54 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 20 Dec 2024 11:05:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.0-rc2/traefik_v3.3.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 20 Dec 2024 11:05:54 GMT
COPY entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 11:05:54 GMT
EXPOSE map[80/tcp:{}]
# Fri, 20 Dec 2024 11:05:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 11:05:54 GMT
CMD ["traefik"]
# Fri, 20 Dec 2024 11:05:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585859b3274a951bc36b95adc08606d5a5f9c3d34a636b612d2100b16ba19e52`  
		Last Modified: Tue, 10 Dec 2024 21:23:31 GMT  
		Size: 464.9 KB (464902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48f0a6f6f12bff8de00fc91b6f75d9335db02123c66b5a958de45c8b18cfec9`  
		Last Modified: Sat, 21 Dec 2024 00:20:36 GMT  
		Size: 44.5 MB (44539730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b002f1d0040aef989c78640ab2f90ed7da2e66b49621026bac10adfe617543e`  
		Last Modified: Sat, 21 Dec 2024 00:20:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:dcaf6dd7e6186b3d470686c3199f4197f1e767c8f098ddb3c3c2052121cbd49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **836.5 KB (836484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c3a82d0ddb81ac2f08a587f53469fb0aa7d4c5eb6626525892d129ff29e5ef`

```dockerfile
```

-	Layers:
	-	`sha256:42dcdbd41794affe87a58df7d2f5e1475336fee7ad1bfcc56d2dd18d495a681c`  
		Last Modified: Sat, 21 Dec 2024 00:20:34 GMT  
		Size: 825.0 KB (824990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c086d41559662e811363e2dd13a4bbe5686e472f179f0a16a301f98bdce69220`  
		Last Modified: Sat, 21 Dec 2024 00:20:34 GMT  
		Size: 11.5 KB (11494 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:saintnectaire` - linux; ppc64le

```console
$ docker pull traefik@sha256:8933d28a03bee730630b62f1d6d1aedd344639c254721db0fbdddc0abce217b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47035158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a0cb89e83760267303d7e1fa4ec12530fe0b1c84cc689ed49c25190fa115c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 20 Dec 2024 11:05:54 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 20 Dec 2024 11:05:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.0-rc2/traefik_v3.3.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 20 Dec 2024 11:05:54 GMT
COPY entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 11:05:54 GMT
EXPOSE map[80/tcp:{}]
# Fri, 20 Dec 2024 11:05:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 11:05:54 GMT
CMD ["traefik"]
# Fri, 20 Dec 2024 11:05:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b179457363cf87dfdcdef35a6cfec4e16b8186a6012d35c4dd8f272c1c3e2c5`  
		Last Modified: Tue, 10 Dec 2024 20:27:34 GMT  
		Size: 465.4 KB (465356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dc64b1b5ef72fa6d2fbb7058173ad759536bf981fd468d183f3ca0c0a32edf`  
		Last Modified: Fri, 20 Dec 2024 23:20:00 GMT  
		Size: 43.0 MB (42992324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ba7e3154c978091c61b4876f07971ff268704403a59ca54f3962aec6254fa`  
		Last Modified: Fri, 20 Dec 2024 23:19:59 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:ff36f63cda1f4b1700fa96ca7ffeec22be6498c67cee8838c6e224bec8e32016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **834.5 KB (834450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d835ca6b5c76c26f12f4df7f65e77fc4893b38cbbde371d041facdc2f8be202`

```dockerfile
```

-	Layers:
	-	`sha256:9bdf0609a55674329a21e57e7efb07e77332057d773efc23ad5508372d859d4f`  
		Last Modified: Fri, 20 Dec 2024 23:19:59 GMT  
		Size: 823.0 KB (823023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c393f23bfbf0234500f87862e14891847d4424776410ec47c9eeff26c5c1509`  
		Last Modified: Fri, 20 Dec 2024 23:19:59 GMT  
		Size: 11.4 KB (11427 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:saintnectaire` - linux; riscv64

```console
$ docker pull traefik@sha256:53ff7efd91626380fce8ae6f69ef6d1f8b1eee3fa87a2c72ad5d7c50a0e4fee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50068171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8410c363d3fe168a937f88c2339bbccb5cf75f13c41334d69e56e44ef869570a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 14:47:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 16 Dec 2024 14:47:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.0-rc1/traefik_v3.3.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 16 Dec 2024 14:47:55 GMT
COPY entrypoint.sh / # buildkit
# Mon, 16 Dec 2024 14:47:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Dec 2024 14:47:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Dec 2024 14:47:55 GMT
CMD ["traefik"]
# Mon, 16 Dec 2024 14:47:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9864328760025978421ee21682a648061ab9574b8a21ad93338990a16f5f27`  
		Last Modified: Tue, 10 Dec 2024 20:33:20 GMT  
		Size: 462.0 KB (462035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4407abd86570b7be1e2a25cedda9a838b55daea3756114e5855c67ed770c6bfe`  
		Last Modified: Mon, 16 Dec 2024 17:34:38 GMT  
		Size: 46.3 MB (46251744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8b084cee52195105ca77b0fac9e171375fca8e5fe5372de706f981687cd657`  
		Last Modified: Mon, 16 Dec 2024 17:34:31 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:9f1b6557b00934cd77d34e3a3591329d72a22857c8985f4a660e0945f740b864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **832.0 KB (832018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36bd0114763ebd68f520245260bb14dcdbefb62f4756fa30b98fc800ccc6619`

```dockerfile
```

-	Layers:
	-	`sha256:db4fce594f70a7f51df5e91df65f9089883047e1f066cd55561c2e6a902f671d`  
		Last Modified: Mon, 16 Dec 2024 17:34:32 GMT  
		Size: 820.6 KB (820591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b24c9b1e1f1ca4f0a9b4dd803444557988d45460cb59fa72d738babb97110208`  
		Last Modified: Mon, 16 Dec 2024 17:34:31 GMT  
		Size: 11.4 KB (11427 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:saintnectaire` - linux; s390x

```console
$ docker pull traefik@sha256:60488b0e84968da6965731e5e7dd58ba8457c6940de65668c0f7871151cc246c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50423393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4cf8e30063842c16f7d633555f254e8f7a08df0b190c021755559b5a5604397`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 20 Dec 2024 11:05:54 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 20 Dec 2024 11:05:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.0-rc2/traefik_v3.3.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 20 Dec 2024 11:05:54 GMT
COPY entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 11:05:54 GMT
EXPOSE map[80/tcp:{}]
# Fri, 20 Dec 2024 11:05:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 11:05:54 GMT
CMD ["traefik"]
# Fri, 20 Dec 2024 11:05:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb6169870253f9ab8474b704a4354969efb86461ccf96e01c840e72f9d0bdf5`  
		Last Modified: Tue, 10 Dec 2024 21:11:13 GMT  
		Size: 462.9 KB (462867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6595d482dc841c25f0ea96b335f1835a5856f48f2e8523011a116372718c162d`  
		Last Modified: Fri, 20 Dec 2024 23:31:50 GMT  
		Size: 46.5 MB (46490637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7765a9ef2b955512d867839c9c4612f3669488861b0da2bdfa1bf88b8e02a5a9`  
		Last Modified: Fri, 20 Dec 2024 23:31:49 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:cc36df3a49b8e8910394c58c65890e283ccb88215949901e065ef72ec6643758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **834.4 KB (834380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff77b5a71b9dda6603163620cc86f4021b509716f0fb780ce50f4ec95ff2cd2`

```dockerfile
```

-	Layers:
	-	`sha256:3383b863d92793041afc33a7e17ddafdb496e1c9bee4f8ce09f89259adabbe83`  
		Last Modified: Fri, 20 Dec 2024 23:31:49 GMT  
		Size: 823.0 KB (822993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37d31a9b15aa4e46d3c41ce03cbd61ec178a06d719d0ab574ed37b89600acfcc`  
		Last Modified: Fri, 20 Dec 2024 23:31:49 GMT  
		Size: 11.4 KB (11387 bytes)  
		MIME: application/vnd.in-toto+json
