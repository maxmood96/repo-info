## `debian:forky-backports`

```console
$ docker pull debian@sha256:f12dbd44657562dae2e3fda03f7269c325519bdd5b644b662754c2062f970ef8
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
$ docker pull debian@sha256:7f34b0d26e0ac0a88d70c975553bb0525b576923871197b767b378db3ae319c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49878613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0fafb7560fd770cfbb0c45eaa524020e7ecffc8ed943ded22f2a34d7dcb29a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 01:16:18 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0c655e94b1afc0d0a4a69ff26686a8cb9fd0349459a4008b02fd7dcb3e6d3ab8`  
		Last Modified: Tue, 07 Apr 2026 00:11:22 GMT  
		Size: 49.9 MB (49878389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c320069844fca5f57dda0f39baecc89bb8f86d72871cbac5bdaaaf14d1210ca6`  
		Last Modified: Tue, 07 Apr 2026 01:16:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a85dc9db536857c4a2e1fd0707367f8c09d1196864324de2019f15a3247157f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10180165a40a6c8e9cbe7ae73e50abe16d532bf5626cd2388d401d8f7cc462fa`

```dockerfile
```

-	Layers:
	-	`sha256:bf049fed9a89b8f6b61408079f59f1c02d3d5983ab58b0c82102be7ab30e4706`  
		Last Modified: Tue, 07 Apr 2026 01:16:24 GMT  
		Size: 3.1 MB (3140491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39cafd857f03cd705ac043f512c1fa735fb9c27dce324b4c0125ac689d1bd2ba`  
		Last Modified: Tue, 07 Apr 2026 01:16:24 GMT  
		Size: 5.8 KB (5760 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:abf80881169f7fd16a0433824658e96d0c4d149eb88557c2e491e3d5bf56c06b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53851461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afbccc1e15e382634be2c45c6d33fc5b5748e2a0fbfba3baf419409875031ac9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 01:15:32 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:82a75a893b6c64944c6f9a45687c1a1f96d90f40ac32f7359ffe0b6755458be4`  
		Last Modified: Tue, 07 Apr 2026 00:10:12 GMT  
		Size: 53.9 MB (53851237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3849c24d5af186a284b9fd91c6389720576428b468e3bed852abc09c69b0d4`  
		Last Modified: Tue, 07 Apr 2026 01:15:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0ba25250cfaa8055089bd48cbf3e82e335ad643522016bf50f88ab988f97f78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059135bbef4a4145f29b012cf62726791f7dfd9a86353599eb52eb307631e1d3`

```dockerfile
```

-	Layers:
	-	`sha256:17566a286084cf771dd45741ea289c98f07c362ce15edff69333c1d29aa66e87`  
		Last Modified: Tue, 07 Apr 2026 01:15:47 GMT  
		Size: 3.1 MB (3146787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a537d3136ac2c4f606888ada73a2191f30e617f0ba9d169a516f31521761d42`  
		Last Modified: Tue, 07 Apr 2026 01:15:47 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; riscv64

```console
$ docker pull debian@sha256:3035c8e169fd59a578cabbe540500e6e704f6470bb62884b929e4081c3612b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46698398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43624d3a0eafb022b3b75a8d48364548ac8c63a782c0a26c8e08087bcde96ad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 02:27:38 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:63b5561c308233dcf634aa914acd8af4b95568018df569d4d43c4791c98cc9ba`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 46.7 MB (46698175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdba16343bc5bb0220400df93d9f261dd2a17b0c823515207ef5eb721cf6557`  
		Last Modified: Tue, 07 Apr 2026 02:28:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:56e5ad02375fd009d7422ff140464b303482f6f6c55a8e8b1f1562f10e219ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3140594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ac65795acdb2e41050bc7a137a4a4a312d539b18b4a16ec1d82ad0504f34675`

```dockerfile
```

-	Layers:
	-	`sha256:d649afef486dccbe7f985d9adeb3e908a0bf8eb57c4972448d331e1503af86d2`  
		Last Modified: Tue, 07 Apr 2026 02:28:30 GMT  
		Size: 3.1 MB (3134790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7dcdf6d87cbebf23b6d1150f4037b3f56a5f7330b59181685cb43a2acbea58b`  
		Last Modified: Tue, 07 Apr 2026 02:28:30 GMT  
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
