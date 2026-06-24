## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:4fcd8b79e4033d61567329602efb0ba4d51cf9323d1b9c9df5da147f6427e035
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0e867891d7ef01b68f61aa6209c4d66ba007bb892fd7fe2d7b93298e9c478b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154872819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c32e898b867781e0dd97442321b08aeeddd6a7f16cb63b919c932d086849b0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 01:41:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:28b937e10116ada256c357287a871c307568d210af49526b0b54d19c0dcdf5da`  
		Last Modified: Wed, 24 Jun 2026 00:28:07 GMT  
		Size: 48.8 MB (48778379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bdf1cc0f4003e9838db969a7f68f358aa3694f09878b6330bfb2bfae2ae4e1`  
		Last Modified: Wed, 24 Jun 2026 01:41:40 GMT  
		Size: 28.0 MB (27989488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d77188881b92a70e569a04653be1cc5a84ad94e829327ec62634c158933342f`  
		Last Modified: Wed, 24 Jun 2026 02:29:06 GMT  
		Size: 78.1 MB (78104952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b4a44b979382603d472afe3cc71fbe90e8d420583517a1f589149db3b485844a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8320107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fae39992c55cece40b8f26b7348767148c715dfdb639eee808f60114386daad`

```dockerfile
```

-	Layers:
	-	`sha256:ade4ea344bb1cd9cd7585d63cb6f22f6de4fd52e2253d71c549c0e1d3bc23494`  
		Last Modified: Wed, 24 Jun 2026 02:29:05 GMT  
		Size: 8.3 MB (8312853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3f8c700ca45713d58cce4ec13ec45b155800e35d60ddc628e6984e398625630`  
		Last Modified: Wed, 24 Jun 2026 02:29:04 GMT  
		Size: 7.3 KB (7254 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:06a1519d8b9f3e4a63f245955e2a270693c66f5f8e7d1ca5a04bbc979cd96b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143587403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b462465103f53d35f3b398fc9092379714a00a608e45bb53211ab571dd74fed3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 02:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 03:55:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d675c589a8a116f3580b1211f18fa575a815f4d2314413ec9c2112d3a61d24a6`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 45.7 MB (45678632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0274b6b7737c2b06a1765a2a054ed7c230000ea352ee09b5b9399df372d1dcb2`  
		Last Modified: Wed, 24 Jun 2026 02:24:52 GMT  
		Size: 25.4 MB (25374390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37df253c6d6f378f0518d7aaea7ba33d75f20fbe83a7121d649368c54d82652`  
		Last Modified: Wed, 24 Jun 2026 03:55:35 GMT  
		Size: 72.5 MB (72534381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0b539976fb0dbc7c987293f0d1834164018070900013470158affd9c56f62818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8320085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8565a96f36367555d19ab8d8b86beca1cdaa6b17ce880bea813a83a238b4da`

```dockerfile
```

-	Layers:
	-	`sha256:45142c4b3d5f0558077f1f345db734346827be98b6111eeecf8dea42f375d793`  
		Last Modified: Wed, 24 Jun 2026 03:55:33 GMT  
		Size: 8.3 MB (8312767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:191553f808a7bf40fdfb85404168928e43c63a28ecbd0ff4d378e2a813187640`  
		Last Modified: Wed, 24 Jun 2026 03:55:33 GMT  
		Size: 7.3 KB (7318 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:70e0593742ce975409951fc394cc1079bef0606c40583b02335e2256d78363e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153211779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73892e0504629b0e3e058f13800229cb5efcf57e911cb9ee83944dcf2097ad64`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 01:45:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4fddf52615bf1690082a9d73cb8346614997b5b51315236c93a190fbd50fb899`  
		Last Modified: Wed, 24 Jun 2026 00:28:05 GMT  
		Size: 48.8 MB (48798835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbfb65123f81cd28e0545a5e6f88cbd0f9d83e9d96851b068d4ef01e4482bd0`  
		Last Modified: Wed, 24 Jun 2026 01:45:17 GMT  
		Size: 27.2 MB (27192471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c9b6ebce9bb29252b4739ec42144f45c77d93770495e8ba1aae33ce9e58fdf`  
		Last Modified: Wed, 24 Jun 2026 02:35:47 GMT  
		Size: 77.2 MB (77220473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:689f656ca55aa242c1f8f75d31928e839025be1ef51d2ce5715f1750f5748c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8331692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0da19cddca0febe2526342a47aa8e744af623154983f19d717abb79d15da1c`

```dockerfile
```

-	Layers:
	-	`sha256:c7e3f35de97477fdbe9b8fcf53d473536fe4122e5ebfe4bb2eef4ed59c222090`  
		Last Modified: Wed, 24 Jun 2026 02:35:44 GMT  
		Size: 8.3 MB (8324358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb141e6e0518222bd7a80dcda823bcdae55b649a4039c87dd11f277c20915155`  
		Last Modified: Wed, 24 Jun 2026 02:35:44 GMT  
		Size: 7.3 KB (7334 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:84118c5e659f265a1708829394063698b84adf38d3106ac1f7e558e391588027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.5 MB (159452310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc87f539f024db3deb914f53993dbc157e6e31b76b57e9195af36a4cac6300ab`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 01:44:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:35:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:466f7f9acdfac81cb720fa13d53a50111bee95182357f963947200187b3ae3fe`  
		Last Modified: Wed, 24 Jun 2026 00:28:18 GMT  
		Size: 50.1 MB (50080955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4172c1f095cffcf024eb812b3d434c5ab119bc7e7ccee1fb4953b378a0a4d2`  
		Last Modified: Wed, 24 Jun 2026 01:44:15 GMT  
		Size: 29.1 MB (29117405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68037f55168642e1ecd0f5957b88e504644e3dce1e630af8a3fb3bd84570fb1`  
		Last Modified: Wed, 24 Jun 2026 02:35:28 GMT  
		Size: 80.3 MB (80253950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5bfa4d0a1f1856f2935982aac926aa5a405d7e6649926291aed9757bbc11bb92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8315577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fdc285c7ce0ba7d212cc36c25d4cbcfdbd38dd9a67c6476aab9feeebb5363e`

```dockerfile
```

-	Layers:
	-	`sha256:edd3742030f96c32247e1e2ab4bb56a96f6561452665c794349e8ff099cc4d4f`  
		Last Modified: Wed, 24 Jun 2026 02:35:26 GMT  
		Size: 8.3 MB (8308345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b75b7d6d15fd8ae2450a3a5e1cf1e2c2b7e503f0741569483b9c67f7c21d4cb`  
		Last Modified: Wed, 24 Jun 2026 02:35:26 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6a5e2b30c7a4b91f7629880ad95dd4d860e9e350ce0ca15511f11fd001a71201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.2 MB (168234605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8fd016749ad1ff8f8ca98767c8c7203c41be5cfcf9cb32096a389b910b454b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 04:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 10:27:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1e0ce2460747d14df6cfd1da4b61c0c9b7caf034c9fddf19fabbcba65c2416ba`  
		Last Modified: Thu, 11 Jun 2026 00:23:09 GMT  
		Size: 54.1 MB (54132513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86f91ba1bf8c0d9e7dee82b12886a4f7ee70c339c3778c5cf99a230830c8d7b`  
		Last Modified: Thu, 11 Jun 2026 04:44:58 GMT  
		Size: 30.1 MB (30117465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a0b6bed36d53f6ece4654f5cea50eb41e560afbf8d24b742882a59a9592eec`  
		Last Modified: Thu, 11 Jun 2026 10:28:41 GMT  
		Size: 84.0 MB (83984627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:20674aac81672ea98ff47a36d451e39477dc7afe25812ef841d4c1582eaafe88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8262210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1e07013c41fac64464c4bdd30f5344638d9815e832680b7166e15b2223bbf7`

```dockerfile
```

-	Layers:
	-	`sha256:15a8e2342c439e8e61963390a51cb03948d70e83f975b2b3c4992b991db5bc99`  
		Last Modified: Thu, 11 Jun 2026 10:28:38 GMT  
		Size: 8.3 MB (8254924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fe5f7903250a5abb330029727f1f043ff61f0205de5bfded645fe0eb10f3d95`  
		Last Modified: Thu, 11 Jun 2026 10:28:38 GMT  
		Size: 7.3 KB (7286 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:c27d61c614331da4fb3550a76f4c36c981d00000fe172a57145a32dacac306c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.8 MB (150797317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea26ce57af4bf26742b37f315902123012a0fd9063a74b79298f29df58a79e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1781049600'
# Sat, 13 Jun 2026 04:41:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Jun 2026 16:58:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e2efc7e0091930e45ea6218e0e9380e67d07fe2085c100b1d3d74190636f5938`  
		Last Modified: Thu, 11 Jun 2026 02:48:51 GMT  
		Size: 46.9 MB (46911636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b18596f8f629861877fe419ef9028caff67b10f2dba8a160480c551f8733fcc`  
		Last Modified: Sat, 13 Jun 2026 04:43:12 GMT  
		Size: 27.2 MB (27238456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbc93acbb612bc5718255bceb11979ccddc1f5a211420ca842ecd80d9a0dd40`  
		Last Modified: Sun, 14 Jun 2026 17:02:53 GMT  
		Size: 76.6 MB (76647225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:285485ef814d0dd3f39c75c128f227adb265b6bca9f79910be3d6ddade286fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8270118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8484b8597e5ca78f7de528ef2762813726454f37cb5784bab1fefb4c2947e2e`

```dockerfile
```

-	Layers:
	-	`sha256:fcf2c87ed39ac47c154a7ece2f3b78714199b79d317fa75352bffa3528803ba9`  
		Last Modified: Sun, 14 Jun 2026 17:02:43 GMT  
		Size: 8.3 MB (8262832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc6d275291583f2a161114137a1a8d63f486758a44897711c886b9179be46a0b`  
		Last Modified: Sun, 14 Jun 2026 17:02:40 GMT  
		Size: 7.3 KB (7286 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:96755743ca0196d408d033625157e2658f275b3af1c19450a6c2127cd7642a49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154729115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a664f484b8ee3b0a70cade4e04723ac4082b93b5db049b60c95ab3e794d0be`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 02:46:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 04:30:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1e9b72b44a72df002ca2c8ad8ccb65d46205892b54ff8d9ce0b5dd7be73544fe`  
		Last Modified: Wed, 24 Jun 2026 00:27:46 GMT  
		Size: 48.5 MB (48517796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d84ec64f6d4462ee570697b4fa616aba8bdae3a994fb4acb8bbc6decb3dc15`  
		Last Modified: Wed, 24 Jun 2026 02:46:41 GMT  
		Size: 27.6 MB (27576084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2315ca2dba4029f39e8aa110e548aabe9feb723a2f86c4188fe0abcb26f9073c`  
		Last Modified: Wed, 24 Jun 2026 04:30:52 GMT  
		Size: 78.6 MB (78635235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:de70214ee0bc93c7688bf0ff5f6db3a53dbd837ac75011377f72ab94c5dc8263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8294183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1dc608dc018ea644518a99911ef054896794290b5c053c8f575677a7d1f2a2a`

```dockerfile
```

-	Layers:
	-	`sha256:68de21d9e63d61eda2dd72a79b7f347173482e3e8de9e15a21d46a8e37ec508b`  
		Last Modified: Wed, 24 Jun 2026 04:30:51 GMT  
		Size: 8.3 MB (8286929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe50f596b5f0157dfce53187542bcad97f3b245ef77be6b97ceddc186e239b59`  
		Last Modified: Wed, 24 Jun 2026 04:30:51 GMT  
		Size: 7.3 KB (7254 bytes)  
		MIME: application/vnd.in-toto+json
