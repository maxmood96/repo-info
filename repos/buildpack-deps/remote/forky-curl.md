## `buildpack-deps:forky-curl`

```console
$ docker pull buildpack-deps@sha256:bcdb277cac9180bbdc46104713037071aff9747aafee1cc652960297be3294a8
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

### `buildpack-deps:forky-curl` - linux; amd64

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

### `buildpack-deps:forky-curl` - unknown; unknown

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

### `buildpack-deps:forky-curl` - linux; arm variant v7

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

### `buildpack-deps:forky-curl` - unknown; unknown

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

### `buildpack-deps:forky-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e058c22ce8cf26f7d2ecd2a316bbecbaab3dd2d8e83f933b9c89368e2b6eab70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74875718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c2e8d32669192f76833cb783825c0218c4e02f163183072c0af521f1649d5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c3ba40fb7e0c033b95f4145478256aa8b70beaf3f8b8ad41dc909fdebc63a611`  
		Last Modified: Fri, 08 May 2026 18:25:22 GMT  
		Size: 48.7 MB (48659751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1cc0aceec664d055c261d350fe983921369e3615a68574b4c33a17a625489`  
		Last Modified: Fri, 08 May 2026 19:42:46 GMT  
		Size: 26.2 MB (26215967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:56e0462a20e3f13ae986445b0d8717d76d988b4ec9c7a3f02ec12c1b89e50ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4088653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86c319eb5b12986d1e14d503be8da0d4b7e21c87897114857bfc6817a942c27`

```dockerfile
```

-	Layers:
	-	`sha256:217e4e82ffad45e0898aa2544c4e7ea322ad722c24c0ecb451ad5dfacfffb783`  
		Last Modified: Fri, 08 May 2026 19:42:45 GMT  
		Size: 4.1 MB (4081800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e31e4e5d7c57987bd97c87f4d92bed3d907d26e2d3856bd740b8ee0e50871c02`  
		Last Modified: Fri, 08 May 2026 19:42:44 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; 386

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

### `buildpack-deps:forky-curl` - unknown; unknown

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

### `buildpack-deps:forky-curl` - linux; ppc64le

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

### `buildpack-deps:forky-curl` - unknown; unknown

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

### `buildpack-deps:forky-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:794a72ad1719a38d76026083da28701aca448ed8fdd838e93fab1e32c9a1c733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73346996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4816c1c80a51e332923a685d95dc6b91e8c622f37832c4ef32a70d11fcd5224`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1776729600'
# Thu, 23 Apr 2026 16:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:04fb0dd36a6b62569331264b3dc244d1f567b4ad68c8c1b27f9d22978f421544`  
		Last Modified: Wed, 22 Apr 2026 02:14:57 GMT  
		Size: 46.8 MB (46771523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67bcef726e432bfd28120bec18ce459483cfe5851a88769e35186b7e9186e99`  
		Last Modified: Thu, 23 Apr 2026 16:16:58 GMT  
		Size: 26.6 MB (26575473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:255c0cef317740df143f2f1561d22a3c25b0bb46ea853e00578b6a7e8a519bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4071219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba18faaa72724822288b8d9985ced3ec9e3c4b8a1649c1055c519fc6cb5339d2`

```dockerfile
```

-	Layers:
	-	`sha256:37a4e729ed2ba75fe6db478c4b02ac32649186890c9ebf95c3f615c04230aea9`  
		Last Modified: Thu, 23 Apr 2026 16:16:54 GMT  
		Size: 4.1 MB (4064414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46ebedb1b9e2ba469f49a86488253cd01419a0f39a68c1757ea53a009dd7fe4d`  
		Last Modified: Thu, 23 Apr 2026 16:16:53 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; s390x

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

### `buildpack-deps:forky-curl` - unknown; unknown

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
