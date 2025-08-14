## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:6bfede1c7573591dd6a2623a5e175fab775996438e578ffcd63cbb8e303681a4
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:499f9636127525ffe27f320a8b60c0908363552019e7da336828e6dab2c499cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48494737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818c6b2340b7a589d80cc44f3e65d144911fd1361aa0fe60ebbe67f191f6d2c4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:15e1075366401815a427be6be6b115a78b149e22b7946582c5f0a7294e269390`  
		Last Modified: Tue, 12 Aug 2025 20:44:44 GMT  
		Size: 48.5 MB (48494514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c586e0cd5fb9ad2909165296693a4d6ada6a53fc2e5690aea53cb2e077678b`  
		Last Modified: Tue, 12 Aug 2025 21:10:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0fc69ddfb7d6d9f3db9e0fcc5c7954decf55f2e6a7a182fc3c49b8b00f9ff9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb011744371a396db8fd9d8e106552e2cf4c9200cdaa68c3562729dd8a69f0c4`

```dockerfile
```

-	Layers:
	-	`sha256:314a81701f72f5f9c234b8591f41d46a4636201da7b679867013e494d6d6e96e`  
		Last Modified: Tue, 12 Aug 2025 21:27:01 GMT  
		Size: 3.7 MB (3726840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:269404b30605192161ad41a2b06a43ef9880b470f8c3b9de291ff79e3c6909bf`  
		Last Modified: Tue, 12 Aug 2025 21:27:02 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:06a8c6d85ecdb4bb8eab2068ae5f63c8efc3ef1785c5dff0032144498aa5cebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46027465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e241242cb393bd5bbac57a53778c6daad1ff056ba48ef74025a7d11c3a46590`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'oldstable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:97f0143997a8334b10cfee1df20521b4a30f1777d9d997780c97773832cdb727`  
		Last Modified: Tue, 12 Aug 2025 20:46:19 GMT  
		Size: 46.0 MB (46027242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c1ff0450298310ae1b98a963c12c0a96d7fb41c3a960f8db9a3d7029962c68`  
		Last Modified: Tue, 12 Aug 2025 21:18:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:89490c4a2b7ccd10639452729499c93d46597b768279cc6112ffd04201ce81cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696828ce85189e94337db7fc701c2ebe00578fb2c2213c3a783b316f48368cb9`

```dockerfile
```

-	Layers:
	-	`sha256:145076dfc8ec8aa2e41bffb48b647bfc0d1a2b1c9d754f49b6d71650376a06cd`  
		Last Modified: Tue, 12 Aug 2025 21:27:07 GMT  
		Size: 3.7 MB (3727041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3862c9344505353c9f416a922b83945a330ec15ed0c1681ff50a76619f16040b`  
		Last Modified: Tue, 12 Aug 2025 21:27:08 GMT  
		Size: 5.9 KB (5905 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:f3f807d5594c5f9a32b6b8613e05152a6898658bd5eaa28bf46a0d7ada0f5368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44209267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25d244bb8376ee02ff711d94c2c5f070835e42114b86bb9590e26388b1a694b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:31be392af26bf0c3a2a13430b20625a1708c53e09311fb719303a0b2643158db`  
		Last Modified: Tue, 12 Aug 2025 20:49:15 GMT  
		Size: 44.2 MB (44209044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c1ff0450298310ae1b98a963c12c0a96d7fb41c3a960f8db9a3d7029962c68`  
		Last Modified: Tue, 12 Aug 2025 21:18:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:06d9f2e7a6c57138bc1c434dfedf51816e50d32e918231c43f8e48fb6b602d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3734924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7dd0d1829573dd4352a743646fbac889663f023a3dae63dc301ca9950c8a55a`

```dockerfile
```

-	Layers:
	-	`sha256:80dc86eb9f9c8ef0a984796797575c598f2dc24bd9c665b8b9ac6c33fe810c4d`  
		Last Modified: Tue, 12 Aug 2025 21:27:13 GMT  
		Size: 3.7 MB (3729019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63bb93b3f496d4f3922de281850bb14e8137001e06b0e5f8d380aeb813414eda`  
		Last Modified: Tue, 12 Aug 2025 21:27:14 GMT  
		Size: 5.9 KB (5905 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:73acd54e9d8781d398c510b89ec01d5227f95d3cda63f3d84d28e45cf9ef8265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48342679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0738b5c104f3d9268898dafe967ac264253d85dae75a3f79650803738c577c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:46528f99331830eb2ca1964fb6d95040b4852af004209ae79084d829595dbee4`  
		Last Modified: Tue, 12 Aug 2025 22:10:02 GMT  
		Size: 48.3 MB (48342454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cb2c954ed97faceb13774788a9ca0a87b0ec09b690b7988fa125d6bebb091c`  
		Last Modified: Wed, 13 Aug 2025 01:49:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3f04d692095de3199ffcd7529440963f6fd3d91d155af84fff9dc4f9cf928036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031ca67156685f610c9f7e69bf370d8e49de1ac0be00f4471f05669b5268d9c7`

```dockerfile
```

-	Layers:
	-	`sha256:3c291f5aa8929cc74beb98180d874f24e5bc4851a1684784f5365fe7abf99fb8`  
		Last Modified: Wed, 13 Aug 2025 03:24:39 GMT  
		Size: 3.7 MB (3727055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64d452374ebe3799d6226c89eefc8ed06d96bc849b5569e86b09114964d3172d`  
		Last Modified: Wed, 13 Aug 2025 03:24:39 GMT  
		Size: 5.9 KB (5921 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:9060d038f2a725e0e2200a4e3fc98e7623554e58c853851acde21995452db11d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49478347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d7638b5e1d1d602ef556d01a1f3e67812350e792c2a79d9893f59bbfcf18e4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4eaf9ccee430fafbda7687771994aa99740695510b84578f373620b602e41fcf`  
		Last Modified: Tue, 12 Aug 2025 20:45:04 GMT  
		Size: 49.5 MB (49478124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f629a992fdc5b1ebe9a19b54c41a8b0db10d21ef7296081865b2f55cd2ef587`  
		Last Modified: Tue, 12 Aug 2025 21:10:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7fc24e9f9d207b26faacf9ce676a4fe29c055f5c982781778a8e87b834ff2184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fce5bf5794e6e5144f9e856bf96f88f0723f9573f095755dde772f06e3133e`

```dockerfile
```

-	Layers:
	-	`sha256:3ad313b0273ff7b5c4e4e1a1a126b9fc8a8a1f79c36008c5b5cf9738c69bc58f`  
		Last Modified: Tue, 12 Aug 2025 21:27:24 GMT  
		Size: 3.7 MB (3724042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22ebdb6a0638cfb131b24a9318a307c74d4822484f94f8ace88bc4df5cb1bd9d`  
		Last Modified: Tue, 12 Aug 2025 21:27:25 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:76da81b67c7890e587adc37f9da6957eb6d941b8c56bbcf64090eb885ba775ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48776889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195a82bc8745ce73e9d84339f4694e0520ad83c201dd2fdbd6a3184aac9db485`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'oldstable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:540bc1ff34258dc082ab6a25f978a00f9cff54c919951a32b66daf502891f026`  
		Last Modified: Tue, 12 Aug 2025 21:11:03 GMT  
		Size: 48.8 MB (48776661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abe0d61df83ae628e0f3d60f231c9a6217787e0214bed2d84a42e89b2888a67`  
		Last Modified: Tue, 12 Aug 2025 21:11:56 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:28d952d54abb4164fbfe23f702ea25defd370aa1394d7855a0048af457922755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b372ba38b1cf7c3d0f78a73d86e0ffc5550f5c07eacd9723c6d841a19777483d`

```dockerfile
```

-	Layers:
	-	`sha256:a00e67150d5e97a2fad37eb501ebe68ae98af397259eeacb25fc4ca0264b121d`  
		Last Modified: Tue, 12 Aug 2025 21:27:30 GMT  
		Size: 5.7 KB (5677 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:c5f5298a66df109664513307442a0d711bbb26fcbfd34fb6ad3af19c86b51e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52338305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cec8a5ae943220aa9d8b7a519b98d2bf7aaffbc4b9f75d51d557d54e01e3e7f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'oldstable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7c433f25549a4356182dae15faa53c85ec249bb6f6726e2298887aec96918c04`  
		Last Modified: Tue, 12 Aug 2025 23:08:03 GMT  
		Size: 52.3 MB (52338081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235d6db66b71468b0d5a6c0e245a66d00ca3caac88d365e79a0bc24dbb180cc2`  
		Last Modified: Wed, 13 Aug 2025 04:29:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:245155a776b1ee59490087eaf85c9c92831bcc69323d4a2da5157b90d53cc429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c879c435fe311d5c15fc299ecd8207dfd1082456d372c4935843e24933562a8`

```dockerfile
```

-	Layers:
	-	`sha256:416fd0699ac692ce141f19c0fe9b4232437776aae2f657d398e585930a125f9f`  
		Last Modified: Wed, 13 Aug 2025 06:24:29 GMT  
		Size: 3.7 MB (3731186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2b112b7865db44593e4a9317804192d2d27f56ce74789ebaf437a591a230976`  
		Last Modified: Wed, 13 Aug 2025 06:24:29 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:8cb7735d9bfcf3b557bb1239327e5166f8b4fba390707fab64fa599f6d22a3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47150092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324c5a07dbe9073393fd6dcc4380242e811f3d93c545c6cca87de3d13c70ba71`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'oldstable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:eb167ab43c95b6d2424123b7cd1bf7c7d922a0b3f7fe2ed0282cbf048cf08825`  
		Last Modified: Tue, 12 Aug 2025 20:55:01 GMT  
		Size: 47.1 MB (47149867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfcb24f543808a98f6dff07ada08b69705a603b004b59d5ab4de7873c21104f4`  
		Last Modified: Tue, 12 Aug 2025 23:11:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1f37e901e3e822b28e17997128af38ebf1d61530688005ad56125e3056a5e522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef8329ebc2552f0299d08557ec1830ce4b7ae73ff9581b0ec60bcfcca7689e4`

```dockerfile
```

-	Layers:
	-	`sha256:a2adf944d1b9b0305242620c7560d350bc976cb226f77a09e009d54ff3fe7d13`  
		Last Modified: Wed, 13 Aug 2025 00:25:53 GMT  
		Size: 3.7 MB (3723678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccde105f303d6a442f26d5485cb10c7d63b072369552ded732dffff9e425a0fb`  
		Last Modified: Wed, 13 Aug 2025 00:25:54 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json
