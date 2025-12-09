## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:20f27a1555bfb1f72e960b03989d631ff0153f970c6bc924738b4cfe397f6d5a
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
$ docker pull buildpack-deps@sha256:f460ef13ace7137fad0fb59a2c9a89b8cd5038c9e7fc324fa208680f6365f18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142256181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121f4083b7b0b86207004cacb9187f5d609368886b3b8623f4e7d29095a3cc76`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097d536d3c26abbb49039062f8d8e471b0c97bdfcc2ecfcfcf56545161524fb`  
		Last Modified: Mon, 08 Dec 2025 23:11:17 GMT  
		Size: 25.0 MB (25020941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb13e64d383cee6a152ac57ad29b9b1116554b1c9daab0e94464d674f3804db`  
		Last Modified: Tue, 09 Dec 2025 00:12:25 GMT  
		Size: 67.6 MB (67585014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a03d57fc9906a1586274290a665945d438af2ea5a0eebcb4a6613cdee837bb12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0008300288bc680a9b8f6b90457920a0fb5df6bf1d3991a05098b89a840e44ad`

```dockerfile
```

-	Layers:
	-	`sha256:174af0b91c1cc6f5d8d0f844dfce41ae1b11c1a16d0c8087036dcc371a822582`  
		Last Modified: Tue, 09 Dec 2025 05:21:54 GMT  
		Size: 7.8 MB (7774773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d1119836bfb1360428d51cf1a69a6634ddc5fde2ab2d8aadd00e66cc737d12`  
		Last Modified: Tue, 09 Dec 2025 05:21:55 GMT  
		Size: 7.7 KB (7669 bytes)  
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
$ docker pull buildpack-deps@sha256:9be638afc4cb836aebc740382a2c5fdcb2e2f9c516855273f3768fdc81adb845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153127339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31355cf61aaf7c221b5bfd3e2125f67c7f70a2149bbd8d85eb216459631c04fd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e79cf54a8287f03b9105a7213ef3a99e05832db0bdcaf506dd64b872bddfd7b`  
		Last Modified: Mon, 08 Dec 2025 23:23:25 GMT  
		Size: 27.0 MB (26996775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbdd943d24ee93fc3b0013d3315e9ace0f4529c7fcae39b318579723e579b6d`  
		Last Modified: Tue, 09 Dec 2025 02:13:21 GMT  
		Size: 73.0 MB (73022086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9b65a039736fa0712f8adeae612d6c130342741ab1d1235b4920d70a19b841b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7781836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417182257df48eeeb32025e981cb561778957cee4821e6dcaa0081e53d1d3d56`

```dockerfile
```

-	Layers:
	-	`sha256:837d7ea9030b359fddae4bf5b73777bd28084f48c7cecc7e257caf34a8d97827`  
		Last Modified: Tue, 09 Dec 2025 05:22:06 GMT  
		Size: 7.8 MB (7774221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dcd6abd7def16fdf778efd1e76f1bc398d9fecf4d4c826152d42141b8b7653b`  
		Last Modified: Tue, 09 Dec 2025 05:22:07 GMT  
		Size: 7.6 KB (7615 bytes)  
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
$ docker pull buildpack-deps@sha256:cf5a4571c21f1a0834f8ca434dbd52a07b66a8c841eb98db2d41582d925644ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144756770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2800fa55610b95d68f94c44c804f6b85362bae87facda03ffe29c1ec35b727`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:47:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98c145469a927f8321c172bcf0ed7919725c5f02b2fea3f4d05ea5083b4b8c0`  
		Last Modified: Tue, 09 Dec 2025 00:12:09 GMT  
		Size: 26.8 MB (26786516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a105dbf5cfcb4e2c38a6c33b07d696009c0c1ce742a7404e87b258f0914a1424`  
		Last Modified: Tue, 09 Dec 2025 01:47:55 GMT  
		Size: 68.6 MB (68624346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1e4f862c71e06995347878d4f7391bd7d9bbab590c29768e96eb728c9408143c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c637b2a4b6fc11a753f8b8e894c70ba016a47223536032067e2a64adb9d31472`

```dockerfile
```

-	Layers:
	-	`sha256:b3516f174b88fe3a07591f25fa495aaabba3bf7f9888a99f1f2a823b54c98ac2`  
		Last Modified: Tue, 09 Dec 2025 02:24:49 GMT  
		Size: 7.8 MB (7768011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cca90cf7e56a630dff6d199d4421f2fced11652c81d76d616763ccc983768ac`  
		Last Modified: Tue, 09 Dec 2025 02:24:50 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json
