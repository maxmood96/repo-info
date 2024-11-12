## `traefik:comte`

```console
$ docker pull traefik@sha256:00369e02b17f0c1840d0c079482efe70badf4ec86e2af991341602965bd18cc2
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

### `traefik:comte` - linux; amd64

```console
$ docker pull traefik@sha256:8516638b18e67e999d293e4ff0e5baf7807674cd4bdd3d36d448497bcbf0a174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50047093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075808f3fdf72baa7b647b63631bf5fee7d143164049ebfc40a54d9f238d4b83`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 11:30:45 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 28 Oct 2024 11:30:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.7/traefik_v3.1.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 28 Oct 2024 11:30:45 GMT
COPY entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 11:30:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 28 Oct 2024 11:30:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 11:30:45 GMT
CMD ["traefik"]
# Mon, 28 Oct 2024 11:30:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bc362d948388693ee47491e72d0326beb3a518bc4536448a4e5b700f1dae12`  
		Last Modified: Tue, 12 Nov 2024 02:11:23 GMT  
		Size: 455.1 KB (455121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e42f1fa21f11615413fc1f88728488444a06e9c34c9b5335e6235b321d659f3`  
		Last Modified: Tue, 12 Nov 2024 02:11:25 GMT  
		Size: 46.0 MB (45967698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2dc5ed6642565fddf74a63c385c0a92b8145bf788d1e5ada3734f7dc17bcfa`  
		Last Modified: Tue, 12 Nov 2024 02:11:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:comte` - unknown; unknown

```console
$ docker pull traefik@sha256:1e29d286a370444b1a0755d469a81e631dd79bdb2c5983f861273585b9c52747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **817.0 KB (816993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16ca3857922eb80f23f3863439c6e6baf68cd0def1ce5fc158893d00cf8f6c2`

```dockerfile
```

-	Layers:
	-	`sha256:bcaabc15990f6b14176a95e22c0c49e922ff647ed0257333f6f24f82b5fee60e`  
		Last Modified: Tue, 12 Nov 2024 02:11:23 GMT  
		Size: 805.1 KB (805072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7322488b112823b8ce31a410f71f3e99b8c0cc95f08340a2d9b53d71a59405b2`  
		Last Modified: Tue, 12 Nov 2024 02:11:23 GMT  
		Size: 11.9 KB (11921 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:comte` - linux; arm variant v6

```console
$ docker pull traefik@sha256:48a454d4a2ab9849937bb20c6d4db10cdba1df87c4f0b75f8ad8e9817b3f7b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46810316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c553ae85a40510a9ae3f1116857079d38acc6699e3fc22dc52cc82988834ac93`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 11:30:45 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 28 Oct 2024 11:30:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.7/traefik_v3.1.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 28 Oct 2024 11:30:45 GMT
COPY entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 11:30:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 28 Oct 2024 11:30:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 11:30:45 GMT
CMD ["traefik"]
# Mon, 28 Oct 2024 11:30:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abc2658b70735f2744c27b0ba22eb61aaa318147f9377f902c5caafcfa0e0b4`  
		Last Modified: Tue, 12 Nov 2024 06:29:42 GMT  
		Size: 456.0 KB (456028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398a8bf707f3d578bff37f7410ece1d6cfe8436561dfb87762db09afd8757d57`  
		Last Modified: Tue, 12 Nov 2024 06:30:15 GMT  
		Size: 43.0 MB (42987322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938a951469e9e89ab01b24be922d42e992ef5b4208d88cbfd2697b9cffa63c1c`  
		Last Modified: Tue, 12 Nov 2024 06:30:14 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:comte` - unknown; unknown

```console
$ docker pull traefik@sha256:0b68ac5c374e1eb09dd35178cc6a83d8127044a1da723b9a1b6a155aef4db704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 KB (11803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1deb38911e20520ca7b1e166227ba1b17ed4d2eb091553f05e4c6d211c4bf02`

```dockerfile
```

-	Layers:
	-	`sha256:019a23925164bb10da7178b2c4b3a823833b0b167f9fc0135fa2035bb3f52adb`  
		Last Modified: Tue, 12 Nov 2024 06:30:14 GMT  
		Size: 11.8 KB (11803 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:comte` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:90ce342d40474dd93f899ea615d235da2eb41e344b7656e9f08d5ef2822c3372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47134901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3030c10a72b32442b164cce6551a7df32c8d2612b679049005725dc7eca6fddc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 11:30:45 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 28 Oct 2024 11:30:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.7/traefik_v3.1.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 28 Oct 2024 11:30:45 GMT
COPY entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 11:30:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 28 Oct 2024 11:30:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 11:30:45 GMT
CMD ["traefik"]
# Mon, 28 Oct 2024 11:30:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd28039cf42b0f64f7e54f78d9ab70163308c6065494ce3c3b94933d8056566`  
		Last Modified: Mon, 28 Oct 2024 17:57:01 GMT  
		Size: 457.5 KB (457469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c976a5d29d51eaf659637b867cd00c52176f1ec913412cab88695479893d83d`  
		Last Modified: Mon, 28 Oct 2024 17:57:47 GMT  
		Size: 42.6 MB (42589417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12863da8cdfa301981863fde273568896f57c23219bcff219968e1ddf633d5ab`  
		Last Modified: Mon, 28 Oct 2024 17:57:45 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:comte` - unknown; unknown

```console
$ docker pull traefik@sha256:ca6df488849f3e28a7ce3c99e6689174164aff632e394aef56e04353d1dd5bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **817.0 KB (816987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734f9fa9522be2c2cdd71e91126a17f6ec426eac03b540435206426f8f46aedf`

```dockerfile
```

-	Layers:
	-	`sha256:3d645e628ba02fb8964f1aec699db35f0a11344755cf4c93d055fd50f6436091`  
		Last Modified: Mon, 28 Oct 2024 17:57:45 GMT  
		Size: 805.1 KB (805140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51d53ae739662dde3de0852efea298678a5959305c5e581d5dc8d968546a4c7`  
		Last Modified: Mon, 28 Oct 2024 17:57:45 GMT  
		Size: 11.8 KB (11847 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:comte` - linux; ppc64le

```console
$ docker pull traefik@sha256:505ea3ecd7f2434aa46fe130e4d9fcffec391141b08f1925e980b0c0a0189c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45154418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febd20380361cdea283551e2bc5ace705f89a6b9b630e3f9b0c21b60073e15ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 11:30:45 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 28 Oct 2024 11:30:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.7/traefik_v3.1.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 28 Oct 2024 11:30:45 GMT
COPY entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 11:30:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 28 Oct 2024 11:30:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 11:30:45 GMT
CMD ["traefik"]
# Mon, 28 Oct 2024 11:30:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7344dfd024f1a54ee674177a4c7c77f21bca6f5d0d59c0709c1ec0da6571fe8b`  
		Last Modified: Mon, 28 Oct 2024 17:57:13 GMT  
		Size: 457.9 KB (457876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3553e59a802067848d9ac62bfeb98c81a8aaebc15e75290ed0671a2becba1a8e`  
		Last Modified: Mon, 28 Oct 2024 17:58:18 GMT  
		Size: 41.1 MB (41123755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555a501e6be753e9b9e8e58a5d3594972d7515cdf3e84cdfb712fdaa3945ef1f`  
		Last Modified: Mon, 28 Oct 2024 17:58:13 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:comte` - unknown; unknown

```console
$ docker pull traefik@sha256:225d4bf5d8a538e37e8afe76b8f9f5661d2c42fb7ae181edd51c5411dbfb03ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **814.9 KB (814926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26cf2ac5df827ea9514a20420d41546b8e37151a88f3f98de389af3f3041eb5`

```dockerfile
```

-	Layers:
	-	`sha256:5de8bcf165475228031a1a1425c4f1f10685ae5594d86007c1b9fbbdaa643099`  
		Last Modified: Mon, 28 Oct 2024 17:58:13 GMT  
		Size: 803.2 KB (803158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:225f76624cc06118ec054c931f242ea42d4670e738eb71f6fae11bc170694483`  
		Last Modified: Mon, 28 Oct 2024 17:58:13 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:comte` - linux; riscv64

```console
$ docker pull traefik@sha256:52f687a2a31f2a03f3cc0599176cc9c11ee58878939ce8fd97b57e9f82138ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48039004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef2a2e875aa242a1b28cf09e2e555cdedfbead5f00de1000fefd78b604a1c99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 11:30:45 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 28 Oct 2024 11:30:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.7/traefik_v3.1.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 28 Oct 2024 11:30:45 GMT
COPY entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 11:30:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 28 Oct 2024 11:30:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 11:30:45 GMT
CMD ["traefik"]
# Mon, 28 Oct 2024 11:30:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9782d9bb651b7b80a5b6dc6b8aa5e197330e400020c92b9e4ba59c8dccfb52`  
		Last Modified: Sun, 08 Sep 2024 17:42:04 GMT  
		Size: 455.9 KB (455888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b291e245efc1fecd8143e5486f9c017042c764b5ce7c9bb7b97e23ebddaece7f`  
		Last Modified: Mon, 28 Oct 2024 18:08:28 GMT  
		Size: 44.2 MB (44211294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf27310800c75dd4039f37834da2f520b246460b7cc32b88cd27e9b7251ac35`  
		Last Modified: Mon, 28 Oct 2024 18:08:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:comte` - unknown; unknown

```console
$ docker pull traefik@sha256:877108c3a1f47e8ad4e69b0539936a4f94d04aab9739a065be08fd2337152e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **814.9 KB (814922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f67f5b2dc59a6477ab8a1db25ba3ba0a954f56f24fe2e32eaa46baf98e9fd9`

```dockerfile
```

-	Layers:
	-	`sha256:e97fa3dc16b42f5e82d0954f7a3f3bb77dfef27fa52281b9658737f4fd95f1e1`  
		Last Modified: Mon, 28 Oct 2024 18:08:22 GMT  
		Size: 803.2 KB (803154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6c28e7ff34006bd3aad069857d8a918f66327f01d754bda4040a1cae9f32445`  
		Last Modified: Mon, 28 Oct 2024 18:08:21 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:comte` - linux; s390x

```console
$ docker pull traefik@sha256:eed37ac983e9d6f9b398854bc12c42bb865a36d1b042c46b6074dde9cd69fa6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48432234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a772372b00d341e871a8c89d14997241ba3771139e6c49ef43555dbc4a0c3f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 11:30:45 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 28 Oct 2024 11:30:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.7/traefik_v3.1.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 28 Oct 2024 11:30:45 GMT
COPY entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 11:30:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 28 Oct 2024 11:30:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 11:30:45 GMT
CMD ["traefik"]
# Mon, 28 Oct 2024 11:30:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559f652fd9a9f8a3a6d224500921f75ec5d4a02e5b286f03b3e0117bcd1ad7ac`  
		Last Modified: Mon, 28 Oct 2024 17:58:27 GMT  
		Size: 456.1 KB (456130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d5d71d785efafaa7b49e7244192e0cd54972d8453a650c26d1ff65876bcb2c`  
		Last Modified: Mon, 28 Oct 2024 18:00:39 GMT  
		Size: 44.5 MB (44514137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b58239d5b7a967630561675edef7ee04edf3fb0e43272b5f0e9e8ce647c318`  
		Last Modified: Mon, 28 Oct 2024 18:00:38 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:comte` - unknown; unknown

```console
$ docker pull traefik@sha256:bfc92d25b4fdfa0b96cff37cea8262c609fc57548ce44941960533b51f2474f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **814.8 KB (814840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84212133c54aa33f64cd396731b3548f4acb3bad6d3b36aef689fd1011e9e0d5`

```dockerfile
```

-	Layers:
	-	`sha256:9d008cb2c84c108c20ade0b6062c816d694d77830903aabd8c4e3818e5ec6dc9`  
		Last Modified: Mon, 28 Oct 2024 18:00:38 GMT  
		Size: 803.1 KB (803118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e846b3936ca648b0457780de69471db5977c80d40d19913ed39c655d42bcff7`  
		Last Modified: Mon, 28 Oct 2024 18:00:38 GMT  
		Size: 11.7 KB (11722 bytes)  
		MIME: application/vnd.in-toto+json
