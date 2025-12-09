## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:238c77479311c9300309538e3d819e4d55697ad41b204e5a25fc42a658a306b3
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:stable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:903e73d5c28ee44e226e665a3ba9a9758acd5ad33a2aa095fa0ac345f7186114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142682030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee06f44d0350eca23332418ed3669bc28aa9218e3b76d697f549e2e3f17e488b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22766554d6bfa95c7325b00ee002f2705a7b8605908c3eb43dbe729c412422c`  
		Last Modified: Mon, 08 Dec 2025 23:07:43 GMT  
		Size: 25.6 MB (25613863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f2d358b447d091790c5ef0943550bbcf57bac46c4b8bfcfc3e6dacf4cb7969`  
		Last Modified: Tue, 09 Dec 2025 00:06:46 GMT  
		Size: 67.8 MB (67778647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d98034b4d5e2b6024a6e8a018a85ab1ca54012222983eb35095cb782905600af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7774675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795df1dbc76ae01e548ef6a81cdeb03db7baf6438a8204b040a81829d04dd47e`

```dockerfile
```

-	Layers:
	-	`sha256:7b19435cb4ecf7ba8a4c9403b3ae63d5bb71b7223b5832f5f2982b6e48ff7663`  
		Last Modified: Tue, 09 Dec 2025 02:23:00 GMT  
		Size: 7.8 MB (7767098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15cecc1aa7301ed302aa53c988000356716df72f57524961b337cf4f18b791a3`  
		Last Modified: Tue, 09 Dec 2025 02:23:01 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:988134c1629eaf2d345cb424aa531fa6784f2891e9ea2031ffe0c4886c78b6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137112744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f092aa99a71ed13000d3911bc1fa8fd3c63c91d199d987e095e1a02395427ef9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:55:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:18:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:123c232a33b986aeccb984e885244b48200c4eb4f9a811e3df109a416dc71f80`  
		Last Modified: Mon, 08 Dec 2025 22:16:56 GMT  
		Size: 47.4 MB (47448721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbaeb213e9fa41da55c6b895ce8273281464b3351c9fcf26aed8d0fc7484a18`  
		Last Modified: Mon, 08 Dec 2025 23:55:26 GMT  
		Size: 24.3 MB (24345927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4936999457f9b45cd7af5bc334afc3525d9cd25bc796f9420e78292f7e4e6d8`  
		Last Modified: Tue, 09 Dec 2025 01:18:47 GMT  
		Size: 65.3 MB (65318096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ce18051311c5fd3b83231605985260d45c68c441d2070efda94b7ba4c6d0887d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a30708ad3ea340710c5eb27a6ed5c84bbe789eebc4ac481667f8ea1db520922`

```dockerfile
```

-	Layers:
	-	`sha256:d7709b39b4a2d91d531f7699361a971cbceb57c7df089dc02efae0c561ac4f6c`  
		Last Modified: Tue, 09 Dec 2025 02:23:06 GMT  
		Size: 7.8 MB (7768136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ca6284e204edcd6efcd52de66a142472e5dda9e2163703939895e50c95ca86e`  
		Last Modified: Tue, 09 Dec 2025 02:23:07 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1da44fa5be4585765a1b5ca749bad86177075e5705e6ea1b77c2088d13564b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132051868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea8e2f984883244e014451768db5434417b032803995ce7e12ddcf4a1a6cd29`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:33:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c4eba7a08ba9825cabd599d8641314a004d500b627e05a38640b9d3c0bf389ef`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 45.7 MB (45718282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6ad1d8bb6e8d2c91990f13409d4d822c19a3b9fb5463aa9033cd860aaa4822`  
		Last Modified: Tue, 09 Dec 2025 00:07:27 GMT  
		Size: 23.6 MB (23620171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067e549495a4594bb4406cebf8990f1500f9fbae204461f2b793444540c774bf`  
		Last Modified: Tue, 09 Dec 2025 01:33:43 GMT  
		Size: 62.7 MB (62713415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6d38243bfa0994423da0e535141da1cd3b3b36eaa03f81ce5fcbbccb347d6bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71eeec56ac957cb9ee625a40933ed78a651366f2ae4a2a086c339bac928080a9`

```dockerfile
```

-	Layers:
	-	`sha256:e4717a6ea5cba2eabade23fa28e61b60b36f7a23db74e4050d75de3e2c12705d`  
		Last Modified: Tue, 09 Dec 2025 02:23:16 GMT  
		Size: 7.8 MB (7767605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d828fee114066f592fca5059c81fa4c7e30f719c7751b034255f06183cca2f6`  
		Last Modified: Tue, 09 Dec 2025 02:23:17 GMT  
		Size: 7.6 KB (7648 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2082675f8200ec3e813d2b879c951599acd992e804474c3fa890f32c8868120f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142256005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8bb37f8ef118943faee16135695230ccbb2f3285d9364560a5f93053b20fb7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14656e63ca309d8cfd09d01a9dbb3d1ea2d59a5efe7d40b9716f822e821385ab`  
		Last Modified: Tue, 18 Nov 2025 03:27:58 GMT  
		Size: 25.0 MB (25021011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9898fed0b4a62008cd3a65adf14beaff9f7a6dbe46176b901f31b3a21db4c6ab`  
		Last Modified: Tue, 18 Nov 2025 05:39:53 GMT  
		Size: 67.6 MB (67584762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a2057de3ad656df413711072abfa0315a1bea04f4e5ebe4d37def284860f03d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2370f9316268ff0f1d3c6345cc49d8981ba331555ed90fb29d762654d86486`

```dockerfile
```

-	Layers:
	-	`sha256:6b90abba9004b0c666c768f7afa5e6648513c094ffaadf84d3fbf4f2a4796b4d`  
		Last Modified: Tue, 18 Nov 2025 07:25:59 GMT  
		Size: 7.8 MB (7774773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13bc2c6b1fb0bc5b66745214d0c70b210e3b6b261460ab4402c860cc4318bfa8`  
		Last Modified: Tue, 18 Nov 2025 07:26:00 GMT  
		Size: 7.7 KB (7667 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:177671a6e5bb5f52f962bd209d1f4fce9659d62c38c0b07f7269ba869d077689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147372605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588e4717354dbf09e27823857537ad98a54bfe17f473662c084fb3f4479c5ade`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:14:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:24:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a63ab7a4f8b10d53e108dbe1e04ab9e369b75bfa91be99da84bbdfb688a906bc`  
		Last Modified: Mon, 08 Dec 2025 22:16:00 GMT  
		Size: 50.8 MB (50801649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d798fea9bbf98ef639c9ca23d745bec44c0d7b28fbd93792d4578fc5b43e7569`  
		Last Modified: Mon, 08 Dec 2025 23:14:38 GMT  
		Size: 26.8 MB (26776300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4d1731e98c6e5aff4c28a002263af9a4fc5c06d23cbc860d258dafbd603ef2`  
		Last Modified: Tue, 09 Dec 2025 00:24:53 GMT  
		Size: 69.8 MB (69794656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0026d50ee3ce0e9704c5ba3f22f7353e11f5e36a951a9ecbb0a66f8f72435dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7770783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d7d6d22b37b719fd5d712e37ba33cb6a919ffff234085a076387d8b7f7e567`

```dockerfile
```

-	Layers:
	-	`sha256:a29795adb99cab0e1b50a067f87ee91567b86bc4100ee3eaf831749041aa582b`  
		Last Modified: Tue, 09 Dec 2025 02:23:27 GMT  
		Size: 7.8 MB (7763233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b702d950a7bdd985614dd72722c20c761dce8e102e638f0998d6b4b6f1342e0`  
		Last Modified: Tue, 09 Dec 2025 02:23:28 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1a99f5c83d8fbddea17d00c4e9380178fab7e833e7d2934479906f5398daabb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153127307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6112f12909ae70305bcf7f1fb4ab5fefe35ffcfbaa00856920f8bce886807537`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ae38687874ad4b2ca525fe856d3d2a658b265c8f3cd684d6e8c1efb9f28a6bb3`  
		Last Modified: Tue, 18 Nov 2025 01:57:18 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a859b52534a1e3522c593c1835bd1bee34ff20a865f32f140257d45048a18099`  
		Last Modified: Tue, 18 Nov 2025 04:09:23 GMT  
		Size: 27.0 MB (26996919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba2b1a22ff6e7093fdd1dd2648adedf5202ef1304de7d17f711c19601d3a80e`  
		Last Modified: Tue, 18 Nov 2025 06:54:27 GMT  
		Size: 73.0 MB (73021903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:44d54013654f423b30611286dc39d13685cfb0a612d7316791f74361fee98f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7781835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796087633620ab195c4f5de5ee7e12d5157f002c12e332874ae4b9d7772d9319`

```dockerfile
```

-	Layers:
	-	`sha256:5c8ad47d2395a36a42430517e855c0b07f3e55e2150c087a7cb213bcf21dbb6b`  
		Last Modified: Tue, 18 Nov 2025 08:23:30 GMT  
		Size: 7.8 MB (7774221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61782dfb82b59570fd6e0aa6ff2c8a00fa86da489a71fdc3667b014657fd7456`  
		Last Modified: Tue, 18 Nov 2025 08:23:31 GMT  
		Size: 7.6 KB (7614 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:924ffd884e01570727de703d26ae0dea0dd1604f3e9c85e4ceb91612cc677e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139385892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5796e5655ad623f7799014b6935d28f268f08adb711c694472e5bbae988eadb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 22:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ed0507b92b5f6d1bbf086936336ca6e85b2d0afbbaab333064cc752190ce52b9`  
		Last Modified: Tue, 18 Nov 2025 01:45:17 GMT  
		Size: 47.8 MB (47771195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccc0dcc6b4231d5f1f223a1330c6630cb9406136f8e738cb2b0e628d1b35022`  
		Last Modified: Wed, 19 Nov 2025 19:38:34 GMT  
		Size: 25.0 MB (24953736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e592ded610a658bb788aebd62d933a07876ce0d2dff630e8511ac1eda3d0dbb`  
		Last Modified: Thu, 20 Nov 2025 22:32:10 GMT  
		Size: 66.7 MB (66660961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bfcb8c69548df6a7f74340a2d4163b0ea23b8f6f69ce6d00fa3f37caa2144035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7764548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1314230f267dc253ea996c17b9922b8946650ed819a259a6ad145660b87d7775`

```dockerfile
```

-	Layers:
	-	`sha256:a2e089966829390c0f9637532002fc0265450b99a5671c839ed9fad083615930`  
		Last Modified: Thu, 20 Nov 2025 23:20:58 GMT  
		Size: 7.8 MB (7756934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:246b2716222c918bd3f89389468a0a47e0077dc1012b81410c53a506f9457f6f`  
		Last Modified: Thu, 20 Nov 2025 23:20:59 GMT  
		Size: 7.6 KB (7614 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0a7a33d7eb4553375570116b5616d7761dc4d6e134d9c24900f1207bc54476b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144756609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd11f2ffaf6dd2bf261d3af758ab25ae16f2d013f989fc2ccda214682fe5ba1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:57:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:af4c50a2cf2848edb9e1797defa12d9a203416cf14b67469a37a418b1d0bb175`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 49.3 MB (49346014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f811fd500c593f696ff4afefd96c823d7f8788d50f510057207bfc40b4a405ca`  
		Last Modified: Tue, 18 Nov 2025 04:06:46 GMT  
		Size: 26.8 MB (26786539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4530c943529730620c01f6bab681e114e8a52bebc697a9164bab0bee08dc992`  
		Last Modified: Tue, 18 Nov 2025 05:58:03 GMT  
		Size: 68.6 MB (68624056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:768d572c83de365a61358fa92ec594649dae312db41d516d8f03b727ebd5fa2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2e626729d72d471e736047d9d196850c2cd8100e0bb3b4e26a47494851d2ed`

```dockerfile
```

-	Layers:
	-	`sha256:547c90bd31c78643ef1e73b5db9671a894bc6ab3f8ce6117e2eabcf4df3beb31`  
		Last Modified: Tue, 18 Nov 2025 08:23:45 GMT  
		Size: 7.8 MB (7768011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c23a9c5cb095ddc343ac0b2712073d4ea32905896e7967e16930154ff4fd19f3`  
		Last Modified: Tue, 18 Nov 2025 08:23:45 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json
