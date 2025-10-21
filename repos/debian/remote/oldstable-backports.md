## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:f7098936d16a92337b6ddcee228198d4bfcc19db5926f8bb530bded8238a07b6
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
$ docker pull debian@sha256:f03f6462af2b7f51180519c30a96ca043db02f6d58470e0064d8ef95c76b7031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48480779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae55a26d23e2deb43aa93335a4608a0244133cb9684f14040a883382f78f114`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9915abf8cad1fec6e139815a5f011926bb6de5ea43eb32e101e2e67468e30691`  
		Last Modified: Mon, 29 Sep 2025 23:35:23 GMT  
		Size: 48.5 MB (48480555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b0edd9ec7d44ad36b0cd2c622acc86e15bd5393d5e10425a75a869410d2898`  
		Last Modified: Mon, 29 Sep 2025 23:47:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:291856235256be91e8c4ada2d66cb4dcf6c67866c3fc23468cbd242f51a85689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7410538723eb8267b5346f65123e3e10e4e21a7e98f2247c64a493381dd3dd6`

```dockerfile
```

-	Layers:
	-	`sha256:b74a99b2e9e08648137eecf8dac726e1b8fb6423317007b736e550bcc1680962`  
		Last Modified: Tue, 30 Sep 2025 00:28:18 GMT  
		Size: 3.7 MB (3733433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb57b82a019b949d72806a30d5a210a84e1f472307b4a386e554a73f6e56cf49`  
		Last Modified: Tue, 30 Sep 2025 00:28:18 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:33d12d3be4df7f21bd858bba3da2ddf9c308468f2e1c8f919d54680474e19c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46015806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3403f6460060e1529ed23539d428ccd2d9b3237c7f239c1c0bc5e117e7f697`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'oldstable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:84739c0eaad5fe093ecdca6fb6fd0ad8eb5367a30e886ed67ee06e76dcee35d6`  
		Last Modified: Tue, 21 Oct 2025 00:20:22 GMT  
		Size: 46.0 MB (46015584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c055477f4d04700226f2d8a1e61fe3e498b71ad8d8488bca98005857e5ca32`  
		Last Modified: Tue, 21 Oct 2025 01:16:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1f70fcd8e44aca1f498493bad159e7901847808c5ecb8c77a43b45abad5bb504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bd6906c699c3a9940b6089d163273dc8f9ce44884b1ccaaaa4b96bacc7df16`

```dockerfile
```

-	Layers:
	-	`sha256:c9e3f99cda1b6b0aa06cbe7602582e7ba6041df4432254baa80853a606d4177c`  
		Last Modified: Tue, 21 Oct 2025 06:24:19 GMT  
		Size: 3.7 MB (3733634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60f90babd9211bda1ac6d5b6664902f2b6110ccce22e6ca332a0f32ada6a87fa`  
		Last Modified: Tue, 21 Oct 2025 06:24:20 GMT  
		Size: 5.9 KB (5909 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:2d878271af8904f6c4d7a7827bd0f7659c86840586d2653901c3b1b5ebc81e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44196148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64900d54f72ce53943ec0c1903e027524f38ca0108538dd49d5c622a776a2386`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c9f0185c4f29996188747504dba8d0828220f9e7c42f3231a4e458d2c8b487e5`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 44.2 MB (44195925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ab0028fe36b8c00502be38e794114f71eb504e07b17876b5e0dff22774dc0d`  
		Last Modified: Mon, 29 Sep 2025 23:52:16 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7ad00178c2a93a068dcc1927ae4e9994240ff038afe3a662f0d4a02eb906360e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501db45a87c10f1cf1c57bc25559b14b2778e034d6bd18f3399f09128784bda1`

```dockerfile
```

-	Layers:
	-	`sha256:d268e75e903aee32c2916df641548c657472cb1d00b1585ce270b6cd6b5728f8`  
		Last Modified: Tue, 30 Sep 2025 00:28:28 GMT  
		Size: 3.7 MB (3735612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7618d6b128ab33ab0dca386af902c0f10cf4819338dca7ea309d00286766c833`  
		Last Modified: Tue, 30 Sep 2025 00:28:29 GMT  
		Size: 5.9 KB (5906 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:14a0a65284413e4682859a22b755b5fe52ffea76b633570ab3b397a35aac1067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48359141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331f92be5e0cf699b32b7cd65723bfc42ff3bca0bb0d9b0ad440ad5ea6fd4c61`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ac7fbfe7a64fc4889c1ee5ffbdbddacd1a2d3a9378d93c192333af15cbcf13e8`  
		Last Modified: Mon, 29 Sep 2025 23:35:21 GMT  
		Size: 48.4 MB (48358918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ea47af61a051f10442f1a4d5d91e5e95d0b7d06d904745006f1b71dcc3a16c`  
		Last Modified: Mon, 29 Sep 2025 23:47:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a5fd9e0e19e12f99701ed41a91ee13e1393f0de93f14cb80b54fce50d26f55bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368b001ec5422ac1901e0ab3bc681e5749cc8e1071c300399fe023bfd44e9a99`

```dockerfile
```

-	Layers:
	-	`sha256:247ff5902c8f1eb27df24e46e025657cca665a0713ab374658f075ec5e4b3cae`  
		Last Modified: Tue, 30 Sep 2025 00:28:34 GMT  
		Size: 3.7 MB (3733648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e0a92f71f44267bbe15a8844d962326db6cf45bb230290de92dc325946aa978`  
		Last Modified: Tue, 30 Sep 2025 00:28:35 GMT  
		Size: 5.9 KB (5921 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:379a439316a0e7dfa88d28c5b4115d3700540a987482d59d56e638e2a0ecf945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49466879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0accac617463b51110db8408f6de6c3a6f943f21ce6f59606c79dbeacc215b93`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:85dbf157867c3d60b6f68925aaba66c305f6e001ed0072e2def1e52ae08e0281`  
		Last Modified: Mon, 29 Sep 2025 23:35:10 GMT  
		Size: 49.5 MB (49466656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44bffe15db14eed38dc15fc1e3231e0f4b2ca902d333437494bb64656f70a02`  
		Last Modified: Mon, 29 Sep 2025 23:47:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:770f30c145776ffd8e70537a4d9ef81c14c2937ef9579b5a37396c9095cb8944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a0fdf0fe560c7b03ec637491a3c0d4f52f252db38392bc9f7b1ff1591573e8`

```dockerfile
```

-	Layers:
	-	`sha256:7f5bab3a306ca530a6ddcd0ea5abd72cd81c8e64138f3d882b087076f05e1138`  
		Last Modified: Tue, 30 Sep 2025 00:28:39 GMT  
		Size: 3.7 MB (3730630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c22566fe5fd306de5201be6a7e3de7755e263dcde4d898fd9173eaa58d93fd02`  
		Last Modified: Tue, 30 Sep 2025 00:28:40 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:04ab1002377d156d7b7b20369530f0409178f2984f669efd12694d3cef87025d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48760972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524c3b20ffdae6e190df78b1dbfaf26b6f68531d4b97b251113d248891db0c27`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'oldstable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0ba815bb7070e4e694b9ffe09db23feb8cc4409f638580b44be95c6adc5f208d`  
		Last Modified: Tue, 21 Oct 2025 00:20:42 GMT  
		Size: 48.8 MB (48760749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe900418eccb839982f0d31aa661308b5d5f896c78935a5fef339d0265b6774`  
		Last Modified: Tue, 21 Oct 2025 01:17:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:61890d096ced4d8eecd9759d5e586818efc84fc9f481d8e5a29bb62f4d4d0cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5cdd6bd4b5573c8ec2e0bbed764b2b265753f8e5a8d83507a45b11e1c33f35c`

```dockerfile
```

-	Layers:
	-	`sha256:5cc6b11e2e1cbd4027d52d59b8aaec3441053cc8ea8236299f439dfcf96e05a8`  
		Last Modified: Tue, 21 Oct 2025 03:27:58 GMT  
		Size: 5.7 KB (5677 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:2d30b85d171bddb0df1875068bf4afa7196b47cf153b4475f09ad5ab7d01b313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52327012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d02d758a3eed17bd2e7f87642de0adb2944aec9e4bc953bd65e45dd6b0528ac`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'oldstable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b8d432a6f4cab1a53781c3fb554c1a8e7c299a62ff180921e034c12166489150`  
		Last Modified: Tue, 21 Oct 2025 00:21:52 GMT  
		Size: 52.3 MB (52326789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebe048295ffbc0adc68c9650b83ad47c3b09b05c81dbaf79e61b8c08e43916c`  
		Last Modified: Tue, 21 Oct 2025 01:18:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8b7b2f8f50fd89b2c23fbd33eefdf4fb0b38bac11f0b2afe120c6fa22cddd549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761a0dc175c804000dfc1ac932208e4680fa5b965083fc2508d14fd5803a9ecf`

```dockerfile
```

-	Layers:
	-	`sha256:3a004574d8992aa99a03aef90842216a7bf7744e9cdd8d993a6798192e5e7e53`  
		Last Modified: Tue, 21 Oct 2025 03:28:01 GMT  
		Size: 3.7 MB (3737789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f840b485cbc46a4d0eec42429b3559a23cb60736c69585d221f52f6e3d8f1b1d`  
		Last Modified: Tue, 21 Oct 2025 03:28:01 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:cfdbc7d0a34f1c5b8aa8a885beaf8013aa052e62428eb50fcf0ee849b56dd9a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47137750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5633298fc133bb5d0b621bef086e79874d77d0fc57a8e20e773b10a2a3f9776e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'oldstable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ac5319e24b05db3522476dd009c8e3e00181d2ef24813ab4b46d3ce75223df28`  
		Last Modified: Tue, 21 Oct 2025 00:23:23 GMT  
		Size: 47.1 MB (47137528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27296d06bbb2114f2c6da323e2530db41fc35ad8a13803d86e451dc71c5c8994`  
		Last Modified: Tue, 21 Oct 2025 01:19:18 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7ff120fae08ab3680bd36b0ece1e1e7ecb20e3fab96b817f4a9f8ba263a549b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80514674f579076adc84bb5a817ddbc1249eaf62f6a51ffe431e6e4cc33878d`

```dockerfile
```

-	Layers:
	-	`sha256:46306e982ca99df5285686679a70fe6405fe59eb29672955c9a762c9bc56fe73`  
		Last Modified: Tue, 21 Oct 2025 06:24:35 GMT  
		Size: 3.7 MB (3730271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a364f7a85afb144aa848ed07fbb5fdc9f7c26fcc6469bc2049dca5bc2665cf55`  
		Last Modified: Tue, 21 Oct 2025 06:24:36 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json
