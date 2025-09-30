## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:c9071928cbb00e4c23ba01c90b2e3228cff2e86e0feb77b594f797d26b12a1fc
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
$ docker pull debian@sha256:74d84b2cbe576dcad5ab811990d1c2943aabb5261f4fb304279a67b3a6437484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46015806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc531bfdcd064c2ab792538274bef7fedcfdb05045b3600ff6a7a8639268ddf5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'oldstable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:dbec438b389eaf2693f81db163c1f0ddfec13aedc0da8708ea46ecc622223639`  
		Last Modified: Mon, 29 Sep 2025 23:34:10 GMT  
		Size: 46.0 MB (46015582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79152864ce4c647f088a662b2eb98a9329b9d872449bcfd6d2a906bdd9b5d128`  
		Last Modified: Mon, 29 Sep 2025 23:51:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:53db4e7c44aac6731fa8a51be6d4b84eb064c2b786771054de9813759a8251e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05bf6325b1d4e3551fd03ed10618259d75d1bba53f3ab3b7e6146c7bf2272dac`

```dockerfile
```

-	Layers:
	-	`sha256:44dc120e23c3d5f5e7401ba1703754735d2cde59921374e5a4285ad56db20623`  
		Last Modified: Tue, 30 Sep 2025 00:28:23 GMT  
		Size: 3.7 MB (3733634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff7ee0becd000a8a93e9e0bbe2b6ec2bb06a72cbfc445b364aa3d42bd4d8f70e`  
		Last Modified: Tue, 30 Sep 2025 00:28:24 GMT  
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
$ docker pull debian@sha256:901d3a2437c4e74913f3a94e0904454576e4dd753388944d375f02c717e3c701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48760962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45de66044ab8954453bd1343cfc1f66dad7c0117e207d7ab32bf5fdbd2e514d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'oldstable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0305930667ad3848e370b8dac3b35f651d85d6e9ff71430c270a1ed6733208c7`  
		Last Modified: Mon, 29 Sep 2025 23:35:23 GMT  
		Size: 48.8 MB (48760739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21bd5da5a7476427935571c33caf47532e69daed1bdef93c4173a2a99af650f`  
		Last Modified: Mon, 29 Sep 2025 23:47:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7e41c913d11e14345dae288343e8bb2e2d2248048a51145d50d2ce536595a3b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e6f9bfd58ca2036cecaf637e4960d577ad51ea87dbe4d63bd7b4e5d0beb7e3`

```dockerfile
```

-	Layers:
	-	`sha256:71ee46ef5a754af86be976fab40d655b6a1bf1bafcd82bd38f4547a544bbd441`  
		Last Modified: Tue, 30 Sep 2025 00:28:44 GMT  
		Size: 5.7 KB (5677 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:2be766767da18d92f66c0960d0f96dfa25b53d8db63e7fa6fec4ee7af5d1e3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52326993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae942a3c228b57e4c581996530f85144eee2e882e392c1059ad70588d799fa6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'oldstable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:38bc282c1b691d53b322103657a5163774178d9c5e909659de4ef453b7833fba`  
		Last Modified: Mon, 29 Sep 2025 23:36:29 GMT  
		Size: 52.3 MB (52326769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f782e49b2818254f8e7ec7166483d50af2fd05e84ef75c3ba65f78998b4a9ce8`  
		Last Modified: Mon, 29 Sep 2025 23:48:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:526465223e04ba4439b63ef6ddbba5c92e7bed884b41d49f8d4111b2c89b8843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937b76d375f9c2ba30d3dcc1e3c3436c2a01456721d9c438a85739d3de5ae3de`

```dockerfile
```

-	Layers:
	-	`sha256:7980a097ee6df8f8134812306139137f387a1982fd9a26a50ef52083e4415a1c`  
		Last Modified: Tue, 30 Sep 2025 00:28:47 GMT  
		Size: 3.7 MB (3737789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbb728ea4b30c795ba1e377bea43060202b844aaf2f7bdc30faede47a9cfe176`  
		Last Modified: Tue, 30 Sep 2025 00:28:48 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:3ef6a86c110a3a281627de3bed832e2b5511d9977971b7a89d94af25449b6446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47137675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e6583de642cc8e07fd30b6048421d763989fc8f3f129f6342554457c7807bd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'oldstable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ed88f686118d62bf539cb687d0f2c355d450753db794a3b36bc4b1db19cbc172`  
		Last Modified: Mon, 29 Sep 2025 23:36:17 GMT  
		Size: 47.1 MB (47137449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5367d88bcbb1eb389db217eb1d0c546a0833ba3939250ca673388d1140ce6f1c`  
		Last Modified: Mon, 29 Sep 2025 23:46:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8940f3abe2c1e4b2a7aa86acdcb453850903a6948f373142412976a3c2eb66a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f867ecfe27c67d563df7b911e13cc91706a961122dad2563f76baac3f0fe067`

```dockerfile
```

-	Layers:
	-	`sha256:0506ba4d28aba7f440b5048cf8173382eca91d15c499deabfade99de426c5525`  
		Last Modified: Tue, 30 Sep 2025 00:28:52 GMT  
		Size: 3.7 MB (3730271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c11b1d478f3aeabc77f49bee83abd832eb3313af789cc3bd851aecdbab62042`  
		Last Modified: Tue, 30 Sep 2025 00:28:53 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json
