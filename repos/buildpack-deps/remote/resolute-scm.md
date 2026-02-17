## `buildpack-deps:resolute-scm`

```console
$ docker pull buildpack-deps@sha256:709046872cc2a4b37027ce6ec5a4f6b49d0fbdb809cb42b5b3a454429322e5a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:resolute-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8d55f7cffdb648d8d1e993040cb156354820ac9e1557a17dee89af77a4a17255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107462613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c10e17fb45b92741386f49ea7d2099d12845c0e1b9e6e57e49ff46619c0694`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 21 Jan 2026 02:04:52 GMT
ARG RELEASE
# Wed, 21 Jan 2026 02:04:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 Jan 2026 02:04:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 Jan 2026 02:04:52 GMT
LABEL org.opencontainers.image.version=26.04
# Wed, 21 Jan 2026 02:04:55 GMT
ADD file:5a3b3d88836037412b2e65304a34ae9b8902e2e18f2142a9d7bd31359c280c79 in / 
# Wed, 21 Jan 2026 02:04:55 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 21:16:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3c261c4d22b0eb03c17e9c8acc3b714b4abd96cd3b2435def412cb5367ae9e85`  
		Last Modified: Wed, 21 Jan 2026 02:53:34 GMT  
		Size: 33.7 MB (33675624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55883c6a0c594fbcd6607363867fa967d79095f04962e66e55fc017c45bdf9ec`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 25.5 MB (25540862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7c12cf5baaadcbf588ddfb059911902c7f881b12e3dfcf590fb3253dbbf76a`  
		Last Modified: Tue, 17 Feb 2026 21:16:38 GMT  
		Size: 48.2 MB (48246127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1063cca78a863fd1719174e371906b0b97fe35997b2b468c7993073ae3d17421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7000743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c56488b45beac0eb5618c69881a224366dd838dd3d077e086b95c53a4840915`

```dockerfile
```

-	Layers:
	-	`sha256:0be23b9663bbd9028d21609f5b63cded17a2eec038a3d1b95f57e27f0bb489ba`  
		Last Modified: Tue, 17 Feb 2026 21:16:36 GMT  
		Size: 7.0 MB (6993463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ae048009c3e31eb01e856f6f0a4f625a5c0631cf88bd86a60ad857e1f4b03ae`  
		Last Modified: Tue, 17 Feb 2026 21:16:36 GMT  
		Size: 7.3 KB (7280 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:38f3a4f97a030a6b3723388be1d3d1bd6853f49a69b0730e3fd7caa6709ff630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105190160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8015903a19f27a023e23e8286773fd39ea8036ab37336bd4fdc3059652760339`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 21 Jan 2026 02:05:08 GMT
ARG RELEASE
# Wed, 21 Jan 2026 02:05:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 Jan 2026 02:05:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 Jan 2026 02:05:09 GMT
LABEL org.opencontainers.image.version=26.04
# Wed, 21 Jan 2026 02:05:14 GMT
ADD file:64f8302e71f30ce19eeb546a74e2f2ee518a1401afcf8395ae4cf115f7f4007f in / 
# Wed, 21 Jan 2026 02:05:14 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 21:16:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:340f1c91e91d4fc6dea29a48d805d764635f314ec829f043b408b97d421fefcf`  
		Last Modified: Wed, 21 Jan 2026 02:53:47 GMT  
		Size: 31.2 MB (31166507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fd26212152f3531f73c0efa5d9e16bb1fa6f236b022d20f6d2a2aa31de3742`  
		Last Modified: Tue, 17 Feb 2026 20:11:45 GMT  
		Size: 23.3 MB (23277470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24ad20d12978bce616b4ffed9f3567970ab2a667a2ba6a1d53f2eca93313a5a`  
		Last Modified: Tue, 17 Feb 2026 21:16:44 GMT  
		Size: 50.7 MB (50746183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dbc126931713aff34a539d64b9b7c96a38d078c6bb69d2b3427ab42812473bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7001304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7cf35a151662e7e039143f6b0246230981a2a3bed57556d67afc79c80be6bcb`

```dockerfile
```

-	Layers:
	-	`sha256:6c377e4fb987bf7710e4b11126d99b148c3afd837eb88ba69feddd5e9cc3f187`  
		Last Modified: Tue, 17 Feb 2026 21:16:43 GMT  
		Size: 7.0 MB (6993959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42e08fc97cb3c660f5814e6e7809c60f8a29ba04d3f4156cd8c30d9869a90322`  
		Last Modified: Tue, 17 Feb 2026 21:16:43 GMT  
		Size: 7.3 KB (7345 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:64a31582ac68f978c5966eb6d328f4cfafdb4cf722c8e9292cbe2450813a02e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.2 MB (106230101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7309988d00d558169301d06d3ed41835e2756b6f634fb66d0119af4f3cc397`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 21 Jan 2026 02:06:33 GMT
ARG RELEASE
# Wed, 21 Jan 2026 02:06:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 Jan 2026 02:06:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 Jan 2026 02:06:33 GMT
LABEL org.opencontainers.image.version=26.04
# Wed, 21 Jan 2026 02:06:35 GMT
ADD file:a11224ce0bf3c5f80538743d4c0625b9323c82858600072ca8c1663ae7960103 in / 
# Wed, 21 Jan 2026 02:06:36 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 21:16:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53aec10ada41ffe8ba1d5de5418a311240cc814b8b270a9f91d069cac334f70e`  
		Last Modified: Wed, 21 Jan 2026 02:53:41 GMT  
		Size: 33.2 MB (33228686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900559816bd40c452d3861268a03da469284a99c9639d5aaa515e1c92b085722`  
		Last Modified: Tue, 17 Feb 2026 20:12:12 GMT  
		Size: 25.1 MB (25115471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f14a12aa56df8b0159701e00f2a970d29375c71ccf8a63f858e744a792ff84`  
		Last Modified: Tue, 17 Feb 2026 21:16:37 GMT  
		Size: 47.9 MB (47885944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e8826dc39acf010277c5a63e8b9f46cff1d5c7d3f32d3d984e35fecd7da9bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7007211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4228292eea71c6e250e8090ecf9c8d11f4d6d234212ce4eda01dc5d5525a5a2b`

```dockerfile
```

-	Layers:
	-	`sha256:b7ae4d6ba9dc63e2225bdacc67dd1a49d30ea83b26d6d3df354f0cfdbfc093b6`  
		Last Modified: Tue, 17 Feb 2026 21:16:36 GMT  
		Size: 7.0 MB (6999850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f418f20623ad42bbcf84e6e40f372b475166dc94bba8508721fbb55955399d7`  
		Last Modified: Tue, 17 Feb 2026 21:16:35 GMT  
		Size: 7.4 KB (7361 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8bb4557b9a65cf9ca9a99ff49703d7aa5eb782ad655027d0174ffb57440e17f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121075020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1907837dea6f2c5d4764ac2d4be27b19a2d0d6e0283f8885a845024c8b3df285`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 21 Jan 2026 02:05:01 GMT
ARG RELEASE
# Wed, 21 Jan 2026 02:05:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 Jan 2026 02:05:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 Jan 2026 02:05:02 GMT
LABEL org.opencontainers.image.version=26.04
# Wed, 21 Jan 2026 02:05:05 GMT
ADD file:965035165b5a9607aa8c5bb045af27bc17ad5f8ba33ecbe10426988d7c087ecc in / 
# Wed, 21 Jan 2026 02:05:05 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:13:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 21:45:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b5ed12c0213034851f152051b56017b1e654738743050659fce37a1a1aabcb6e`  
		Last Modified: Wed, 21 Jan 2026 02:53:54 GMT  
		Size: 38.8 MB (38812135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218b035f88d928ca302b9ff3aa9991b0d88cdc1af3c26cf3a2e90174b06d0494`  
		Last Modified: Tue, 17 Feb 2026 20:13:43 GMT  
		Size: 28.3 MB (28317642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf98c8b2a343a74d54a62e9cc6362df8445c47cce3a012b806527aa4d9383c2`  
		Last Modified: Tue, 17 Feb 2026 21:46:52 GMT  
		Size: 53.9 MB (53945243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bbd3ad66889300fe0a7335160443a4c7cb0dd2b7885d4cdb6702d12a72db6bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7007834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414db67b44f7ec372b0f3fdeca3af6d80261d0ca5bb47e4cd2591af8d511cfca`

```dockerfile
```

-	Layers:
	-	`sha256:bb1356b8ec059d929962d1833456f948d158fba45e0cd838d68e6dc19d808481`  
		Last Modified: Tue, 17 Feb 2026 21:46:51 GMT  
		Size: 7.0 MB (7000521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0055df7f324baec24b62d22d1b1227294ecfa38f15f79420a225ec8cb13e416c`  
		Last Modified: Tue, 17 Feb 2026 21:46:50 GMT  
		Size: 7.3 KB (7313 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8b8fb1ecf66755eac281663b2ae8166989a3612f79fe02191eaad9bc26929f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108582478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d5479b38708dfbe7a2815927b8043ddcbe8f9a4b9fa3955ca5704e58dbe63f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 21 Jan 2026 02:05:26 GMT
ARG RELEASE
# Wed, 21 Jan 2026 02:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 Jan 2026 02:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 Jan 2026 02:05:26 GMT
LABEL org.opencontainers.image.version=26.04
# Wed, 21 Jan 2026 02:05:28 GMT
ADD file:a31148f1b2b73c9ddb2dbcb9c6eaf377794bd2a5545e9afc25bfda0d0fc4e29c in / 
# Wed, 21 Jan 2026 02:05:28 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:10:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 21:15:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:880c3ab78503e9d5bd5e9fa7f060185c8b708bbe723e3ff052d6be540d75a79b`  
		Last Modified: Wed, 21 Jan 2026 02:54:08 GMT  
		Size: 33.4 MB (33399085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f623ab4e89aede42d0ac17c3ab466b025e769853ef72fb583d67b2bf772fa96`  
		Last Modified: Tue, 17 Feb 2026 20:11:14 GMT  
		Size: 26.1 MB (26085879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248536fb814edf3e4faf020a543efc6bf472f95f7150cc07072ae3a9b4e79ca4`  
		Last Modified: Tue, 17 Feb 2026 21:15:53 GMT  
		Size: 49.1 MB (49097514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:35655a1b51acb6acf1f12c61e7158e506e30a6bf668af65b6201832df5acc2a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7002282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67d3d0b9e081c42bdaefd5cddef8b5bf5a11a9f4ea5e965fccebfa0446ce5e5`

```dockerfile
```

-	Layers:
	-	`sha256:0e612487869765f96bf021b3023a2ecf2bda0f250c6eec8ca9bb6a408a12501e`  
		Last Modified: Tue, 17 Feb 2026 21:15:53 GMT  
		Size: 7.0 MB (6995001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d86b400626ec93038276ba47b450218e66d9edfa032c5de796fbb9f9854efdf5`  
		Last Modified: Tue, 17 Feb 2026 21:15:52 GMT  
		Size: 7.3 KB (7281 bytes)  
		MIME: application/vnd.in-toto+json
