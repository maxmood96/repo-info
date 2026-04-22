## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:600364bcf455186e12fbc75cc9375d36f2721285062a61e0e35c81b0cad872bb
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
$ docker pull buildpack-deps@sha256:f51de756ea8307fc039592b64364f9fb0f746e9c03e6c7da8c46ec264f0c6d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78177300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294cfad8d9fcb059e546a7c0dfa42e7394d01e2169c09151ea00749b16ac3925`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 01:46:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0c655e94b1afc0d0a4a69ff26686a8cb9fd0349459a4008b02fd7dcb3e6d3ab8`  
		Last Modified: Tue, 07 Apr 2026 00:11:22 GMT  
		Size: 49.9 MB (49878389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74970d6f811b29c802a9f3c8d694bfd2f422255c20b66bcc271ba0c7bcc9dbfc`  
		Last Modified: Tue, 07 Apr 2026 01:46:17 GMT  
		Size: 28.3 MB (28298911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4a59989cdfad3be8ebc844aec5cd89d1027fd7d5316f6847b250f2d88c7ca5e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4073083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad414e49a630ecf1d8cb569182c6c49a651469b7e8196c0429a5308bdc0f5e6`

```dockerfile
```

-	Layers:
	-	`sha256:c953a104f3c70ea8d78cfeae8cd9ca7fa0d70b97e3b99766b86ba08336c3e1d9`  
		Last Modified: Tue, 07 Apr 2026 01:46:17 GMT  
		Size: 4.1 MB (4066333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56ccbafea9b64cd15e8bf0ad97f7e7e9e62540f1e3504f167b2e84c258b7b670`  
		Last Modified: Tue, 07 Apr 2026 01:46:16 GMT  
		Size: 6.8 KB (6750 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a3e0d5a8487d4fed364ccdbbaf4f6c4eae82aa3d4eca63349c09285ae541bfba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83169879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47614eb7e8a505a4452711b26abbfe119221b5592d112e3b63b53a585e8eec55`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 04:21:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:82a75a893b6c64944c6f9a45687c1a1f96d90f40ac32f7359ffe0b6755458be4`  
		Last Modified: Tue, 07 Apr 2026 00:10:12 GMT  
		Size: 53.9 MB (53851237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b159d77ae23ff0a537f251333a902815f558c4d2eb7e7cb1124f2b5ba37262e`  
		Last Modified: Tue, 07 Apr 2026 04:22:08 GMT  
		Size: 29.3 MB (29318642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bda6ca762081affe9b354e6e88d9c4dab0ac76ff95ec4624021577626b80cd08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4079874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ca888256909a5170231f5af3961307d16ac4f29c55964d18c64976fb5cd7ec`

```dockerfile
```

-	Layers:
	-	`sha256:78916060eac2c475ee96b220ed8cf2691914e4a34e7830726e19f7eb40258a69`  
		Last Modified: Tue, 07 Apr 2026 04:22:07 GMT  
		Size: 4.1 MB (4073069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85c404b897d413a82c1ba9c1bba6793bf3e020b836d49a6ce42fd64364462479`  
		Last Modified: Tue, 07 Apr 2026 04:22:07 GMT  
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
