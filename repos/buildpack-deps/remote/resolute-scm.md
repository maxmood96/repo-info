## `buildpack-deps:resolute-scm`

```console
$ docker pull buildpack-deps@sha256:6960b133325cc05c0960871c1d4a0c6dedb81b2838390beda334a81ee925feb9
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
$ docker pull buildpack-deps@sha256:d921dc849f211ee8f72cfd5da222e872a467c4ef9b48a2c26ce93e7f8fe333e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101725054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b785c118614dfb29083ec5c15051e7764d307a6a2e4fb036a619968b66a3ca14`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 08 Dec 2025 03:12:22 GMT
ARG RELEASE
# Mon, 08 Dec 2025 03:12:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 08 Dec 2025 03:12:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 08 Dec 2025 03:12:22 GMT
LABEL org.opencontainers.image.version=26.04
# Mon, 08 Dec 2025 03:12:24 GMT
ADD file:20d5e915d0d393fcb7e648f66e92f60aae8aa4008ec9f474084335d6b517afe4 in / 
# Mon, 08 Dec 2025 03:12:25 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 20:11:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 21:10:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1930ad95e8edfa40a67fed625a6b952de1df4b24c225dd737adb00346824f4ac`  
		Last Modified: Mon, 15 Dec 2025 20:02:05 GMT  
		Size: 33.7 MB (33742427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc032e9d150edca71ca527020eb733586080f7bda49bec4c3582b3f374be743`  
		Last Modified: Mon, 15 Dec 2025 20:11:39 GMT  
		Size: 19.4 MB (19428885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34e03e630d58ec8ee7cf7211a1e391f98a0ccd100cc5f40ec4beb6f17291111`  
		Last Modified: Mon, 15 Dec 2025 21:10:50 GMT  
		Size: 48.6 MB (48553742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4825bb43b4945e8dfde68309bb944229d8b30258088b414daaf7d9d230b733ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5764201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be6320daa2191aadc2d5fb9eb36bf9fcbf6fba5538dff4b7a1bf859440bf563`

```dockerfile
```

-	Layers:
	-	`sha256:2c27ea453b292b38dac8d4dade0f699297734a1c32b546f5e9e1d46e4adf2e6b`  
		Last Modified: Mon, 15 Dec 2025 23:20:11 GMT  
		Size: 5.8 MB (5756920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b32a9bac1dac58c8d5989ae9a8d757fe037b8590a40d3b9d5c8bc19bf5041308`  
		Last Modified: Mon, 15 Dec 2025 23:20:12 GMT  
		Size: 7.3 KB (7281 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1b35d4e9d9225c03f719fbe0761def6130b2c82a2e63196dc339ee1b7d14a73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (99951705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc42d991ff4ac72a306e190e090edbaf9226ed8c0b3f277b90ba80919fdbda56`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 08 Dec 2025 03:13:34 GMT
ARG RELEASE
# Mon, 08 Dec 2025 03:13:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 08 Dec 2025 03:13:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 08 Dec 2025 03:13:34 GMT
LABEL org.opencontainers.image.version=26.04
# Mon, 08 Dec 2025 03:13:39 GMT
ADD file:b61e9f94116cf2f68a6415698661ee2b700e7d672508b7326845bcf886232f85 in / 
# Mon, 08 Dec 2025 03:13:39 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 20:10:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 21:10:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2bf29d7486c7e629372c92e4748c184d88f0e4e34b33e49f296e9c9c32039dec`  
		Last Modified: Mon, 15 Dec 2025 20:00:53 GMT  
		Size: 31.2 MB (31156573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df541f37757c7ee3123bb95436fe3a3bf9cac7e92450e3a3a87b55d80bf8aee`  
		Last Modified: Mon, 15 Dec 2025 20:10:55 GMT  
		Size: 17.7 MB (17745313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae46f09dc50163ba4eec305ba6b855deff0220e28d3b3422e7a56d10557f4029`  
		Last Modified: Mon, 15 Dec 2025 21:10:42 GMT  
		Size: 51.0 MB (51049819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0e56ceceb5673314f85c155b694f617e0df368d250fc2193f186bd739904f900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5764760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77963c6f1e12c6e5fcc064f282f628b77dca45576af3aa27db0a91d365378e25`

```dockerfile
```

-	Layers:
	-	`sha256:ec81568f42b51994392e75b218e15c6060b933a5a9476f034b3569dc109016ab`  
		Last Modified: Mon, 15 Dec 2025 23:20:18 GMT  
		Size: 5.8 MB (5757416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32e252f701d12d80532d76a120ced97def70715f93bfca44574ba801be750f51`  
		Last Modified: Mon, 15 Dec 2025 23:20:18 GMT  
		Size: 7.3 KB (7344 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b8678e650fa70b95be1f986c6e6ad61efd5738e23c80077596776a739610a308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100467337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909aa0be1c00f221a8ad92595b5d9b948aa8ae135c5af7bb922c0ff7f7e2fa4e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 08 Dec 2025 03:13:36 GMT
ARG RELEASE
# Mon, 08 Dec 2025 03:13:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 08 Dec 2025 03:13:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 08 Dec 2025 03:13:37 GMT
LABEL org.opencontainers.image.version=26.04
# Mon, 08 Dec 2025 03:13:40 GMT
ADD file:880dc0c9ea14ee504f2d3c0432440022eb7cb1d8e051e9c517689f394260958d in / 
# Mon, 08 Dec 2025 03:13:40 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 20:10:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 21:10:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0196ed0ac4ca95d4c74a0629deb6468dc9b8d3f3bbe0834d244c1ef7c9bdd8b3`  
		Last Modified: Mon, 15 Dec 2025 20:01:51 GMT  
		Size: 33.3 MB (33300910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40970ea46a6648d5c0acf6872b257eeae96e2929f52e0a4991f153cd5c126ccb`  
		Last Modified: Mon, 15 Dec 2025 20:10:54 GMT  
		Size: 19.0 MB (18953427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d06c4b4a1abaa456ef1a4e4a8a431922173ff3082858910d3b60740353a6d1`  
		Last Modified: Mon, 15 Dec 2025 21:11:09 GMT  
		Size: 48.2 MB (48213000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ac33aac3374d81f530e58cf4f7fd8d4378690e38fb25e105b19a3ba088be2b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5770668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715fcd3224f8ea9a2cdfbda770c6463b6700ddcb8c0b3355cdbf45dd6e8ad578`

```dockerfile
```

-	Layers:
	-	`sha256:65e540bfc1715d9d0dea51ead04ffdeb313ba59ebb51929430fa09ba209837c8`  
		Last Modified: Mon, 15 Dec 2025 23:20:24 GMT  
		Size: 5.8 MB (5763307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:569ede0ea6973da253412eccd2010bd2a0ebc3d393e50e5c3145a6b93e936cb6`  
		Last Modified: Mon, 15 Dec 2025 23:20:25 GMT  
		Size: 7.4 KB (7361 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:86153792d620b39f37bcc0ce965d641fc668ed2ed88aa47c7acf118737cd63c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114917360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b340c7ebc409393f8a49348cf8cc38b9d158878345577f7522a80b3e161f7e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 08 Dec 2025 03:13:14 GMT
ARG RELEASE
# Mon, 08 Dec 2025 03:13:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 08 Dec 2025 03:13:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 08 Dec 2025 03:13:14 GMT
LABEL org.opencontainers.image.version=26.04
# Mon, 08 Dec 2025 03:13:20 GMT
ADD file:1ba64fcb8425d92e42a4dcd6299abe7ca1abca89c8ada8bca11d7804b715a1b7 in / 
# Mon, 08 Dec 2025 03:13:21 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 20:10:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 21:10:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:99d2753c6e5d3b5e655cfd1b57108083b422a46cfe597843b023a4e2c7c000bd`  
		Last Modified: Mon, 15 Dec 2025 20:01:29 GMT  
		Size: 38.8 MB (38808598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e9c4708e4fcc9ce73471d9e3d813efeee0cfcd5a8afd3b763ae4d5927a0d5c`  
		Last Modified: Mon, 15 Dec 2025 20:11:35 GMT  
		Size: 21.9 MB (21906882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90b16e5bd388001855f31a9018a7801bc4713e3ed4803e64c0e957a08a7ff85`  
		Last Modified: Mon, 15 Dec 2025 21:11:32 GMT  
		Size: 54.2 MB (54201880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2e4e7e84abac76d9b3ad8bf4ed22a919096b5e82ee4f24f1918098bd8eb2ab79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5771291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc061a6374a8c0769909c2b8b5b749bad2e18496745aa3e79a9055480ba7eced`

```dockerfile
```

-	Layers:
	-	`sha256:99f237e1ed8d6ac7b03e685aacfe8157ed8cace505af68208da9fe43c0423b39`  
		Last Modified: Mon, 15 Dec 2025 23:20:32 GMT  
		Size: 5.8 MB (5763978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b61c67ffba381ddc1d03c951a8c223b42e17380fb58390cdb83c2c585a347a0e`  
		Last Modified: Mon, 15 Dec 2025 23:20:32 GMT  
		Size: 7.3 KB (7313 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:469d16eb8a20320e1d0b1ea2abe58b1977bb27075a068d41162fb1ec8939ac37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102693973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243d4df80c95e5bc91fc061f5b7eb600cefb2ade8d8d6d8d6e2d7a7ea0ae2faf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 08 Dec 2025 03:12:49 GMT
ARG RELEASE
# Mon, 08 Dec 2025 03:12:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 08 Dec 2025 03:12:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 08 Dec 2025 03:12:49 GMT
LABEL org.opencontainers.image.version=26.04
# Mon, 08 Dec 2025 03:12:51 GMT
ADD file:9d8d73794e21475bdd8f856aa959b4a2af7fda40f696897caf099eefd5628d0b in / 
# Mon, 08 Dec 2025 03:12:51 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 20:10:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 21:10:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9a53a9f36e89cb17b371244f4700e0e70e68c792d70ffa6f555d0497c602d741`  
		Last Modified: Mon, 15 Dec 2025 19:59:57 GMT  
		Size: 33.4 MB (33395288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32929a90664eb992dfded2cfe05892d67b8b30f3ec5f2a61699955dd20048079`  
		Last Modified: Mon, 15 Dec 2025 20:10:56 GMT  
		Size: 19.9 MB (19882916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d63b6cc2121582b69aaa364c4666d8667029a1d6a0a63422f73b702d28d3d8c`  
		Last Modified: Mon, 15 Dec 2025 21:11:09 GMT  
		Size: 49.4 MB (49415769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5d51bbadda255f6f5ee1fc4f1f0980dd4da59f3275549a7993e3310b589f533c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5765739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e7fe3ba8282706a610907ae8913e7bee819ed5fe50f588dd661f7f36739c2c`

```dockerfile
```

-	Layers:
	-	`sha256:928bfe0705c6f1cf9111ffaf1107ef63269b2c648fe39413fe942c3ef58deac0`  
		Last Modified: Mon, 15 Dec 2025 23:20:38 GMT  
		Size: 5.8 MB (5758458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b18f9d77175ab09e3d79b2b977c2b65ccca5feb8441bf3dd1e5c609041dbcaa6`  
		Last Modified: Mon, 15 Dec 2025 23:20:38 GMT  
		Size: 7.3 KB (7281 bytes)  
		MIME: application/vnd.in-toto+json
