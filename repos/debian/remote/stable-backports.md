## `debian:stable-backports`

```console
$ docker pull debian@sha256:61f55890577e730fd88ce635f323e23afb085e7651652dc866b25d4f0a5ed325
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:e478b02c6f97b3797e904716dbf762834a89f8c163703228bf8d08ef93676525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48494496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da44fe96903f844026ba8b014f7540bd2538022dcf1ba7aae859736f8eff4ca7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0917e117371d10fed7da23c980bf7ab4e6a95a9a6e5a794a229095af300aaab2`  
		Last Modified: Tue, 10 Jun 2025 23:25:01 GMT  
		Size: 48.5 MB (48494274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3d629f196e05b57c5c6797130b74d1facfcfe0f956ab43cd57c5ade982e3cd`  
		Last Modified: Tue, 10 Jun 2025 23:33:00 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:579e8f5a5c82af9fdacf706efaee7137202d6f05be110c53dc2b70fb141ae7c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8860ec024b66721e58950fcc7801ee2919dd375036e80118f5d6db4365583ca`

```dockerfile
```

-	Layers:
	-	`sha256:18661315966cad49c7a288b6be73d608ae089bdf6d97e48254620a983a0a910b`  
		Last Modified: Wed, 11 Jun 2025 00:28:10 GMT  
		Size: 3.7 MB (3726834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f0c46ed606c78bf744edb1fc1d2c76286038f830580fb9a240b24d302afc9ec`  
		Last Modified: Wed, 11 Jun 2025 00:28:11 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:572c1f62f692398ae7bc34050fef6d7e678608d2f6c8d482ba0e8517b21dffc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46026782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846cbceda91e14893153ddcbfd2fe2e8022e4ad3e14ff77afd3e91726ed2ecda`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:adc4062a4c4f08f190d1677c2d2c2f5abcb5d077f5ecc053644c35fa7d8a42fc`  
		Last Modified: Tue, 01 Jul 2025 01:15:54 GMT  
		Size: 46.0 MB (46026560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aabb675e919341281ccfa8c5fd5149aa257677c5eaaefb1a89cd3b5b09af607`  
		Last Modified: Tue, 01 Jul 2025 02:12:26 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d643eb0c885c8ff76d2fb768cd0b2efcaa1d0a30381fd090b6c4d0b1327356f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101b5e5374b02e1e473a249e9de187839c85fe69f7ce6bb04f17f967caa0697b`

```dockerfile
```

-	Layers:
	-	`sha256:9740bf52d7e2d4a8505883826f1ae6ad47d32809e6f2cf1eca2e53c6d6f4b948`  
		Last Modified: Tue, 01 Jul 2025 03:27:54 GMT  
		Size: 3.7 MB (3727035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d521b4071435d5e8257444a0d2d1c4d78e70ecc4ab2ae912469c6361021c8d2a`  
		Last Modified: Tue, 01 Jul 2025 03:27:55 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:6150cf9dc6386088f69752caf0e7c5391ec70cbde7ef74e4725712e1e3925d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44208400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af40949d0ddc6f245b80579444e2116be7962398be25691a1f153cdba5e4f82c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:136085bb411e4782763423aa96ba957476a8d006302c4dab3087714322595584`  
		Last Modified: Tue, 01 Jul 2025 01:17:07 GMT  
		Size: 44.2 MB (44208178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae0fe186decc9f3c2d1d224769676b0d5df2f7f1e03040930ad2671e4212fa0`  
		Last Modified: Tue, 01 Jul 2025 02:13:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:bfe500bbabe415d9ff8e75dd5494e4038bf108fd5870765fb6c40d6133ae3c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3734892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982175c1e6c36f995842d1cc7fbaf0c590acdcea886c0a480da3f7fbc1740256`

```dockerfile
```

-	Layers:
	-	`sha256:7e14e3a9271a96a2cf0e564c8be40b4d6f5b83c54e75bd36cbc9ddad0c1be126`  
		Last Modified: Tue, 01 Jul 2025 03:27:59 GMT  
		Size: 3.7 MB (3729013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a22be05a7d696be0f159d811d5e135a97d54c9b0afdb7b1cafac6a90b63f23e`  
		Last Modified: Tue, 01 Jul 2025 03:28:00 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4750d9e62b5a92e260e4ff8f9a9979bc71da4838ffddd549fc056f90082eb4c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48339011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226b9410b8a8e571a260a6d6cf4d05bfe28a2750aa5bf0940c558d7949d4e652`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3ad5cd95c485f9c52772d06ca069ebc09ad5c7ec608e4300ece09d31c5ac2711`  
		Last Modified: Tue, 01 Jul 2025 01:17:00 GMT  
		Size: 48.3 MB (48338790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561894e80d6bc445e50c847f3f8514bcaeac049691b4b61f1f905b4a079ad8d6`  
		Last Modified: Tue, 01 Jul 2025 02:12:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:17ea69331afad25216541487c888bf725c6d84c4c78447fd1acddf361435590a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a6fdccc8cceb00f75d28cad831534123e026c44141d8438dc7b7343128ceec`

```dockerfile
```

-	Layers:
	-	`sha256:97a55bbf29138f59d1f523db0a068fcf39429f98024612a79734597e83a90c5a`  
		Last Modified: Tue, 01 Jul 2025 03:28:04 GMT  
		Size: 3.7 MB (3727049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a715c687dfff59b79fcbce66bb76690aa5c2908c632d8557e64d740c7fe7c67`  
		Last Modified: Tue, 01 Jul 2025 03:28:04 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:00c5773a64a8eb2db5c35237ddf54d7a4dc0aa18534d9a98d93b04d733e27841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49477639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabd66f1cfbf3fa13a8e8e51717e07fa6366ab6162a84692e1d9f7a90dd42d22`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d287a5ae8f93f0b6c060d82a64ae08394c0dd24cbcc24fab3d4088e81e6a0f1c`  
		Last Modified: Tue, 01 Jul 2025 01:14:58 GMT  
		Size: 49.5 MB (49477418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607bdd8220be34f0fcb8df29781da2c3476b1722ddd9c0fbef95e3e7b2d2d3e5`  
		Last Modified: Tue, 01 Jul 2025 02:12:07 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:55a7f797902726c9118400a89a4fe8795e1bf64587be1abfe87bdf8187a286d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24388aebe88d323b44b55762eed14c29e133084f4aaf1c8ed403df9aaf363933`

```dockerfile
```

-	Layers:
	-	`sha256:d215a67dea6f12fff8a6d56f8f91d1d894a951c92d86681ab1208cb434700afe`  
		Last Modified: Tue, 01 Jul 2025 03:28:08 GMT  
		Size: 3.7 MB (3724036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b02b5fc2a22c1b3657b8f73dc0bb9129ec4b5747c83bc331f9a058107287a96`  
		Last Modified: Tue, 01 Jul 2025 03:28:09 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:f4767a138fc7023161f0044ae0663cf2f386de351942d6d58a59e4da0260923e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48775765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cad8a2fffa5db366678c1817ef7083449f5be4c57cf25487a2af4a72e39c78`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'stable' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:fea6be8935e877f61d60700596494d41a86e2af2a9e86cedab87a3cc1d194611`  
		Last Modified: Tue, 01 Jul 2025 01:16:24 GMT  
		Size: 48.8 MB (48775545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb615e12450a71ed2cc5b0576e87e17ad6436687b740403854fa2b9454ccb4ec`  
		Last Modified: Tue, 01 Jul 2025 02:19:18 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4d5ea252c2f08bba4d5fd6d722e89acae4502965fcbea86095dc73280dc64428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c08237840da9cf16baa6819051597a60d4b0e8073b9830a2c38a7d12539c122`

```dockerfile
```

-	Layers:
	-	`sha256:4210b5a86d366ced5e5c737de79da8069ad3393b9703d6cfab9b7c3b613a1517`  
		Last Modified: Tue, 01 Jul 2025 03:28:13 GMT  
		Size: 5.7 KB (5651 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:4f38eef03df66ac491e2166d7379c8a84bc845d5de534715ec5ebababe09e6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52337465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5da8270ba7c79db5d68ce50da973f7a0365d18486b9a3cdac098bfcdfea4321`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d849a3730ddfc41ec1e43f2c4f5669e6f9d3bb71323fb0cf1112f7c1ae1da46c`  
		Last Modified: Tue, 01 Jul 2025 01:16:57 GMT  
		Size: 52.3 MB (52337242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897c41c68fd0e1679946deb546a244b0a8d4b898201477ae84584aac564764fe`  
		Last Modified: Tue, 01 Jul 2025 02:13:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ef0ce3ab91054e34dd290d7d396e57c4414e715c78b6908f59863785bb3a6d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29ff880cc08522d4062eafea230626f72684ca43c89122bf19a5105edc9d3fa`

```dockerfile
```

-	Layers:
	-	`sha256:ad4c882d276e5ada534bc0b09ad60426fd4fb1ad4a8d885250816380f626540e`  
		Last Modified: Tue, 01 Jul 2025 03:28:17 GMT  
		Size: 3.7 MB (3731180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05e384ff3b321e0e92b9d9253425c190411ff4316a523d6395551441fe9c6df2`  
		Last Modified: Tue, 01 Jul 2025 03:28:18 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:28e68f1eaea6fe4dcd0d176b24f277896548c5192752a5cb3c87910668b7d9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47149510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de6fb5723786350e241467afa2d726a193a5135ef54f371a21dc7c67155f93a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8854bea54cb8d09e175e0ab01385b11c941905a2fe5551c0e5f801012539015e`  
		Last Modified: Tue, 01 Jul 2025 01:17:07 GMT  
		Size: 47.1 MB (47149288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ec2765256c12bfe1022bddbc24f237507d32f9c79547dd097847278e3aad5a`  
		Last Modified: Tue, 01 Jul 2025 02:12:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b3749e105c1f6df4ce1da12ad2ba262a131c2bb4d5ee7cda6d867d4e53051f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c93c87611513757a068a9c1e72cb0e53e51829b02face49207694a0461760d`

```dockerfile
```

-	Layers:
	-	`sha256:07e93c6fc9d5cfaa90a697d6007439b0a1a8854677bf7b8cda33645963d3a071`  
		Last Modified: Tue, 01 Jul 2025 03:28:22 GMT  
		Size: 3.7 MB (3723672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d47168ff710308a097413c08e9d2ebc851b182eb9d7d8655cb8e5c418841ed9`  
		Last Modified: Tue, 01 Jul 2025 03:28:23 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.in-toto+json
