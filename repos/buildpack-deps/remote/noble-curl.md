## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:0591c4ff26a20c9bd55f2531bc515396f6d356830bbe9e1136205dcabcf857cf
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

### `buildpack-deps:noble-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:644a9f032cf50b2a91f1c4e7312425a77195879e7178d6a6076c084e9d7457cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43366523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d93add3ca2246e80a01713194ef3cc70909c3ccce2b0fc64adb66e63e0d3fce`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 03 Feb 2025 23:00:26 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bca5f89848ce8fced9fabc99051bd86546e9b21ec911faa12d1b57517b419d`  
		Last Modified: Tue, 04 Feb 2025 12:25:48 GMT  
		Size: 13.6 MB (13612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a4e685fd1a1fdc8c51f92015aa36ade4193a409acedff0d9fc53f6f0e5e2a403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312348ef20d91871237e8ce4d0b2263ae4f719aac1e1106d85629a329e842c8f`

```dockerfile
```

-	Layers:
	-	`sha256:2a3a10bb9dcd0dd89b1e24f079336b7b12e0e0ce7d66b51b53ebd2caf71bdebb`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 2.5 MB (2462082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:876478e0a9dd99b90b311614b8a249982e408c423a64c5b1cd1f707df848452c`  
		Last Modified: Tue, 04 Feb 2025 04:37:53 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5ae44b9cc101087fa183a9f8269d6d8f0d1c86230044d58ec0015e1fa706e1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39645632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c0792edbcf8119e6ef8d42938209118401d44f50d9674972ff99beec67a6aa`
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
ADD file:22301ffa2fa465db7a0f07e0c3ddc488f07cc6a745c39e6f450fdbe37da97418 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3492abb11babfb77cfc5a8904e67b22f4e4fd68c8d8a7fe1119861ed6503b36f`  
		Last Modified: Tue, 04 Feb 2025 08:31:36 GMT  
		Size: 26.9 MB (26874983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d26a8223ab81b7619d0fa204eaa4a52bd9e82a52dc44e8e3fd181d828b57c69`  
		Last Modified: Wed, 12 Feb 2025 05:51:46 GMT  
		Size: 12.8 MB (12770649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:88d98aa301ddf4ba195ae435b272e8dbc57ada124bc050d9584e020a2d0ed4cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f632e6a7a1f74c013a8732986b2644111dec9298d7588b4e37b61e3e5f87211`

```dockerfile
```

-	Layers:
	-	`sha256:e39ed50c31a6f47c59f9ff236393152bf088df00a815272e7d5f17eb16b93ed5`  
		Last Modified: Tue, 04 Feb 2025 10:45:28 GMT  
		Size: 2.5 MB (2464386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0299afeb76c3ef583558026c326712b4428d9f8d2f847835de29e219d670197a`  
		Last Modified: Tue, 04 Feb 2025 10:45:27 GMT  
		Size: 7.0 KB (7019 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f81e78c5e8cd92e7c0dd2c53f678e502b5539f88f7bbd62dcf110e487cdbd9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42341516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53f3d5ba81a42da827fd1d0fb748b572c23998d6ef79331d126adf57704c8da`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Tue, 04 Feb 2025 06:04:53 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e873299a39c8bb8cb3b5d978575339de6ade976cca414b5727de8d362ef599f2`  
		Last Modified: Wed, 05 Feb 2025 03:41:50 GMT  
		Size: 13.4 MB (13447918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a09851342c2a390434b8403c6567a044084514acfe1c895374c0d61cfd2021b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4fa8fa439cb9f6ef86fbfe6287983813d43ba022d392271dd37d7a11f8049b`

```dockerfile
```

-	Layers:
	-	`sha256:c45cb91762aa9ce3109b687f2eb31f4ee68d9a8723cfb10b81ba0e79e052a3be`  
		Last Modified: Tue, 04 Feb 2025 09:03:20 GMT  
		Size: 2.5 MB (2463140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be9ae4d5b446fb6dfc3bd1fa724ccedac7ac8e17b189771cdb3a350e25c59adf`  
		Last Modified: Tue, 04 Feb 2025 09:03:20 GMT  
		Size: 7.0 KB (7039 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b8a5136a89a7e6d03e7dd3aeffd99e0e9c7c281cc4d587c6c13bb18c89933e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50348767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec08d7af4854f7616cd6c24d855e9825f8d7b0a7cc3b33d388bb26bbbf087fd0`
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
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Tue, 04 Feb 2025 07:01:00 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb3acc4132c7aebe44f31c42e40cc094c5403d3a66fea37f2373bf78812b25b`  
		Last Modified: Fri, 21 Feb 2025 19:15:01 GMT  
		Size: 16.0 MB (15958943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7780e111e7985c50976ae1a4c5c08bfb9c544701dadd2e2c140f1962ca104727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2473560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6409635aa1c47b491672f8162339c57a539d38011229da817788051e22787bd`

```dockerfile
```

-	Layers:
	-	`sha256:b5e2dfedfa809e8174ffef851627e9bf5e80f70465fbda8b396404490e83284b`  
		Last Modified: Tue, 04 Feb 2025 07:28:51 GMT  
		Size: 2.5 MB (2466569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a0559ba321ef6c4284cc87f3b5369d46603219db294ec6bf7e0a32e77f5486a`  
		Last Modified: Tue, 04 Feb 2025 07:28:51 GMT  
		Size: 7.0 KB (6991 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:31ce75f451962f5cb800331842c9a621e15380dc7a0d5e76cc27f614fb0789d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45301140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054c4b3eb9ab81c609b9e82f2d951c6cc3a86dd499d31378a9ed2556f5980ffe`
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
ADD file:69c46ae9666e78c27ca5b5f25cec1a5536ff16f17cb00104e5c77e722bd8d643 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6e1053d729cc1718daa9369927cf6ddfbf892a846041de0e610d1c77ade136c5`  
		Last Modified: Tue, 04 Feb 2025 07:00:41 GMT  
		Size: 31.0 MB (30983910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1ff2b444c4e8d1278840900c3e27c00e5987f3c54a529299dbf9a2ed443657`  
		Last Modified: Mon, 10 Feb 2025 19:57:15 GMT  
		Size: 14.3 MB (14317230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1a87e48a82b50c374c47c2c34dcd6c3fa330f2d9871e29fa616af48a4edc3cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d637e0f6a904b9c985a5da321c9640e3c0f45e9288c8c31a84d6fe2281ce3cc`

```dockerfile
```

-	Layers:
	-	`sha256:1db32f151df67541b0541f324d7b140e38f2e4207414a4155bc3af99f47202e0`  
		Last Modified: Tue, 04 Feb 2025 04:47:42 GMT  
		Size: 2.5 MB (2456141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18f60c2b0b80254a366d8c7acb2cd5a488b2f72afe32467a2a687d6a7d8b17c4`  
		Last Modified: Tue, 04 Feb 2025 04:47:42 GMT  
		Size: 7.0 KB (6990 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:98518dff71ac71a87d5d35456508f00745860a4b1d5b936c9e65950ac33a07e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44964949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07262228767cdfdf011a42ed5559b01db0f589b6db2cacdf342b615fbe496383`
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
ADD file:1a65bb049384da7e51a2b1e9180f11d6ec22b1427da7ca5682814abd261ba57e in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8e1d25585ef2d346b71072d258a697a9d190e3c5754512c7cb978dbbe80911e6`  
		Last Modified: Tue, 04 Feb 2025 08:21:20 GMT  
		Size: 30.0 MB (30027563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cacc91036ba2e7e50d76ff2b2593ea149a0df971bb8069b913263b87ff517ac5`  
		Last Modified: Mon, 10 Feb 2025 19:57:43 GMT  
		Size: 14.9 MB (14937386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:89c4abc3a60eb48bcbd7a232595cc99c156532030ab21917410f175b25de736d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d0978b12b5385265529a2eb8e826ef6bed43e969869849f3968bd2061fbfb4`

```dockerfile
```

-	Layers:
	-	`sha256:1145ed6e6cc241993da9952d8c94810c5bdfc8691a649a7c93c330bbd18a2193`  
		Last Modified: Tue, 04 Feb 2025 07:34:26 GMT  
		Size: 2.5 MB (2464907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02a52d892c2d4165e68754e24393ef9f9addb502befc69210f9f58ff272ee843`  
		Last Modified: Tue, 04 Feb 2025 07:34:26 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json
