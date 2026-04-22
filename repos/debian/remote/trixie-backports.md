## `debian:trixie-backports`

```console
$ docker pull debian@sha256:37607a69aa3fca3bd1e204a0bed103afbb30b03556213bf3e8944a7b9a1ebc7a
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:752b4e0bdf01cf7907fde43530f6d9e6d068ed8cec98d816751c246ec030f079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49302326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795ed6ff827a3e204f7c6c360f89f651d8492fff2818159e32d9b3e016d4eca9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:42 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedd1d07a6249c8164bc3082d8c3100384f8c52525cd3a576c1f820ce4d60db3`  
		Last Modified: Wed, 22 Apr 2026 01:15:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d8e1dbbc77b83e570589bfc38a1674c19bbf2d6d92e2d6342127e5e3f8fa9845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c0be88e123244069045ef00800307a069ce64e51fa47c91411226f4d481338`

```dockerfile
```

-	Layers:
	-	`sha256:123cce6ce36f55e69c7baf09e7fdf69f4c791ef298df6afd3f63ce08e1699a06`  
		Last Modified: Wed, 22 Apr 2026 01:15:49 GMT  
		Size: 3.2 MB (3170913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf84d24d8928cd05f088331824113282c864469f521ef7a60a5d374ac89ac31f`  
		Last Modified: Wed, 22 Apr 2026 01:15:48 GMT  
		Size: 5.8 KB (5783 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:41eab2d12e9ea8cdacdf2a686e9c0d7967cbf18400754a08c521167088bf9e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47461116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9463bf32b170c24edbcb2b11b689c05ea91c744144c6b1240f2dd7b99cf4e019`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:33:01 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e2d99f94edc3d8dd6e6b758a4671793ae83d782d6d01f35ad2caf70b714b475b`  
		Last Modified: Tue, 07 Apr 2026 00:11:04 GMT  
		Size: 47.5 MB (47460892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df894928d7c0c3a7bd4a64d7629ca01d2ff6434a8d2cc0650c5ed3ae240db383`  
		Last Modified: Tue, 07 Apr 2026 01:33:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5564ae0c0ed58de5d916b5e654fd6a9a0de724b98aaacbe3fb3f31247aab8e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08dd6830c177e810a11c4f18bb0f33100e3e02ecf6d11d25f232c512018b513e`

```dockerfile
```

-	Layers:
	-	`sha256:c5ac353d90f2f6ce4548ef025da962a32e32def5402a058f66f9271cec5472b9`  
		Last Modified: Tue, 07 Apr 2026 01:33:08 GMT  
		Size: 3.2 MB (3173850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:193582b803f6bc17cc729ee84c62b44884a8c24b657f875b14496a4977389a49`  
		Last Modified: Tue, 07 Apr 2026 01:33:08 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a2ead23cd07ced5392c1db37de136924fb5a9307a18e3046dbd1891a769d706a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45738417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3bec21c6979752e09a8876dcd28189b4daddb1f4d49acd2a28e9e0e3a3493d7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:49 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cc74239df6a59971739f1b7a0758f97ae57e6ab4f74daa64d264ec77db24169f`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 45.7 MB (45738193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62605cfe66216afd10bd4da40aacdc9d0f446a8c533c96f90c123dde8ddd5b7a`  
		Last Modified: Wed, 22 Apr 2026 01:15:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b65931098e001c744b2f4e28e8dbd491ca40409b4b06b8bddb6e8428b9de7066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644e42ebe9f71828c6006c90d13c8941930d7f4a4597a836547a24d3edf38274`

```dockerfile
```

-	Layers:
	-	`sha256:8b8acb2c027f7bdff8dde5ffbaae0c031fef20be7f69d8b0622e0fe05f29d4e5`  
		Last Modified: Wed, 22 Apr 2026 01:15:56 GMT  
		Size: 3.2 MB (3172287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f4af60bbdf31ebd2e6637490bf741a3a97395ef309ff019bf1d75b5d7dd8d34`  
		Last Modified: Wed, 22 Apr 2026 01:15:56 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4836b2c12ff767086abdf07aea722678b46c78923b3f8ac9f14d670d6aa1db3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49669469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a210c63042af955b16ba2a5e4fea3465099ee6dd6d833fac0388959efdb0e58`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:14:55 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662da7c9b759849f09861842faed2a945baadbce03bf1a9ea65943f34a7013dc`  
		Last Modified: Wed, 22 Apr 2026 01:15:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d90191e4cdb9912c373b13ed103f67d303e54ee3aa7f5dbebacbfbac45e8ab22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df808af76eff7944f8a663108d7421b05ddb29ba1e129b5a3865b6ddefaeb3d`

```dockerfile
```

-	Layers:
	-	`sha256:134acbd8e280f1c8ad3268bc77512a349af2ac43ca21e8a1d2e01ba2fe25ff7c`  
		Last Modified: Wed, 22 Apr 2026 01:15:02 GMT  
		Size: 3.2 MB (3172394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:792ce9b167833e208ed4199e8e894e734f58ff580eea73ec601f4e0e4a2875f5`  
		Last Modified: Wed, 22 Apr 2026 01:15:01 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:aa334e70fecdbdc8f6b69f6361324e6480f354e8b9b9da0df25a7929458cf9a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50819311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a8bd981786835ce4bddb7309613faba2817db34af777f8345187c877199d5e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:16:29 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cdc6802f3021d1c2b9488d1de8ce2706686229997f4dcbab2461da2a3a1f115f`  
		Last Modified: Tue, 07 Apr 2026 00:11:26 GMT  
		Size: 50.8 MB (50819088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6c5856c72859cb0ab9165938b30882c355e036152449dffe4ab503b028908a`  
		Last Modified: Tue, 07 Apr 2026 01:16:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7ff3a81554921ead4e5bebf15a326aab3ae2da3e46fc67feaf1322fa148d6fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8bf4a634936bd7ad8a3494fa71390e2cc4fac45ca6f3b27ee03b0811ee1c754`

```dockerfile
```

-	Layers:
	-	`sha256:ca7307d95b16f9bac249008c2adaa110592be2b76b529b323cfc6d7096346b40`  
		Last Modified: Tue, 07 Apr 2026 01:16:35 GMT  
		Size: 3.2 MB (3168115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5af4096321283481a4f7cf183c8e6182cc5487519933788a15198acc8efa0579`  
		Last Modified: Tue, 07 Apr 2026 01:16:35 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:cc57dabc994b63d96df2d2491db476b2cec8ce2e1eaf400e55e3a6eba31b952e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53118893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d949702e9606d34e5778262761021df51bfe8852b8cc6ac7b3a0fb4c4191de`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:06 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e381eb3f2c560dcec0fb42c3a64a8d68f2f9ac5d7b7b4628db77581829d4c233`  
		Last Modified: Tue, 07 Apr 2026 01:17:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:502a905a9078d8f9b4ac8bdc60cafee7cccb8894db96a3b51dedb31abe94cee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da54b9dada9d6482aa5b08f48b17479216cb208e08af1924100bbfab78f857dc`

```dockerfile
```

-	Layers:
	-	`sha256:5c9dfc71cd25f3587dde64ff53ec6b0c9fb2c70c8b7c659c4c5812574006d0e5`  
		Last Modified: Tue, 07 Apr 2026 01:17:24 GMT  
		Size: 3.2 MB (3174426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:009bb1176ad39fe2abdf7efff2b95844523d7d709d88b383ba68ac639c8de73f`  
		Last Modified: Tue, 07 Apr 2026 01:17:24 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:537e959f54bffa4e18a697f4bd05bc3c4b9c0533c0449969a25d81886c5883a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47792849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9420fe2408faab33d084d01b398858ee5e36db54c4ea4bc749baf80f33b3e3ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:32:54 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ab4796b2b5b187910f8971147259f70041e00951a1d00ecdf7c3e8e12f62d9`  
		Last Modified: Tue, 07 Apr 2026 02:33:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4e68fcfe48e766b326b80439740d5dfbd240a827d8fcc5d11bdd877c42cf4ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6600701c0b616e571b685ec454751f04dc2643b5755aeedb2e842c331737b657`

```dockerfile
```

-	Layers:
	-	`sha256:1a3332d0ee32c289ae463dbee92978e913386fc115569c40323e04fb9854a8a4`  
		Last Modified: Tue, 07 Apr 2026 02:33:48 GMT  
		Size: 3.2 MB (3163238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81b036edb19dd7150ade2c9e1617ea2d323758d583da108ac42449d29c158557`  
		Last Modified: Tue, 07 Apr 2026 02:33:47 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:57170629bb2c0935859468ebb6ae576f20a11dd13af07ab9e793aac4a350ba85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49372329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf466befb3ef61831caf9b45052b7c39634a23e85820c566239113d8fe91aff7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:14:36 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5653c2a2ae826aeda11c931196627567a732bd4f4d7dbfd6b121302a53cb1470`  
		Last Modified: Wed, 22 Apr 2026 01:14:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:34c23b2734e2a7fc3f804e97cf68804e7664faed0e63c095dce335b0237c9a55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5206c3d8cd1f4a865160c5e9ffec12a739790c9260f0cf73e80c45af306b7813`

```dockerfile
```

-	Layers:
	-	`sha256:e253eb60b3492d142473155d0efdbf19bccfd83c4c88783aa8b96921d034d744`  
		Last Modified: Wed, 22 Apr 2026 01:14:47 GMT  
		Size: 3.2 MB (3172360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c2528043a551a647f21807ee7c9ddaf813f10cec867610cbe38557e8313235d`  
		Last Modified: Wed, 22 Apr 2026 01:14:47 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
