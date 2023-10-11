## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:89dde88afc7c3198636b824910a2e817f7eb0767eeb85d8fc2e4f42145048570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1990a27deee85ef82e5e7db5911f3bce00816665dcefe5707a3af83c4a475b06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73815884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ad0a9e2f51e6708323942514a13590ee1d9cdf18f85099379432a644ee082a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:57:17 GMT
ADD file:bc0b5b71ee53adf6297821668404ace4f79c4256461b99497849721dbd8e86ae in / 
# Wed, 20 Sep 2023 04:57:18 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:25:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d036181e87bed9eb2432498f0ccbf7baa06719a2d8360c3bc9c496bd9f853a7c`  
		Last Modified: Wed, 20 Sep 2023 05:03:10 GMT  
		Size: 49.5 MB (49482728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a1e6c60efbe0c0012665a19f7b4b47dbdad105e96128f40794e9aa23e0da2c`  
		Last Modified: Wed, 20 Sep 2023 09:33:06 GMT  
		Size: 24.3 MB (24333156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:2facb29855ce778449935650ad0bf8f05285f5bc037e27c0abc545731ade43e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70157877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3ce55c97d64bebc6d52e5b52a1e5ec90df23921d54256da45d2978fabdcf44`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:38:22 GMT
ADD file:32bc859b55e9b4aada411b379418b1cd95da1e1f72e89ade7698d0132f8edafd in / 
# Wed, 11 Oct 2023 17:38:22 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:09:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2f4ea7fe7b8690c3ca25a1b3c670c2f82209d55ff6d955af872eb0ab8df5ff97`  
		Last Modified: Wed, 11 Oct 2023 17:42:28 GMT  
		Size: 47.2 MB (47164847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f544479290fab5feada5ea10b06b543b11d0716abc190b0d608b218fa5128b85`  
		Last Modified: Wed, 11 Oct 2023 18:16:56 GMT  
		Size: 23.0 MB (22993030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:59ce3291fd617342981a641a2faa5bf248fd75bd280ae2ce75a98b5212ec2fd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67147763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ff6efaf97a5d9f44cffc37ffe493201a75cb93c95308854319e4d274592681`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:58:39 GMT
ADD file:bcf56497ef1c60145d8d33d6611db5afce8122c3b654e448011714e12ab569e2 in / 
# Wed, 20 Sep 2023 04:58:39 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 15:30:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9d3df769ad992dc9a8483f18e8dddf99140307545a5d1930bf5937f68b3c1589`  
		Last Modified: Wed, 20 Sep 2023 05:04:05 GMT  
		Size: 45.0 MB (44956764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d705d8b764c841b69aecadbfac5375ae37ed8e88fc3d6fc44d1d1cf476578a50`  
		Last Modified: Wed, 20 Sep 2023 15:38:27 GMT  
		Size: 22.2 MB (22190999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:230771fb7fc85d148cbe20322880a7e10f2619754e883be36ba88073f78c69d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73335707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c1ca1fb8cdb9b67fbfe7e7094eaff64f8588d297f78b83b65755475c6cc387`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:45:16 GMT
ADD file:3493f4ad2710629ee9ad4c981682b2afcc1d9964cb5034de77189556f0c0e810 in / 
# Wed, 20 Sep 2023 02:45:17 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:28:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d83e3b52cf7f7a250777a05d8d2d7960fd6dba8a6438beed3879ff3c389bb01b`  
		Last Modified: Wed, 20 Sep 2023 02:50:04 GMT  
		Size: 49.5 MB (49450488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3c1d25120e8f2e9e343e08182a50d4c8702fe0c41bd340742c6b29f86d2bd7`  
		Last Modified: Wed, 20 Sep 2023 09:34:51 GMT  
		Size: 23.9 MB (23885219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6c5a3c841432a3311b27c5d3b9ab74fbfd33f1fc8c9c5570adcbd1a3449f301c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75645770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b139468ba853f4e64f72ad3a626476ad17acf6b17286e5b697e458ab16986cd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:19 GMT
ADD file:e8e1c13db04ddce5a6b3f4e29283e75eeecf85f213c2433ccb342a253457abc1 in / 
# Wed, 11 Oct 2023 17:42:20 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:16:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b15be2fd60b9adae282f32076fd2c71211d17ebbacfcd05f447fd925da0b81a7`  
		Last Modified: Wed, 11 Oct 2023 17:49:04 GMT  
		Size: 50.5 MB (50485267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723c0728b8af72632afafd3935c3ba7ea6efc560054e0c90b0e9ac50ffb83d95`  
		Last Modified: Wed, 11 Oct 2023 18:26:25 GMT  
		Size: 25.2 MB (25160503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3a0c2190efe62428b258355c499a180455075666e0b4b8204d21f59678153e03
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73184646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2294428dc2869d80a8f9f2f8c3b2d027393086d728e2d992cd421ecd9b253b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 03:13:05 GMT
ADD file:d3d484dbfd0f0dc6ecff269124b80444453666776b40afc16452523a3cc9dd00 in / 
# Wed, 20 Sep 2023 03:13:11 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 22:02:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d916b18191c13bb0519a1e7808ab4f18b1becaa8745ab10fbd22162e95dd7c8`  
		Last Modified: Wed, 20 Sep 2023 03:24:25 GMT  
		Size: 49.3 MB (49295906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37dac64b63353ff1a16ae4fc5513c18b3d2c448042a7486b231cf5bf73a658b`  
		Last Modified: Wed, 20 Sep 2023 22:27:05 GMT  
		Size: 23.9 MB (23888740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:cd232f49802d24b109a6845c69de40da722b1c48414c6b7198c904425c111923
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79394432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff07d1542982f90245cadfde4cf3d10fe51356a3b06794d5b5de4fb83cb01e2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:45:44 GMT
ADD file:5f062baf648f8cba61d84347ebedbe11eca129a318a8146b4c7c30586cbf0436 in / 
# Wed, 11 Oct 2023 17:45:47 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:25:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba8528ad854acf64973cba0749a6cf58ce475318878f99dccc45c01a8b19dafc`  
		Last Modified: Wed, 11 Oct 2023 17:52:11 GMT  
		Size: 53.4 MB (53418284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271e36b4d4e036584f3b2cdbde2fbfbc08b9134b8b07ed792b7e85266c0094e2`  
		Last Modified: Wed, 11 Oct 2023 18:39:33 GMT  
		Size: 26.0 MB (25976148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:463277650cb87ff963c4f3e246c78101c2bf595bfdcfda04fb4db350e9dc1592
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69007846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46d4dea6048745e0f58711f73e97cfebd76971edb90fbbf0cf7dc14a24ec144`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:09:51 GMT
ADD file:fdcff160dcad587bb28b0cba721c24193be4ab5de90a2d503cba3d329b78797b in / 
# Thu, 27 Jul 2023 23:09:54 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:32:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f8b93f818da821e670e126126d6da395bdf2888315b8baa1a6912378c2f4e02c`  
		Last Modified: Thu, 27 Jul 2023 23:12:55 GMT  
		Size: 45.7 MB (45656956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdc8d46a9f89f9d06db33ee07cddd8aa1a54e242cd6463179064bb8e0711848`  
		Last Modified: Thu, 27 Jul 2023 23:45:49 GMT  
		Size: 23.4 MB (23350890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:083ea004eda803fc309e6aa3d3ac48803eafdb955ff04c376f851589c3f6725b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73428841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9f4b88e77849051008e504e21a80474917e990b322c262ffad5c86e1c2e732`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:55:43 GMT
ADD file:aeb19ed2c9b92cbe76bb1e733b04de5bcb32489c00c1c06504aef79cd36c3c3f in / 
# Wed, 20 Sep 2023 02:55:50 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:52:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b1b4950b21705690e4b15e5257a0efcf7d334776307aaa893216166a5c37f2c0`  
		Last Modified: Wed, 20 Sep 2023 03:01:02 GMT  
		Size: 48.9 MB (48852678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bea1485478ab1093cd60cf0d37627157771e79e9a675510ea1e4233d2499a85`  
		Last Modified: Wed, 20 Sep 2023 10:00:18 GMT  
		Size: 24.6 MB (24576163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
