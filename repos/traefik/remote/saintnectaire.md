## `traefik:saintnectaire`

```console
$ docker pull traefik@sha256:baf1453551f7591b18bf418548de1197355a51b5d99748892e18bcdc7882bf74
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
$ docker pull traefik@sha256:5809533c5b3fdfd961aa20af1cfbbc7d0e8ce3c4c3b1ee9acb0da00b7871c53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58265978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1e150bf4c5610ac288b87c5e42e9ddc514e72b7ecdc43bde4776bda41edbc9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 09:28:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 18 Apr 2025 09:28:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.6/traefik_v3.3.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 18 Apr 2025 09:28:25 GMT
COPY entrypoint.sh / # buildkit
# Fri, 18 Apr 2025 09:28:25 GMT
EXPOSE map[80/tcp:{}]
# Fri, 18 Apr 2025 09:28:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 09:28:25 GMT
CMD ["traefik"]
# Fri, 18 Apr 2025 09:28:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d25ded108050aa875a5af7cbca2d83323dd64c0b272ad91d619202869c89adc`  
		Last Modified: Fri, 18 Apr 2025 13:59:51 GMT  
		Size: 460.2 KB (460208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30110bda10635a550383aa97f87314c0e20928ce15e7e21aad9bbd2b6c8d5d23`  
		Last Modified: Fri, 18 Apr 2025 13:59:52 GMT  
		Size: 54.2 MB (54163154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d79802b571c42930afa7bc01ccff9523fba04e653b74f20bd0a3e6693982807`  
		Last Modified: Fri, 18 Apr 2025 13:59:51 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:5324e68ce35987ccc478c709ff94da9c96d631f30db7f3f50ba5f3c076faf4eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.5 KB (838508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7007595ecd63d0f1a9b8c4f27dc77297bedd6765143c095c605bd0751f24239`

```dockerfile
```

-	Layers:
	-	`sha256:8675464bdebc76dfa1718beff59b37db8318ec617fc1b353f2e83c0c26e08fcb`  
		Last Modified: Fri, 18 Apr 2025 13:59:51 GMT  
		Size: 825.7 KB (825689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f267dcad7389cc9c7ee182014d97a8e337304c54641055da539a9eb4bfe1185`  
		Last Modified: Fri, 18 Apr 2025 13:59:51 GMT  
		Size: 12.8 KB (12819 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:saintnectaire` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ad82f5eded2146173eeabce51f95ed3c117f832c7b8a5c3a97d5ff5c05cccaaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53666107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6170b0776eb68ad316624ac8209906069b7a9660c3e9c4912711f9598d04502`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 05 May 2025 08:53:41 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 05 May 2025 08:53:41 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.7/traefik_v3.3.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 05 May 2025 08:53:41 GMT
COPY entrypoint.sh / # buildkit
# Mon, 05 May 2025 08:53:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 05 May 2025 08:53:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 05 May 2025 08:53:41 GMT
CMD ["traefik"]
# Mon, 05 May 2025 08:53:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f151b7863e2fb434ea3dcaca468a02986e2de68b280fc64073e5a41a84fd087`  
		Last Modified: Fri, 14 Feb 2025 22:10:21 GMT  
		Size: 459.4 KB (459424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ca0e5f85e85ce8d09d805a3a81e82e71d47379a289bc083b1f80746c8ae07e`  
		Last Modified: Mon, 05 May 2025 17:22:29 GMT  
		Size: 49.8 MB (49841584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36400b36662ec065e91dc040b1f9ad605c8749707cf43f4c5b61691bfb3b8f47`  
		Last Modified: Mon, 05 May 2025 17:22:27 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:82f502ba320ee4bb8d6f0e95131b1c1392e3464ff2f19373439ec37563870f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 KB (11819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82409393c99f46cdb859bfd6d9155216a8f3c9679f13f010aab5eea67d52ef70`

```dockerfile
```

-	Layers:
	-	`sha256:94e97615dded7a4806bcdc2f04be5f8413f7a44f7f097e638a87e2a02aea1ead`  
		Last Modified: Mon, 05 May 2025 17:22:27 GMT  
		Size: 11.8 KB (11819 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:saintnectaire` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:2393433ae917804739c08081d64399efd3b596d76f9b006a7e91424e28c11c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54448882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f80de43fbfef0ace6ad5e3f670ceb6818d2d346f87ddcb59680c1e42f025cf2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 09:28:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 18 Apr 2025 09:28:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.6/traefik_v3.3.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 18 Apr 2025 09:28:25 GMT
COPY entrypoint.sh / # buildkit
# Fri, 18 Apr 2025 09:28:25 GMT
EXPOSE map[80/tcp:{}]
# Fri, 18 Apr 2025 09:28:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 09:28:25 GMT
CMD ["traefik"]
# Fri, 18 Apr 2025 09:28:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5767a026dafabae556cd462be7925c367eda59c781152c498b6703f4aed3f2b8`  
		Last Modified: Fri, 18 Apr 2025 13:59:56 GMT  
		Size: 462.1 KB (462068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442e8ef1858cc11a87bf0c901c7326137263bf45324071ee91e3af8b8422b0f3`  
		Last Modified: Fri, 18 Apr 2025 14:00:46 GMT  
		Size: 50.0 MB (49993416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9867893076682e52b7054988a5ebe3031fb4b357f9fc945567fa6796c5de6ab7`  
		Last Modified: Fri, 18 Apr 2025 14:00:39 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:d07fc755d507c2739d881445d8aa85ca42a38d7a218905bada50b92d342fd2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.8 KB (838779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a5f99f91c439ee5836c926e36f9f2bfef389e1220f7986b9ea9e63f7b5f7d6`

```dockerfile
```

-	Layers:
	-	`sha256:067993f64567bee54112c7fbead35a58a11bda281657c22c2cc88034a02c821a`  
		Last Modified: Fri, 18 Apr 2025 14:00:39 GMT  
		Size: 825.8 KB (825793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f171748f41630d8eb10fee57e5a12eebe0e32ec304fb9448ace2b3278b9a9441`  
		Last Modified: Fri, 18 Apr 2025 14:00:39 GMT  
		Size: 13.0 KB (12986 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:saintnectaire` - linux; ppc64le

```console
$ docker pull traefik@sha256:906022050aed05c8f35862bb95f747f855c6967738982e7bb45d17ccb3aff4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51767394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b2b2e9ac5ad99a67557f069af77874e084cfdf1ba6234ab14c36ce35e7bdb7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 09:28:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 18 Apr 2025 09:28:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.6/traefik_v3.3.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 18 Apr 2025 09:28:25 GMT
COPY entrypoint.sh / # buildkit
# Fri, 18 Apr 2025 09:28:25 GMT
EXPOSE map[80/tcp:{}]
# Fri, 18 Apr 2025 09:28:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 09:28:25 GMT
CMD ["traefik"]
# Fri, 18 Apr 2025 09:28:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e071b328b50063f749f347ba8d94858140ac210384e481fbb657c3ed08fa7`  
		Last Modified: Fri, 18 Apr 2025 14:00:22 GMT  
		Size: 462.6 KB (462561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea7684060bf91b2bd314945d00c26ac00e2f99323ab34d13d6256e1712fcdcf`  
		Last Modified: Fri, 18 Apr 2025 14:01:52 GMT  
		Size: 47.7 MB (47730119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9042f3b7c59473e10585a23ce819095d52d1e258fac976fd427f84ca53939c52`  
		Last Modified: Fri, 18 Apr 2025 14:01:50 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:3ea74f7a1c1898ac9883d7e3d32fe278fea13a0d1281a4cd75a58ef17c52e4f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **836.7 KB (836683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5c84877c75bccb87c1592dfb21e72bad85a112a30674770a136b8c16617e65`

```dockerfile
```

-	Layers:
	-	`sha256:4adace20a5e3690272145f2878395ec69274323343a98e99cd927a3cc8abafac`  
		Last Modified: Fri, 18 Apr 2025 14:01:50 GMT  
		Size: 823.8 KB (823796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c88b1d34f30136021a471386cd7ba4fa0b155927607521dcc5eb4f86a251b15`  
		Last Modified: Fri, 18 Apr 2025 14:01:50 GMT  
		Size: 12.9 KB (12887 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:saintnectaire` - linux; riscv64

```console
$ docker pull traefik@sha256:47cafc0a3ea1aacf3dfc83148d8e865ef263e9dde9d74aef67f515ccfaabc33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56442749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922a5d450319ba06caab4c7afc64f4f394b332a3620875867c6353bba3aec93b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 09:28:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 18 Apr 2025 09:28:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.6/traefik_v3.3.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 18 Apr 2025 09:28:25 GMT
COPY entrypoint.sh / # buildkit
# Fri, 18 Apr 2025 09:28:25 GMT
EXPOSE map[80/tcp:{}]
# Fri, 18 Apr 2025 09:28:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 09:28:25 GMT
CMD ["traefik"]
# Fri, 18 Apr 2025 09:28:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786ed68a7bdb8d6cbb892f36c5788bd24eade8a9ab923e332fadb031b5c122a5`  
		Last Modified: Fri, 18 Apr 2025 14:06:56 GMT  
		Size: 460.5 KB (460548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d348c282518511d1d770755cf7c4915fa0bfa627e2e0d51d9c0ded776fea04`  
		Last Modified: Fri, 18 Apr 2025 14:14:27 GMT  
		Size: 52.6 MB (52630393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5870e89e21e0c186d7355a7e9dccbf4671c28d313a828edc02996e7f1e123668`  
		Last Modified: Fri, 18 Apr 2025 14:14:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:efa7403bbde9e3ea1b8f40e23c2263552f29029ceccf6b240025469c615d5864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **836.7 KB (836681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225dd7dc9d3a93bb2f119670faaf9e49d84f2b0de81ee448bee3a763ae84465a`

```dockerfile
```

-	Layers:
	-	`sha256:568c62871c82728b16b6469dd991b995a4f93801c530262e8b8a3b1a971de4d4`  
		Last Modified: Fri, 18 Apr 2025 14:14:20 GMT  
		Size: 823.8 KB (823792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f67e79774cbafaca78221f14adab3eb0131e0ffce5fab8fd3379ddef087dd5fe`  
		Last Modified: Fri, 18 Apr 2025 14:14:20 GMT  
		Size: 12.9 KB (12889 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:saintnectaire` - linux; s390x

```console
$ docker pull traefik@sha256:8190ef42233575cd52b59c889f1c678246ee0dc695053be0794cde85d841035b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56231656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93001d74f4b02ac2c8953583777c07fe4712258c5e2fcdd61e9054a1d8be270e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 05 May 2025 08:53:41 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 05 May 2025 08:53:41 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.7/traefik_v3.3.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 05 May 2025 08:53:41 GMT
COPY entrypoint.sh / # buildkit
# Mon, 05 May 2025 08:53:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 05 May 2025 08:53:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 05 May 2025 08:53:41 GMT
CMD ["traefik"]
# Mon, 05 May 2025 08:53:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d59721489ac6dff8b0da7cbb2d4407a68304471beb9fb1e92380ca152f5160`  
		Last Modified: Mon, 05 May 2025 17:46:08 GMT  
		Size: 461.2 KB (461153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9079e1a281c552e61560a3c97f28920794dd4d960a844e9328fc637397020ac`  
		Last Modified: Mon, 05 May 2025 17:47:17 GMT  
		Size: 52.3 MB (52302567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d60cd42227afc989b967feec18a36ec4861e49d9ef73a1b01d81972e1aaacaa`  
		Last Modified: Mon, 05 May 2025 17:47:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:25a1a7f2a2bc0bf4bc233c40535da8f7e61afe1d5470d76d7cb73e0f62b0afa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **834.8 KB (834793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa829f99ed36d5d88576100802ac239a49d7321a6e61841d4c59fae7ae2c9c12`

```dockerfile
```

-	Layers:
	-	`sha256:2a97deae364c766e7eb04e90de0ae53169cfa889e61ddb8a694a2435cea9dbcf`  
		Last Modified: Mon, 05 May 2025 17:47:16 GMT  
		Size: 822.9 KB (822856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:732bb005937c6c6e63a662900d0ebf8e896c20cb9a2fe4c5e05c28851df71baa`  
		Last Modified: Mon, 05 May 2025 17:47:16 GMT  
		Size: 11.9 KB (11937 bytes)  
		MIME: application/vnd.in-toto+json
