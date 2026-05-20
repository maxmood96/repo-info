## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:a7bb9819c2080a6ff7b0cd8ce763a2fbbc0bca8f28cad5961ebab6ecba6e4445
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

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5a70bad6584206ca70e7f3f001aa9e9777eb9f767e205f16ac8354c553a6b076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152489582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32365da3a306301ee60c7f36392540c9540c4ed3c441f2427ddcfe14dbe3057a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:23:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:30b85315dec2d58f35c416abc0e468c9a5fb485e83af8c76ba1b33292e721633`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 48.7 MB (48697206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2642fa4ec2a9746c709cd3ea129863f7b5d0a1937a5b2a2f95a75245bf1fe8`  
		Last Modified: Tue, 19 May 2026 23:23:23 GMT  
		Size: 26.9 MB (26891116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4107cf9efb8684cd0abf2860b1e6b4e583e2c7f47cdcfb7a25f6b4e3148e16e4`  
		Last Modified: Wed, 20 May 2026 00:26:36 GMT  
		Size: 76.9 MB (76901260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ccc0a408cff3c324872907ba7b8c843f2a0dd482164cf92ef342f6387c29e0d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8277618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f115e234d2df405fd61e51f249fcd8fd0e0a7e105496570d7217034a65f238f`

```dockerfile
```

-	Layers:
	-	`sha256:e585307c1cf9344ae6d8eef4461a1cfb0e51f2de2861812435d12ab3d3ed2a33`  
		Last Modified: Wed, 20 May 2026 00:26:33 GMT  
		Size: 8.3 MB (8270352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46edbf089d160a1b8f9cef1b81703f2c04e7aaf68d6ebd3cb1004643aeb9165e`  
		Last Modified: Wed, 20 May 2026 00:26:33 GMT  
		Size: 7.3 KB (7266 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:52ebda8eb909bef1a5f10e3e56c865775d8f264a686f60815a1978c6fc5083e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141623399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39aa74206478b774023ce5aa1f54d3ba7a61fa94a30fa8b93be508df331c483`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1779062400'
# Wed, 20 May 2026 00:03:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:34:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b6df9d4a408084133e98c8d6c8e0e3de38b9e95851bc2206e09b39135c71bba1`  
		Last Modified: Tue, 19 May 2026 22:36:31 GMT  
		Size: 45.6 MB (45603185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd97129e166740f6b7d385932f0e29058407c0b25cd1d04df0d94fe382e494c`  
		Last Modified: Wed, 20 May 2026 00:03:41 GMT  
		Size: 24.6 MB (24602913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f41170f5eafbd474b965f1d2e3462304d25531cc0394b9f6f241c79cc0af46`  
		Last Modified: Wed, 20 May 2026 01:34:40 GMT  
		Size: 71.4 MB (71417301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0e938159b873af2a78df83c3453d170502071b694b31d806c7b1c2119290adef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8277587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a0ee5d129f4b29ad1f20ad8edd0599878726a189f8852b61f9931a27d15bc2`

```dockerfile
```

-	Layers:
	-	`sha256:4f7c16e75c3f66f9666e42cc17a5df6aba42029649c9bfefce45349a0d72c19c`  
		Last Modified: Wed, 20 May 2026 01:34:38 GMT  
		Size: 8.3 MB (8270257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b75e84de9fefe783eb1d129ebe6ae2b8e46a7b268ea242e89cf882fa7b5af60`  
		Last Modified: Wed, 20 May 2026 01:34:38 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:caa6e6aa0e557c2fd87fb915158ee287321e0ab10bda51c7f8011096395f174c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150956189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7112756433a60cebf376f713a43ce9c9c9d58567cdcbadb608433bebf2b2a0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:26:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d4360d64f4e71c17817e39372cada00ee239c7d2715cf79f6e6cdc602a7cd46a`  
		Last Modified: Tue, 19 May 2026 22:36:44 GMT  
		Size: 48.7 MB (48720031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6efa7756521280bd54091d885e5326bdeb8ff205564db4dd0b7c81ed203199`  
		Last Modified: Tue, 19 May 2026 23:27:03 GMT  
		Size: 26.2 MB (26170165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c09d09dc4bc7143e7855d920786955805f4275e7095dd6a2b7367a2b39b19c`  
		Last Modified: Wed, 20 May 2026 00:27:51 GMT  
		Size: 76.1 MB (76065993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dbd06290390bddc8fe6e60cca0b8a7a90d2073f6c9b9c1666aa643676e8c19ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8289200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a13da6e45009ebf07679b8be6b88d757f3e24040b2ca50e16ffa018e289a69`

```dockerfile
```

-	Layers:
	-	`sha256:d463e67e0d6302246e389968cb87955721599f77ff3091948f4154ca38e76026`  
		Last Modified: Wed, 20 May 2026 00:27:49 GMT  
		Size: 8.3 MB (8281854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:928cd655fa68ee434588acfe49f55256703fd4e9db8c1dc8a18649e1ac2c8591`  
		Last Modified: Wed, 20 May 2026 00:27:48 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e0529bebd0c2a2ef3900e5327e86ea1cb605087a2a3d2e49a4f8065140b74939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157282963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819b979713e039c0870a561602ad3151837b5474fe2ed8d96442f9f5b71a9514`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:45:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7af1962edabe3d58af5fbd06f3e345528b78b672a4b879b72fcf2e0d92549637`  
		Last Modified: Tue, 19 May 2026 22:36:57 GMT  
		Size: 50.0 MB (50001944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3497fcbfcc0cfec531a77167884014e2e81ee738aa6aca34516d78ed1b945bdf`  
		Last Modified: Tue, 19 May 2026 23:25:23 GMT  
		Size: 28.2 MB (28207970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696b7c5b17f8f533e68966e1ba0cf608f2e2d4de56a6745dbacaa12f28dbc238`  
		Last Modified: Wed, 20 May 2026 02:45:41 GMT  
		Size: 79.1 MB (79073049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:298b967855372184d51991bc7e705e47bb5dd68bdfdadd8de5887b6f8d557cc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8270636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9012e7880b0ab1c2ca7dced71cb6291bc5ab88c094fa9beb13b99eeeeb52a359`

```dockerfile
```

-	Layers:
	-	`sha256:8c2b6f8d8b9f52cf369467774f0108a7677bec3799f1373d59f9db93210ad618`  
		Last Modified: Wed, 20 May 2026 02:45:39 GMT  
		Size: 8.3 MB (8263392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54427c944227a3ca23c91e2e1bac87b9cb032b665e764a6a323911e08c3ea959`  
		Last Modified: Wed, 20 May 2026 02:45:39 GMT  
		Size: 7.2 KB (7244 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f23a656104ff37603d66b08dbadee385f3d034582f12cfcbab57ad51b4009a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166751228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40118e7055f963d9315f64da0ee4b73e7f87a60d74de651e5397695a0ab2f62e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1779062400'
# Wed, 20 May 2026 01:13:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 06:51:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2e5564b9da7290f7430ffd86cfc5f2b22a68586fade0aa81c8610704c43fd41e`  
		Last Modified: Tue, 19 May 2026 22:35:40 GMT  
		Size: 54.0 MB (54021281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24877c775bac285836892c60f877392eff4299b16fa48a35fb91c222b64558d`  
		Last Modified: Wed, 20 May 2026 01:13:54 GMT  
		Size: 29.3 MB (29285894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4dc79d08e369fda0605c037025da8b1333ff074dcf4bb801aa3f65c8ba0a35`  
		Last Modified: Wed, 20 May 2026 06:51:44 GMT  
		Size: 83.4 MB (83444053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0e5269854ab2c6d586b111a966c6bc3631a411c6a7d7aa8b07675a6a9fb15c3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8260159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278e6ab5856a94fd1a4d23d1bb65cbcffab583f07989ec64cef3d616e4f39d0f`

```dockerfile
```

-	Layers:
	-	`sha256:03d62303dc507ee61bc6cb27960caf658e491c81b9eacba9d7fedc882256a369`  
		Last Modified: Wed, 20 May 2026 06:51:42 GMT  
		Size: 8.3 MB (8252861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4595418f93ac97cff4bea8c02008a38b099d87ab6d13f67d11d7501635c2c01`  
		Last Modified: Wed, 20 May 2026 06:51:41 GMT  
		Size: 7.3 KB (7298 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:dc8cfd1189b5089bd2875e9012b107b317644e29b482808e73159a177856bb1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149359183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d557709bdcdbdf3d696eb7d51da5cc149e77819bd1a7a31dbabafdd87835edfd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1777939200'
# Mon, 11 May 2026 00:48:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 May 2026 00:34:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f7ac0cf25d901b0f78c05ace03b84988d685b5007a5c2ecdb859ecb56d3b46f4`  
		Last Modified: Fri, 08 May 2026 20:22:22 GMT  
		Size: 46.8 MB (46773178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3f17a612f2a3435e0c1ae9abad061b774e7306b25478218d81e34d30f64a36`  
		Last Modified: Mon, 11 May 2026 00:50:05 GMT  
		Size: 26.5 MB (26492191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16d7c25eb5f654458e4aad845eb30dee96526bec66f681e9ed9963f8a04e964`  
		Last Modified: Tue, 12 May 2026 00:38:40 GMT  
		Size: 76.1 MB (76093814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ac3c71ae72020555c3ef30e42d820e7047c3b2e7589e52ba823c066a5401dd4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8271897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fa0143d7a0fc94d2922d84ce5b84d9fc6faa00e518fe8075004d9de2b4771c`

```dockerfile
```

-	Layers:
	-	`sha256:d2c6c0141667df41ef72737b9dee05d15393614fb844a995530bf1fbb0ae6de5`  
		Last Modified: Tue, 12 May 2026 00:38:29 GMT  
		Size: 8.3 MB (8264599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05e0dbb8847e27df57bd15eb511abc778dd5083b7cb6cf83840485267f3b507d`  
		Last Modified: Tue, 12 May 2026 00:38:27 GMT  
		Size: 7.3 KB (7298 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8c5afe481f44a83465a4102b438b1a1ddd1793eeda8f82b40a90326d14d4a211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152552766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee0399bcb4b7e5bed3a93e13d8a4b144ec84c9c555f51d084031f23e5e9850b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1779062400'
# Wed, 20 May 2026 00:18:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:05:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7394ea10bf5bc140ccf55e31841e993aa40f4cd465376d373dbae4fff2479c30`  
		Last Modified: Tue, 19 May 2026 22:35:35 GMT  
		Size: 48.4 MB (48440526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fee0ef4f478ac4a827949260fdd413d25005b05e8864d837f644813aef5311a`  
		Last Modified: Wed, 20 May 2026 00:18:29 GMT  
		Size: 26.7 MB (26688667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee9f47b39dcfa33283603429ed1ce4fdc019feaebe8a99bcdad2e79cfa369ab`  
		Last Modified: Wed, 20 May 2026 02:06:10 GMT  
		Size: 77.4 MB (77423573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3f3c27407b25a5b1de0d0b3444e0cba975992de093c57157ca12f08a77652b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8253027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6165f4324bb403da31998678db084e31584508c7d33999ab3f0774427d183872`

```dockerfile
```

-	Layers:
	-	`sha256:ee2060f71bb86b48e9fa31bd928a948f7ec9769536292f7de81d322fb10c91f8`  
		Last Modified: Wed, 20 May 2026 02:06:09 GMT  
		Size: 8.2 MB (8245761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:878cf6ab19775d9efcbfa978f393ff41b1926b9bc8283422d5e060ef19f4e7e1`  
		Last Modified: Wed, 20 May 2026 02:06:09 GMT  
		Size: 7.3 KB (7266 bytes)  
		MIME: application/vnd.in-toto+json
