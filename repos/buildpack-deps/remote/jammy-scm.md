## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:0cc050ba84fcae8b958bee3bfd127be0e0be1d04f2ca185ac3e044a00f143211
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

### `buildpack-deps:jammy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a39aeea9582248ea8750874d666f02305a45fa33b3739652e22ca3e15e3f86d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76130988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6051a7272b5a70586cb288700908d88d7709fc0ff4c73261abd4b006e7e55ba8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1718e536deb534924f0e24d75c0ad8cbe941526cffc1ff3ec1e0d1c6ec3f68`  
		Last Modified: Tue, 12 Aug 2025 17:23:37 GMT  
		Size: 7.1 MB (7106301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0af6b0da3685a9691a0c2dc93fd4622ce033ebe2d18799fe3d2f24527356a2`  
		Last Modified: Tue, 12 Aug 2025 17:52:57 GMT  
		Size: 39.5 MB (39487694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:828d2796cb348ac8677dbabd215995f15eda94a4b07964f233f12618dfed4d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5820006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b017a544d765fdd7ad1d8c63bba3992ccf77214b8cfbe5285dcb28679f3d8103`

```dockerfile
```

-	Layers:
	-	`sha256:dc42b1e8043cc8ddb6970d2260f90468d64ded6c901644b9a2b6b418548369c7`  
		Last Modified: Tue, 12 Aug 2025 19:19:48 GMT  
		Size: 5.8 MB (5812682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:728835799a77bd80be75217d6bb89c48efc28cfe5e80c66b7d6b3108751829dc`  
		Last Modified: Tue, 12 Aug 2025 19:19:49 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3ce02c0e600d62828d1d35eb2eef27fbcaacfb77b4c187b6dd86451ffe84e9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75903011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f55cc9bc47160429aa0940f15821873ec70c26c050149128a051539b150041`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:56dd1608fa49343c3815b8373825d581303e97b21994ce0e1d099bf09251caea in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6530e67fdf3958f32e486561f05a1170b5fbcd419c51eb435b13993ecadad7b3`  
		Last Modified: Tue, 12 Aug 2025 17:02:44 GMT  
		Size: 26.6 MB (26642919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247ab3b4ef805c703a200af320c236c49a0ffab6a53a288323350767589e6b1c`  
		Last Modified: Tue, 12 Aug 2025 17:22:41 GMT  
		Size: 7.0 MB (7010313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac244b8047a8ede8039467f8c639786b33bbeeeb871907f772115d141b28e78`  
		Last Modified: Tue, 12 Aug 2025 17:53:06 GMT  
		Size: 42.2 MB (42249779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e288406f255291c2d3a23d4b42b61f7b34a458e43b087d6880c8614a8a3c7c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5821346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4f1696a8178a6bd89f0fa54eba28ba4325337dba874f0598626e95d71eaba0`

```dockerfile
```

-	Layers:
	-	`sha256:799ae16ac5fe3baf5a3166d3aa6578e2dd03a3d3aab4c867101d3547c3298be2`  
		Last Modified: Tue, 12 Aug 2025 19:19:57 GMT  
		Size: 5.8 MB (5813962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c594d4b1b1c7ff97dff86400b2a6509ad00f4a4b1b0743e52d6b6afe84954416`  
		Last Modified: Tue, 12 Aug 2025 19:19:58 GMT  
		Size: 7.4 KB (7384 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:104aecc12f0f30f1c916154e9f5b5ff5151800f22fa13252596448f8d3c0691c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73796919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2384c09d9cc356770522463024ad6661e42194b721be2f00ac6bd2856eb6e91a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476a9430580cac739e29f524f2d4fa032c5bfb4d16c97a34238459efc663af4e`  
		Last Modified: Tue, 12 Aug 2025 17:24:37 GMT  
		Size: 7.1 MB (7051909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff81fac6a1179a5e3cbb2d54ab761676b2cfd9b578137b5d20d478f05d90d7e0`  
		Last Modified: Tue, 12 Aug 2025 22:14:13 GMT  
		Size: 39.4 MB (39385763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e91e78e30f5b167610784cf521df19baf8ecf92532b7bf4ac70cdf381e0dfdd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5826479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f976f12cb12c612f5aab22b3ec04dafa912da083712fe7732eefbbb60c5076`

```dockerfile
```

-	Layers:
	-	`sha256:e8ada15c01e5ec788982c9fb067151950b78728a298611ca6af80f92739d4f8d`  
		Last Modified: Wed, 13 Aug 2025 01:19:30 GMT  
		Size: 5.8 MB (5819076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfb5e37b77d42157cbd0943c7fff144a62695bdd209100c5d08d23c1582964ef`  
		Last Modified: Wed, 13 Aug 2025 01:19:31 GMT  
		Size: 7.4 KB (7403 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c32ef4e31c0f744b3b46e5e23562f484da7bfc47f624c2a04900080186239182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86395608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6de77e0f05969abd641c131f85ad910b7749bee57a8764d79f900ebc6ac3a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deeace24228f2ecb190bb960497ccea7acc7d82389a0af77723f03f86f2a09b7`  
		Last Modified: Tue, 12 Aug 2025 17:25:05 GMT  
		Size: 8.2 MB (8184873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b14242d8340dade2d7f016981f02241d8ec2f1f4d9662de8bcace23ae887ee`  
		Last Modified: Tue, 12 Aug 2025 23:15:45 GMT  
		Size: 43.8 MB (43767590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6436d1a76fa982496f96f6e90648404433fe0ef1b942cfbac4a8133d0868f913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac2338294221e5af4cbc7f161096d98dde2d733f8205fff9fe67348ddd3e476`

```dockerfile
```

-	Layers:
	-	`sha256:3983df65b444c6f89b937223eafd0c40999329ae71999a10e8cbec4eb3d66ce4`  
		Last Modified: Wed, 13 Aug 2025 01:19:36 GMT  
		Size: 5.8 MB (5820526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2abdac46b71b8406b051be399aebdc58931a2328fddf43d91acb58cb0021648d`  
		Last Modified: Wed, 13 Aug 2025 01:19:37 GMT  
		Size: 7.4 KB (7355 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:6e026a24d294effe0ccbab5ed531747a832cf914ad0b7edfb4dbe3a2c14caa71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76465073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece21f6da7ccf95bfe642ad8fb1369e8a1f2d42162e8b7a2a6b2ec7ff6998527`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:35770e06fa2c1cc2b759aaab361c62ab900fac2d6b612a4403b76189d7f2ce82 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1de6ca2b6a61e33f0f8fae9da1d47f9afcb02341cbe72eeb6eed6979ef59b090`  
		Last Modified: Tue, 12 Aug 2025 17:04:15 GMT  
		Size: 27.0 MB (27042020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2831747a0034f903385b005efb41ad90f86cbeed2dfb31e5afbe06beb4de45b9`  
		Last Modified: Tue, 12 Aug 2025 17:26:12 GMT  
		Size: 7.1 MB (7118185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328660fbda39277d782f765a5900fe7c253fb97800d915b2c262f417749954f0`  
		Last Modified: Tue, 12 Aug 2025 20:48:45 GMT  
		Size: 42.3 MB (42304868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:97114143a5c03f8fbb741e14188163c2c58e00cec790325d055324bfd30865fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22702e0d346e9b2eb05a3e2e7db261fa141c8183b04edac5b7f5d6e08e7dd3ba`

```dockerfile
```

-	Layers:
	-	`sha256:35bd34ccce32be209a8d7b7f898f76c76919f97e096eb33a0b0fd79ac8d1e584`  
		Last Modified: Tue, 12 Aug 2025 22:19:42 GMT  
		Size: 5.8 MB (5803068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:607206c12c984fc4e14cecd646752b8daba754316f25ba97069505abd15ebc32`  
		Last Modified: Tue, 12 Aug 2025 22:19:43 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f93ac960e78a5f8bc5c4bb9e6584f1f05ee1cc2bbd406ff50d01a60d14ae02c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74442115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3acd02bb3a1ef886c8a62cfaa6ef8d5ae89c9a01b25190d8aa5b75a168b9f3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2109104756ac117958527cffddc193d2cf33d0621953649a7d5800a93fa86665`  
		Last Modified: Mon, 01 Sep 2025 22:59:18 GMT  
		Size: 28.0 MB (28003668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa3acd4828544874bb6a8619273470054d87a7f950b1770dff8640fbeed8822`  
		Last Modified: Mon, 01 Sep 2025 23:08:39 GMT  
		Size: 7.0 MB (7018642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fc7403e651ec72941a77cf7eb2a35d461bb2dbe2f532ebf625eed2e5ab8e5`  
		Last Modified: Tue, 02 Sep 2025 00:18:29 GMT  
		Size: 39.4 MB (39419805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d15943bca5988ec35360fe9c2c7dea4b23b6a96c46577cbf88bd7585e5b3f73f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5820941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065d91560ff1b32f9a4eaa4cb6edb307a407c648d9f5677bb952443f3704e039`

```dockerfile
```

-	Layers:
	-	`sha256:537ccac0ee39a6bfda27c031b43950f7d03c8e962df719b5a125e5e0944e4981`  
		Last Modified: Tue, 02 Sep 2025 01:19:55 GMT  
		Size: 5.8 MB (5813617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9407b3c220771e382961fd7661f60884a15132ddb01663183ffc63b14028df22`  
		Last Modified: Tue, 02 Sep 2025 01:19:57 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json
