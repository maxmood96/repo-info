## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:ec7dae1c6a87d57fa58b12205076f482150ffc2f3ae377fbed47bc18fcaea9b7
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8c2984e73e78ac530e68341df8a201ebfec90871f66aa178601284ec06bfffcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76132850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ea82ada02adf635e147992ddc0ccdacfb7c90bc13a2b1fce95e6b6a50f6ec5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:10:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b2184fb6462644b6acf50283df065d3d00ff827c80b1fe7de520944b5c1333b4`  
		Last Modified: Tue, 13 Jan 2026 00:42:32 GMT  
		Size: 48.8 MB (48841950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a867a2ba4f56034ba2804ac22169357a40437b8b6a997f3bb612def250ed9f2`  
		Last Modified: Tue, 13 Jan 2026 02:10:56 GMT  
		Size: 27.3 MB (27290900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3861447f4ef960c9f57d6229e23306a7cdf8a6e3efa6b831f013e02714598d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4120852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf743ae1aba91bfdb11056454e80360a6d4b339e784a1649af6f0fada374ba09`

```dockerfile
```

-	Layers:
	-	`sha256:21f590de8bfcd2362e1d6ced1e6e2a4a9049aab1aeddc1882bec91456f8125be`  
		Last Modified: Tue, 13 Jan 2026 05:24:33 GMT  
		Size: 4.1 MB (4114091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65cc8ec2b8c993415a59409b6e9a033bb8e9830aac91d12e051dcfef4cc2aa29`  
		Last Modified: Tue, 13 Jan 2026 05:24:34 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7967103d176625c3a543011976cfcbbf6cf142b1ce572ef4e999ce98de43e979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70027078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6cb3fec0e7ab90137eba73184e99c179d01dd302d4d500b9a8a7c7b4c6e365`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:58:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8b7f582255e583d8176a24d49b58b25ef2ab11e30f1f26c271dc02b42befa1ec`  
		Last Modified: Tue, 13 Jan 2026 00:42:32 GMT  
		Size: 45.1 MB (45124955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f363fb6b9543f81f86efd0aecc6d9e12898921b7bd5ed58e85c04a1426057dd9`  
		Last Modified: Tue, 13 Jan 2026 02:58:31 GMT  
		Size: 24.9 MB (24902123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6b17c2a149937d82f5d6d8630b53a75563d8b2ce7b84c0602455ff0e6bff1621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4122411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d5f34b7769145a9bedc0892adc8dc1be51eccb658af5560a7410b6d41432c1`

```dockerfile
```

-	Layers:
	-	`sha256:1d3ae6ed7a776e2c49e6a37670219908d8f9eeb23803022aac297fb7c4e053d0`  
		Last Modified: Tue, 13 Jan 2026 05:24:38 GMT  
		Size: 4.1 MB (4115587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f45da1c0e5b432120b875c0b22a52b98452e09910c39a048a10fb7b5bdfe2a95`  
		Last Modified: Tue, 13 Jan 2026 05:24:39 GMT  
		Size: 6.8 KB (6824 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6a4cad6c54d5fdc67ca7f86bc99d2266e34369b83273585f36119b712f66a212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75377442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbe8457dee6e50f0194d44cdcf4d3f1b307ba2c30c4a616633cdfb13659cb4e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:14:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6d947e77c03f512510d8bed1eff4f80727f54732f6ae212199524bdf89493609`  
		Last Modified: Tue, 13 Jan 2026 00:42:16 GMT  
		Size: 48.8 MB (48824718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d83fa1af402d6122143d9e5834df76a1ce4536b0e53fa05dd6ae332f4c77b6`  
		Last Modified: Tue, 13 Jan 2026 02:15:12 GMT  
		Size: 26.6 MB (26552724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:93420b48cbfc249b51124d501d31421d656b365b663219555c043821d7221cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4121825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd540dd4023402b21a836cb8c008b62ec3c2168653b72aec3b9b274a9c359a9`

```dockerfile
```

-	Layers:
	-	`sha256:2e0c476488926d4087b162f0a8f9e95888f394afc45f56f485693d31819c23e2`  
		Last Modified: Tue, 13 Jan 2026 05:24:48 GMT  
		Size: 4.1 MB (4114984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b354444a9ce93fcad3c5c0795594dd8cdaa120f73f0a68d25f4a973f756b64c`  
		Last Modified: Tue, 13 Jan 2026 05:24:49 GMT  
		Size: 6.8 KB (6841 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e384e2230154686142f53ca72493a18d49803169f475fe8afca5a2b2bd6547b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78418470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed78c757db10ddb1c7603df0201914cfe30eee9f205d652b4277aec6ff5ba40d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:02:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:621ee2827046628793df0c5176988fc0eef90eb94ab1b862f17e074ba6064e3d`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.9 MB (49943816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ebc798fc10f8015cd27d3c8885c010f05e57b86cddfc6e327bc7f746362b1e`  
		Last Modified: Tue, 13 Jan 2026 02:03:10 GMT  
		Size: 28.5 MB (28474654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:346e67b76f430cbcb1c8c5b35c41ab9101f6ba2a9aef7471241310bd04a26972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4117944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec905e2f147f2cb763b076e4b3f304892c351d98540b72ed076f4d647dd1f5fd`

```dockerfile
```

-	Layers:
	-	`sha256:43ea74d05127301ebbef6d74988b833530d4508d106e09b8569fc9f5e34e798f`  
		Last Modified: Tue, 13 Jan 2026 05:24:53 GMT  
		Size: 4.1 MB (4111205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f4b0cfec9b6e2424591b0ed8c10274cbcfb171d07c12a065c52c9d3fe60fc71`  
		Last Modified: Tue, 13 Jan 2026 05:24:54 GMT  
		Size: 6.7 KB (6739 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5981431738267961045a18683190cd44a1b312503b7c7269865fcfb69f0ee2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82370131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca09df6c9310d21d44dffee2f8a8990199ad1e014a4f2471f76825cd4b2751a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 17:38:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4751b9b2bc723252279cfc4495d1386aada5bcd65548da744f319db317b21560`  
		Last Modified: Tue, 30 Dec 2025 15:09:27 GMT  
		Size: 53.5 MB (53504917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2461812a9f73d501a89daf3b185dd9b6d6fb2e0eebe88b30b17f3f49a5419e7a`  
		Last Modified: Tue, 30 Dec 2025 17:38:54 GMT  
		Size: 28.9 MB (28865214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e4cb12744cfd7f558bcb298beeb5683b36b59489e5c0784fce8458b819bcc5af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4121469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec386fe236a300607d3e63cadf658f7437c969c187c76cea16f0218dd58a77b`

```dockerfile
```

-	Layers:
	-	`sha256:1cc590d380a93c39448dcb0222b258e7000654c6523afe464ce609d9342d0988`  
		Last Modified: Tue, 30 Dec 2025 20:20:50 GMT  
		Size: 4.1 MB (4114676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b41be2dfa7471cb69b89908680c19959a57416c39cc0578eb7c000e0e20886fe`  
		Last Modified: Tue, 30 Dec 2025 20:20:50 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:f37887b9f5a6ceb1280e2d3cef98dfd5e336055878ce79c5ffd7db51b844b85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73195385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1edf6bf54f9394131bdeced41c69012dac03283ab532611536e231bae8e326`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1766966400'
# Wed, 31 Dec 2025 10:12:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:992d8af34d90a1736cf1953fc1b6a42478d3f56705880d255aceac14902fb105`  
		Last Modified: Tue, 30 Dec 2025 00:37:42 GMT  
		Size: 46.8 MB (46842840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a59f77af8fac6fe633c43cf8effbdd88f2374763db6aea46bfef4f1a063d920`  
		Last Modified: Wed, 31 Dec 2025 10:14:20 GMT  
		Size: 26.4 MB (26352545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1609dc2c5b4d27a7769f271b0b137883fa99d9b2d93c560f402d16645590e0a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4109304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a821fee1c1d9716d1b6e474caa46ad7063106bc83f5709e9f0b968b2970779d9`

```dockerfile
```

-	Layers:
	-	`sha256:5875ce8337b613feda088973de395d8523102bc71f79c848b628d58f2baa6081`  
		Last Modified: Wed, 31 Dec 2025 11:20:37 GMT  
		Size: 4.1 MB (4102511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eed89aa90419540429736c50f251a1839cbe573bae4c711b151fd8c7cddd3a51`  
		Last Modified: Wed, 31 Dec 2025 11:20:37 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cc14760726100b1d6d75c0205185ccea9913f7273199cc07918150f9d40da2cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75384647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b49afb84c0097dcebbd77f4c8aab9eba53d5e665d8ad9635be3cd2931f44c2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:09:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1e9a1f6e22461ab2a7c3b148cd7fd0131848ded4c904183b11402001b4c02c1f`  
		Last Modified: Tue, 13 Jan 2026 00:40:59 GMT  
		Size: 48.4 MB (48388631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023c3faac75568557121b3e0aa2c658af780e8a1a9143b42405a60dbbef8a126`  
		Last Modified: Tue, 13 Jan 2026 02:10:05 GMT  
		Size: 27.0 MB (26996016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e7c3aa477019ed40a0bb5a742a732924361caa7bdb470213ec10490be875aa76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4122260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af165d6ce81b6957311cbdf2692fea62c64bc8d6b97e71035c4020df4ce8a648`

```dockerfile
```

-	Layers:
	-	`sha256:5c2dbc2a95f6898b449a27bee4635e77cbbed6a2edc41521c08e5d7cb26f4f8d`  
		Last Modified: Tue, 13 Jan 2026 02:23:49 GMT  
		Size: 4.1 MB (4115500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:365fc79afa8a92050c662b7e6d2b970314ba9805a62ed6300c0dbc1dcdaf6858`  
		Last Modified: Tue, 13 Jan 2026 02:23:50 GMT  
		Size: 6.8 KB (6760 bytes)  
		MIME: application/vnd.in-toto+json
