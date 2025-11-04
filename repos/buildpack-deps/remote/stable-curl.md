## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:9705d922589b2523d8e07e7378d7b9849df8539a8b862f9c7a8dee1015e532a2
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

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2e8ab2c0b206e8b2a20676f3fc2b9a24e4728e69b32f1fa1cc421e0574d1e411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74900516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a099a9b3a6053550a7070d0200a3d1ca073701f4cbea2f54087ab73f9652d7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d573bf42b377ce6a5a0451c15388849686fa4058efd68999f3b014daeb5b55`  
		Last Modified: Tue, 21 Oct 2025 01:42:47 GMT  
		Size: 25.6 MB (25615545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a3f359ff36b17a9d34788f0d5f2484ef7759310a82a1e415ca0e72d695b57d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4125973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696d72e370edfc614053b3731766b0cd0d4fed3a27873db5b148f65980461c27`

```dockerfile
```

-	Layers:
	-	`sha256:96f96f6970a271065bc7cb7b8a8cf783bfe89e6cd29f40d23f21659fd7b45dda`  
		Last Modified: Tue, 21 Oct 2025 09:24:48 GMT  
		Size: 4.1 MB (4118844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e3dad8c0ab1987fa1578a414c89c6914544de428ab734d48e229bed05faba9c`  
		Last Modified: Tue, 21 Oct 2025 09:24:49 GMT  
		Size: 7.1 KB (7129 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:299ad5b1767c7a2a9504527892e634bd1a1c386212d1a55a7385b49777982ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71792555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1870bfd20bb4afcc8c3dc5b86291c7055ea4341fb37adc6c6cdbdd45db88ad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:28:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ece3d43cc91380b968e97ebcb749d1c0cc4d780ea6ab83e3cb6fd3762b28d8b8`  
		Last Modified: Tue, 04 Nov 2025 00:13:14 GMT  
		Size: 47.4 MB (47449426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e91b819b99c2c8690acb5b01465ae84356bc40a50656db0ab817eb28337198`  
		Last Modified: Tue, 04 Nov 2025 02:51:11 GMT  
		Size: 24.3 MB (24343129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0fbdb6f08160dc6e1220268c86e89d27e8de7c748b6c32a6c6385821c94064ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56bc2212b3db85fe4280adedbbc8a9c852c464851d5d7ced47b80d5d24ab3b41`

```dockerfile
```

-	Layers:
	-	`sha256:5427e2415e325957e12f249c2bc5ab6e6cedc15d338337fbb460e593a57dc5e2`  
		Last Modified: Tue, 04 Nov 2025 08:20:59 GMT  
		Size: 4.1 MB (4121834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2811a87cb0162a12f9c56cce6b48bfad5bd21c08a55b06facffa4245e10b561`  
		Last Modified: Tue, 04 Nov 2025 08:21:00 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:88ee4bf9a5af96b6fa358994afda4c72ba83485871a60b8653fe3ef62b0ec561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69333156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38dd43dd1f8cfcf4bbc74f59176594d5f7190e87dee640296749cdbaaa5b101f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:25723cf5ae8b10c461d8c699bc5f9e41058f8fd5113212d106848ebe89fc0ffc`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 45.7 MB (45716494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452a743b80bee0c18e49576c93efcfb6c736c07dbdda0e38658362cec14c6415`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 23.6 MB (23616662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2df55e9b842032366e757f9b726f1be21b270be4f9971cc15e309d5bf8e8dffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165d63596eb588ff131d4d86e5f7dd1a119bcba2d405d6ae7f05ead3512bd0f5`

```dockerfile
```

-	Layers:
	-	`sha256:18de0cab970bccee1530be2e820ab2b956311c90d2e2308d4a573d445e927855`  
		Last Modified: Tue, 21 Oct 2025 07:20:20 GMT  
		Size: 4.1 MB (4120345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17821d20681cb41cea177cd0f1345261b67d363e6a027d34e0689a1858c46dd`  
		Last Modified: Tue, 21 Oct 2025 07:20:21 GMT  
		Size: 7.2 KB (7201 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a8499b21d59a6760d0516fc48d559047979dbd082509d732e239f1bcb7f0d085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74667206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364ca4f25455e161430c68493a8747dfcc94edca2228f2a67b91414c228a0d1d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510ac7d6fe76c0362c0162daee6964c5b93b20f5ddf65021b0bf3bcce16f306`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 25.0 MB (25017463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f21509d8259fbbb97727e390c64260c8cb2752aed58ad907cc31aec816647ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39ebfa99ee8e694bcac03b83b5e0e305d282e7ca5c2e3f980aa9a598d2c6b52`

```dockerfile
```

-	Layers:
	-	`sha256:54367fe7848596d58320b818f79e6fdd567b2eb1326bfede0a8e14191b248b9f`  
		Last Modified: Tue, 21 Oct 2025 08:25:16 GMT  
		Size: 4.1 MB (4120386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75d65825b8d5e974c77cd2eb6bfbb048e6380e5f4477caba0fa120c5dd6413f5`  
		Last Modified: Tue, 21 Oct 2025 08:25:17 GMT  
		Size: 7.2 KB (7221 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a9786cd58c54de28ece861125d968f8c699aeb72e2cdcac0d2f9c3b21518f58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77576253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada4a97c96f5e217ba8ee130043fd5780f57c171d61b1ce4fbefa6e4bf3dca95`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0c4647ea5bf10ee4302f28d7b05ac3b18ede5c510a3bb65671353e4dc5445f11`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 50.8 MB (50800574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68e11ad5a4fd5be41f07ac93311f8ae1f7dfd6455edf9f5cf950e26d70ee4c6`  
		Last Modified: Tue, 21 Oct 2025 01:53:30 GMT  
		Size: 26.8 MB (26775679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fd4d2cd61d8a4cb80bb68e0e0b4724911a57b484c5e86849b8868c40ab067ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dedeae9a2e607d69a2da342fddc3f1269ddace2962e6e9ea63841e2ff81051`

```dockerfile
```

-	Layers:
	-	`sha256:0bdb51a2cae5b32247d7eb314bedfae310a675d135ca6f115eae60c76aea3208`  
		Last Modified: Tue, 21 Oct 2025 10:20:51 GMT  
		Size: 4.1 MB (4115952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ba48337a6ac7710f758b1da9fd848185b1608e28cac80cece61a32ca403139e`  
		Last Modified: Tue, 21 Oct 2025 10:20:52 GMT  
		Size: 7.1 KB (7102 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c3c3f9c4ca2ce647ec7c24fb12622f40fe344f6c8307f4b6d1393fe3005163bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80106760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a46336f05cf00988685a920ba0522c279a066418c07e407dd83cc74542fb25`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c598502b2d4d7d278f56bfb7b6960ccd64d116b7bc7b02516bad5cdad4a631`  
		Last Modified: Tue, 04 Nov 2025 06:28:57 GMT  
		Size: 27.0 MB (26996633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6025e079c1ace6f4c9be10250b09658183690acb8fd42dce86a6d32307cada2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4129814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144c77b9fd928d449799f081f638ce2f8c4a7f54905605b5640a831184dddccb`

```dockerfile
```

-	Layers:
	-	`sha256:73ee5246fdfef4f103b47654f8b0b9557062a77abbd0d4e881b6da02452e4d2a`  
		Last Modified: Tue, 04 Nov 2025 08:21:13 GMT  
		Size: 4.1 MB (4122690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a679869adcb6c152468a9993a99990fea1166cf3961ace4e52c6f8aec1577957`  
		Last Modified: Tue, 04 Nov 2025 08:21:14 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4548580a24f3c30de91f1db6e1b941200fe1746b4cff1a95134e51567ac67bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72724180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d7098f368f0b845afa6586462918a1989742829483eb5ca57ea005e525b534`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f99bc11a75f6f7a676f3f49bda98f8ef1b59f2c8ba74759e5fa155fda025bf88`  
		Last Modified: Tue, 21 Oct 2025 00:35:52 GMT  
		Size: 47.8 MB (47770306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c640441904d97046ee4a137483e3b6745e0a18782c3b688fede8e9ddf18261f`  
		Last Modified: Wed, 22 Oct 2025 18:09:29 GMT  
		Size: 25.0 MB (24953874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:089e2bd695fb7bdd244b441f94e4724e409493eb148173595429d045c9eb0a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4118521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d866d005aa053255bc5f40ca2dc51429ea233d443c6c7ee5d033b211e538517`

```dockerfile
```

-	Layers:
	-	`sha256:18dca1e03417b8df4c711b7709eeb0acbd77a3b6f766ab1d4ff5cae4b7e4ebf5`  
		Last Modified: Wed, 22 Oct 2025 19:19:57 GMT  
		Size: 4.1 MB (4111354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cfcdb9894264a2abf895c1e78fb5ea2f5115f5c46d1051437dc7d43661ef61e`  
		Last Modified: Wed, 22 Oct 2025 19:19:58 GMT  
		Size: 7.2 KB (7167 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0a8d26783372a664ab4e7794db3b3d90827796b3e21329aaeb139963c00993c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76135013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3dbd35b45d245a347b8ca504ca1e93a627eaf486f457c7973e5c5a80d6d23b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:be7c8533c3f8dfcf5ab5c0fd76b47a568dc971c853834a20808defd1e88a5ffe`  
		Last Modified: Tue, 21 Oct 2025 00:27:58 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9f518343ed4506c34ae7900f538c56bac66f4fad9740034ee8b819bd8d15e`  
		Last Modified: Tue, 21 Oct 2025 12:43:19 GMT  
		Size: 26.8 MB (26783314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:459b73b1219c10e0049e1640352c672f901f44884a3bc0b92cc15c1a2ecc2f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6e5c0395f17193f9bd2f3cc79587638dad4149fbeffe29dda9473d3f67912d`

```dockerfile
```

-	Layers:
	-	`sha256:07baecdd3860a500eb4f75605285931a696906d73c9ae24cb9e5d05962519285`  
		Last Modified: Tue, 21 Oct 2025 13:19:57 GMT  
		Size: 4.1 MB (4120254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:975adcb855159ae7a817e9b93aa3094b741ac876c391381a351a5814c511adc2`  
		Last Modified: Tue, 21 Oct 2025 13:19:57 GMT  
		Size: 7.1 KB (7129 bytes)  
		MIME: application/vnd.in-toto+json
