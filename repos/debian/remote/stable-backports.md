## `debian:stable-backports`

```console
$ docker pull debian@sha256:88c6ef04d978cd2ada373a21cc22febe21f9e6e9a710d1d7a3c153c4c78153fb
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:e9b9cb12a4532f568bf76a23e3ff5422965734436bdb1b459b2f772b84e39805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49310848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a085c300d5ec987d307099156b8769ef9bfd5f60522896b11c779ab2f6a87ef4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1779062400'
# Tue, 19 May 2026 22:58:30 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:02403a7c7b54f96f85b743b5fa0711b127e5017a48db3d024adec33a72247eec`  
		Last Modified: Tue, 19 May 2026 22:36:52 GMT  
		Size: 49.3 MB (49310624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23170b4f205a27cdf5268d8c381882a118b3b04ad256cf97a7e623d3e2ef17d4`  
		Last Modified: Tue, 19 May 2026 22:58:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9bc41716acdb86aef4bdad9a061714e7ecabbb4c5f6aa6f9b054bbc69ca55e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a56ce6e10ffad990a8da82d62d62b3c528094ba961c823ab07393c83e79d6adc`

```dockerfile
```

-	Layers:
	-	`sha256:46932f91da00f5f1d0351462d237b5381871524602db8c45f4fa25ea428b898c`  
		Last Modified: Tue, 19 May 2026 22:58:37 GMT  
		Size: 3.2 MB (3170955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea35af03f267217a5e0d1d800c51e2acb080d53a712c8716a0600be1b056d759`  
		Last Modified: Tue, 19 May 2026 22:58:37 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:89567688cee7e9a7132d3aebffd8fa1a8e635c231e503836000bcef2b5ff3c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47488269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8389b16d8f4d3d6798762942e2b17fb45747dacb1b22a5e5cfa2aa34d725144e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1779062400'
# Tue, 19 May 2026 22:57:08 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:04266c847c8cd13eb385dc7e561f70f41a8a214ba1a8489822b77a063e597694`  
		Last Modified: Tue, 19 May 2026 22:36:31 GMT  
		Size: 47.5 MB (47488046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0418b764ec16291249436a709dcba0363faa0e1beff8d9801e6e0cf0cc5e984`  
		Last Modified: Tue, 19 May 2026 22:57:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:19ec11ed11df06d2fcc1692f8d668e58d63e6c084245d81d9cfa32af14b578d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b64e7d1020cc7b306d1f5daabd5a6757f5cbe2790f77486866c5f6e40ed729`

```dockerfile
```

-	Layers:
	-	`sha256:75d1b4bcbae078b768699438765fca5748eb164d2bbdf9dda3d66f1c3012e49b`  
		Last Modified: Tue, 19 May 2026 22:57:15 GMT  
		Size: 3.2 MB (3173892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d98f21478f245db25e9b9d921748487351ae54e8136c67d137d28fd2e6988779`  
		Last Modified: Tue, 19 May 2026 22:57:15 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:8e014447edab549bc873f6c357cbff2a04f418c0404e85fb56b4bb015b1fa4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45742259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac775ce8cdadb352d3b5a972cdb16a4c8bd2522126c555cc29eb1bc21ea4317a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1779062400'
# Tue, 19 May 2026 22:57:28 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1835be7a986c6ce252412b4618e22ef1c6092cf889c683a5d26a09a411168004`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 45.7 MB (45742036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d8be44132109463ac521007e13408c7e3475ad9a78d4d573fcc422efd4d0ad`  
		Last Modified: Tue, 19 May 2026 22:57:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:87bfafed0f56c123942ba8a7cf3897d1eca12011dbf63e757bc363c4c3f89c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b7c589be3354e6fd442e47d38f7c46ff2500bd84f957e056c5a78650cffc5a`

```dockerfile
```

-	Layers:
	-	`sha256:7cddc0bac430daffdd57dc47322d3c96731aae2fd005ad84e07d85ef6c5437d2`  
		Last Modified: Tue, 19 May 2026 22:57:35 GMT  
		Size: 3.2 MB (3172329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58d9c42f6e83755d49131d30c3367c6a1f1371f4c785dd4a499d87e90b2be104`  
		Last Modified: Tue, 19 May 2026 22:57:35 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f4efe817437fffbf289013ab6895ea67f0fd6b4432b6e603f64d3956481126a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49672440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bcf763a34b5093e697403bc63683709914b5f4c88668cc38bf51a15e7943dc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1779062400'
# Tue, 19 May 2026 22:55:41 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c87ec3b8ceeec4c29d991a29a646026aa4878eb6788572c2bcb9a2f5524916bd`  
		Last Modified: Tue, 19 May 2026 22:36:48 GMT  
		Size: 49.7 MB (49672218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f902c719ef6c3ecb946c4cc430e997af6598da4bc6b4bfba1e07eae62eff712`  
		Last Modified: Tue, 19 May 2026 22:55:48 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c5dfb8f220118f761c2996c32c59cd5cf00ac7a98f6589b447f4837f3f6f0cd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c330facb500f1eead0de7ffa2859a45605688129566d01ee384cda108bd3f9`

```dockerfile
```

-	Layers:
	-	`sha256:b7c7229a820020ce9fd8192e895ba3986a537dab9356934038b68d03110c6e70`  
		Last Modified: Tue, 19 May 2026 22:55:48 GMT  
		Size: 3.2 MB (3171799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f6009f12ac1aa40da622424393e5df245e8b0eae89c96c3de2da2b7e4ab2527`  
		Last Modified: Tue, 19 May 2026 22:55:48 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:b8158c51b2f69768a99dfe6b7c6bb8d5b552aa261f0170d401191fa2b2109aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50829776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aace0a462f0bed42aea732d4790d0e096cf8503880b09131ca02ac9030c1d64`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1779062400'
# Tue, 19 May 2026 22:57:53 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:01c263b7fb0dee8e1ce69aa4821aeee0d0b3794d888011c7377115d62034e55f`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 50.8 MB (50829554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f48d520a33729e6e97cd86e1440492a8869c8f97db736b3f8490be324a5acdd`  
		Last Modified: Tue, 19 May 2026 22:58:00 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:77ec7e834143299ee57dbe57a3e7f82b5c7d0ca2d3c094ce4a25f46ada6c3f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade3f4b21f4456d6f9b1e869d89af8bbd6130c908c51efa80359b71af201f6e6`

```dockerfile
```

-	Layers:
	-	`sha256:f0f36b93cec9f4a8eb9f4723282188836f5593ce67d84b5f85ec31e155250ca2`  
		Last Modified: Tue, 19 May 2026 22:58:00 GMT  
		Size: 3.2 MB (3168157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab666f33dae225220bcaac6b3cff97bd1860b15655771add20f51001e9ed71aa`  
		Last Modified: Tue, 19 May 2026 22:58:00 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:0eff0b3bd6b8900bb96c6553b5ce98d6f9f5ceeb2694f13f74d8e41b503a78e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53132401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7e84ddeb62e75603a91ea4c661dee6adfe141a35d883de687e7e269528346a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1779062400'
# Tue, 19 May 2026 22:56:01 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:86d0d3e18e233beb7ef1f2174145e73e9101bcde6ec6bfdadc484fb3e927c1b0`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 53.1 MB (53132179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76c1b8b946cd2d86a3822a53cc0203b5bee8f50d2f8e0e32a4c8206d98195d7`  
		Last Modified: Tue, 19 May 2026 22:56:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:18f4454b7daf05641f154c83472dfd9c04952164f11758477e2484e612d768b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3af42fbd08b64978d9b8c0b0e542ff246185d586bc832732e043acb0cee9285`

```dockerfile
```

-	Layers:
	-	`sha256:69c49851dd42d2a7049195c386a151ec6b5502c38469000a30dccfb59c3b7f9d`  
		Last Modified: Tue, 19 May 2026 22:56:13 GMT  
		Size: 3.2 MB (3174468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4077404237bd54c55bc7b0165dcca7cf179869029c7833b40528e46eb58c9e8e`  
		Last Modified: Tue, 19 May 2026 22:56:12 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; riscv64

```console
$ docker pull debian@sha256:e3783e4e045daef46f6fba7f2167bb2838108fc085158eed53f15fb641438d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47796488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:334c3d28f6378c6aa90f8e20b434f95cc6e9e9f75d5368745057ed5bfa8998a7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'stable' '@1779062400'
# Wed, 20 May 2026 01:46:08 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:50231e3e29c227e9c827d501e4b2b6ca59a487369ac285149c2863b26496abca`  
		Last Modified: Tue, 19 May 2026 23:42:57 GMT  
		Size: 47.8 MB (47796265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62c9d62500d9f3178eb84e27ac52395834abf80bb4a92e0c2a310c7dd4ee465`  
		Last Modified: Wed, 20 May 2026 01:47:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:557d0b6ad1393b01fea9a152a69103a45af41b13025e50825bc1852dd13702c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c74f41ad5d07b2345c0b2ca365cd83218f1cff7af63f09563c57a3a5af173f`

```dockerfile
```

-	Layers:
	-	`sha256:fb8ab41c31da1e0d84a9695a6691133d53e4a960642673a069aac38a19efb05a`  
		Last Modified: Wed, 20 May 2026 01:47:02 GMT  
		Size: 3.2 MB (3163280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27ceaee335a5b1b71ea97c0be24722e5463d56f99db194dfd15c0b6dccbdd332`  
		Last Modified: Wed, 20 May 2026 01:47:01 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:0c99b36a54cac47434532ddb2ee50b200bf9213b55b719c453271bf96769e003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49380006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aba07fe60f2c83d5d4e234a76e494da7f48c7ef537285516172033d52f13436`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1779062400'
# Tue, 19 May 2026 22:56:01 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e6ea7a415613e4493b14172dc29da346239d3314dfaf2d594e9b9caa3a24f856`  
		Last Modified: Tue, 19 May 2026 22:36:31 GMT  
		Size: 49.4 MB (49379784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76c1b8b946cd2d86a3822a53cc0203b5bee8f50d2f8e0e32a4c8206d98195d7`  
		Last Modified: Tue, 19 May 2026 22:56:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:422719969b724460931fa20154d0a6890898f49c173f6d14397b421dc576acef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15af29846ad006cc6b37d420bd5666546c95b605135dd202a7c751c781917108`

```dockerfile
```

-	Layers:
	-	`sha256:aa541775c0121579300600dcab9b19430c3938ed7a6e03d11df481fdbcdfc915`  
		Last Modified: Tue, 19 May 2026 22:56:14 GMT  
		Size: 3.2 MB (3172402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65188eafbe31ffc7e86eeb72c7a1509586ca37f40dc8e4849b0b4532e2e480f5`  
		Last Modified: Tue, 19 May 2026 22:56:14 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
