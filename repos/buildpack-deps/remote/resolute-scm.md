## `buildpack-deps:resolute-scm`

```console
$ docker pull buildpack-deps@sha256:a0a369a2c47a66286842d787b1cacfc1d553ad78e92cea544f3d8d5299b8dc72
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
$ docker pull buildpack-deps@sha256:e45f1658f07b095f36986db042d9b2a42f106182199b7fe8836c5a4b45ddd895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99646289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09273ee1a0f5bf712bb2a7ec48f00cf760c8c1bb29a726499fa8e054476be9eb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 06 Jan 2026 16:12:47 GMT
ARG RELEASE
# Tue, 06 Jan 2026 16:12:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Jan 2026 16:12:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Jan 2026 16:12:47 GMT
LABEL org.opencontainers.image.version=26.04
# Tue, 06 Jan 2026 16:12:52 GMT
ADD file:2badcd83b204d640ccedc4ace52673007514f420a84bd8c139cdf292ab0fd3e4 in / 
# Tue, 06 Jan 2026 16:12:53 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 22:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a9ee0a3989db9dc297303b58491eba6d69952baa6b2827fc54ee64ce18e07032`  
		Last Modified: Thu, 15 Jan 2026 21:43:51 GMT  
		Size: 31.2 MB (31161903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afba882eabc4fb690fa94f15129818fcf2958502ce348f72e1f4978f4fb0a975`  
		Last Modified: Thu, 15 Jan 2026 22:08:16 GMT  
		Size: 17.8 MB (17784528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e787e849e38a2c06b825e1d0dc7a2ac35b36e530488241b0cd53030551589a46`  
		Last Modified: Thu, 15 Jan 2026 22:35:30 GMT  
		Size: 50.7 MB (50699858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e99ed929bee32cf0bdbaa3f0ff4b9d66c3cd4a7974123ecb31cd24e1090d2674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5764385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7101c47aeaec5a3c9f1a964ff1677260807f5984ea8b1b275a4cc618f2d04149`

```dockerfile
```

-	Layers:
	-	`sha256:3ebb5234afcddd09d8e4d643a54f130c4e727dfdaa47565c54f26ad536c79e5d`  
		Last Modified: Thu, 15 Jan 2026 23:21:20 GMT  
		Size: 5.8 MB (5757040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb1f7e5b72a5861bbe204b11a3d99fe203c2457e55c528fc619a49987e21f340`  
		Last Modified: Thu, 15 Jan 2026 23:21:21 GMT  
		Size: 7.3 KB (7345 bytes)  
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
$ docker pull buildpack-deps@sha256:f2e77f6beab63c3725d83166659adc1e1fd363beaba4fcc566846849ffd82425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102394429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686271774376416c4c50f4b691e62f05ffcf9af056e8e5083d247b16f902453b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 06 Jan 2026 16:12:54 GMT
ARG RELEASE
# Tue, 06 Jan 2026 16:12:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Jan 2026 16:12:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Jan 2026 16:12:54 GMT
LABEL org.opencontainers.image.version=26.04
# Tue, 06 Jan 2026 16:12:55 GMT
ADD file:9266e4011fb5ad8a3df9e390fc8165ed1fd44560192a8470907993912a77df90 in / 
# Tue, 06 Jan 2026 16:12:55 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 22:46:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f779d014bea281c13f5bd15e791164db36f27117b06bcc6a0832c49e20ca6c3f`  
		Last Modified: Thu, 15 Jan 2026 21:56:50 GMT  
		Size: 33.4 MB (33397954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66829f85ee6a4ac10cb285e12e8d836204a87759cfb752c0e2b65010651a3b0f`  
		Last Modified: Thu, 15 Jan 2026 22:06:49 GMT  
		Size: 19.9 MB (19947648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00ffb09829df0d3df34b27f7b2ec620dde52eb10796d930fa7f7a852d0ed178`  
		Last Modified: Thu, 15 Jan 2026 22:47:24 GMT  
		Size: 49.0 MB (49048827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1bd75ba92c874d9f1464e9b33c2443ac374f62d11abd1539486c6bafa941dc2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5765363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ad44ba9e282b58eb9e334bb1705d054fd3b21669941b3249c97cf99d1955b9`

```dockerfile
```

-	Layers:
	-	`sha256:d55d65b637db5782ddca9934df7ec0dc707717ad9516c1a3fbd31092e0e0f5c5`  
		Last Modified: Thu, 15 Jan 2026 23:22:27 GMT  
		Size: 5.8 MB (5758082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:092b8f4d29a1daaffedfbcade318826121fec0b301604fd47a5ff977bd75981e`  
		Last Modified: Thu, 15 Jan 2026 23:22:28 GMT  
		Size: 7.3 KB (7281 bytes)  
		MIME: application/vnd.in-toto+json
