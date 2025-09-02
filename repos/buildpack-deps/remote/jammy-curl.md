## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:4c0b4e5cddd73e3b6d43715bc5651235c111ccc502b4aa6c12e30ff6a3ce7203
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

### `buildpack-deps:jammy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5400f308c6bcd2372458c017ffc1fe9211e8dc16ca860fd8e7ae1a5e07543a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36643213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f7326f56b6a7be2d279d5d709b84e244c9fee82f1bf0775be80dd1b85ed2fa`
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

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7eae46b5140c2df1ca7b22c6dd511dbb0afde5cfac58287f30d974eaa644fc7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3212139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2ca58684023bab14aa86865d2bd5078d9adb382bcdd95baa60d3b80266834b`

```dockerfile
```

-	Layers:
	-	`sha256:c69900e3e5fc82e4a871234407570892a51bdc463d7bbaba076216d80f76f656`  
		Last Modified: Tue, 02 Sep 2025 01:19:28 GMT  
		Size: 3.2 MB (3205215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96423776f1092a6fba1f4faef5007db4c7c3275809f4112bdba076c4d34f7b8c`  
		Last Modified: Tue, 02 Sep 2025 01:19:29 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:706edf1ad8fd432122452c4bcc8b3b014a86801f744855fd9bc650d0ca10908f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33653119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69de34a12e2812a45d8d6e1c68ce4799d927d4c84554130ae5ac50c8fec337f0`
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

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f4a55ce0b76f3e25fc5f39732ba73c83cb47ab290aa5ec8052aed703943b9d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3214506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7b978402fe0658d103e7454945c83722c5305aa5fa548e1511b892d4d1a94d`

```dockerfile
```

-	Layers:
	-	`sha256:658c24d6fed8c417311c5d9b81753b288ef94c7ddf07392dcd7ef99a76284cdb`  
		Last Modified: Tue, 02 Sep 2025 01:19:33 GMT  
		Size: 3.2 MB (3207522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42dade6b7e675ec307dc6129362f359aad09aec81e8eed66e2d87fb2830ffb5e`  
		Last Modified: Tue, 02 Sep 2025 01:19:34 GMT  
		Size: 7.0 KB (6984 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c44a7d0332d662c91dcbce117c5a37b4e8b6de569034b6f0745f1348ad0af715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34413409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e6a1c98b4c509a0f704ef26b528ceb659a59c27c49b5568530d33a572b7c7d`
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

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5ef8262d245673c70797e7e5dee7078bb0afa3fb1e51145bcf0a5f480323d79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3212486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd518e7401b8c0290f893a505a885f1075240361d0a5e8f4fec42d0c8b45d90`

```dockerfile
```

-	Layers:
	-	`sha256:008b5d7a8157d456fbde43b606221673233f5f3fc4b7abcbd41a87c35c923efe`  
		Last Modified: Tue, 02 Sep 2025 01:19:37 GMT  
		Size: 3.2 MB (3205482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:159fcb6245cb07bd462ae2d46674c97bfc609425f6529c07f536070085c78562`  
		Last Modified: Tue, 02 Sep 2025 01:19:39 GMT  
		Size: 7.0 KB (7004 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c424fb12aff7ca90837dfdb076c74f09c12a4761f030c8fec5ac63fb4987be9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42628157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e48905734586c3ff50ef818cbf0d71232706f538ed77582f052f6576baf225`
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
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3f77bc9e4ab6e5fb5af578f087cd1cd7d1b42df4ce3edcb7205e77fa641e55`  
		Last Modified: Tue, 02 Sep 2025 00:12:15 GMT  
		Size: 8.2 MB (8184933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e92680267a2c45de344efd0cf6d14385f93b322f206ff3bb8b7318617a88c9a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3216806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92daea4f013928afd354433b65df51606a1b806ccc02dde4d7b22894f937bf5c`

```dockerfile
```

-	Layers:
	-	`sha256:0accaba1ae050be0d0ff58333157b34fd4ad9a1f2df0b2e6d53cd23b0afc69cb`  
		Last Modified: Tue, 02 Sep 2025 01:19:44 GMT  
		Size: 3.2 MB (3209851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20822fe52981639e26550f9a99491415dc439dea201c7afaefa38dc7724be949`  
		Last Modified: Tue, 02 Sep 2025 01:19:45 GMT  
		Size: 7.0 KB (6955 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:aa0e9f627bb83c2f8acfea1e3cf39fda33de1bdf9a1c744fcf46163019ef09bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34160205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e843d5f7c0ee82294319cedeaac7a28c1931aeaae75caabc61c8d358768606`
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

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9f7911b9d823942a94ac5d21066deb3db1050f347dc4e31b763320052be2972d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3206043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80312b42867bf046de57a093e00d02858eb91068437f3704481d1aa636e6f4ab`

```dockerfile
```

-	Layers:
	-	`sha256:774bc713fbaa48094b5cb5c50ff25eaef315ee000af291979ed33f7b7b34097d`  
		Last Modified: Tue, 12 Aug 2025 19:20:02 GMT  
		Size: 3.2 MB (3199087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1a48768b3d5870b71532530290e42a80d6abecbd81cf5779ae252fe267857a2`  
		Last Modified: Tue, 12 Aug 2025 19:20:03 GMT  
		Size: 7.0 KB (6956 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2da2aa45b5d1791876b7ac43d16dfbbea6b74f4ad36cbf693288eb98bf7db0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35022310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8fbf7ffbf3d85e4abfbafef7c367df887471f81519267cfb7f8cb271ef6144`
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

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f5cbf11b9220fb4081c5a1647de6b16209ce8229503b6def431db3e7e369c078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3214356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf185b4d51ca702e663e0d8809ecd9891e9e159b97d3c83f096b7b761e36cf8`

```dockerfile
```

-	Layers:
	-	`sha256:51ae9461262feaf4a6cfb50093196c663da7e7de9dba6839fb5bb991c3449981`  
		Last Modified: Tue, 02 Sep 2025 01:19:53 GMT  
		Size: 3.2 MB (3207432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02a9b56050086e9bc399ed336c4f823a194551fbab2f0f76602304aad8a87149`  
		Last Modified: Tue, 02 Sep 2025 01:19:54 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json
