## `buildpack-deps:plucky-scm`

```console
$ docker pull buildpack-deps@sha256:d3cb82cc1c3652bff225ee9109f990ee8c4b5c0eb6ffc4a468bafc14d862beab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `buildpack-deps:plucky-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ea22d278e0bb8f6d1cb2bdc8712ae68cc8432ba83ef101810ef5cdf26d79a35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101439819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c843181c3532be5793216558fa98ce03230b4cabc857ecdc2d2aed3a6e0f49`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 03:57:01 GMT
ARG RELEASE
# Fri, 13 Dec 2024 03:57:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Dec 2024 03:57:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Dec 2024 03:57:01 GMT
LABEL org.opencontainers.image.version=25.04
# Fri, 13 Dec 2024 03:57:03 GMT
ADD file:32ef9166a8f23ab3dc96211cd8eb67bc36b7d8924ed441e7bd44b6381f327352 in / 
# Fri, 13 Dec 2024 03:57:04 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ad59fed61efbf10dd3068c2c52eeb888d0a8a23fb6c49a362829a3e7b94aa0e`  
		Last Modified: Fri, 13 Dec 2024 04:29:45 GMT  
		Size: 31.6 MB (31553358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb50c1181a6b2959e4f4f24a825c4968a88bb31c7de6fd37e417e447af76f7e`  
		Last Modified: Wed, 12 Feb 2025 18:31:05 GMT  
		Size: 20.2 MB (20232727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23a0c0d6e7514eaa4d197f9e9c7edc48c3f3d5522b715bb1ae5c5ee752cced7`  
		Last Modified: Wed, 12 Feb 2025 19:08:36 GMT  
		Size: 49.7 MB (49653734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8cb47db292191bfa723bcce0bfa0ae27f667731e2533102f224264f78df5864f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f151bfa880edbce35d0454fce85546c63d2974cd9ccd1a56f3856f1f10626b88`

```dockerfile
```

-	Layers:
	-	`sha256:4f6235bc13281461de3e41e22c9b0e256667ab9daad3b7846503be2dc9e7f4f9`  
		Last Modified: Wed, 12 Feb 2025 19:08:35 GMT  
		Size: 5.2 MB (5207520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd0b781cecfd3e0196fa2cfcf71442b45c2363102761749e9fcf1da68975a2d2`  
		Last Modified: Wed, 12 Feb 2025 19:08:35 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c65634302d33c6733b93ddd10b94b8a66929de9380d47779a427c036359d9fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95628606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552cefd983b69d50e2a318b04cb2a97e1434caef34fc323dc6f326107267b9a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 03:57:17 GMT
ARG RELEASE
# Fri, 13 Dec 2024 03:57:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Dec 2024 03:57:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Dec 2024 03:57:17 GMT
LABEL org.opencontainers.image.version=25.04
# Fri, 13 Dec 2024 03:57:19 GMT
ADD file:6f9e46de69cd0f87c8e7f99c02f9c86d7255b291b3d64c9acf6d3664842a11b3 in / 
# Fri, 13 Dec 2024 03:57:20 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:30edb5d57d6dcf9a2d6c372642827a2271cc4b4b697e28bf865c61a4cbde43dc`  
		Last Modified: Fri, 13 Dec 2024 04:29:57 GMT  
		Size: 27.7 MB (27738902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f812cad0ddfcb6da97c6cca7682590669793920cf55e9ec9857cda771d0d13`  
		Last Modified: Wed, 12 Feb 2025 18:36:50 GMT  
		Size: 17.4 MB (17431763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799efdc1254c10713006775b38bd235f3c0421b73cabe61926fd9522f07cc640`  
		Last Modified: Wed, 12 Feb 2025 19:09:01 GMT  
		Size: 50.5 MB (50457941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:85712d23831d89f42b924dba038d1c2ebe6c585fbf313032ee2265cb56cd81ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be23006c2f73186386b7659e18321b5b7b81b5f9eff350cdeff0b0813f9ea84a`

```dockerfile
```

-	Layers:
	-	`sha256:d4e15cbe348fb6a06c34fc28afab5c899e68088b05b63992eeff72facf8c875a`  
		Last Modified: Wed, 12 Feb 2025 19:09:00 GMT  
		Size: 5.2 MB (5208842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89390dd720a4bf3be4da5a45ab2574f657a731b2084cc21daba2bd2c462d36bc`  
		Last Modified: Wed, 12 Feb 2025 19:08:59 GMT  
		Size: 7.4 KB (7370 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0f1574b822f64df75b2f726fca44013f0ddd6c61f73e39917b3fce1b61410097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97603669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03551a0f3bef4344101823bab8eaa375e96009f73d8ec3005ec5167d11bed2a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 03:57:26 GMT
ARG RELEASE
# Fri, 13 Dec 2024 03:57:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Dec 2024 03:57:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Dec 2024 03:57:26 GMT
LABEL org.opencontainers.image.version=25.04
# Fri, 13 Dec 2024 03:57:29 GMT
ADD file:1e284110dbaa3cdc60b201ce362eb0ecbf56624b0a08b9f4cf8f66b644dcdce7 in / 
# Fri, 13 Dec 2024 03:57:29 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5d061b7d25b8082e18fa752b37dff8e14092abb693bda6d900a16a7dcab48a0d`  
		Last Modified: Fri, 13 Dec 2024 04:29:51 GMT  
		Size: 30.5 MB (30499497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d2670c6da46959ea27b1b971d462aaf78f068c9c573ab63326386200fe9085`  
		Last Modified: Wed, 12 Feb 2025 18:35:45 GMT  
		Size: 19.7 MB (19672439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039c09726ddbaff4bb3befe67d4b80c4181eaa18651dbd7b4977a15eabccb48e`  
		Last Modified: Wed, 12 Feb 2025 19:08:43 GMT  
		Size: 47.4 MB (47431733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:44ed1143be61d1547206258f79c8e4aaceb159b9a4a2e4339e7dddc2c0dee019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae82ef48a5ce739d55981bf58f81720f10f8c29ef69aa1b4fb2f549675ccb56`

```dockerfile
```

-	Layers:
	-	`sha256:d04fbe78b5c1da63deee68a5a357eba784c47e56a62e4b72b2cdbf239a615645`  
		Last Modified: Wed, 12 Feb 2025 19:08:42 GMT  
		Size: 5.2 MB (5214715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959c0649ac2a76618f953759e9b462f31a9a13120bf6d0c869f96650561eb693`  
		Last Modified: Wed, 12 Feb 2025 19:08:41 GMT  
		Size: 7.4 KB (7390 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:940371fcfffbae7c62fe9e18efddbe5fc8f017a850837810d9449811b720e3e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110066881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c157c35bd6b4ef66660ac97f39e7693059b32c9181c65c53dfd1777c50fdb1e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 04:05:50 GMT
ARG RELEASE
# Fri, 13 Dec 2024 04:05:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Dec 2024 04:05:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Dec 2024 04:05:50 GMT
LABEL org.opencontainers.image.version=25.04
# Fri, 13 Dec 2024 04:05:57 GMT
ADD file:f463fe3764cb56f51ce431a4abb09e109ba806b3a785a3fc25e1f69c2065dbbc in / 
# Fri, 13 Dec 2024 04:05:57 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9900e81109ec0ccb44d7bb5d6d45a02573dda94fa8343fb11051f5a0b60d9fb8`  
		Last Modified: Fri, 13 Dec 2024 04:30:03 GMT  
		Size: 35.3 MB (35281944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20aece5c23f3c01801adef45cec06ef7bd2f0002eadebffd4e9678c7d4a4cc80`  
		Last Modified: Wed, 12 Feb 2025 18:37:19 GMT  
		Size: 21.9 MB (21859806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c9258328195f1d98c16c956aabe59b460ba69e0f035e75013a7a534ee12d1f`  
		Last Modified: Wed, 12 Feb 2025 19:09:05 GMT  
		Size: 52.9 MB (52925131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:580676cb64abc78994bc865c09d45f6037ee05e8c3a498f000f58efff169ba34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931d5ebff5005a3bfb6b0b1a136e3cedcc3010ef65d2c9cf7aee9262ac2d09b0`

```dockerfile
```

-	Layers:
	-	`sha256:faf4ab914149e9d017c5d0884fa6bf7d580ae5396e4b5d50f1e13b670f8d53ff`  
		Last Modified: Wed, 12 Feb 2025 19:09:03 GMT  
		Size: 5.2 MB (5215252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a13e2ff1d3da866c1bdc81a45ae436dafe6e43354e469b1941027c95f116160c`  
		Last Modified: Wed, 12 Feb 2025 19:09:02 GMT  
		Size: 7.3 KB (7341 bytes)  
		MIME: application/vnd.in-toto+json
