## `debian:forky-backports`

```console
$ docker pull debian@sha256:173296c35a8343f396383ae3d24de55518a6312be3e005874a5ed34988b2b1e2
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

### `debian:forky-backports` - linux; amd64

```console
$ docker pull debian@sha256:7593cb55e880c3197c305d6b831ec0c12775b4505aed7c8b27ed1808d8c5e5e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48697874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e1255afdd61fde7ef9b0fd0ba905d0c901d9c56aa131e01f27dfdf75fbfac3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:15:17 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a35d765211154bb582ec48d2d95cc0c5953f360f8d0a39b91475c8b05f9c59a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:42 GMT  
		Size: 48.7 MB (48697651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6c74281c042d5d7fa47d470453e7304fcb2b265aa1db0a1161caff50fb0d47`  
		Last Modified: Wed, 22 Apr 2026 01:15:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d960768096a14eddf89b24f2823d07060a1ffe62ef3fdd8bccd28e42d2c1fff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a00a3da738b741481e0e87ade68ba508c1f3b0a5551363873e7cc225ccaecef`

```dockerfile
```

-	Layers:
	-	`sha256:ef207794418a62c0c668ae533897da6f4a882064f8a610c30a6d9ec3885f0c86`  
		Last Modified: Wed, 22 Apr 2026 01:15:23 GMT  
		Size: 3.1 MB (3144420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c07742210db24a758ba0e68f7cbbf5d9b601985d11a64e667a14bc424cca824`  
		Last Modified: Wed, 22 Apr 2026 01:15:23 GMT  
		Size: 5.8 KB (5777 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:e3da07f78a6bda8137e6c7b448b72e35e6bb0d8d74f63df7ea7c0d455269abdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45622357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46445d6bf349d594330beb63501cc9841721522c84f87a8a5593e77e83a49e93`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:14:45 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:616f54f84dee8932180832c344695078e63789301eb12467ca880323e3400586`  
		Last Modified: Wed, 22 Apr 2026 00:16:48 GMT  
		Size: 45.6 MB (45622135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e35b6098fcbc50b673c70c4698f3a6f61f9bde6e3140f22a04908996d7317cd`  
		Last Modified: Wed, 22 Apr 2026 01:14:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1b1b897c0debb0e100fdd4ca374b7b1217465ddc5db33d9b434267ec65203e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b259d2cf7a7f2de1620f6215f92261fb3df80e1d9d46f7c8cddac93bdaf09b`

```dockerfile
```

-	Layers:
	-	`sha256:2e5094be9c1d9ed419445eba7941edf28686c8f63c9c2dd33e21f10a709f8311`  
		Last Modified: Wed, 22 Apr 2026 01:14:52 GMT  
		Size: 3.1 MB (3145782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c98e51b7801eac6c28b1e92c1a56922310687114de1bb409342afada79991849`  
		Last Modified: Wed, 22 Apr 2026 01:14:51 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8d1af21f6dd8303c6b603ea13f83040c5fac2bce6eec0f3a425c0e02686ccdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48726327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f7ec8670f15b4bf228855835d030cb560c4a0035b18a33edfcfff2c92c1cc9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:15:07 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:52be3b7a34a0f7d63c36fadfd1767c3f064e11b65df7fb6243fae9b94dd9f7c8`  
		Last Modified: Wed, 22 Apr 2026 00:16:24 GMT  
		Size: 48.7 MB (48726104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd818c77a824a7888f038607139377c5826f920280b18a2665b94966dc5cef16`  
		Last Modified: Wed, 22 Apr 2026 01:15:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:bc7431a31a5692181440df564924426f5f0fb55e69cbf50bab843c408b8f2d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b4df41bcffca58c6d3e2f5509ac9b4003da10dbb2bd127fc4ae94856bd6201`

```dockerfile
```

-	Layers:
	-	`sha256:cc72c3cf169ffcb1eab70273452ca2dcbbc8c8957055c69e96b7277954638a48`  
		Last Modified: Wed, 22 Apr 2026 01:15:13 GMT  
		Size: 3.2 MB (3150370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:359dc98dc80add5c7c6e90995bbba20ce431d5fcbf1d2df181e8090902772219`  
		Last Modified: Wed, 22 Apr 2026 01:15:13 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; 386

```console
$ docker pull debian@sha256:01ee765bdc43a237cd6ea7cc382d9d6df7222048cfbc7f49b81e9e5458e90a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49982859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc499b1d3557466ea8ea564a4d8775d45f8f4d64faa0f449d22bd82c6eb468b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:15:23 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8e493ed078c2b75bcf190124b24d66f817692d9bedad987963efb47f7e3eef1b`  
		Last Modified: Wed, 22 Apr 2026 00:16:48 GMT  
		Size: 50.0 MB (49982635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cccf9d0700bf50fcecbacd03c0bfab024c0d6d1703c4b9cc7125c44f6e2abe8`  
		Last Modified: Wed, 22 Apr 2026 01:15:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a7a547d2038b34724e561f0ce39967182dbf9626d6f5f27c4aba879c51de3577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3147381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85442ee2a0c5999e204898f46de1f1b9768629976eefc5952e458f7b1aaf7b50`

```dockerfile
```

-	Layers:
	-	`sha256:168d5764e74a26d41a4d743a2b72b52a755f25b5b21659f61a0f24ec3e80d99c`  
		Last Modified: Wed, 22 Apr 2026 01:15:30 GMT  
		Size: 3.1 MB (3141620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0980fce6903686f2dc3da6e153d4dcc9dd7650c3eb8c3f3e9165576af8ddbbcd`  
		Last Modified: Wed, 22 Apr 2026 01:15:29 GMT  
		Size: 5.8 KB (5761 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:231540dfe76a8a8dfed38360933ea000bcbde36db7d78e9e04492a52eff38194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53984158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df95a56c89361967c861a137f77b0c4ce88767e99c1056f09c0a9b40e6087e7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:13:55 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4acf335ca95a581f78a61de78111418bda596ddf71257299393203995ee7ea4f`  
		Last Modified: Wed, 22 Apr 2026 00:15:35 GMT  
		Size: 54.0 MB (53983935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a91ddef1d76696c891727df851e11a5fa9a27e7aa158fb48c15cd443f7d4362`  
		Last Modified: Wed, 22 Apr 2026 01:14:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:14c76aea2e8535d852698ab50b270dda93eb85468463e4f4c015cb9333daa4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a5de1c82003816b5dba1f569519ca0d4cdb063036d4c8f1100404014b68499`

```dockerfile
```

-	Layers:
	-	`sha256:699376a578ac6897dee0ea9786e88e5e2a9373599da20529da62a8a83482959a`  
		Last Modified: Wed, 22 Apr 2026 01:14:18 GMT  
		Size: 3.1 MB (3147925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dba3ab8246b705427a4364ee3a18ee3c85374c9f8301d1e6156ff953e1be18e1`  
		Last Modified: Wed, 22 Apr 2026 01:14:18 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; riscv64

```console
$ docker pull debian@sha256:bc4f3f0eccc6f1af7010f81235da244d6cd8e57b7d7fb56bf35788a25da96c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46771747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba503b185dd1fdeccb5e196740afeea4203f97d451cad6829d7ee6d8df027b86`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 05:55:42 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:04fb0dd36a6b62569331264b3dc244d1f567b4ad68c8c1b27f9d22978f421544`  
		Last Modified: Wed, 22 Apr 2026 02:14:57 GMT  
		Size: 46.8 MB (46771523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9dfb5ce5da29c7eb899dc5bb8267d2db95d4cee8224c3da3ef8362aa7c751f`  
		Last Modified: Wed, 22 Apr 2026 05:56:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:529dea12026d6331377885003b390d5f3691e8bb1c8a8e9421bc33dd4ea9fdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3141732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1baf6641f6cb6512799a4158cc8f43c03a5fe044fc716c915820ebb2ee1af789`

```dockerfile
```

-	Layers:
	-	`sha256:6e7030fa9fa8577c9e789bad81e0605790e83b2a7b81bc6b5110ae986e2ec431`  
		Last Modified: Wed, 22 Apr 2026 05:56:36 GMT  
		Size: 3.1 MB (3135928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fa9ebf0b926727254d0f49148310018796cbb7637ed30be91f1826e291f9ebb`  
		Last Modified: Wed, 22 Apr 2026 05:56:35 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; s390x

```console
$ docker pull debian@sha256:bf3bf117ad43105b42d238abdb3bb040dfbf9330cda733b9f68ddddfeec6448e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48407830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ad2c6fecd30b0d263dc95130772d03e1c56efdba4427a4932593ca10849002`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:14:14 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a1060191b9434ca828b6395f3c2782a999320b4babb35dd20cb17592437fdf4a`  
		Last Modified: Wed, 22 Apr 2026 00:15:37 GMT  
		Size: 48.4 MB (48407607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e420abc5e1c7dbc86ee00841d055b43274192ba9ad91bc6575bcb8d3c78dee78`  
		Last Modified: Wed, 22 Apr 2026 01:14:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f19f17dc47c506c5e41cb60a048a9cf6967faa8a40f2a36d73edacfbd13894f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc163fc1b079bd99dfe9046d4f57cec246a5ac3e1472273e3a5702019ea5360`

```dockerfile
```

-	Layers:
	-	`sha256:7e5bc743df469cc383f46aeaafd31aa316fbf2dc7baa1255593fa867ca1d81f5`  
		Last Modified: Wed, 22 Apr 2026 01:14:26 GMT  
		Size: 3.1 MB (3145871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77a367838525b9aa537aff5e36e98a3416e58d8a8920cc10c5e655cb68147c0b`  
		Last Modified: Wed, 22 Apr 2026 01:14:26 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json
