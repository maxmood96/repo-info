## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:4b15c25b02db6c8a6a22e48e7f0d285faf51ad5de9db58885e28ebda78045751
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:bookworm-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a878b4aebb8c4d59f5a5be65c1ccba7a9565156c17220da55594d7e3c7c0ba68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136906593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a618d38ac8480666de1c800b5a4b4393a310b5f6ab1b6d06581dff442cdc7c3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:05:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c237534654fe7a5c118fcee78652af952e57a4a07cc322c0ae3c367839bb0ccc`  
		Last Modified: Tue, 09 Dec 2025 00:06:16 GMT  
		Size: 64.4 MB (64396522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ba87277710bc6ac5aa9582896662e03790825bbf6ce0348f989d07512b9c2aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7972715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a127612264a1cdb670465c0c8ab908b8ccd9db915da5bbf5d4d55e056702c576`

```dockerfile
```

-	Layers:
	-	`sha256:1cb08006bf7e03dcc9c1ad259ad37a8745e6b3f5540277d12c6fd492c83defae`  
		Last Modified: Tue, 09 Dec 2025 02:20:48 GMT  
		Size: 8.0 MB (7965405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82e9c94b3bd142c7d64f8ab9a42a8e9c27f4d1ac41bb64c8754860ac593336ef`  
		Last Modified: Tue, 09 Dec 2025 02:20:48 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:bbd4f6da03529dfb14589a209c7df918127033f877671712320f0829e041cb10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130732190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5a5d69ed00bf5fd992e7be16a91544bac83fb2334ff34acd5160ebba217e8b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:53:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:18:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a635f54eaf3a9fce0549b1b49b875e73326ccbc501c3133d86c2ac8fd7828fb8`  
		Last Modified: Mon, 08 Dec 2025 22:16:16 GMT  
		Size: 46.0 MB (46015801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f70892cf40cf00afad948163124cb46c26422ae7a58c48384378f9afd91c3e5`  
		Last Modified: Mon, 08 Dec 2025 23:53:57 GMT  
		Size: 22.7 MB (22705745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8089c2b20fedea36afc932499843f6245377677804c10ff2c0e867c4b27513c`  
		Last Modified: Tue, 09 Dec 2025 01:18:41 GMT  
		Size: 62.0 MB (62010644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ab845668f94ccba327b50da933c5e05fa000029c1c4f0e74a9b1d6add6c79058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20825c4e9880fec13fd3b2e1ae2914726d7853f43f5c1ec43f0cfba87bc0bd23`

```dockerfile
```

-	Layers:
	-	`sha256:096cc9a75b6373f977afde282089af21fca7582a2fdf455d50470785f31e047b`  
		Last Modified: Tue, 09 Dec 2025 02:20:55 GMT  
		Size: 8.0 MB (7967263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f26e2b6a0c3640f557fe5739e90aef24156f8d318f864a397b60a3042545ce`  
		Last Modified: Tue, 09 Dec 2025 02:20:56 GMT  
		Size: 7.4 KB (7371 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ed928db37d4906fad5159c9067ac2ad085447ff86fc45bdf3ae603c549ecd9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125783601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec33167b2b0b801cbdecd7faa9dd87e7d5d02aa112f4120684344f60fe7b783f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:04:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:32:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c3d6a83e736aa77820543663b2d6579ddd98b0f465c0fcad8aa9bd98a5b72a9c`  
		Last Modified: Mon, 08 Dec 2025 22:16:46 GMT  
		Size: 44.2 MB (44196066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0a258ea9a718fb1bf2331996816ba335715a3c786bd79934d265fd78fb7f5a`  
		Last Modified: Tue, 09 Dec 2025 00:05:11 GMT  
		Size: 21.9 MB (21934635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66aa6761aa99c557c882b6cb71cf839a06b4634c5e4d98e4a93d946b4554c6f`  
		Last Modified: Tue, 09 Dec 2025 01:33:23 GMT  
		Size: 59.7 MB (59652900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9e7195ad66cd0a4fe8c0f3c9755ad2cee091853f7571d64fb16ec86c5ef6d505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185652ae0db8a275c635e37fd2f78e48ad83920a6887f63415e44ac515d89e46`

```dockerfile
```

-	Layers:
	-	`sha256:9fc07513510af84fc29bc742340a5bf5a9b0d54a7ac39dcdd7bb4119c9b28198`  
		Last Modified: Tue, 09 Dec 2025 02:21:02 GMT  
		Size: 8.0 MB (7966682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c435c4fa0890a45d9bb5365ca57e2c0fbba8ecf3476fa765e39a3325629959c6`  
		Last Modified: Tue, 09 Dec 2025 02:21:03 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:60c5491b5f504c9802b959bc053b92f8b00cc3773cf3e3b96071d1de1f8f5506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136328872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9594da32f43b559cc4182d237e1001b0bc07ed8bd1221ef41d3f160120c475a2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:38:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25d805ffe4d6247a3ab7494e663f6ae84d04e36c5270a200f1d1d34db32a26c`  
		Last Modified: Tue, 18 Nov 2025 05:38:35 GMT  
		Size: 64.4 MB (64371414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d38f3456897674e16e5dd4f76c775aabfdda78df3e6dbbf0a3afb02d3dcba8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7979188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35536d30e919872b14b8905b2f572b1f9f24f5a6b2beaa1c7da6e6d96d44d550`

```dockerfile
```

-	Layers:
	-	`sha256:a3e82f73958eba177c44b9a5dc758a964664d11febb5a65e2583e3972eb8e138`  
		Last Modified: Tue, 18 Nov 2025 07:25:36 GMT  
		Size: 8.0 MB (7971798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fd8854845629e842f3d16b729e56a0134079ec99340bb62e868e4ac8a839443`  
		Last Modified: Tue, 18 Nov 2025 07:25:37 GMT  
		Size: 7.4 KB (7390 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c21d7d6e43dd2971221e0c6f63ee31066994f64442fddecdcfbf175f65dff54c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140565016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600c16f9d364bb56f785e8372ac3f8e961d5c227cdc763eb6dbef2dc2e28df59`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:14:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:23:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5a0767b6533dfa923197197a2adf3860bde889326cc3199fec46ced873deb7e1`  
		Last Modified: Mon, 08 Dec 2025 22:16:44 GMT  
		Size: 49.5 MB (49466819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8c9cca3d9f455dde3fab1917d275b029f5f2978fcd1f8f1b757098b58abc9d`  
		Last Modified: Mon, 08 Dec 2025 23:14:28 GMT  
		Size: 24.9 MB (24864339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd442778352104a3bf918f8351b8ac2573f9aa7b0d9136092884f7f79017f9a2`  
		Last Modified: Tue, 09 Dec 2025 00:24:01 GMT  
		Size: 66.2 MB (66233858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d301abaf448cafafec0b1ee5ac21f34ddc27eef34cd8e2ceb418e8671e0f5fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7968852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b84f4d1d4cb072d336eb585911bb883b26b7321bd20030921fdef11e14b11b`

```dockerfile
```

-	Layers:
	-	`sha256:12412f14c9a0c794d3a3e9d29712248d0369d8ea2d5ee8b135affe2f804091e7`  
		Last Modified: Tue, 09 Dec 2025 02:21:16 GMT  
		Size: 8.0 MB (7961564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac1daca0ba9e0b99d2892906e8afaec176b91a7ec6716a848bcd21855bd453e3`  
		Last Modified: Tue, 09 Dec 2025 02:21:17 GMT  
		Size: 7.3 KB (7288 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:dc7da414708bb9f400864b40e99b2644e8d1b14464c3a577bdd6626f41c26959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135684290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a85a60561104e7f47d68629ca53643c8fdc21ebe32b516d2bd66ad92438dc3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 19:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:11:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6d4a3f53f449c0e9b84d889c71d1f21df5764d821465bd1337060660aa78c65e`  
		Last Modified: Tue, 18 Nov 2025 01:11:17 GMT  
		Size: 48.8 MB (48760956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754bf41c56cb3beefc6b6211c26bdc048d41c337f12bc0bbfcfa89dfb5de99b7`  
		Last Modified: Tue, 18 Nov 2025 19:40:58 GMT  
		Size: 23.6 MB (23614038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7a4cb619dbd7fcb3e0be3246f973ccbe692039c1fd01a193751c60045de0d3`  
		Last Modified: Tue, 18 Nov 2025 22:12:34 GMT  
		Size: 63.3 MB (63309296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7483e2f5aa6a5d102a7bf7aa7d3cad52a939107fcfa7499945663d0a58a2aa88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2d024e66befa5d9c67b7bcd36fb9c6a01f43287418b60ab667a5d16477f50f`

```dockerfile
```

-	Layers:
	-	`sha256:9f605995184cb2dc7aadc2355d7d34606ce9ba91f1695b36eea388afbc962b06`  
		Last Modified: Tue, 18 Nov 2025 23:20:48 GMT  
		Size: 7.1 KB (7143 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:54aaa7a023a00228a176a206fdee5f4449b8c6598c4142ddb7d662251fc61169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147845194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae534232c71e49bbb926c009cfe2855b3559ab58b28cbc059130273d27b7cec`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:21:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4109a037ac4c69c3ce26e6d14e10c867842083c363485abd63db45502611991`  
		Last Modified: Mon, 08 Dec 2025 22:28:59 GMT  
		Size: 25.7 MB (25672209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2b93c70c0b05a907d16ae217d77a407e9aa88f69499ffbfee4375b49ab6c01`  
		Last Modified: Mon, 08 Dec 2025 23:22:14 GMT  
		Size: 69.8 MB (69846008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cacb0dbfbb3d2db204ee7bd2cf74aa92456175e564bd6503e2a0d2d330cdddd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2f1010fc531d4476d125a4ff954efcad6e49f7d246805f8f72e610f5b8e49d2`

```dockerfile
```

-	Layers:
	-	`sha256:cc0e9b8313355630d7fa22455b2abcec1ad8712ab926fa5fb1204591f28f97d7`  
		Last Modified: Tue, 09 Dec 2025 02:21:26 GMT  
		Size: 8.0 MB (7973276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdeb553230d9cd2587c42a3529ece94e559f448bf5b27489563fd4b0c4283561`  
		Last Modified: Tue, 09 Dec 2025 02:21:27 GMT  
		Size: 7.3 KB (7342 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:36b27b0345efca0a3faf224112971842bc888aa8e1c16623b45682be1d9fa85c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134666268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7983ba75782de998c39275f1b8b2fdc525ce295b2bc6a2509703e275a4ecefdf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:56:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f80247bcc58a5a903807561f3aad626158855a07b7817a9ed9975e9775ae2`  
		Last Modified: Tue, 18 Nov 2025 04:06:46 GMT  
		Size: 24.0 MB (24027180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b099f215b279a7199da193e9e90d7e8e46ea9dfcda3ebe6c6379eb56d436eeae`  
		Last Modified: Tue, 18 Nov 2025 05:57:22 GMT  
		Size: 63.5 MB (63501447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:731b503260a52a68ff8fc60ff84e43af2315f4a7ea3113f0e049f57c96d24817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7969028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0caf03b920bc434f4e2dd0e9b73c1953ec26764148de538f7f31db573afc6dd4`

```dockerfile
```

-	Layers:
	-	`sha256:0eaf7176873b2fe9a2b8c2de2fd09e4c3e8e4612544c445e853be3d0330c629e`  
		Last Modified: Tue, 18 Nov 2025 08:21:12 GMT  
		Size: 8.0 MB (7961718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd23260b46a45272fda15fd6d4fc45103a7eba9fc6fc810ffdb972e736f96268`  
		Last Modified: Tue, 18 Nov 2025 08:21:13 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.in-toto+json
