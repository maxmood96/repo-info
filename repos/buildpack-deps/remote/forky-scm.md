## `buildpack-deps:forky-scm`

```console
$ docker pull buildpack-deps@sha256:714ba353893fef548f736f47a3ec8d8fbaf816e350012bc9239811c5248f2aef
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

### `buildpack-deps:forky-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8c48ea51b09dc1c4937fb6f7e54be4bb9a35f1e03451b5e113e315fcb7b0ed1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144117850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd66cb921257b0336c94eb52af1579828130a88d6df955b25ed7677a4f9ed46d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 05:10:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:38:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:76694dc296168bbffa890c84fb372e9c250bf33e0ad63a6146b169a57d983e2f`  
		Last Modified: Tue, 18 Nov 2025 02:29:31 GMT  
		Size: 48.5 MB (48500434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cde0e5673dcde1a0a75a6006c0aa8bc722df9feeb622b9a6bf212e2f178a04`  
		Last Modified: Tue, 18 Nov 2025 05:10:46 GMT  
		Size: 27.2 MB (27217534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2932c8b98dae86ed0b1c8a1e3e5c71392f9692dc656a3abbb9118c188f27292f`  
		Last Modified: Tue, 18 Nov 2025 06:38:41 GMT  
		Size: 68.4 MB (68399882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8ac6ca00fcb5c57bce3df42896a61733b452362feb23f00b24d2142b3ad8d813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7754957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa716b7ad1317068ef63cb2c1d7629631ccfc922adf6e6dd7b5136a591031262`

```dockerfile
```

-	Layers:
	-	`sha256:1e54c84b2fca4181e9c56063ccb0d7f7c070ca0ce242e5a4958fbb68accd104e`  
		Last Modified: Tue, 18 Nov 2025 08:21:21 GMT  
		Size: 7.7 MB (7747691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce3da8cc6fc0a9628a197b8c0e0a06c67db3267515ca523b6990bb04e39db523`  
		Last Modified: Tue, 18 Nov 2025 08:21:22 GMT  
		Size: 7.3 KB (7266 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:17584135bfe41749ffe5da08e97d57b48cd9d5c6dcb4f348715335c5b2464b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133257917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa31670f244857e7db7aeec2f2ac624348fc775ecb6aac0878e1756aee5ea511`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:27:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1dd1fa3a56d87bf4dcae80a33b02589ad31d81e866bca9f061ada67db33c8854`  
		Last Modified: Tue, 18 Nov 2025 01:12:58 GMT  
		Size: 45.0 MB (45003762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6f4451a2be0f51c6d1714f46485883bd5db54f8b6d9217e249d632dee61a5d`  
		Last Modified: Tue, 18 Nov 2025 03:59:12 GMT  
		Size: 24.9 MB (24945403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e16a5a4071f52927a7f28d9d0587c256392be28c985fb8945c4f1d6790bca96`  
		Last Modified: Tue, 18 Nov 2025 05:28:19 GMT  
		Size: 63.3 MB (63308752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:48d8dd6db117dd823811217de00cfcfa9c090f624a1ddd937df8725d11d17643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7755520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a0b11aa2a0fdf31ca3ecd32899cc59f64d8ac0c15b6ee7105f629a9f278349`

```dockerfile
```

-	Layers:
	-	`sha256:62aabed80b6ca209fa9f8a06d97867fcefdc805949a6e46293b9696e2c7cc83c`  
		Last Modified: Tue, 18 Nov 2025 08:21:28 GMT  
		Size: 7.7 MB (7748190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98f11030fd8a4aadecf446efdc55de0d025753bd9cd9e35b7528581270646375`  
		Last Modified: Tue, 18 Nov 2025 08:21:29 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ed1517310284f962a580c07a56498bce0c724adc3319a493b672e29cc6e19771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143153480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b621b9dd908d766388368f831bef759c964c775cdbb1afed7478deb37c40205`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:25:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:38:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:25dea15c4ffeb70e1112f1ee06dd948a8ab9dfc3b79ef239cb96080cc27ff1be`  
		Last Modified: Tue, 18 Nov 2025 01:13:47 GMT  
		Size: 48.6 MB (48591184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e989d2e0e09f298fb48c4d6ff3605064bc05169f4e2b9891ccb3261afe85988e`  
		Last Modified: Tue, 18 Nov 2025 03:25:51 GMT  
		Size: 26.4 MB (26444649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d766a3fcd99b3870f8097a1cba056eadc6327b86dc0436d4998b4bd42fba2bf`  
		Last Modified: Tue, 18 Nov 2025 05:39:16 GMT  
		Size: 68.1 MB (68117647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:92948d0f4174659669ed9c19e19b6ef39828dd54d24cc81c82fdef2e11fa90de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7762062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2a457e12b24d74194f23f6d91f4ba187cebe9a170c6e8b3f3a2c2ea98ea387`

```dockerfile
```

-	Layers:
	-	`sha256:1d4efdd2dcbb350f0497654cf395d22f2c2747ab4725366557105e828445e3ff`  
		Last Modified: Tue, 18 Nov 2025 08:21:35 GMT  
		Size: 7.8 MB (7754716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:664e79481f3dddb56e2026033777f3b186877e409898c34a3695b9014f0932d7`  
		Last Modified: Tue, 18 Nov 2025 08:21:36 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c6a14f61e57c884a0d87278c525c20a729c01e3ae1fd6909e393fb6c9d7b961b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148681451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45328bbebbc4b82ab6bef1f4d88888188956c2239d61a74cf3acd5b8498b76d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 02:56:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:09:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:898cf630ac245ec9ad865c96204520b86bb7b8760d5bd2f14bd02745e43d82f4`  
		Last Modified: Tue, 18 Nov 2025 01:13:40 GMT  
		Size: 49.8 MB (49832238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2307ec487a47570033147c5c7a8c176eb531df9120f57bf768d32ef164c1efb5`  
		Last Modified: Tue, 18 Nov 2025 02:57:08 GMT  
		Size: 28.4 MB (28443569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afe2397c32fb7c8e88a8fb46c9042ce37ea62165c0c00b13dd2c00d1596507f`  
		Last Modified: Tue, 18 Nov 2025 04:10:32 GMT  
		Size: 70.4 MB (70405644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b42fe572b41030960cc7121796200908cee2dcc9f00f0f030675ea13e43be90a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7751086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf017932051364e2d9cb52b7160811d6bdb743e012a67b75e713565aa36a989`

```dockerfile
```

-	Layers:
	-	`sha256:fe974eee6c19e89e5b334880dc446e81f136f10caf5357d465ce0d70088aea8c`  
		Last Modified: Tue, 18 Nov 2025 05:23:20 GMT  
		Size: 7.7 MB (7743842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f62214cdaccd72666320e40afbad800b5542de705f55d5ce85fe91aab5afa9b0`  
		Last Modified: Tue, 18 Nov 2025 05:23:21 GMT  
		Size: 7.2 KB (7244 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f8a9d4a2a19a434d1e4258ff9ba32dd8b478e0cef716feba635491e5dd53b7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155978892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81fe6b67aab89a63bc3e2ed02e7a67e2b991f558842bbfad2fb00324951d87b7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 06:26:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 15:58:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9422d47ff8508a211c5181db20a5b72bab47758f9bcd0687b05752ead1b35a5a`  
		Last Modified: Tue, 04 Nov 2025 00:14:32 GMT  
		Size: 53.3 MB (53315240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11aed674c331384a39236b4b411559b275037202a43d78e434b1d5c25b1e6d72`  
		Last Modified: Tue, 04 Nov 2025 06:26:53 GMT  
		Size: 28.8 MB (28798376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb8defd21903bd4a9c5ce27e534598f52e2a1e6029872b40ca09576c2e165d5`  
		Last Modified: Tue, 04 Nov 2025 15:59:56 GMT  
		Size: 73.9 MB (73865276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:793e6fbc9e86e269ac9e2d0c3b20f398d526ca39a532adeb126a4da27259ce03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7762930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b1242e1a581734dcf1f2e81effcf4fa4dd7928fd52567a3468bb8f839d16d5`

```dockerfile
```

-	Layers:
	-	`sha256:e63662ab8ea620e2ff516e4c07ef9a08bf961998d090f831087735354d71f2e8`  
		Last Modified: Tue, 04 Nov 2025 17:20:14 GMT  
		Size: 7.8 MB (7755632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5cf2cbf10a4207d6177f22dd9d46a577ac1aac1cd9f844d81b26a3fd8847edf`  
		Last Modified: Tue, 04 Nov 2025 17:20:15 GMT  
		Size: 7.3 KB (7298 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:c94e458ce0ae55bf6c75ead9714877a63b515ef0483cf8c8b868b8630ad70499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140381592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea7ebfd947b4e5666012f5d0580a22a85cded1bfebda63b8824b69662c27d1e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1762202650'
# Wed, 05 Nov 2025 11:56:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 06 Nov 2025 07:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:81afe9ed9d72ebbd06999820f64e36aa62bc978725062b4cc32efc39c6a99213`  
		Last Modified: Tue, 04 Nov 2025 00:13:41 GMT  
		Size: 46.8 MB (46791125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de80c58c6e8800ea08ee90fdc845007e21de17aea53e05a410b042fb2c91d58`  
		Last Modified: Wed, 05 Nov 2025 11:57:49 GMT  
		Size: 26.4 MB (26387683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba38582987e4915b52f0e092e29ae54ca12e102a825bf157a95190c5f836e50`  
		Last Modified: Thu, 06 Nov 2025 07:28:26 GMT  
		Size: 67.2 MB (67202784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:17dead85b5e1f68bec27471b6d01470e08060b5f5f211641e68b59ca91bacb41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7745633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c142a1a1858fa5893e7066850145ce325d0462e36df857f138782687271bc9d`

```dockerfile
```

-	Layers:
	-	`sha256:6d2ee025152ecb102dab46098937eebee32cee2bc07b295db99ee739f872119e`  
		Last Modified: Thu, 06 Nov 2025 08:20:06 GMT  
		Size: 7.7 MB (7738335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa3cbecc64742cd78c29db579c150b92c0b209368642bbbb799dac8a4049092b`  
		Last Modified: Thu, 06 Nov 2025 08:20:07 GMT  
		Size: 7.3 KB (7298 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f71cf74ef3227f5fcc707b32b4387188e72ce494ecd10ac0bedd943ce58fdf93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145849396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfae9af8a4c9a3f87db6c16077779542f364aa886dea742817c12f18ec959430`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 10:00:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 14:50:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:aa89048d1c3c931b297cf2d408ea7138528530c43e452af625223e71f97282b3`  
		Last Modified: Tue, 04 Nov 2025 00:14:09 GMT  
		Size: 48.3 MB (48343062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fd290c851a8e221175041f9832e015aa1560214f438629f7d489ba726030d3`  
		Last Modified: Tue, 04 Nov 2025 10:01:24 GMT  
		Size: 28.3 MB (28319729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc578ee5dbdb569a00fdc4f0f6cf56b364e8c2a978570ac8bfe2654c08bf3c0`  
		Last Modified: Tue, 04 Nov 2025 14:51:10 GMT  
		Size: 69.2 MB (69186605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:34328bb6d99140c46cd0099f292f43ad5a6b463b87ab1e644738a0058b693f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7756714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caecbafe3cd326fc91113b4d197aef38f1396ddd385990d18e689b53e4a0f3ce`

```dockerfile
```

-	Layers:
	-	`sha256:8db3a646664b3fa7a9ac74be72b1a8fa0dcf6bcb9f5b9a808baa2eb84fca6bfc`  
		Last Modified: Tue, 04 Nov 2025 17:20:25 GMT  
		Size: 7.7 MB (7749448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fc9eb862c97040fdde16fd129360a14396b52bae1f90381cd9a7d11ba2be353`  
		Last Modified: Tue, 04 Nov 2025 17:20:26 GMT  
		Size: 7.3 KB (7266 bytes)  
		MIME: application/vnd.in-toto+json
