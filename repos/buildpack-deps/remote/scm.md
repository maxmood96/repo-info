## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:612e3037dbceeb0ac914af248452bc94f0adf825fe90ae0f18f9a30cbf425f2d
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

### `buildpack-deps:scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c469d4661071c99936a7578a472b5b3ede17c96434ffc323c6f47f0c6bc74a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142714634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e9f19e4871bcbe0ff87efebf7a6e541346920f84ddc66e98478896e6f05b4c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:45:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467f93954cfe1451f4333422086d00bd066cf33f42112b531804ffe06f0a929`  
		Last Modified: Wed, 22 Apr 2026 01:39:50 GMT  
		Size: 25.6 MB (25622443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d12c8f3f3fbb5bd2b8369adf3213e09d6b33f975462543ddfece85b2fe85e5`  
		Last Modified: Wed, 22 Apr 2026 04:45:50 GMT  
		Size: 67.8 MB (67790089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fef4b7650a555db71ca9c8d59dbc6fd05f75db159826b3be0f166c989b03f3ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911cfdeadefda712eba8203b74abb5a79876b8f8f356968880ea5843ab9bb686`

```dockerfile
```

-	Layers:
	-	`sha256:c488e559f0692289396096dfb175fee6acc4a6e4712a6db44be8726b1da37d46`  
		Last Modified: Wed, 22 Apr 2026 04:45:49 GMT  
		Size: 7.8 MB (7768265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb3bfd89f11477934c5ea936d1c504523bb92f803c5677aed6a9efc5736a38af`  
		Last Modified: Wed, 22 Apr 2026 04:45:48 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:05fdd9a0fb643d13b6310feb9f904c87bffc9a7353ac8c866708fcb3bb87301e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137154274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82788045d232db560d6da063ab23ab743de4aa17d3050279a0a2f7870ea81bcc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:17:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:08:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2a20d1d425bc7f9412bd28183d8c6af38f835b7563f035cf6476381816d73dd3`  
		Last Modified: Wed, 22 Apr 2026 00:16:22 GMT  
		Size: 47.5 MB (47466106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850bd1c760e36c64cea860128e609cb23ecd251d01c38d67fa6179d5cca0da73`  
		Last Modified: Wed, 22 Apr 2026 02:17:34 GMT  
		Size: 24.4 MB (24363601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ba959356b2294f9c3156bf888a9b762bdd922efa57422268742976c4c2656b`  
		Last Modified: Wed, 22 Apr 2026 04:09:07 GMT  
		Size: 65.3 MB (65324567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e62a92e6a2829bf93928bae50c264b934f1d8ab30bdc967f2ece39b2031a1422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c91281bfa62fda64d60bb146c8bc8520763543fe76332a34c0453b8a157be52`

```dockerfile
```

-	Layers:
	-	`sha256:17ab1847f70ea24bfbd719a27c94622a17258ab94a1b3a6247178ed9ba3ed75c`  
		Last Modified: Wed, 22 Apr 2026 04:09:05 GMT  
		Size: 7.8 MB (7769303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6b854f1f9e6994bb01b064b70fca47724f2fa5b9dd7eca468d15e651529cdc5`  
		Last Modified: Wed, 22 Apr 2026 04:09:05 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6f1a4c879e550ef28a7d01438974b3b568b58c94c41dad1d707c43d07a4d0a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132096264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d47b8ba41008736f70c9bca7c74bed35eba0692f4fa63bae3459c61b1cdcdb2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:19:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:52:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cc74239df6a59971739f1b7a0758f97ae57e6ab4f74daa64d264ec77db24169f`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 45.7 MB (45738193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9f411318175ae51ff20f60969311f63c366288f8aad04eda4d0389d8b016c9`  
		Last Modified: Wed, 22 Apr 2026 02:19:59 GMT  
		Size: 23.6 MB (23636616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341da7892f7aceb1342cb554bdaf16f78292d5247e1ef9fb0f351c24aadb1f0b`  
		Last Modified: Wed, 22 Apr 2026 03:52:40 GMT  
		Size: 62.7 MB (62721455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:650efbf1797a20499efdf39329aa2ce7c245b637d82e687c8d55fc50a7e2c26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e936ab58618f92924717c72ac639217ee2662f3b07d383ef45538b3bc8a74952`

```dockerfile
```

-	Layers:
	-	`sha256:21a275ab2cbd068fea4225d126058d82ec9a5fa51c59341f611cbe61c9085306`  
		Last Modified: Wed, 22 Apr 2026 03:52:36 GMT  
		Size: 7.8 MB (7768772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ad438c19fbaaed54702ad6a8cd7e5a484e16317767ad3a22b462e64d3d7987`  
		Last Modified: Wed, 22 Apr 2026 03:52:35 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1ae9930d214ce1a56d11f00ff1b1bd13692310edbe5712089db674438d375f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142277389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c2a8724809e657f339ed407c233037d3a4258902fead060873dacc174eb2b9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:32:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f67984ab3d0b84dba0bf1b9e75bc42547713ab962aa5b392bacb0e61fa68b`  
		Last Modified: Wed, 22 Apr 2026 01:43:34 GMT  
		Size: 25.0 MB (25023409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c17e454c787ef19107fbea0250c33a4b6ca95fe0319ad68539a7bae9d9cad57`  
		Last Modified: Wed, 22 Apr 2026 02:32:52 GMT  
		Size: 67.6 MB (67584735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4e13c28303faad8810ac1262a140e46f5ada438a8f321243004cbdd92d042c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b96668924e3a6ff61aef45463c1141637089695cbfefbba5126ac38e5a9e67`

```dockerfile
```

-	Layers:
	-	`sha256:fae95cd7a47751b765c053a33e83ee6c474d05b34b044637ec2e8d7458591c55`  
		Last Modified: Wed, 22 Apr 2026 02:32:51 GMT  
		Size: 7.8 MB (7775940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3abb2c9f68c1c9ad71d2bf59fc79ebf75ce73c5dbbfb4a4cd58b8bbff04ef021`  
		Last Modified: Wed, 22 Apr 2026 02:32:50 GMT  
		Size: 7.7 KB (7669 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:261450ff74bf1eb5b78c5df0583b3f98846242e087c0ff09430d13b8b3ba9b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147419985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530c63d39f2ad5abb5c46c99504ced5a32e6a427e55a2b4e0c4e42c51fac36f8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:94f4ed96005686cb93e9fa3c8665cf2919ba40f9e10ece9df171f9948eed4c0b`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 50.8 MB (50825357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5321bfd0f3573fe94aa2216d1519cf604989d7a9e912196633f5d9b7a4e8097c`  
		Last Modified: Wed, 22 Apr 2026 01:43:12 GMT  
		Size: 26.8 MB (26784835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66cdc00799a2a5d425863c783516cdc5139f867d081df458a78cfa749e9d7c3`  
		Last Modified: Wed, 22 Apr 2026 05:03:55 GMT  
		Size: 69.8 MB (69809793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:16faad0e5dab962c2538bd0447cedcc8b3122437bae40e15251c111484ca87c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc336a395778e06e358e23f85e85a00226bcf658b52735fbafab6fa0f003233f`

```dockerfile
```

-	Layers:
	-	`sha256:d5255dc09e5bcd8cf85180405d37d1424cc6a2163392ada48807c774df6d8d0a`  
		Last Modified: Wed, 22 Apr 2026 05:03:52 GMT  
		Size: 7.8 MB (7764399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be1ebe7e3634fdb4ce42c91d6443f6d079275daecda254fb5997a4abb3e3f995`  
		Last Modified: Wed, 22 Apr 2026 05:03:52 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:478337b766dd3c823c37f6d99f2e11834faf2a3293eece5f78beb23460200e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153177289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35751459cc03f6804f7cb8ba35f3470c705f35f2e50cb5c6ea0938169f8bee3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:40:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 09:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2454d511c21492888baf49902a298f334e8095ce0fe93b53b274ab3f39febd31`  
		Last Modified: Wed, 22 Apr 2026 03:40:51 GMT  
		Size: 27.0 MB (27014616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f9e1a80821bce13187cd275a074ab44791a07c4796e61afbcda3a692b97ac4`  
		Last Modified: Wed, 22 Apr 2026 09:39:58 GMT  
		Size: 73.0 MB (73039689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b07dd969f432a4b217eb926cb7d67530ffc82bea65fe333c2ab3b70119895624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1245ac1eaafc3ae7e68c7c336f18461c922ce831d4d2e4f1c565acef3258ab8`

```dockerfile
```

-	Layers:
	-	`sha256:095f86cdb85f0047082940f77fb73747f84eeb2c0be698bfc0ae5622d5f13cf5`  
		Last Modified: Wed, 22 Apr 2026 09:39:56 GMT  
		Size: 7.8 MB (7775390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30a220697d545eb5e55c8eea276f338a0e6f3be5533d14257266955e4b61dfdd`  
		Last Modified: Wed, 22 Apr 2026 09:39:55 GMT  
		Size: 7.6 KB (7614 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:55361b68210c1481a36963c9cc8e30d553d7649b76f355a2641ded0c7272202d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139402096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33f8596cea0573b8d5f7b2733f4494e2d810ebdebe863f73410e644e5fa02ac`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Sun, 26 Apr 2026 15:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 26 Apr 2026 19:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad20ed76b58e7abcec15ac3129845a802887c092560883b4939e006992099b`  
		Last Modified: Sun, 26 Apr 2026 15:22:58 GMT  
		Size: 25.0 MB (24955805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a233e35e9c32890f2d416d3e6707a14b173707fad25985773c22f4606dee5c05`  
		Last Modified: Sun, 26 Apr 2026 19:10:01 GMT  
		Size: 66.6 MB (66648074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:65a6960ab48642ce777aa0804ac70dd6a804024f7f7b2d479b352215d7656bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7765718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53aa4e290b570d2c697406000fd0c0ffcc3ef2c1e75ea21ecb99e6656cac45a5`

```dockerfile
```

-	Layers:
	-	`sha256:1233e5e0bf5dec259acbe932a2671f00de815409feb1cd18e37838729366dcb9`  
		Last Modified: Sun, 26 Apr 2026 19:09:52 GMT  
		Size: 7.8 MB (7758103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb471324dfff6d73b9a1665ebc12b955f09ad5dfeb567322d790a27a02bfa526`  
		Last Modified: Sun, 26 Apr 2026 19:09:50 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8c18678ffd7b6eaf716411f0b9b427c61b20e7631c887c40940049d540b9a2f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144811431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c69a4b931b8b50700ead1ccd401f172f2da4db9513ea29254e0501fa1a7d27`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:21:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c2a3da428dd91e4b5df556514e279e6a571eec116b1f2b3ed1bc95489fcee4`  
		Last Modified: Wed, 22 Apr 2026 02:32:51 GMT  
		Size: 26.8 MB (26802425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c81397603fbb04688ca83ea8697469c3a01388a59e003d38dd37d22beb13789`  
		Last Modified: Wed, 22 Apr 2026 04:21:39 GMT  
		Size: 68.6 MB (68636900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e0062bc15cc6be9c89ecc741578272b619f5bcc315afe16dd84e6988dfdc4370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253c908adbb7c72d5615fa24ad721332c1ea0cf8ea1734d459c63e9fff3112f1`

```dockerfile
```

-	Layers:
	-	`sha256:5be19d09d5949829436a44b7b93045ccbbbbf71fd6ede7f4de4025e457e15c6e`  
		Last Modified: Wed, 22 Apr 2026 04:21:38 GMT  
		Size: 7.8 MB (7769178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b900555ce90e991cc8bc8facf1b51c2b1b8bd41056ec901e621dd1a96138935f`  
		Last Modified: Wed, 22 Apr 2026 04:21:38 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json
