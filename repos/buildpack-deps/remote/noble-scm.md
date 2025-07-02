## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:d4718da465064c99294ce629318c18fcc8d97a87dcceadd4c04255dd352a2c76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:noble-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c1e6806c1d1bd2c4245286e71e8530c473cc6b012dd26838ef39646af95d6850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88729756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2af433422337714b59f8420f8267826573e7003e71a9e3f261cce29a2fa4429`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fdbabbfc2d2357c11d06b94c29d86f9283ba38506222a230cfe31c410f7d61`  
		Last Modified: Wed, 02 Jul 2025 03:09:59 GMT  
		Size: 13.6 MB (13621201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743668f722e37fbf61a19f14a10a6cd8fa02930295eba1e6fcc7c625738ad375`  
		Last Modified: Wed, 02 Jul 2025 04:11:45 GMT  
		Size: 45.4 MB (45390189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7d52fc94b21d1f795daa209f0e554770bbcd87bef397c64e7780c4d0dd903889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89673dfd0c4de0d1fbf3b3dbc5c825864dea085c47f41bbf8998b3b7a86613dd`

```dockerfile
```

-	Layers:
	-	`sha256:a281b77bdac84d95710d43b9bd898f2a1653ae4c237c324cc97903adbdc5ef12`  
		Last Modified: Wed, 02 Jul 2025 07:19:58 GMT  
		Size: 5.3 MB (5274548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d02b584b7d2538b32a33016788da5ec6a5a96355e3d8b6f2b61574db1159816`  
		Last Modified: Wed, 02 Jul 2025 07:19:58 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:dbaab5c406d33f9bcfd5d53541ca7a349b29adbf78eaded3d633a0e653894df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88490262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af322ff335fcae7921d3fde09f4867779631119b0f8aa976a4671e886a5d7cb4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:88b7ca184cec1707b10b6b543ddfa7abfcacc2605cdd5919877294ff5290aa3e in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:149362fdfa6e6a5d9f009b896da3be3172c395ba2287b57d4969f3f46e573055`  
		Last Modified: Fri, 20 Jun 2025 10:02:42 GMT  
		Size: 26.8 MB (26844462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1d9f8310665c797125d138ed753e806103dae0482e1526f2b5e096604fad68`  
		Last Modified: Wed, 02 Jul 2025 10:21:22 GMT  
		Size: 12.8 MB (12780426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e84727bd3386a9d424abaef39047f5659957d0a5ae0dd3fbf45a2876550c29`  
		Last Modified: Wed, 02 Jul 2025 11:11:08 GMT  
		Size: 48.9 MB (48865374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d5326d0e33dbdb2af06239764137b048a418d959b79f9380fcca4800dad82799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5283211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d616cbaaf7b64b59a0f28f21bd02edcbcea4f7625f2c64cd6452a040f4046285`

```dockerfile
```

-	Layers:
	-	`sha256:05bd26d1b5a349fd781d0671a2b260a8e5b0ca9a67030fdeb4c14f3eb3964d00`  
		Last Modified: Wed, 02 Jul 2025 13:19:48 GMT  
		Size: 5.3 MB (5275846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a1582d55f52e81bb1405af6068e7459bfe9e5ada3b31675ff50e1f21c7ce6c`  
		Last Modified: Wed, 02 Jul 2025 13:19:49 GMT  
		Size: 7.4 KB (7365 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1e6b4128dcca0fb59b1611e7def90121240344f4b07a20849cc6b2bc3a1cdb78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87619077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2f25b56e191554317302a593d69fce4ac88f41831d0686d9f8fe042a12ae5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b66004928f8c394a026eb75e60764cdc2913b001d64b1a1688836d025824ec3`  
		Last Modified: Wed, 02 Jul 2025 04:19:26 GMT  
		Size: 13.5 MB (13456044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbfc9c385f102b13831ee3af48899ea04e4a2d1d5abef9aa8665d6d4c16ee10`  
		Last Modified: Wed, 02 Jul 2025 07:37:27 GMT  
		Size: 45.3 MB (45307015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6cbeec71206d310e30154b7462eadbeb10aa22d9a6967f4763720de25d4e8c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ee44de63df659458c986b2bbb218ec6f1f59dbd266e796cc2e8136c5746fc9`

```dockerfile
```

-	Layers:
	-	`sha256:f022f6b975317b9eaee0442e35c1983b5eb0b6cd17974891ef794ca7fa060838`  
		Last Modified: Wed, 02 Jul 2025 10:19:46 GMT  
		Size: 5.3 MB (5281740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29edab4c6bfe96f425981240cb8917aaf97c5fea29161b7c5a1722125bef2ed9`  
		Last Modified: Wed, 02 Jul 2025 10:19:46 GMT  
		Size: 7.4 KB (7385 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:95ab081574c6881ff494539b935a2acc770feb00d84d7167d8ff700a972a7a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100690920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1434e97abba92cd917b4a6796953ac323a1f3568dcd446978c25aef5344d754b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22221e46c866dbeb7893d2cb7aad53cba8ff901b321833a29ce219ca59c94224`  
		Last Modified: Wed, 02 Jul 2025 03:10:27 GMT  
		Size: 16.0 MB (15954131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c4107c0e0b1ffc9509be350498b215c9d27502e32c6baf9993f75d87a22a7e`  
		Last Modified: Wed, 02 Jul 2025 05:11:23 GMT  
		Size: 50.4 MB (50415283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0c8f2556848c7284831e70c94fd60866fece59579b38c28bc382a744be437262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b7ff21bd2cfca49e49b7c3af55ff63fc9af8296f54d003491dfa6aec1d82d4`

```dockerfile
```

-	Layers:
	-	`sha256:2319ac6c560086bd10284e4fd349802b96c987bc07f1450237e2e71742891584`  
		Last Modified: Wed, 02 Jul 2025 07:20:16 GMT  
		Size: 5.3 MB (5282402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fdc025e16cb8eeb48f49749d25e2aa976b3832fc353f76bdf17591f84410e3b`  
		Last Modified: Wed, 02 Jul 2025 07:20:17 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:893c6bdd8de9b7019ba5f818ca1897fc18bb74c480d03702286bdacec33943c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99124099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5b3380060297cf178500bbb80bf7b4eb5b363f9f74f935c29f4c9c3a711c5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:202c5a7a84e813495c089800398f2ba18952221717db2c10e042ce4179ee6fc0 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4ccdff8fdb11e14b8e0dab6804aeebce5855635c68b20f199dcf0efcd9b4c462`  
		Last Modified: Wed, 02 Jul 2025 01:17:14 GMT  
		Size: 31.0 MB (30951024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ce57c66749f825da8658484f946ccac9fb912f45d0ce0e0acba90acfe400d8`  
		Last Modified: Wed, 02 Jul 2025 03:14:22 GMT  
		Size: 14.3 MB (14328100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bf6f7c3bc8228ad88b0e4bae7134d543b54568474048b9f5886b7f1bf2b0c2`  
		Last Modified: Wed, 02 Jul 2025 06:28:10 GMT  
		Size: 53.8 MB (53844975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:25d8131211eb5642897078f51be49ddf423b147796dfd82c60a6023876598ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb44fd9a422be80c47989fb75aec391e10faee7d54f5e712320335d331c3a6d`

```dockerfile
```

-	Layers:
	-	`sha256:752182687054002aa114908c7b8c8d59d4d7a48faef82cb499a068074e467b8c`  
		Last Modified: Wed, 02 Jul 2025 07:20:21 GMT  
		Size: 5.3 MB (5264944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0bbbf348e9f263b486d5c7ece185890fb27e5560fbd48085b184d9ee059a49`  
		Last Modified: Wed, 02 Jul 2025 07:20:22 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:aee4130fe6fcc07606d00e911924cb145902dff54c451f0cf9b9c05dd1c31e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91638444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b11a7419523c9a264f7af9c68828dadb803dd34244383b0e4d92325694ec75a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:80b0b0c2a08a762cf6a520d8428a5c769c29e72f4a51630adb2231f2816c50c4 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:30d64ca13d9d94eb48bf3fece3e38a4e60931d72f1a8c633dec981e43a0515a4`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 29.9 MB (29925630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0a7472d36ac954b6ad8ae016bc95c96fed55c2a6dff7a2277fb2905ea71cd5`  
		Last Modified: Wed, 02 Jul 2025 04:13:00 GMT  
		Size: 14.9 MB (14938086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006872a7d3dfbb370d9b9ad9f173b1cff4ec2ed138890295c7fcf7af3bc38370`  
		Last Modified: Wed, 02 Jul 2025 05:18:26 GMT  
		Size: 46.8 MB (46774728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:de74e1c2af5588de7809ceab435261f5790e2153119dd8001020351a6d57559c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5284184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21e9f4d5ecc4e627c79d615e2522e73b8d2011e5d13470bdf11a1d1a397610f`

```dockerfile
```

-	Layers:
	-	`sha256:8339ab8a3a4cb05fd62c07d91e9074a26dbc45ca091cf54e8a779d3c5290ff9d`  
		Last Modified: Wed, 02 Jul 2025 07:20:27 GMT  
		Size: 5.3 MB (5276880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:931fe954a8e59d4570dc07aa25bef9ae86c01539346f3b18f4eb3baac3dc4a57`  
		Last Modified: Wed, 02 Jul 2025 07:20:28 GMT  
		Size: 7.3 KB (7304 bytes)  
		MIME: application/vnd.in-toto+json
