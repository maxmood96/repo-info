## `debian:forky-backports`

```console
$ docker pull debian@sha256:124a7ed133e4d4822c12c7cb240adbd0a4a5aed6b8619f579279a87fc6a3fa47
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
$ docker pull debian@sha256:750658e21b3092fffa3497701cd84e449ec7783b8adccc60e3dc41547f106c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48587307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cae5d3d3fdf2b0c671c41374690c4712277fe68c82307f34b27a0f191571f1e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 01:16:52 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a619bb3c1f14c591cc163d929ea3f43df5d6acebdd877fecaacf054d56531b3e`  
		Last Modified: Tue, 07 Apr 2026 00:11:23 GMT  
		Size: 48.6 MB (48587084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9d1a3e59b233ae2b108181d1a350f5e54b9f402b9d56256a46ffec0b823080`  
		Last Modified: Tue, 07 Apr 2026 01:16:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:86ed4fed9c889fa5a02780eda600533ba2241222fc6fbde9d1bc81e410bb23d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d63b23156c23306af3dd06a9633d930d434ce7bba96d4a94e6c8f3caeedac8a`

```dockerfile
```

-	Layers:
	-	`sha256:776afb870959dcb566b88c56da882dca6198a0234750e6260627d0b4418bfc09`  
		Last Modified: Tue, 07 Apr 2026 01:16:59 GMT  
		Size: 3.1 MB (3143288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96e479af58567dbd05b0fbc295d87e0bec27e5c2310a0fbe8f5c0fcef9d834a5`  
		Last Modified: Tue, 07 Apr 2026 01:16:59 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:8fd764596f578649f114651b8a683f7a7975a663479d079e931d2e99a83f1bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45541013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b6a23512cd9dd65e4731af8ba81d27ba340d14f9dfa8881542bd433e7b7e26`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 01:15:52 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:94c1a7288fb6578b9efe4cfec6d86c90bcbd7f6b3ded72757e8150ba2d22a63b`  
		Last Modified: Tue, 07 Apr 2026 00:59:45 GMT  
		Size: 45.5 MB (45540788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049956c913ce9295f077c313dbba76c105c8f9dde0d4599d29c5fdb2c7ac5d4c`  
		Last Modified: Tue, 07 Apr 2026 01:15:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d295849f964128602b0e01e7b9821049e63e10af6a8bd0d38a5efa0d0af6fe1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5df05338fee5bd37600f33819d963566fd8f74e77b5f0c62e813ebd155d200`

```dockerfile
```

-	Layers:
	-	`sha256:ad65cbbe2ec5f9c3857abbce24de2aaf5d81512e394e3160ba076dc41d477090`  
		Last Modified: Tue, 07 Apr 2026 01:15:58 GMT  
		Size: 3.1 MB (3144650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8ec636f63e9f80bc29bddae8d8da7d61cc8d82bcc6a9001887f729c696c660e`  
		Last Modified: Tue, 07 Apr 2026 01:15:58 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:1025ac56346ef65a90a699bea3166650f5a15dc9c343f29ce5ac5a7e88cb4a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48643580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ca7aef1fb28ca4deca7ab607d3c72d79b7acb33e49e892f2304c88dfea7abf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 01:15:54 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8be2228c7df976aa0c1c2333d6e8d72b206ff7533d4625ffeae3663f7240d98e`  
		Last Modified: Tue, 07 Apr 2026 00:11:06 GMT  
		Size: 48.6 MB (48643356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1f794e901c79cde1e2a6e5108efde7479c40c352c8d80267295f8eb6add13d`  
		Last Modified: Tue, 07 Apr 2026 01:16:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b51ccb44dfa27b19ee6d8d2eb005951b44af320c5d3d35a814dbaf468a11325a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a89d27c3fd3c1bbfd04de2b4384eb97c7060573ddd76dc0687d65c7a01b8c58`

```dockerfile
```

-	Layers:
	-	`sha256:746a67496e3999722b19f8faac535a01e8a03a3322ff79c11e763979b8c73d86`  
		Last Modified: Tue, 07 Apr 2026 01:16:01 GMT  
		Size: 3.1 MB (3149238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5e303e77d246c249e116803e7eca7c0667ead74400eb54da9fdab355a332a2f`  
		Last Modified: Tue, 07 Apr 2026 01:16:01 GMT  
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
$ docker pull debian@sha256:5cebaa5786f11ed84049b4d56d6d8dbcd3f2c41ee8810bff08adb3f1d163a936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48291819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1572e2b79b0725582363a263fb6efb12d496de14f739a3788526bcf4de127b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 01:16:12 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d387cf27b8c74bb29905817ad867265b401af02fdbc21b522a98041e86095a47`  
		Last Modified: Tue, 07 Apr 2026 00:11:00 GMT  
		Size: 48.3 MB (48291595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e90d5fd70db4ed371643a7f44072876fc70f52b29d34e3d6b4aae8562c5f16e`  
		Last Modified: Tue, 07 Apr 2026 01:16:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:930c41e7d860a95b2bfd846ca8235143670ad2f898007cc0b2e47e55eb266d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286dab71f53e0b6efc33683b5ab02db51b03468568166e0ccd93ce7616f5ef4d`

```dockerfile
```

-	Layers:
	-	`sha256:34650cf1fb412c0f59e6e12bd2cbe2f69944d8a172757a1189ec55511d3e1ae2`  
		Last Modified: Tue, 07 Apr 2026 01:16:32 GMT  
		Size: 3.1 MB (3144739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:738495c864454df0eb624fdb7479e15aa2196408bebaf583a9df15634dc1de9a`  
		Last Modified: Tue, 07 Apr 2026 01:16:32 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json
