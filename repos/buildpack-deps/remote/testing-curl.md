## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:38cfa38ae78a427a498e4fbfa91a4ee782711a697f68ab64dad734d59aab97f8
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

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4cf6fb9cb4d32dc95c6a5107b9645d4315c5b2e391e8e382d1eb90409690c83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75705653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65155a39c4c75126853cb798a20437f7a48abb2537f782ffe70e658a4a1fddc4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:39:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a35d765211154bb582ec48d2d95cc0c5953f360f8d0a39b91475c8b05f9c59a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:42 GMT  
		Size: 48.7 MB (48697651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e592cd2ed9323d51731ff2e060da4790d904454d4dd8c0f58dc124b12854233`  
		Last Modified: Wed, 22 Apr 2026 01:39:43 GMT  
		Size: 27.0 MB (27008002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:98cc779f13cb55833fba8113be734f3e00e23254a07741d0efc50260f51d1aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4079485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7904dae17d5d4d76bda22a974a90ed63df03767b0242e6072d1021a5ace8c41`

```dockerfile
```

-	Layers:
	-	`sha256:7db6d07dd8a9fe4d7393744da5fd53b75b9b5ac105fd9a2422d4679ea6b6b623`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 4.1 MB (4072712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc202a9a1d8a2da4823f9e11d17b9f94495907388f16a154fdd3239b4024884c`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:87da8613e6b0d8c245f4ac73c5138901293426f5bf052089fe13927fa3a8c1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70308023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3734638dfbf6e20e75a804cc5b375fd9284f111329a8cae235b9c732c57023e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 02:18:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:616f54f84dee8932180832c344695078e63789301eb12467ca880323e3400586`  
		Last Modified: Wed, 22 Apr 2026 00:16:48 GMT  
		Size: 45.6 MB (45622135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61970639d217085f63010f6da0cad6e9f8e048924120803b4eb157ac1c2f651a`  
		Last Modified: Wed, 22 Apr 2026 02:18:59 GMT  
		Size: 24.7 MB (24685888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bf7f4098d5168cc59a03ff0b21140269c4c4733f18202961542c53dda15d6063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4081039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681930e8ece6108c389ba4016eefefcbbf9ae63a6ab2fcf58d7517fecca13d3d`

```dockerfile
```

-	Layers:
	-	`sha256:2f1a81fad2d5cd86720f328d7dd46bb1bce069350b7028929df9f5b8db3c2787`  
		Last Modified: Wed, 22 Apr 2026 02:18:59 GMT  
		Size: 4.1 MB (4074202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e344c0bba41f0e480cdf50a8ad58805ff226468e679240838a2ecc12806d6d1`  
		Last Modified: Wed, 22 Apr 2026 02:18:59 GMT  
		Size: 6.8 KB (6837 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:955f699e004a8f753ff9447da371d56eba10f0c437841f09a130e625b90bb5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75015316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9934d25c134297406ef0427de3ea65a849dd834eca461c4a227fd0325613ef9a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:43:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:52be3b7a34a0f7d63c36fadfd1767c3f064e11b65df7fb6243fae9b94dd9f7c8`  
		Last Modified: Wed, 22 Apr 2026 00:16:24 GMT  
		Size: 48.7 MB (48726104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7406cf4524d3710a69a6e4bbba357df8393b55da990695b89997aa04b54031`  
		Last Modified: Wed, 22 Apr 2026 01:43:16 GMT  
		Size: 26.3 MB (26289212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:289b3a4b120e468ff0f3077584d6b0ae0f83fb95c18118c52749509c88f03ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4086205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d53a617b74cac8a7932d72bccdf6777a623f2a38f0e57439c408c7a79fc7387`

```dockerfile
```

-	Layers:
	-	`sha256:a74570b4ad2bfce5c992455a0d8481898f446582fe6fc452019d8ee032a5e4dc`  
		Last Modified: Wed, 22 Apr 2026 01:43:15 GMT  
		Size: 4.1 MB (4079352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce1aa1db3398395dee7e0732a16ffe2d23d0c0f2be33d4c07b26928106ba5080`  
		Last Modified: Wed, 22 Apr 2026 01:43:15 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b3a75f1d4cbc77918659ed2e0182d30ff879ee73e781f80950ea0f692cacb56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78267420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669c33a54872f6b8e0e17f40c3b11555c35e0959143b13c26dc571c75333f932`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:42:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8e493ed078c2b75bcf190124b24d66f817692d9bedad987963efb47f7e3eef1b`  
		Last Modified: Wed, 22 Apr 2026 00:16:48 GMT  
		Size: 50.0 MB (49982635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c764a369daed85f9b52e15146ccfcd0c76380aeab0914a25d45d32d7e95e4f6b`  
		Last Modified: Wed, 22 Apr 2026 01:42:57 GMT  
		Size: 28.3 MB (28284785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e3e7dbd8b1690b5f5a719fe2f87938a760b5375d4420e0738a4a6ee2d711a364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4076568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac5dc063d530a50a4df7a0c16e8076f2f2808f43536e94fb7258d312e16286e`

```dockerfile
```

-	Layers:
	-	`sha256:1a92c642f62fb946b4e54121833f716bef25333072aa0116ee27bae00e31e84e`  
		Last Modified: Wed, 22 Apr 2026 01:42:56 GMT  
		Size: 4.1 MB (4069817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc3daba3fa20acebc43613e935d3d0680687e68cabe72fb6474aaf72727ef22f`  
		Last Modified: Wed, 22 Apr 2026 01:42:56 GMT  
		Size: 6.8 KB (6751 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:150857d6543a5c4902140a3e1b4a49d722eff865e6206065932f9f1ee6032e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83389972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5010380ed706d8f1faa8d3e1d94f247021f7c70ae8a71bd1dd0d116ccd52fa4a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 03:39:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4acf335ca95a581f78a61de78111418bda596ddf71257299393203995ee7ea4f`  
		Last Modified: Wed, 22 Apr 2026 00:15:35 GMT  
		Size: 54.0 MB (53983935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d29dcef074d70bcd1e851f17e286abd94e829b11cf89631a079de7a5d724304`  
		Last Modified: Wed, 22 Apr 2026 03:39:43 GMT  
		Size: 29.4 MB (29406037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:85d811eb0f3cc12ba03584ec5a461376dd0e692a30228c57d53566ae18fad359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8b509d5d131c9fd05470ca265dffa62a1513526082603da847eba854b1b7d1`

```dockerfile
```

-	Layers:
	-	`sha256:86e500d8ef6968ef116171bfab436a592c67a071db1bed17e6176318913ff2fc`  
		Last Modified: Wed, 22 Apr 2026 03:39:42 GMT  
		Size: 4.1 MB (4076571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73bb9f584f5fb8bc03e53234a89789ded7a208c2f5afc248436cfa481f1f3df9`  
		Last Modified: Wed, 22 Apr 2026 03:39:42 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0966b65c98817e56af7e5db9f6bd1d905937423853f4599185d23b24fa59278d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73279026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5840e3a4c1f30f903ec830dc928fdb79eba3d8dd1e8436910bac2c526eba4fe5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1775433600'
# Thu, 09 Apr 2026 01:46:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:63b5561c308233dcf634aa914acd8af4b95568018df569d4d43c4791c98cc9ba`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 46.7 MB (46698175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d867396e8c8691cbd2e099e7a0d3c7c33eed2261193868cfa5cfdebbe037af`  
		Last Modified: Thu, 09 Apr 2026 01:48:33 GMT  
		Size: 26.6 MB (26580851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5c27fa34de88c83d4221f6907e20288faca4aeef0da72a090ba3758ccb9f9c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4067715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d28d2cb4b6ae5202a26ac8ca84c0d8ffd43832af50b6a567fabc7601cf44a5`

```dockerfile
```

-	Layers:
	-	`sha256:a636ed630bcb591975c3ca18b939776f1831812f22d0441f2657b78918603a12`  
		Last Modified: Thu, 09 Apr 2026 01:48:29 GMT  
		Size: 4.1 MB (4060912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6ff9aea7718b8a19ffd3e59ff9a806546b115f6c0bfb778c46b7aa699d450ab`  
		Last Modified: Thu, 09 Apr 2026 01:48:28 GMT  
		Size: 6.8 KB (6803 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0a183517d3483df560a44ecddf11c87fa3f9bcb726d70956f0ec4708e2d0e138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75188844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b5bb34ddd71f5f61fc319fbc2dee617e23b9c04e9cb37ea5d230054f13ba8f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 02:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a1060191b9434ca828b6395f3c2782a999320b4babb35dd20cb17592437fdf4a`  
		Last Modified: Wed, 22 Apr 2026 00:15:37 GMT  
		Size: 48.4 MB (48407607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca628a02ce8552e3ffa145824b47810287e1d695728e354379828ee1a246028c`  
		Last Modified: Wed, 22 Apr 2026 02:32:22 GMT  
		Size: 26.8 MB (26781237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2bbe6bef658c6ea71d8391a249ebc7f752676ff99e9ea9083d25295f5dd0a70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4080896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a0ad29266d9d47192a9c1ba3e19879a525f3bb2e810a27a598d6a7975e9415`

```dockerfile
```

-	Layers:
	-	`sha256:6b22089c50f8f19b2f07ce6f7964fa7a3165787bd55f9337b7c92374868eb566`  
		Last Modified: Wed, 22 Apr 2026 02:32:21 GMT  
		Size: 4.1 MB (4074123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdcc756731611418f89babe84b1ecbefa536c5e05f5fe2122bfc222835fab6b9`  
		Last Modified: Wed, 22 Apr 2026 02:32:21 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json
