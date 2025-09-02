## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:55685abb46c3baddcd7252c7de25b8d6750068b10407c4f2d74a336ad226575f
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
$ docker pull buildpack-deps@sha256:b3965b386cbda02f0b375e37e2a3cadda2d59865dd4de02e8025671cb2cb815b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76130414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ccba197902a5acdd764e8c87d76e22f33c3e214508339bf0b8a8ba3684edd3`
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
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6828c7dda7e5e4b9c82ddb483379bdc791aa9b7cecdce2c883c603e7806ea9a`  
		Last Modified: Mon, 01 Sep 2025 23:07:56 GMT  
		Size: 7.1 MB (7106278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3856fb40e8823986f0d2b16e4bb928a603347223ee232458482a4a5a7b70b7`  
		Last Modified: Tue, 02 Sep 2025 00:12:14 GMT  
		Size: 39.5 MB (39487201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b198a17f0568b7e3bc5c04488cbfe35139de3befaac1a8508837ffd57eeea5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5820021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549f45c2f7c4418688c8f668b736e712247cf3648bff90eb94559ac4e8cf9fe5`

```dockerfile
```

-	Layers:
	-	`sha256:0b6b164c4cd7b05b52190a315968a6006e0b967d46907835af5a67112b439727`  
		Last Modified: Tue, 02 Sep 2025 04:19:43 GMT  
		Size: 5.8 MB (5812698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80912376a1c4a1bd214d2b3dd79e73f2f68afb244f66923cd71fe06b79212b07`  
		Last Modified: Tue, 02 Sep 2025 04:19:44 GMT  
		Size: 7.3 KB (7323 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f303bbb62671f6094e60b45151351b603f85f83c3f0d93df7b6f04666dd5ef6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75905114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7258c8d93e3e14b7abf4ab4bc46cac3d375e2f0f1b08c08b53ad6d4c261567`
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
ADD file:1b718ac25471aa07aabcef27ec2e737bdbf36fd950c8d6e6103ad3dfeacd8e98 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9e6391cf5a380a152971ee67d9bbbdd494023e7e2a2da9c7b92dd6d51593fee6`  
		Last Modified: Mon, 01 Sep 2025 23:13:56 GMT  
		Size: 26.6 MB (26642908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bcfda65d1847d88965f302b038b1be953284583ebd165847009e51bcab6359`  
		Last Modified: Tue, 02 Sep 2025 00:11:15 GMT  
		Size: 7.0 MB (7010211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5839f3de1edd0068423e4ae7e1e8d6070d3ebddb4b805fa9906bbef0f54e2c05`  
		Last Modified: Tue, 02 Sep 2025 01:12:25 GMT  
		Size: 42.3 MB (42251995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:22b0fe0f1991c093bd0bb4b24d6179a3222bee18f6277d2394abfe1e3d0a7dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5821361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce5b38769c44deb2768da2085c412db689c553c0d114a18fd9fc38d1ba809fe`

```dockerfile
```

-	Layers:
	-	`sha256:3a4874397321cf7c247278d67887d93a8097ec80555cdf39cdf6ae28fd075d82`  
		Last Modified: Tue, 02 Sep 2025 04:19:50 GMT  
		Size: 5.8 MB (5813978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbb7791441da32ddc9cc70500a499f5ebed9af93d9233c9c2cb043fb9804eb96`  
		Last Modified: Tue, 02 Sep 2025 04:19:52 GMT  
		Size: 7.4 KB (7383 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:70d5dbbe4185252acfe5ec6f58054797408821979370bee4b067349644d0fa18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73797816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb89bbebef01d7b3f7239c42d27b9402978e58ad2a3809683fd1ced22d14638`
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
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b56f55094f2d14930c686b1a46091f6f5d62cadec0da94af57c5297b32867`  
		Last Modified: Tue, 02 Sep 2025 01:18:59 GMT  
		Size: 7.1 MB (7051940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508724dd86b6f1e696d30cba1d227b5e49b51dccaa040b0346816bfab7e8160d`  
		Last Modified: Tue, 02 Sep 2025 03:45:54 GMT  
		Size: 39.4 MB (39384407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:df238c64d85fa622d93172d4d4da1710a4dec349e97138ff50c758022e23d77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5826496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f471861bd32cfe30b87a6f5c86c0fa89386d9f828ab756a354eef4f5541b2d9e`

```dockerfile
```

-	Layers:
	-	`sha256:c0701a111c786e9559a150a1960f8caf925dde6bbcd2d48687c1fd31a3c129a9`  
		Last Modified: Tue, 02 Sep 2025 04:19:58 GMT  
		Size: 5.8 MB (5819092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3813fddc2583ced11f3dc73baa7b3c5fcefa3beb64082804c033f2b7a3af5ca4`  
		Last Modified: Tue, 02 Sep 2025 04:19:59 GMT  
		Size: 7.4 KB (7404 bytes)  
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
