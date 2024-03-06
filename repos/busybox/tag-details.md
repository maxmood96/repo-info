<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `busybox`

-	[`busybox:1`](#busybox1)
-	[`busybox:1-glibc`](#busybox1-glibc)
-	[`busybox:1-musl`](#busybox1-musl)
-	[`busybox:1-uclibc`](#busybox1-uclibc)
-	[`busybox:1.35`](#busybox135)
-	[`busybox:1.35-glibc`](#busybox135-glibc)
-	[`busybox:1.35-musl`](#busybox135-musl)
-	[`busybox:1.35-uclibc`](#busybox135-uclibc)
-	[`busybox:1.35.0`](#busybox1350)
-	[`busybox:1.35.0-glibc`](#busybox1350-glibc)
-	[`busybox:1.35.0-musl`](#busybox1350-musl)
-	[`busybox:1.35.0-uclibc`](#busybox1350-uclibc)
-	[`busybox:1.36`](#busybox136)
-	[`busybox:1.36-glibc`](#busybox136-glibc)
-	[`busybox:1.36-musl`](#busybox136-musl)
-	[`busybox:1.36-uclibc`](#busybox136-uclibc)
-	[`busybox:1.36.1`](#busybox1361)
-	[`busybox:1.36.1-glibc`](#busybox1361-glibc)
-	[`busybox:1.36.1-musl`](#busybox1361-musl)
-	[`busybox:1.36.1-uclibc`](#busybox1361-uclibc)
-	[`busybox:glibc`](#busyboxglibc)
-	[`busybox:latest`](#busyboxlatest)
-	[`busybox:musl`](#busyboxmusl)
-	[`busybox:stable`](#busyboxstable)
-	[`busybox:stable-glibc`](#busyboxstable-glibc)
-	[`busybox:stable-musl`](#busyboxstable-musl)
-	[`busybox:stable-uclibc`](#busyboxstable-uclibc)
-	[`busybox:uclibc`](#busyboxuclibc)

## `busybox:1`

```console
$ docker pull busybox@sha256:acdc29f25f9c5d678b264007f6f0ea63f12756dcef1cdb043f3fd2a13ba735c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 17
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `busybox:1` - linux; amd64

```console
$ docker pull busybox@sha256:538721340ded10875f4710cad688c70e5d0ecb4dcd5e7d0c161f301f36f79414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2220094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f57d9401f8d42f986df300f0c69192fc41da28ccc8d797829467780db3dd741`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9ad63333ebc97e32b987ae66aa3cff81300e4c2e6d2f2395cef8a3ae18b249fe`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 2.2 MB (2220094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1` - unknown; unknown

```console
$ docker pull busybox@sha256:253eb45864243efd740aa87ba169151e4d165538b168d77284396469217ee5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 KB (12149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9095a17baa618e6b1b5b3da6493f78682688b3c18f07a524e30bd47a404d4cb`

```dockerfile
```

-	Layers:
	-	`sha256:e1104929ee0cb0e8ea3d2c3b4024ce9f852364d233aabe800ea7789df99cfc23`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 4.8 KB (4778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d186640ac3f58c681ac3bc3aa314992df65409336eccb7e94bd7c4b8174a2b`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 7.4 KB (7371 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1` - linux; arm variant v5

```console
$ docker pull busybox@sha256:491e28080f41a345b794a1528e23525f67f8693d8c541b9ef8f4990f6af501f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1776853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6578b94d614adfa46696754ab33bdd8b8b70ac8adea2fb6061d90e2b01f90e3`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:e209cc4af23c3ed4ac3e8cf58f8e9ea90d51fe28fcfca3ad91d91e74aabca274`  
		Last Modified: Wed, 06 Mar 2024 00:07:47 GMT  
		Size: 1.8 MB (1776853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1` - linux; arm variant v6

```console
$ docker pull busybox@sha256:b64a6a9cff5d2916ce4e5ab52254faa487ae93d9028c157c10d444aa3b5b7e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.6 KB (987570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5059e5cce9929da538b30d11caea9231836d6b937083115b4058ae4649341b74`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd544bbcb8b286d4a58e2b02357bb516d089d281fc87ae2b375921b8d2389923`  
		Last Modified: Thu, 18 Jan 2024 23:58:56 GMT  
		Size: 987.6 KB (987570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1` - unknown; unknown

```console
$ docker pull busybox@sha256:0c1556654c58755833235ba840bb04258b5cf8d3e1771be01a2c48e38c266c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e96145e5c30a04c819cb052df4fa049365de24673fc3afdc9d5305cc2999a8`

```dockerfile
```

-	Layers:
	-	`sha256:1bbd274efa1896b02a475d573d66e47cc60d67dfb2334eef4aefc1d23763fe11`  
		Last Modified: Thu, 18 Jan 2024 23:58:56 GMT  
		Size: 7.2 KB (7231 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1` - linux; arm variant v7

```console
$ docker pull busybox@sha256:8a4415fb43600953cbdac6ec03c2d96d900bb21f8d78964837dad7f73b9afcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1554425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9903cc888814e8feef24381cdb6d29d8598385dcb109a9908a4a98e1ab021532`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:a7cbd68a76a020b8b283c940bc267cd88a66013dcb160cad746344483dfc4b52`  
		Last Modified: Wed, 06 Mar 2024 00:10:11 GMT  
		Size: 1.6 MB (1554425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:8f03917912ea995c637b6c0295846aaff5665f06ac82a29b421fba4c379494e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1916607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4fd538a9a0b729be05707cf805388be2fb701cfd5d44c6542f1988e8aef6e3`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c2bf9493c1bf786e95e3eac7d406c20aa1b8a2d40916756e891627e9e8f8d119`  
		Last Modified: Fri, 19 Jan 2024 00:32:32 GMT  
		Size: 1.9 MB (1916607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1` - unknown; unknown

```console
$ docker pull busybox@sha256:a69e011a60760aba5dd1209f91c05980c6fab54d8b25ae169291e63377f51cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 KB (12193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd1ff0b19ae0f0339dfa452087f6e62d3885ac4cd6d87c8b93b3893fa44b0b6`

```dockerfile
```

-	Layers:
	-	`sha256:24ccf6b7ae0e49578be9c4155a809a71d3e4b9c5486ce7c4086d68e3d1acd22f`  
		Last Modified: Fri, 19 Jan 2024 00:32:31 GMT  
		Size: 4.8 KB (4800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53a196fbf5767399864392abcd4b090e16c2f74821ac8b44d3f139986875dae`  
		Last Modified: Fri, 19 Jan 2024 00:32:31 GMT  
		Size: 7.4 KB (7393 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1` - linux; 386

```console
$ docker pull busybox@sha256:99eabec0f153fb38feb80682492123326c994a6857f7ef9b73d46eecd8b81684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2268883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a422f55b78a61a0acf17d1ad4cea56c7542f1a09e6a256def15b8787d41ad7a`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:b6f95b873e20279fb8550d2d0b30bff9e72de3fe85f2ff4cfbf5f8f8aa6dabf4`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 2.3 MB (2268883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1` - unknown; unknown

```console
$ docker pull busybox@sha256:deb0f17418ba410fceb230e48f01a2056732cba642d66a812901fa3d039c7e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 KB (12043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e79a31fa88e6a7c031f212bf2849dfb712003711e72dcae4abf34405846cdcf`

```dockerfile
```

-	Layers:
	-	`sha256:347076177c54f21c7c7fd98a9a45a717898d8441f14a94c5248a682a00008516`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 4.7 KB (4725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcf8fff8866352521d3aef70307e34f73f9951524290a8b4b36ffb75b6e6c138`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 7.3 KB (7318 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1` - linux; mips64le

```console
$ docker pull busybox@sha256:8c4284fa9cc28d0b9455f84527de8b58d5d4df00abcd18e47f2f1dc4e89f7ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2077641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c67790aa14859c61c94e0b7e727a8c50a5e246783c252e080ae41187e8ec52`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:b9f2f1866e3467e8735b90ecad932b7c1f122f80426b5beda6fb8a4c87f45757`  
		Last Modified: Wed, 06 Mar 2024 00:08:46 GMT  
		Size: 2.1 MB (2077641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1` - linux; ppc64le

```console
$ docker pull busybox@sha256:4b36905f6e9385ec2234f41dbb9d67ccd99ee2b50ef225c08746b2276991bb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb40c4cff2a5d1551f5a9e79b6fac3cf2d655f702041d0ae8d670e027645bd9`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1e329ff3bf1d3bf69d13da2954652acf3457a6fbd276780a232bb5254c915148`  
		Last Modified: Fri, 19 Jan 2024 00:42:12 GMT  
		Size: 2.5 MB (2528609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1` - unknown; unknown

```console
$ docker pull busybox@sha256:17110abebf0882f7e23b68ea936ab719a49047e1b4a8e0ab0118ff0abff0066d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 KB (12281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48490b9b70ffd6de2941a4f2dbecc81750fe06d0c527e787a94fff4504c7721`

```dockerfile
```

-	Layers:
	-	`sha256:07f1bfa21dee33589c5658c47aa84655e024d44ef684cbd102571f1fdaa89c48`  
		Last Modified: Fri, 19 Jan 2024 00:42:12 GMT  
		Size: 4.8 KB (4842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f2fcbb930547c7a7fa4783062b75854e39e225a8dc9dbf51df1bcb5b2580c4`  
		Last Modified: Fri, 19 Jan 2024 00:42:11 GMT  
		Size: 7.4 KB (7439 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1` - linux; riscv64

```console
$ docker pull busybox@sha256:41af629cfa908c7ed7550db6a260c79d6dd55fe4996d7481595e3d547ab829c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.3 KB (914275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9673ad33efcd24dfd28f0415f23ee1c42d743140691e10781669692ef3af1ba6`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:917dbba7e6e14feb5914ca2711ff13b50b1f9a2b0b8315b79bbceabde34d11c2`  
		Last Modified: Thu, 18 Jan 2024 23:05:50 GMT  
		Size: 914.3 KB (914275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1` - unknown; unknown

```console
$ docker pull busybox@sha256:126af02605028b8076a4a47fe1c707c795ce58c66a266c67b447519ebf1f3b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 KB (12303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa149c79ad9040800185662b3a226758c08cd6d612ca2a1abf6ebf0d9716f32`

```dockerfile
```

-	Layers:
	-	`sha256:1acfa35c63c5a80ca903c34528318a0b6b614a7060738be73b2b8424004473b1`  
		Last Modified: Thu, 18 Jan 2024 23:05:50 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97288386ab763b23aa899ebcfaa85d4b1708c86df318569f03865c7fb2b7ad4f`  
		Last Modified: Thu, 18 Jan 2024 23:05:51 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1` - linux; s390x

```console
$ docker pull busybox@sha256:df5506ae24620e67cb668f0137869babd6305cf4912190ee7de781c412b9bad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1926831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a46af96236bcedbc5591856e442999857d24fd51f5ff2135ede6486c79e2e7`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:230db3ea6af07ccf4b5f3ad6164f90d07967b83607909a587631245cc7c84ef4`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 1.9 MB (1926831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1` - unknown; unknown

```console
$ docker pull busybox@sha256:b2a97dca77d5ae1e0ddef0cbfba271b5f0597c9ea7b8cb8127b397c7c9d03dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 KB (12149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e23940337a50804f81942abe24849f22423565ad3dabdfeefa3ee5cc61fd96`

```dockerfile
```

-	Layers:
	-	`sha256:5f4fdc6f7194500531229dc2d7aa2b54119cdf908b5e842b6ae1bfbf57487b79`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 4.8 KB (4778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ad8320e0617081f2bb73e6289f33979e1ee192d12ef3459b3bfe278084c075c`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 7.4 KB (7371 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:1-glibc`

```console
$ docker pull busybox@sha256:eba7ad4cfa554dd96910090a41fa8eee6d4231f92bf5587dbd05a4badfeec2cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `busybox:1-glibc` - linux; amd64

```console
$ docker pull busybox@sha256:538721340ded10875f4710cad688c70e5d0ecb4dcd5e7d0c161f301f36f79414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2220094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f57d9401f8d42f986df300f0c69192fc41da28ccc8d797829467780db3dd741`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9ad63333ebc97e32b987ae66aa3cff81300e4c2e6d2f2395cef8a3ae18b249fe`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 2.2 MB (2220094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:253eb45864243efd740aa87ba169151e4d165538b168d77284396469217ee5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 KB (12149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9095a17baa618e6b1b5b3da6493f78682688b3c18f07a524e30bd47a404d4cb`

```dockerfile
```

-	Layers:
	-	`sha256:e1104929ee0cb0e8ea3d2c3b4024ce9f852364d233aabe800ea7789df99cfc23`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 4.8 KB (4778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d186640ac3f58c681ac3bc3aa314992df65409336eccb7e94bd7c4b8174a2b`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 7.4 KB (7371 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1-glibc` - linux; arm variant v5

```console
$ docker pull busybox@sha256:491e28080f41a345b794a1528e23525f67f8693d8c541b9ef8f4990f6af501f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1776853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6578b94d614adfa46696754ab33bdd8b8b70ac8adea2fb6061d90e2b01f90e3`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:e209cc4af23c3ed4ac3e8cf58f8e9ea90d51fe28fcfca3ad91d91e74aabca274`  
		Last Modified: Wed, 06 Mar 2024 00:07:47 GMT  
		Size: 1.8 MB (1776853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1-glibc` - linux; arm variant v7

```console
$ docker pull busybox@sha256:8a4415fb43600953cbdac6ec03c2d96d900bb21f8d78964837dad7f73b9afcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1554425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9903cc888814e8feef24381cdb6d29d8598385dcb109a9908a4a98e1ab021532`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:a7cbd68a76a020b8b283c940bc267cd88a66013dcb160cad746344483dfc4b52`  
		Last Modified: Wed, 06 Mar 2024 00:10:11 GMT  
		Size: 1.6 MB (1554425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1-glibc` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:8f03917912ea995c637b6c0295846aaff5665f06ac82a29b421fba4c379494e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1916607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4fd538a9a0b729be05707cf805388be2fb701cfd5d44c6542f1988e8aef6e3`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c2bf9493c1bf786e95e3eac7d406c20aa1b8a2d40916756e891627e9e8f8d119`  
		Last Modified: Fri, 19 Jan 2024 00:32:32 GMT  
		Size: 1.9 MB (1916607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:a69e011a60760aba5dd1209f91c05980c6fab54d8b25ae169291e63377f51cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 KB (12193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd1ff0b19ae0f0339dfa452087f6e62d3885ac4cd6d87c8b93b3893fa44b0b6`

```dockerfile
```

-	Layers:
	-	`sha256:24ccf6b7ae0e49578be9c4155a809a71d3e4b9c5486ce7c4086d68e3d1acd22f`  
		Last Modified: Fri, 19 Jan 2024 00:32:31 GMT  
		Size: 4.8 KB (4800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53a196fbf5767399864392abcd4b090e16c2f74821ac8b44d3f139986875dae`  
		Last Modified: Fri, 19 Jan 2024 00:32:31 GMT  
		Size: 7.4 KB (7393 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1-glibc` - linux; 386

```console
$ docker pull busybox@sha256:99eabec0f153fb38feb80682492123326c994a6857f7ef9b73d46eecd8b81684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2268883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a422f55b78a61a0acf17d1ad4cea56c7542f1a09e6a256def15b8787d41ad7a`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:b6f95b873e20279fb8550d2d0b30bff9e72de3fe85f2ff4cfbf5f8f8aa6dabf4`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 2.3 MB (2268883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:deb0f17418ba410fceb230e48f01a2056732cba642d66a812901fa3d039c7e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 KB (12043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e79a31fa88e6a7c031f212bf2849dfb712003711e72dcae4abf34405846cdcf`

```dockerfile
```

-	Layers:
	-	`sha256:347076177c54f21c7c7fd98a9a45a717898d8441f14a94c5248a682a00008516`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 4.7 KB (4725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcf8fff8866352521d3aef70307e34f73f9951524290a8b4b36ffb75b6e6c138`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 7.3 KB (7318 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1-glibc` - linux; mips64le

```console
$ docker pull busybox@sha256:8c4284fa9cc28d0b9455f84527de8b58d5d4df00abcd18e47f2f1dc4e89f7ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2077641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c67790aa14859c61c94e0b7e727a8c50a5e246783c252e080ae41187e8ec52`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:b9f2f1866e3467e8735b90ecad932b7c1f122f80426b5beda6fb8a4c87f45757`  
		Last Modified: Wed, 06 Mar 2024 00:08:46 GMT  
		Size: 2.1 MB (2077641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1-glibc` - linux; ppc64le

```console
$ docker pull busybox@sha256:4b36905f6e9385ec2234f41dbb9d67ccd99ee2b50ef225c08746b2276991bb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb40c4cff2a5d1551f5a9e79b6fac3cf2d655f702041d0ae8d670e027645bd9`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1e329ff3bf1d3bf69d13da2954652acf3457a6fbd276780a232bb5254c915148`  
		Last Modified: Fri, 19 Jan 2024 00:42:12 GMT  
		Size: 2.5 MB (2528609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:17110abebf0882f7e23b68ea936ab719a49047e1b4a8e0ab0118ff0abff0066d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 KB (12281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48490b9b70ffd6de2941a4f2dbecc81750fe06d0c527e787a94fff4504c7721`

```dockerfile
```

-	Layers:
	-	`sha256:07f1bfa21dee33589c5658c47aa84655e024d44ef684cbd102571f1fdaa89c48`  
		Last Modified: Fri, 19 Jan 2024 00:42:12 GMT  
		Size: 4.8 KB (4842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f2fcbb930547c7a7fa4783062b75854e39e225a8dc9dbf51df1bcb5b2580c4`  
		Last Modified: Fri, 19 Jan 2024 00:42:11 GMT  
		Size: 7.4 KB (7439 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1-glibc` - linux; s390x

```console
$ docker pull busybox@sha256:df5506ae24620e67cb668f0137869babd6305cf4912190ee7de781c412b9bad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1926831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a46af96236bcedbc5591856e442999857d24fd51f5ff2135ede6486c79e2e7`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:230db3ea6af07ccf4b5f3ad6164f90d07967b83607909a587631245cc7c84ef4`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 1.9 MB (1926831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:b2a97dca77d5ae1e0ddef0cbfba271b5f0597c9ea7b8cb8127b397c7c9d03dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 KB (12149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e23940337a50804f81942abe24849f22423565ad3dabdfeefa3ee5cc61fd96`

```dockerfile
```

-	Layers:
	-	`sha256:5f4fdc6f7194500531229dc2d7aa2b54119cdf908b5e842b6ae1bfbf57487b79`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 4.8 KB (4778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ad8320e0617081f2bb73e6289f33979e1ee192d12ef3459b3bfe278084c075c`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 7.4 KB (7371 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:1-musl`

```console
$ docker pull busybox@sha256:9a7f0d2407780a98013e227ddc43f87bf5fbe626fb59f98280efd591c75ccdec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `busybox:1-musl` - linux; amd64

```console
$ docker pull busybox@sha256:d4707523ce6e12afdbe9a3be5ad69027150a834870ca0933baf7516dd1fe0f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **878.7 KB (878681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59888ccc9e6510deabb10bb0452f184f40cec7064c0fc522a01924f66c7fdfd8`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8dfc70c9a1cfc61f5873aed748e446239a5cb27faddd51d118180665010c02b7`  
		Last Modified: Thu, 18 Jan 2024 23:03:35 GMT  
		Size: 878.7 KB (878681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:864e79c6eb0056047a68c6c717ee53d548519ee307dec471696a5e6d0fab0a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c89e5c4f095b960e7a950b75e8f1386f0c1d1d43c108818b9b3922c803c1f1d`

```dockerfile
```

-	Layers:
	-	`sha256:aa7db50a9fdf0d3338cc08bc515695143e4aaf3e3e4b276f5f6d6d3bba5cca05`  
		Last Modified: Thu, 18 Jan 2024 23:03:35 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce0dddc950954bfb91430621087a12e68a552255f8c49ff243c27b22fbc6280`  
		Last Modified: Thu, 18 Jan 2024 23:03:35 GMT  
		Size: 5.9 KB (5871 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1-musl` - linux; arm variant v6

```console
$ docker pull busybox@sha256:b64a6a9cff5d2916ce4e5ab52254faa487ae93d9028c157c10d444aa3b5b7e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.6 KB (987570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5059e5cce9929da538b30d11caea9231836d6b937083115b4058ae4649341b74`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd544bbcb8b286d4a58e2b02357bb516d089d281fc87ae2b375921b8d2389923`  
		Last Modified: Thu, 18 Jan 2024 23:58:56 GMT  
		Size: 987.6 KB (987570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:0c1556654c58755833235ba840bb04258b5cf8d3e1771be01a2c48e38c266c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e96145e5c30a04c819cb052df4fa049365de24673fc3afdc9d5305cc2999a8`

```dockerfile
```

-	Layers:
	-	`sha256:1bbd274efa1896b02a475d573d66e47cc60d67dfb2334eef4aefc1d23763fe11`  
		Last Modified: Thu, 18 Jan 2024 23:58:56 GMT  
		Size: 7.2 KB (7231 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1-musl` - linux; arm variant v7

```console
$ docker pull busybox@sha256:f2939eb0b529af5706172c10db02a0894949c461b81ed4282ff4df5bf18c14d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.6 KB (843648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855943b02ba3319e1345d803a557c4a88bfd0c18954db6869f2ac791e17c4ae3`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (musl), Alpine 3.19.1
```

-	Layers:
	-	`sha256:83dc776fdc81b19e8a0c134d8eecfc7793d00ca52c1cc4292e973750e3684712`  
		Last Modified: Wed, 06 Mar 2024 00:10:38 GMT  
		Size: 843.6 KB (843648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1-musl` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:fed6b26ea319254ef0d6bae87482b5ab58b85250a7cc46d14c533e1f5c2556db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.0 KB (920992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f13cdcd8df2876053fd8dc5d01363344a92ea4d6537bd78625b9209e988edf`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d997961b9429e6c49b53a709a914c6578f5ff5ba7166ee52de62d1ac94887c1e`  
		Last Modified: Fri, 19 Jan 2024 01:36:22 GMT  
		Size: 921.0 KB (920992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:1cbd2ff89d7ff09ec11e246f3a887f3a914ab78b5d7445c43487b8c6fbed88cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83f629b0163590a531f21a762bb0cbaa263d937678e8f68d96a31c90ef4a07b`

```dockerfile
```

-	Layers:
	-	`sha256:3c2685448006e438049a85838a6b8137f2e8454a9bc20b249241ff956b520505`  
		Last Modified: Fri, 19 Jan 2024 01:36:22 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6177450e2c462aaedbb8f947886eb918cc00046a7fdc55ccca512c51f9243ee4`  
		Last Modified: Fri, 19 Jan 2024 01:36:22 GMT  
		Size: 5.9 KB (5883 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1-musl` - linux; 386

```console
$ docker pull busybox@sha256:b6678a8456f13554d339f393c4bcf798b3730a4f1662f6d9842129cbeeb5c665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.5 KB (875482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e9971e1ff6c5b5940f3f82628fe182aead284575c0ae4a798ed91e15ef08d7`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:769db000cf23b44ad2664168ee3886ca8883b18f32581f08cd06ce00f41ff872`  
		Last Modified: Thu, 18 Jan 2024 23:03:39 GMT  
		Size: 875.5 KB (875482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:fcc65e203ef7a06b3c9852b25de034cc8472405e5d7f033e818752a15778a758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa92905283639dceabeee0502770622fc73c4856e769907a58b011d8c5ea776f`

```dockerfile
```

-	Layers:
	-	`sha256:9020223ee3ca8d6d37dab73b397baddf426d3d408db20f63d02b1e9d2faff9d6`  
		Last Modified: Thu, 18 Jan 2024 23:03:39 GMT  
		Size: 3.3 KB (3254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6eae553040cde89419e4a177c32658f1d867ec25cf9a30b7655184d189a9439`  
		Last Modified: Thu, 18 Jan 2024 23:03:39 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1-musl` - linux; ppc64le

```console
$ docker pull busybox@sha256:74dfdbf9d13a59af2f6aa61ad738fa1fdade6dfd0d6f687eb3b0d53ffc8b5623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **967.1 KB (967138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f646f514a9f9bafe5483609c8bb0c3c64f9628f35d9beffda459a7fc992d9fe0`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:e4d8791bb918bc69b870f21a553724ec9b2812219040885317ce57b6eb4e6ab3`  
		Last Modified: Fri, 19 Jan 2024 01:03:30 GMT  
		Size: 967.1 KB (967138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:832836469bae4830469c6b70aa0ca4cf84181eb2a11484479ea37d6ce6143846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376ae5066f35abd2be10b0eacfecd79b91086e268f707d436e7b8798c411fcf9`

```dockerfile
```

-	Layers:
	-	`sha256:1ecc1159b446640a86f9969f010bbc8178567a5b46e779b2ce340b9229dac07e`  
		Last Modified: Fri, 19 Jan 2024 01:03:30 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a8411155c9d98fe9609d4ca6e64859296085c39baa2e804ebae951ab5b80b8`  
		Last Modified: Fri, 19 Jan 2024 01:03:30 GMT  
		Size: 5.9 KB (5909 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1-musl` - linux; s390x

```console
$ docker pull busybox@sha256:e7e0969b47c05409c0fa5c909e006a620f845d5b119869c8346e4f3cb93f8c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **940.3 KB (940326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774f60d2b6d3daa542d524858ddb90ae71c4b3cc014a0235132a36c51e1d4515`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:48e10ecef46b18109935c897c4fb6ba3b06fea3fc7b54588e2aef37a9ecc7db9`  
		Last Modified: Sat, 20 Jan 2024 17:54:57 GMT  
		Size: 940.3 KB (940326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:6ac7f239a3bffeaff764ae1948e58f80497ce3fe2d2bdfb42b7c9899ac58270e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2deb03e82c885a1c5de5b9ffc72f3b12beb43f880ffec52862abecf85ba22e4`

```dockerfile
```

-	Layers:
	-	`sha256:72517eef4c47c126a39ac1b293ba0bcfcb63a31962064a4a8bc3907115262d23`  
		Last Modified: Sat, 20 Jan 2024 17:54:57 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:990936cff923ba93c536c3d8f4ba7db950b54f638d8ca2d0b278ed1e0110f3b9`  
		Last Modified: Sat, 20 Jan 2024 17:54:57 GMT  
		Size: 5.9 KB (5871 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:1-uclibc`

```console
$ docker pull busybox@sha256:61651f1730187bbbfaa01e81d31eb082a1853a14118255c7dff5f1365d0ca3e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; riscv64
	-	unknown; unknown

### `busybox:1-uclibc` - linux; amd64

```console
$ docker pull busybox@sha256:21de0dff31b277e0d37fe21f6e89e461f5c07415719d225235121c144287dc17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **783.2 KB (783164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e537aeebf5260fe6cb054017b3af5862945ab73f5a7091cd6e2127cdfdd5a14`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cff2761077a7b33f0ac06f806d159087b8c79413afc45167a232c5b9394615f1`  
		Last Modified: Thu, 18 Jan 2024 23:03:48 GMT  
		Size: 783.2 KB (783164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:385fe86cbfdf640c4538befe889e1e9bf93fa21eeb9955f7ea076e6d874a2d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7796465a33cc98caddbb8bc190b367eaeb431320484f406887f0d1c8578327c`

```dockerfile
```

-	Layers:
	-	`sha256:165aad5817a1de48ec8d7d517f5332a81840adf0cc4836a6c3f4aad1ac31e128`  
		Last Modified: Thu, 18 Jan 2024 23:03:51 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f647335cce5641a56b28c17896a32f125e7d6823621a542398ee88b0754d863`  
		Last Modified: Thu, 18 Jan 2024 23:03:48 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1-uclibc` - linux; arm variant v5

```console
$ docker pull busybox@sha256:2e2d13aea845763e5152bb8116738d5179f67b79fc6fde83bf813896829d4bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.2 KB (744233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be06eb6ec3aaf1ca11f443876561f4e75e1dd0ceb407c1880033d7ff6328b3e`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (uclibc), Buildroot 2023.11.1, Debian 12
```

-	Layers:
	-	`sha256:120231968b7db68bb2d25cd765a3eee8fe0ec5be354a4306354fdd9606bd7774`  
		Last Modified: Wed, 06 Mar 2024 00:08:00 GMT  
		Size: 744.2 KB (744233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1-uclibc` - linux; arm variant v7

```console
$ docker pull busybox@sha256:b87edd76d8d0b9e848a0059a3014d87dabf763bc6cfcb9df52d13f4523a3d371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.9 KB (708929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2858fb01eb20e8b8f27c5d3108e9df3065a5c3196a170111aabbf09b81d4bf9`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (uclibc), Buildroot 2023.11.1, Debian 12
```

-	Layers:
	-	`sha256:19210f7552436b95fa7de660fcbf9e9425a0813bfccb850b3fcd053709caf443`  
		Last Modified: Wed, 06 Mar 2024 00:10:24 GMT  
		Size: 708.9 KB (708929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1-uclibc` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:b8879bdf897086348b8048b0a5ae3d85addc583ed20050328ec7146858e847e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **836.8 KB (836843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80467bacead9d1b091a5648f067f735716b201eba3fd71a4fb44e13f5341f0cd`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cea42dbd04d75d2786e9fef4399413709452debd69b417e4c200743b4b844c00`  
		Last Modified: Fri, 19 Jan 2024 00:57:12 GMT  
		Size: 836.8 KB (836843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:d872e2c2932c6bd7821197d583a23869fdb68bf056a7d7dac8a97e20e62bd6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a42e696a19934cb4621a011849c38a5b99a99a7db2a5f5914af4bd5c886b3f4`

```dockerfile
```

-	Layers:
	-	`sha256:4f836af667398f1a6feb5e25980960f902daf9096ca799ab436dba129c2c8698`  
		Last Modified: Fri, 19 Jan 2024 00:57:11 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:880e28375df06f638d5045451a8dda0fc51cc28429dba1387275de009fd5d3b3`  
		Last Modified: Fri, 19 Jan 2024 00:57:11 GMT  
		Size: 5.9 KB (5909 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1-uclibc` - linux; 386

```console
$ docker pull busybox@sha256:b805bdb43c275243e31c549abcc71d98c1323a225598b74e5a9b9dc91fdf4073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **747.9 KB (747949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992d7e8ad26e67c26250373ac39142b725403b68173a52edacc7c191cf5f097a`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d6a6d95c0da603317dbc3d49423910ecb730bb5d4219de536cfd7120bd1d792e`  
		Last Modified: Thu, 18 Jan 2024 23:03:27 GMT  
		Size: 747.9 KB (747949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:3cb35ce2ebff606afe19b8965ea3f0fe093bbbfc9fabc67a3158c7f4cd146068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c6ca91c6552ef25e52903cad76d996d7b60375a160b4205a35c7b060549a35`

```dockerfile
```

-	Layers:
	-	`sha256:cd8b24a6892d4af4db2582c4db92db552c251baa708fd3d249742144a1f06c65`  
		Last Modified: Thu, 18 Jan 2024 23:03:27 GMT  
		Size: 3.3 KB (3274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3117b42969c2d3cfbd84681cccff735d766b482184839bd402d14f12180792ad`  
		Last Modified: Thu, 18 Jan 2024 23:03:27 GMT  
		Size: 5.9 KB (5868 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1-uclibc` - linux; mips64le

```console
$ docker pull busybox@sha256:388eed10bf5614e88ae1e2b2c1d237cbef877a07858125415556e3d9edff526d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **948.9 KB (948864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd60f88674723ffdec05a32d2bee1157f95e335ced9c3efea5686b9b15cd1416`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (uclibc), Buildroot 2023.11.1, Debian 12
```

-	Layers:
	-	`sha256:16b2225af5a2181079c894731b1031c046d90aca99349dd3487cfc6d6702d0e3`  
		Last Modified: Wed, 06 Mar 2024 00:09:07 GMT  
		Size: 948.9 KB (948864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1-uclibc` - linux; riscv64

```console
$ docker pull busybox@sha256:41af629cfa908c7ed7550db6a260c79d6dd55fe4996d7481595e3d547ab829c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.3 KB (914275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9673ad33efcd24dfd28f0415f23ee1c42d743140691e10781669692ef3af1ba6`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:917dbba7e6e14feb5914ca2711ff13b50b1f9a2b0b8315b79bbceabde34d11c2`  
		Last Modified: Thu, 18 Jan 2024 23:05:50 GMT  
		Size: 914.3 KB (914275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:126af02605028b8076a4a47fe1c707c795ce58c66a266c67b447519ebf1f3b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 KB (12303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa149c79ad9040800185662b3a226758c08cd6d612ca2a1abf6ebf0d9716f32`

```dockerfile
```

-	Layers:
	-	`sha256:1acfa35c63c5a80ca903c34528318a0b6b614a7060738be73b2b8424004473b1`  
		Last Modified: Thu, 18 Jan 2024 23:05:50 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97288386ab763b23aa899ebcfaa85d4b1708c86df318569f03865c7fb2b7ad4f`  
		Last Modified: Thu, 18 Jan 2024 23:05:51 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:1.35`

```console
$ docker pull busybox@sha256:4a598f8a53a7fa34917d24f9dad23b614810c7b528a84559fd5caee7f3c1e17d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 17
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `busybox:1.35` - linux; amd64

```console
$ docker pull busybox@sha256:462231a4068d238616e330a49aa4c0896a61c4003adde5cbe6879caa7f1992de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c00acac9c2794adfa8bb7b13ef38504300b505a043bf68dff7a00068dcc732b`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2354422721e449fa3fa83b84465b9d5bb65ac5415ec93c06f598854312e8957e`  
		Last Modified: Thu, 18 Jan 2024 23:03:25 GMT  
		Size: 2.2 MB (2212939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35` - unknown; unknown

```console
$ docker pull busybox@sha256:ce63139305fd383ca8e320211f874a624b8b4a2e05307b9c18f37f69d0d98913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 KB (8551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ce1c047b16326ce720cd6e2d12a9189050c9306cb350864a132f836b56280c`

```dockerfile
```

-	Layers:
	-	`sha256:25c6d85b554105b1eb62bf541d8ba40745768e287fe13dd71a9fc2fe9680197d`  
		Last Modified: Thu, 18 Jan 2024 23:03:25 GMT  
		Size: 3.0 KB (2976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81c7c2a7711e2add234a2694186a75c0c1ceb5c852a72c96af466f4f24e41c69`  
		Last Modified: Thu, 18 Jan 2024 23:03:25 GMT  
		Size: 5.6 KB (5575 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35` - linux; arm variant v5

```console
$ docker pull busybox@sha256:3cb1d74becebf3031646d8d4822728973482e2e56b73a6669243a52aaf1544ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1772716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f419b164f0f391706417345127f8bbf8d7b747e24283b6a5ee48a348d5c157a`
-	Default Command: `["sh"]`

```dockerfile
# Sun, 26 Dec 2021 16:56:57 GMT
RUN BusyBox 1.35.0 (glibc), Debian 12
```

-	Layers:
	-	`sha256:b59bb812a84f8d3e6554de2334ce709ce2ddd45b2122f4243d195d8311296290`  
		Last Modified: Wed, 06 Mar 2024 00:08:14 GMT  
		Size: 1.8 MB (1772716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35` - linux; arm variant v6

```console
$ docker pull busybox@sha256:c7f19b2a99f29f55049763f30c63c47c9bdca74f1eb58129c90cb200565cbafd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.2 KB (982203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eeabca632d8676e6d6c1acf9811e4bccda69f8182c70709058b96af9e30c520`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:eb75023da78324fbaccf28f5cfe7d06a00358e27f865593f058b0c72c1c47131`  
		Last Modified: Fri, 19 Jan 2024 00:06:15 GMT  
		Size: 982.2 KB (982203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35` - unknown; unknown

```console
$ docker pull busybox@sha256:d89dc84838ba45e53a43defc1f4b6c61fe74afeb9ef4200e12427dd1767e0c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 KB (5392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50180279f5b44900fd416af7735026eba4b77c710780d7c9e30c5ec845699577`

```dockerfile
```

-	Layers:
	-	`sha256:9606dc24cdf8f1271dcc65fa1f9a3b1484d93e64d07de2986fc9b512532257e8`  
		Last Modified: Fri, 19 Jan 2024 00:06:14 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35` - linux; arm variant v7

```console
$ docker pull busybox@sha256:9ad13fde87c1a28d0f81f25851b9bbf442691310607311ec8c563e2103536e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1550275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d335b8de554e790e78e0b1a84e0b148c3ac7ada67f91b0c22b34b3c3dd946b8e`
-	Default Command: `["sh"]`

```dockerfile
# Sun, 26 Dec 2021 16:56:57 GMT
RUN BusyBox 1.35.0 (glibc), Debian 12
```

-	Layers:
	-	`sha256:bbcae909f65630db46bda0bbbbdca543c71fec5233df65620405f8e11b831d9f`  
		Last Modified: Wed, 06 Mar 2024 00:10:56 GMT  
		Size: 1.6 MB (1550275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:05d019b284f629eddedf2d63b6a62c084bcadc1d7b1deaabdc76c66b609f6c9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1913311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcedb5826f9d4e187e358214a4a1d503c33448d15b57eacc882aa8da640b19c`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:37dfde395fb0e71c422335995f1b44064442171f53b0979f11f6bf919fbdda28`  
		Last Modified: Fri, 19 Jan 2024 01:52:11 GMT  
		Size: 1.9 MB (1913311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35` - unknown; unknown

```console
$ docker pull busybox@sha256:c0c7478f2d9213e1550dcd040149b1cecb49b771a73ab320568fc79c47f403ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 KB (8571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5ed5d452b1f21eb43710dbeda0fbf5d6570d6856fb028961604f050f45a22a`

```dockerfile
```

-	Layers:
	-	`sha256:5595c6eb9287ff73c8d8e69d0e880190d4fe189a94f52a032784aafcec3aa238`  
		Last Modified: Fri, 19 Jan 2024 01:52:11 GMT  
		Size: 3.0 KB (2986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a430708e41abcad94463dce7ba8976703febec19dae1e6ae1918639864896b0c`  
		Last Modified: Fri, 19 Jan 2024 01:52:11 GMT  
		Size: 5.6 KB (5585 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35` - linux; 386

```console
$ docker pull busybox@sha256:acb951a45cc2407d4a7bc8af187d477254694faf7590b9396fdda5fd04c90c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2264085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72caec8a3c0377d18f5f695b63ead89d34e3768907d63c7060bbba98d000993`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:18964fea37a7ba3237684b9f0850daecc248d4422709cdc7f495301c3f2025f4`  
		Last Modified: Thu, 18 Jan 2024 23:03:32 GMT  
		Size: 2.3 MB (2264085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35` - unknown; unknown

```console
$ docker pull busybox@sha256:022caa5a29959876efc12343dbd422bffdf80b800c5c47b7a84ed71881eea784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 KB (8505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ad2f8aea767ef2e9d2b36fb3c8b0b69913679e4cef86d70109bad47e06b7b6`

```dockerfile
```

-	Layers:
	-	`sha256:a17e8c3966826c87cdb35d0a9249aa1ae7e7d867e28fe07bdec612fb21334a6b`  
		Last Modified: Thu, 18 Jan 2024 23:03:32 GMT  
		Size: 3.0 KB (2953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40844810caa868ad53fa21b45e474a7f3e3f71d1702ff917265abbcdc22d69ca`  
		Last Modified: Thu, 18 Jan 2024 23:03:32 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35` - linux; mips64le

```console
$ docker pull busybox@sha256:4f42e99c852996a8f560b737046a8501fb714664914b9aab6c08796739497195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2072932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0905a181f6a06656547a117e6ddf579ddc6706a18ec7334c91af5d737b9b6c3a`
-	Default Command: `["sh"]`

```dockerfile
# Sun, 26 Dec 2021 16:56:57 GMT
RUN BusyBox 1.35.0 (glibc), Debian 12
```

-	Layers:
	-	`sha256:bde827b12c95d1ece79ad25f0839a526e44b3fe4e8148f21957b007c3b8e5488`  
		Last Modified: Wed, 06 Mar 2024 00:09:28 GMT  
		Size: 2.1 MB (2072932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35` - linux; ppc64le

```console
$ docker pull busybox@sha256:d2b10a11ed4117229cb399588b887956ff05a9541577a825c3ef12390a29a00e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2523465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64849f6b691d998aef552e64ed2aa7d2428421b3cbffaf6530bc0cfe78231aa7`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:de183f91e330998a45a7ce3945ce6cb95565b808920d4f702326d757519d7a0d`  
		Last Modified: Fri, 19 Jan 2024 01:38:22 GMT  
		Size: 2.5 MB (2523465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35` - unknown; unknown

```console
$ docker pull busybox@sha256:869d38b81c849a53e15d3bcce944e075cc69be0be325d5978187bae28778df09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 KB (8611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac98edb286e659de67f172339c6d2609921c484ead187c9a9b47b2382e6272a`

```dockerfile
```

-	Layers:
	-	`sha256:a9bba9b2a154c8acc57919e4ae0fca4a9c4f8ef796580ce577e66f0c6d30697f`  
		Last Modified: Fri, 19 Jan 2024 01:38:22 GMT  
		Size: 3.0 KB (3004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b743576ba60eaebb52475f473cf8e9c8250aaf3ad0e1467e6f6e9c4de23943`  
		Last Modified: Fri, 19 Jan 2024 01:38:22 GMT  
		Size: 5.6 KB (5607 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35` - linux; riscv64

```console
$ docker pull busybox@sha256:9acc76dacdcf324e5349d8bb516f93a6bd51c3dd056b1e54f84ed232d7218663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **911.2 KB (911232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adeffaa38ccdb1bbf3208a6a7cda3c5e4befe92ff57391761f07be40f5aac113`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:429ffc68429126516047bcf0f37ad1d12806c4e3f8cf5892c65772562d564ee8`  
		Last Modified: Thu, 18 Jan 2024 23:07:04 GMT  
		Size: 911.2 KB (911232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35` - unknown; unknown

```console
$ docker pull busybox@sha256:a4b903347f20af97e226ac6c5553192e6e0563286ca0dc467ce5a94c4a035aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 KB (8620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36435b18a0c8b949ad5fce71f28a40615a5331bd80583e1ffd0d09a9c3b9e684`

```dockerfile
```

-	Layers:
	-	`sha256:2d0c8c4ab41c1ccc8b6646d553eb938c137550644dd90942b5bcc77bcd65a72b`  
		Last Modified: Thu, 18 Jan 2024 23:07:04 GMT  
		Size: 3.0 KB (3008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:226dff263f3c0631e353a897768994cd9ebc5e40aaf34f2adcf22a6a0f8f6482`  
		Last Modified: Thu, 18 Jan 2024 23:07:04 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35` - linux; s390x

```console
$ docker pull busybox@sha256:09940308e5ef4ce1f6b5d387a8cbb44d1804f070abfe81bf55a3af042b8910c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1922049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef688f9f4132329a7ff47e9c1cc1f05cfb1f36837810f4f63c81d2be575224b1`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:adc2171e0b3598572ea7d01d4357650afd9ae4738448d7a0e0026f1515534596`  
		Last Modified: Sat, 20 Jan 2024 18:14:07 GMT  
		Size: 1.9 MB (1922049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35` - unknown; unknown

```console
$ docker pull busybox@sha256:8f7a48f61b52419691fdfdceffde48a9a7c5ed5c2a633d84732ba5cb2a84ad6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 KB (8551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7169f6898aed40beabfc0aeaf537dbd02ad6a808f7673edcf3a3b3fa16c04fc6`

```dockerfile
```

-	Layers:
	-	`sha256:0a442a3071463dbde8edaf572fd34cb061e3d8e1d7fda870f8aca02db0a426c6`  
		Last Modified: Sat, 20 Jan 2024 18:14:07 GMT  
		Size: 3.0 KB (2976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67458a838c7895e03f3f415cfb1c6cd11667c947945a823b0af1fd33d6af7dd6`  
		Last Modified: Sat, 20 Jan 2024 18:14:07 GMT  
		Size: 5.6 KB (5575 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:1.35-glibc`

```console
$ docker pull busybox@sha256:ba3d9c56716804e60357233fed1f5df28da28e3804253d27652c173d0429373a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `busybox:1.35-glibc` - linux; amd64

```console
$ docker pull busybox@sha256:462231a4068d238616e330a49aa4c0896a61c4003adde5cbe6879caa7f1992de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c00acac9c2794adfa8bb7b13ef38504300b505a043bf68dff7a00068dcc732b`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2354422721e449fa3fa83b84465b9d5bb65ac5415ec93c06f598854312e8957e`  
		Last Modified: Thu, 18 Jan 2024 23:03:25 GMT  
		Size: 2.2 MB (2212939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:ce63139305fd383ca8e320211f874a624b8b4a2e05307b9c18f37f69d0d98913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 KB (8551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ce1c047b16326ce720cd6e2d12a9189050c9306cb350864a132f836b56280c`

```dockerfile
```

-	Layers:
	-	`sha256:25c6d85b554105b1eb62bf541d8ba40745768e287fe13dd71a9fc2fe9680197d`  
		Last Modified: Thu, 18 Jan 2024 23:03:25 GMT  
		Size: 3.0 KB (2976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81c7c2a7711e2add234a2694186a75c0c1ceb5c852a72c96af466f4f24e41c69`  
		Last Modified: Thu, 18 Jan 2024 23:03:25 GMT  
		Size: 5.6 KB (5575 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35-glibc` - linux; arm variant v5

```console
$ docker pull busybox@sha256:3cb1d74becebf3031646d8d4822728973482e2e56b73a6669243a52aaf1544ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1772716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f419b164f0f391706417345127f8bbf8d7b747e24283b6a5ee48a348d5c157a`
-	Default Command: `["sh"]`

```dockerfile
# Sun, 26 Dec 2021 16:56:57 GMT
RUN BusyBox 1.35.0 (glibc), Debian 12
```

-	Layers:
	-	`sha256:b59bb812a84f8d3e6554de2334ce709ce2ddd45b2122f4243d195d8311296290`  
		Last Modified: Wed, 06 Mar 2024 00:08:14 GMT  
		Size: 1.8 MB (1772716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35-glibc` - linux; arm variant v7

```console
$ docker pull busybox@sha256:9ad13fde87c1a28d0f81f25851b9bbf442691310607311ec8c563e2103536e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1550275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d335b8de554e790e78e0b1a84e0b148c3ac7ada67f91b0c22b34b3c3dd946b8e`
-	Default Command: `["sh"]`

```dockerfile
# Sun, 26 Dec 2021 16:56:57 GMT
RUN BusyBox 1.35.0 (glibc), Debian 12
```

-	Layers:
	-	`sha256:bbcae909f65630db46bda0bbbbdca543c71fec5233df65620405f8e11b831d9f`  
		Last Modified: Wed, 06 Mar 2024 00:10:56 GMT  
		Size: 1.6 MB (1550275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35-glibc` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:05d019b284f629eddedf2d63b6a62c084bcadc1d7b1deaabdc76c66b609f6c9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1913311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcedb5826f9d4e187e358214a4a1d503c33448d15b57eacc882aa8da640b19c`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:37dfde395fb0e71c422335995f1b44064442171f53b0979f11f6bf919fbdda28`  
		Last Modified: Fri, 19 Jan 2024 01:52:11 GMT  
		Size: 1.9 MB (1913311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:c0c7478f2d9213e1550dcd040149b1cecb49b771a73ab320568fc79c47f403ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 KB (8571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5ed5d452b1f21eb43710dbeda0fbf5d6570d6856fb028961604f050f45a22a`

```dockerfile
```

-	Layers:
	-	`sha256:5595c6eb9287ff73c8d8e69d0e880190d4fe189a94f52a032784aafcec3aa238`  
		Last Modified: Fri, 19 Jan 2024 01:52:11 GMT  
		Size: 3.0 KB (2986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a430708e41abcad94463dce7ba8976703febec19dae1e6ae1918639864896b0c`  
		Last Modified: Fri, 19 Jan 2024 01:52:11 GMT  
		Size: 5.6 KB (5585 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35-glibc` - linux; 386

```console
$ docker pull busybox@sha256:acb951a45cc2407d4a7bc8af187d477254694faf7590b9396fdda5fd04c90c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2264085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72caec8a3c0377d18f5f695b63ead89d34e3768907d63c7060bbba98d000993`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:18964fea37a7ba3237684b9f0850daecc248d4422709cdc7f495301c3f2025f4`  
		Last Modified: Thu, 18 Jan 2024 23:03:32 GMT  
		Size: 2.3 MB (2264085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:022caa5a29959876efc12343dbd422bffdf80b800c5c47b7a84ed71881eea784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 KB (8505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ad2f8aea767ef2e9d2b36fb3c8b0b69913679e4cef86d70109bad47e06b7b6`

```dockerfile
```

-	Layers:
	-	`sha256:a17e8c3966826c87cdb35d0a9249aa1ae7e7d867e28fe07bdec612fb21334a6b`  
		Last Modified: Thu, 18 Jan 2024 23:03:32 GMT  
		Size: 3.0 KB (2953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40844810caa868ad53fa21b45e474a7f3e3f71d1702ff917265abbcdc22d69ca`  
		Last Modified: Thu, 18 Jan 2024 23:03:32 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35-glibc` - linux; mips64le

```console
$ docker pull busybox@sha256:4f42e99c852996a8f560b737046a8501fb714664914b9aab6c08796739497195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2072932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0905a181f6a06656547a117e6ddf579ddc6706a18ec7334c91af5d737b9b6c3a`
-	Default Command: `["sh"]`

```dockerfile
# Sun, 26 Dec 2021 16:56:57 GMT
RUN BusyBox 1.35.0 (glibc), Debian 12
```

-	Layers:
	-	`sha256:bde827b12c95d1ece79ad25f0839a526e44b3fe4e8148f21957b007c3b8e5488`  
		Last Modified: Wed, 06 Mar 2024 00:09:28 GMT  
		Size: 2.1 MB (2072932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35-glibc` - linux; ppc64le

```console
$ docker pull busybox@sha256:d2b10a11ed4117229cb399588b887956ff05a9541577a825c3ef12390a29a00e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2523465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64849f6b691d998aef552e64ed2aa7d2428421b3cbffaf6530bc0cfe78231aa7`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:de183f91e330998a45a7ce3945ce6cb95565b808920d4f702326d757519d7a0d`  
		Last Modified: Fri, 19 Jan 2024 01:38:22 GMT  
		Size: 2.5 MB (2523465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:869d38b81c849a53e15d3bcce944e075cc69be0be325d5978187bae28778df09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 KB (8611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac98edb286e659de67f172339c6d2609921c484ead187c9a9b47b2382e6272a`

```dockerfile
```

-	Layers:
	-	`sha256:a9bba9b2a154c8acc57919e4ae0fca4a9c4f8ef796580ce577e66f0c6d30697f`  
		Last Modified: Fri, 19 Jan 2024 01:38:22 GMT  
		Size: 3.0 KB (3004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b743576ba60eaebb52475f473cf8e9c8250aaf3ad0e1467e6f6e9c4de23943`  
		Last Modified: Fri, 19 Jan 2024 01:38:22 GMT  
		Size: 5.6 KB (5607 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35-glibc` - linux; s390x

```console
$ docker pull busybox@sha256:09940308e5ef4ce1f6b5d387a8cbb44d1804f070abfe81bf55a3af042b8910c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1922049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef688f9f4132329a7ff47e9c1cc1f05cfb1f36837810f4f63c81d2be575224b1`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:adc2171e0b3598572ea7d01d4357650afd9ae4738448d7a0e0026f1515534596`  
		Last Modified: Sat, 20 Jan 2024 18:14:07 GMT  
		Size: 1.9 MB (1922049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:8f7a48f61b52419691fdfdceffde48a9a7c5ed5c2a633d84732ba5cb2a84ad6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 KB (8551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7169f6898aed40beabfc0aeaf537dbd02ad6a808f7673edcf3a3b3fa16c04fc6`

```dockerfile
```

-	Layers:
	-	`sha256:0a442a3071463dbde8edaf572fd34cb061e3d8e1d7fda870f8aca02db0a426c6`  
		Last Modified: Sat, 20 Jan 2024 18:14:07 GMT  
		Size: 3.0 KB (2976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67458a838c7895e03f3f415cfb1c6cd11667c947945a823b0af1fd33d6af7dd6`  
		Last Modified: Sat, 20 Jan 2024 18:14:07 GMT  
		Size: 5.6 KB (5575 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:1.35-musl`

```console
$ docker pull busybox@sha256:e9058ccf9dd60cb6f036f180d9a80305cf51bd9ab6b599fedd382b36d6026da4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `busybox:1.35-musl` - linux; amd64

```console
$ docker pull busybox@sha256:7fdca99f8229ad55e0a648308d50bd57f702b101f2376464c42d61987d20cffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.1 KB (875117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e491ab50c8a13432fd590754deddbe140eeef8e168236cbd059d40316be5d0d`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7f1728eb6f84b32300bdb38048b4382c6345a43b0ff86015bcad473c716b71e7`  
		Last Modified: Thu, 18 Jan 2024 23:03:29 GMT  
		Size: 875.1 KB (875117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:d6fe6e87c9b601a2e371b4ddbcba9c37156ee863e9723067b122ad1af105cd4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 KB (7347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe88d4b1313eef327248160f2b38c3d0696063587c30a247f915c2a78199439`

```dockerfile
```

-	Layers:
	-	`sha256:9ba329d343ecfa06ec1f9208af38a0c95f6b2bc103a70c6e2114c806fd0a03fc`  
		Last Modified: Thu, 18 Jan 2024 23:03:29 GMT  
		Size: 2.4 KB (2376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60ea2dc67ba2a041c8abc3dbab5c710f74decbee703454db58f9ebd841e8e1d3`  
		Last Modified: Thu, 18 Jan 2024 23:03:29 GMT  
		Size: 5.0 KB (4971 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35-musl` - linux; arm variant v6

```console
$ docker pull busybox@sha256:c7f19b2a99f29f55049763f30c63c47c9bdca74f1eb58129c90cb200565cbafd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.2 KB (982203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eeabca632d8676e6d6c1acf9811e4bccda69f8182c70709058b96af9e30c520`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:eb75023da78324fbaccf28f5cfe7d06a00358e27f865593f058b0c72c1c47131`  
		Last Modified: Fri, 19 Jan 2024 00:06:15 GMT  
		Size: 982.2 KB (982203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:d89dc84838ba45e53a43defc1f4b6c61fe74afeb9ef4200e12427dd1767e0c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 KB (5392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50180279f5b44900fd416af7735026eba4b77c710780d7c9e30c5ec845699577`

```dockerfile
```

-	Layers:
	-	`sha256:9606dc24cdf8f1271dcc65fa1f9a3b1484d93e64d07de2986fc9b512532257e8`  
		Last Modified: Fri, 19 Jan 2024 00:06:14 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35-musl` - linux; arm variant v7

```console
$ docker pull busybox@sha256:b3b36963e5429889ca5dce40d4a861fc29a82367e9ba15b5f59e8f8bb99e6520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.4 KB (840429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcb8e8a21628e66f548247868e3165ab6a60464c4ff9b4a0e29b04af369aec4`
-	Default Command: `["sh"]`

```dockerfile
# Sun, 26 Dec 2021 16:56:57 GMT
RUN BusyBox 1.35.0 (musl), Alpine 3.19.1
```

-	Layers:
	-	`sha256:029b6487ed7f95712a2317b02fd31472ed9d382733b25df1c71c777208b5057b`  
		Last Modified: Wed, 06 Mar 2024 00:11:25 GMT  
		Size: 840.4 KB (840429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35-musl` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:b64cf69654e04e01c19e3886a2ef189f6eaffe92fab50852f1fc208fd50ad694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **916.7 KB (916712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a0a9c5d45e7d3c6221ee1a243aeceb3343ce8f85726528cb00334d88f1d0cb`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:21d07345bea875bf0be1c1b74ddee035dde4f480d8fc75095a52b6211b01d5a7`  
		Last Modified: Fri, 19 Jan 2024 02:41:06 GMT  
		Size: 916.7 KB (916712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:797346742db20df832edc1b731e1052b75c2f11fc244fe9d37a7dbe5af4a2fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 KB (7359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be58d86e7b4a2687802aa503a66b0766b8b554c6410dfe00de04324e06fde2af`

```dockerfile
```

-	Layers:
	-	`sha256:832407fdb33401d33901161bf6f9f1b18696a3b053502d6bee6a0dfdbffad732`  
		Last Modified: Fri, 19 Jan 2024 02:41:06 GMT  
		Size: 2.4 KB (2382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e162294a58a5703b4243d9dae5184390c0d742553bae041014108711cc1e237e`  
		Last Modified: Fri, 19 Jan 2024 02:41:06 GMT  
		Size: 5.0 KB (4977 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35-musl` - linux; 386

```console
$ docker pull busybox@sha256:9cc63fc991901dd3b16eb689b51589899afb47239e27172f5af96804730eff76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **870.8 KB (870838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b19ff4d06c974c384a4a0d1e734436fc9c23ac7070c1dd4a15899824868476a`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:b3a8068e19de6b6a1cdcf1c86727a2943522e32ba84f7ad5bf70375aaa5e271e`  
		Last Modified: Thu, 18 Jan 2024 23:03:29 GMT  
		Size: 870.8 KB (870838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:788f41ab09b68d5990162c843cb0a0b56987914473ca9bfe4e19cffa18ab7ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 KB (7321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2804ba03e92c5bf796ba12073f89cf19f74b1d347e6f261729a19977b207f40e`

```dockerfile
```

-	Layers:
	-	`sha256:fe10b08719796b49403b967fa5bf96efb123deff08307efe13ca26dde7d94c96`  
		Last Modified: Thu, 18 Jan 2024 23:03:28 GMT  
		Size: 2.4 KB (2363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8461c6c04734fa524664be72c646359dd883a587e0dd8c6de63337f2e5ea2c43`  
		Last Modified: Thu, 18 Jan 2024 23:03:29 GMT  
		Size: 5.0 KB (4958 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35-musl` - linux; ppc64le

```console
$ docker pull busybox@sha256:5f542805890190cfde0a3ca951b6d91742aa985029f9aa6c3da31b0505f1f8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **962.4 KB (962431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19a44cfb0217719948f2a746c334963c3307afb8099dd1a345b09f21de52ec8`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:51673f3dc3d728d27086c5e9fdbb36b13522ff7386083a957880b1e827361124`  
		Last Modified: Fri, 19 Jan 2024 01:39:39 GMT  
		Size: 962.4 KB (962431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:45e2246eb4bef0b69b69f89d48a76afc2285dacb02394beca8b4c80805378e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 KB (7383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af9bd8c6fb28d03eb4c20f6dbad203b085106a4462d14e3e0f45d2518c6f79b`

```dockerfile
```

-	Layers:
	-	`sha256:636e89bc10d1ae01c93df2e01943123d3344a0de34deac2e0eb196fa73a76aca`  
		Last Modified: Fri, 19 Jan 2024 01:39:39 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8b3a1baba5ba53d1bf50717954c9e488072dfb0d6f8d02e0062c927d8d9e748`  
		Last Modified: Fri, 19 Jan 2024 01:39:39 GMT  
		Size: 5.0 KB (4991 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35-musl` - linux; s390x

```console
$ docker pull busybox@sha256:3db0ce1ab0adcc77156eed3e90af31afdf2e1c92cc364a78d6b2cc94208bae7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **935.6 KB (935603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc46a864d450d1fc19132dfd7a6f95c31121ac8e769c4bcbb38cb6f95e12ff8f`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:84ca1d5a2d4d3fa6b50b5a299c612c49fbdd10f943b4da57fd050990059cd2f4`  
		Last Modified: Sat, 20 Jan 2024 18:16:44 GMT  
		Size: 935.6 KB (935603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:c3490fb2b6c2de4d9deb64b0acddf5678231e7dd840aa2d1677588581d831f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 KB (7347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efca67582df92ac6fc8411dbf3368b5e89d2756a2933e4a0042133965ab26324`

```dockerfile
```

-	Layers:
	-	`sha256:92d34425a64bb0c15a14200e7f6bc0354f89c3da9f05b3a5b4715c6ec557389f`  
		Last Modified: Sat, 20 Jan 2024 18:16:44 GMT  
		Size: 2.4 KB (2376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55f022a45f40f554098e298f83f75c4b152b4596cb03278d7bef4a078c0387d3`  
		Last Modified: Sat, 20 Jan 2024 18:16:44 GMT  
		Size: 5.0 KB (4971 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:1.35-uclibc`

```console
$ docker pull busybox@sha256:f8c1d34481f6f0984c4c4acd3a35465bbb05d32772019802b146045af1c678fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; riscv64
	-	unknown; unknown

### `busybox:1.35-uclibc` - linux; amd64

```console
$ docker pull busybox@sha256:acbb3f26329f0a965e70bb008bbee0e343f1696539661c86567dec773cb1cf78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **778.0 KB (778023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a718d91a1fd2bc0258ad5bebd7fb76b6f3e48a75522e46765ecd57ebfcd86d1a`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c71ea4fbb52b203d1a1656e4360a35b09d0a8e726cbfeb2aeb455639b2bdc36f`  
		Last Modified: Thu, 18 Jan 2024 23:03:38 GMT  
		Size: 778.0 KB (778023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:d25fa1adc91178d832a246eb483f1e6af4432bb2667deb461bb9ce944d7c8bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 KB (7369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e80ebe025235b99a478b21e8904d146580f271c042162ca041160dc4752359e`

```dockerfile
```

-	Layers:
	-	`sha256:d1ae6abc4db8f6f3bf4f2d7b7c72e4d51467ff1074b74f857bb43b99c73264a6`  
		Last Modified: Thu, 18 Jan 2024 23:03:38 GMT  
		Size: 2.4 KB (2384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01ea378a620c1f27274d8c5a36723ef41a85b0271d203771c4c7a0bed28d16c2`  
		Last Modified: Thu, 18 Jan 2024 23:03:38 GMT  
		Size: 5.0 KB (4985 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35-uclibc` - linux; arm variant v5

```console
$ docker pull busybox@sha256:3bb1b0a88048e60fe19936f65786af4b21cabb00fbfe0ac7b382829bf5aeddc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **740.2 KB (740233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8334aa380a491218db8cf437a7ced14fb21d249c6bdefe7ed942313e4eafc1b6`
-	Default Command: `["sh"]`

```dockerfile
# Sun, 26 Dec 2021 16:56:57 GMT
RUN BusyBox 1.35.0 (uclibc), Buildroot 2023.11.1, Debian 12
```

-	Layers:
	-	`sha256:061baea95096df67af0fc29e9937847ed58ccc1d56acea395b67771e7f4986ae`  
		Last Modified: Wed, 06 Mar 2024 00:08:30 GMT  
		Size: 740.2 KB (740233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35-uclibc` - linux; arm variant v7

```console
$ docker pull busybox@sha256:22257afa60fc1528c2c6ad730e22ef2f6ba2cbcf71b48a9b0e90ec3f23fc20de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.7 KB (705698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7438374a62f6706adaa7ad9d221598dbb30cd4c2b075b3d121d386c0d00e06`
-	Default Command: `["sh"]`

```dockerfile
# Sun, 26 Dec 2021 16:56:57 GMT
RUN BusyBox 1.35.0 (uclibc), Buildroot 2023.11.1, Debian 12
```

-	Layers:
	-	`sha256:392ca4c865185a559f72a503e3ce6c18b19ef690b40f3b95aff438547165abf3`  
		Last Modified: Wed, 06 Mar 2024 00:11:10 GMT  
		Size: 705.7 KB (705698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35-uclibc` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:27d4ba64accf0014cb911a27a897bbc00fa5e2016bd8645ffc6574e6915f5867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **833.5 KB (833500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbdb38e89580db8f50fb544140206cd99df16e27ab126cd2fde506ce23e72960`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fafc658f82bac17e0166814952a32fc7d5cc966e74021f5b0a80ed22a2dcadc0`  
		Last Modified: Fri, 19 Jan 2024 02:28:37 GMT  
		Size: 833.5 KB (833500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:964f27751362808974dc8e093bbdafe4abf2abc052f96f28e341371de54ba586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 KB (7381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7978fb78b8bb38ad16e4ee3af13b3ff1a0cd8315f5d071d1b34ce2e1e6eac7a`

```dockerfile
```

-	Layers:
	-	`sha256:7956df5b59b8ecf364039b2f31cd8402b67fe73aa6766cc8b03302b74b093102`  
		Last Modified: Fri, 19 Jan 2024 02:28:37 GMT  
		Size: 2.4 KB (2390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3ba3ac29866c0bc27810969f16a1de3711a8f9708bd07222f7d0081d0ebd510`  
		Last Modified: Fri, 19 Jan 2024 02:28:37 GMT  
		Size: 5.0 KB (4991 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35-uclibc` - linux; 386

```console
$ docker pull busybox@sha256:1481cfb16dab22e60956f77bd115496225f33a105456cd1343cf0ac3efda8d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.2 KB (742193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8662e56a995d2ed22d171b46a9f53ac72b5d437e7ccb5a719e0079f59955a7`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8e125412f16939f8b61ee9ae53850beca915b7ac4c17f513250c115c5ae15fc8`  
		Last Modified: Thu, 18 Jan 2024 23:03:37 GMT  
		Size: 742.2 KB (742193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:2fb625106c3daec0c3f1022e9abb5510f3baa6cb2482b7c8e5785ce670cc4dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 KB (7343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d181eca6ed16c05b75fc1661e73b940a23536061c37a36566702d653d330cf3`

```dockerfile
```

-	Layers:
	-	`sha256:7bfd870d605cdd3cf51a69a0cca7ec591f1ac0bf3d21970588d688437b75ac6a`  
		Last Modified: Thu, 18 Jan 2024 23:03:37 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d21bd876b22da57b0a668775b7d1a85f6b5de13c883f72a0e62c255388233af1`  
		Last Modified: Thu, 18 Jan 2024 23:03:37 GMT  
		Size: 5.0 KB (4972 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35-uclibc` - linux; mips64le

```console
$ docker pull busybox@sha256:2c8059e4a59bdbca443286b089d5e12e4933de22278bf25095ed8610892bb863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.2 KB (944244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b3dd53233406d5fe45807a5a057343e53001147aa5ab2669c4400cee324242`
-	Default Command: `["sh"]`

```dockerfile
# Sun, 26 Dec 2021 16:56:57 GMT
RUN BusyBox 1.35.0 (uclibc), Buildroot 2023.11.1, Debian 12
```

-	Layers:
	-	`sha256:6bec3ab929b6ce9fd0f9128cfae9a2190c7e094102488b7f34cfffa80e2e44cc`  
		Last Modified: Wed, 06 Mar 2024 00:09:53 GMT  
		Size: 944.2 KB (944244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35-uclibc` - linux; riscv64

```console
$ docker pull busybox@sha256:9acc76dacdcf324e5349d8bb516f93a6bd51c3dd056b1e54f84ed232d7218663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **911.2 KB (911232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adeffaa38ccdb1bbf3208a6a7cda3c5e4befe92ff57391761f07be40f5aac113`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:429ffc68429126516047bcf0f37ad1d12806c4e3f8cf5892c65772562d564ee8`  
		Last Modified: Thu, 18 Jan 2024 23:07:04 GMT  
		Size: 911.2 KB (911232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:a4b903347f20af97e226ac6c5553192e6e0563286ca0dc467ce5a94c4a035aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 KB (8620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36435b18a0c8b949ad5fce71f28a40615a5331bd80583e1ffd0d09a9c3b9e684`

```dockerfile
```

-	Layers:
	-	`sha256:2d0c8c4ab41c1ccc8b6646d553eb938c137550644dd90942b5bcc77bcd65a72b`  
		Last Modified: Thu, 18 Jan 2024 23:07:04 GMT  
		Size: 3.0 KB (3008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:226dff263f3c0631e353a897768994cd9ebc5e40aaf34f2adcf22a6a0f8f6482`  
		Last Modified: Thu, 18 Jan 2024 23:07:04 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:1.35.0`

```console
$ docker pull busybox@sha256:4a598f8a53a7fa34917d24f9dad23b614810c7b528a84559fd5caee7f3c1e17d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 17
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `busybox:1.35.0` - linux; amd64

```console
$ docker pull busybox@sha256:462231a4068d238616e330a49aa4c0896a61c4003adde5cbe6879caa7f1992de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c00acac9c2794adfa8bb7b13ef38504300b505a043bf68dff7a00068dcc732b`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2354422721e449fa3fa83b84465b9d5bb65ac5415ec93c06f598854312e8957e`  
		Last Modified: Thu, 18 Jan 2024 23:03:25 GMT  
		Size: 2.2 MB (2212939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0` - unknown; unknown

```console
$ docker pull busybox@sha256:ce63139305fd383ca8e320211f874a624b8b4a2e05307b9c18f37f69d0d98913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 KB (8551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ce1c047b16326ce720cd6e2d12a9189050c9306cb350864a132f836b56280c`

```dockerfile
```

-	Layers:
	-	`sha256:25c6d85b554105b1eb62bf541d8ba40745768e287fe13dd71a9fc2fe9680197d`  
		Last Modified: Thu, 18 Jan 2024 23:03:25 GMT  
		Size: 3.0 KB (2976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81c7c2a7711e2add234a2694186a75c0c1ceb5c852a72c96af466f4f24e41c69`  
		Last Modified: Thu, 18 Jan 2024 23:03:25 GMT  
		Size: 5.6 KB (5575 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35.0` - linux; arm variant v5

```console
$ docker pull busybox@sha256:3cb1d74becebf3031646d8d4822728973482e2e56b73a6669243a52aaf1544ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1772716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f419b164f0f391706417345127f8bbf8d7b747e24283b6a5ee48a348d5c157a`
-	Default Command: `["sh"]`

```dockerfile
# Sun, 26 Dec 2021 16:56:57 GMT
RUN BusyBox 1.35.0 (glibc), Debian 12
```

-	Layers:
	-	`sha256:b59bb812a84f8d3e6554de2334ce709ce2ddd45b2122f4243d195d8311296290`  
		Last Modified: Wed, 06 Mar 2024 00:08:14 GMT  
		Size: 1.8 MB (1772716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0` - linux; arm variant v6

```console
$ docker pull busybox@sha256:c7f19b2a99f29f55049763f30c63c47c9bdca74f1eb58129c90cb200565cbafd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.2 KB (982203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eeabca632d8676e6d6c1acf9811e4bccda69f8182c70709058b96af9e30c520`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:eb75023da78324fbaccf28f5cfe7d06a00358e27f865593f058b0c72c1c47131`  
		Last Modified: Fri, 19 Jan 2024 00:06:15 GMT  
		Size: 982.2 KB (982203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0` - unknown; unknown

```console
$ docker pull busybox@sha256:d89dc84838ba45e53a43defc1f4b6c61fe74afeb9ef4200e12427dd1767e0c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 KB (5392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50180279f5b44900fd416af7735026eba4b77c710780d7c9e30c5ec845699577`

```dockerfile
```

-	Layers:
	-	`sha256:9606dc24cdf8f1271dcc65fa1f9a3b1484d93e64d07de2986fc9b512532257e8`  
		Last Modified: Fri, 19 Jan 2024 00:06:14 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35.0` - linux; arm variant v7

```console
$ docker pull busybox@sha256:9ad13fde87c1a28d0f81f25851b9bbf442691310607311ec8c563e2103536e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1550275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d335b8de554e790e78e0b1a84e0b148c3ac7ada67f91b0c22b34b3c3dd946b8e`
-	Default Command: `["sh"]`

```dockerfile
# Sun, 26 Dec 2021 16:56:57 GMT
RUN BusyBox 1.35.0 (glibc), Debian 12
```

-	Layers:
	-	`sha256:bbcae909f65630db46bda0bbbbdca543c71fec5233df65620405f8e11b831d9f`  
		Last Modified: Wed, 06 Mar 2024 00:10:56 GMT  
		Size: 1.6 MB (1550275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:05d019b284f629eddedf2d63b6a62c084bcadc1d7b1deaabdc76c66b609f6c9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1913311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcedb5826f9d4e187e358214a4a1d503c33448d15b57eacc882aa8da640b19c`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:37dfde395fb0e71c422335995f1b44064442171f53b0979f11f6bf919fbdda28`  
		Last Modified: Fri, 19 Jan 2024 01:52:11 GMT  
		Size: 1.9 MB (1913311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0` - unknown; unknown

```console
$ docker pull busybox@sha256:c0c7478f2d9213e1550dcd040149b1cecb49b771a73ab320568fc79c47f403ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 KB (8571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5ed5d452b1f21eb43710dbeda0fbf5d6570d6856fb028961604f050f45a22a`

```dockerfile
```

-	Layers:
	-	`sha256:5595c6eb9287ff73c8d8e69d0e880190d4fe189a94f52a032784aafcec3aa238`  
		Last Modified: Fri, 19 Jan 2024 01:52:11 GMT  
		Size: 3.0 KB (2986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a430708e41abcad94463dce7ba8976703febec19dae1e6ae1918639864896b0c`  
		Last Modified: Fri, 19 Jan 2024 01:52:11 GMT  
		Size: 5.6 KB (5585 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35.0` - linux; 386

```console
$ docker pull busybox@sha256:acb951a45cc2407d4a7bc8af187d477254694faf7590b9396fdda5fd04c90c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2264085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72caec8a3c0377d18f5f695b63ead89d34e3768907d63c7060bbba98d000993`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:18964fea37a7ba3237684b9f0850daecc248d4422709cdc7f495301c3f2025f4`  
		Last Modified: Thu, 18 Jan 2024 23:03:32 GMT  
		Size: 2.3 MB (2264085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0` - unknown; unknown

```console
$ docker pull busybox@sha256:022caa5a29959876efc12343dbd422bffdf80b800c5c47b7a84ed71881eea784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 KB (8505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ad2f8aea767ef2e9d2b36fb3c8b0b69913679e4cef86d70109bad47e06b7b6`

```dockerfile
```

-	Layers:
	-	`sha256:a17e8c3966826c87cdb35d0a9249aa1ae7e7d867e28fe07bdec612fb21334a6b`  
		Last Modified: Thu, 18 Jan 2024 23:03:32 GMT  
		Size: 3.0 KB (2953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40844810caa868ad53fa21b45e474a7f3e3f71d1702ff917265abbcdc22d69ca`  
		Last Modified: Thu, 18 Jan 2024 23:03:32 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35.0` - linux; mips64le

```console
$ docker pull busybox@sha256:4f42e99c852996a8f560b737046a8501fb714664914b9aab6c08796739497195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2072932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0905a181f6a06656547a117e6ddf579ddc6706a18ec7334c91af5d737b9b6c3a`
-	Default Command: `["sh"]`

```dockerfile
# Sun, 26 Dec 2021 16:56:57 GMT
RUN BusyBox 1.35.0 (glibc), Debian 12
```

-	Layers:
	-	`sha256:bde827b12c95d1ece79ad25f0839a526e44b3fe4e8148f21957b007c3b8e5488`  
		Last Modified: Wed, 06 Mar 2024 00:09:28 GMT  
		Size: 2.1 MB (2072932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0` - linux; ppc64le

```console
$ docker pull busybox@sha256:d2b10a11ed4117229cb399588b887956ff05a9541577a825c3ef12390a29a00e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2523465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64849f6b691d998aef552e64ed2aa7d2428421b3cbffaf6530bc0cfe78231aa7`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:de183f91e330998a45a7ce3945ce6cb95565b808920d4f702326d757519d7a0d`  
		Last Modified: Fri, 19 Jan 2024 01:38:22 GMT  
		Size: 2.5 MB (2523465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0` - unknown; unknown

```console
$ docker pull busybox@sha256:869d38b81c849a53e15d3bcce944e075cc69be0be325d5978187bae28778df09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 KB (8611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac98edb286e659de67f172339c6d2609921c484ead187c9a9b47b2382e6272a`

```dockerfile
```

-	Layers:
	-	`sha256:a9bba9b2a154c8acc57919e4ae0fca4a9c4f8ef796580ce577e66f0c6d30697f`  
		Last Modified: Fri, 19 Jan 2024 01:38:22 GMT  
		Size: 3.0 KB (3004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b743576ba60eaebb52475f473cf8e9c8250aaf3ad0e1467e6f6e9c4de23943`  
		Last Modified: Fri, 19 Jan 2024 01:38:22 GMT  
		Size: 5.6 KB (5607 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35.0` - linux; riscv64

```console
$ docker pull busybox@sha256:9acc76dacdcf324e5349d8bb516f93a6bd51c3dd056b1e54f84ed232d7218663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **911.2 KB (911232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adeffaa38ccdb1bbf3208a6a7cda3c5e4befe92ff57391761f07be40f5aac113`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:429ffc68429126516047bcf0f37ad1d12806c4e3f8cf5892c65772562d564ee8`  
		Last Modified: Thu, 18 Jan 2024 23:07:04 GMT  
		Size: 911.2 KB (911232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0` - unknown; unknown

```console
$ docker pull busybox@sha256:a4b903347f20af97e226ac6c5553192e6e0563286ca0dc467ce5a94c4a035aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 KB (8620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36435b18a0c8b949ad5fce71f28a40615a5331bd80583e1ffd0d09a9c3b9e684`

```dockerfile
```

-	Layers:
	-	`sha256:2d0c8c4ab41c1ccc8b6646d553eb938c137550644dd90942b5bcc77bcd65a72b`  
		Last Modified: Thu, 18 Jan 2024 23:07:04 GMT  
		Size: 3.0 KB (3008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:226dff263f3c0631e353a897768994cd9ebc5e40aaf34f2adcf22a6a0f8f6482`  
		Last Modified: Thu, 18 Jan 2024 23:07:04 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35.0` - linux; s390x

```console
$ docker pull busybox@sha256:09940308e5ef4ce1f6b5d387a8cbb44d1804f070abfe81bf55a3af042b8910c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1922049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef688f9f4132329a7ff47e9c1cc1f05cfb1f36837810f4f63c81d2be575224b1`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:adc2171e0b3598572ea7d01d4357650afd9ae4738448d7a0e0026f1515534596`  
		Last Modified: Sat, 20 Jan 2024 18:14:07 GMT  
		Size: 1.9 MB (1922049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0` - unknown; unknown

```console
$ docker pull busybox@sha256:8f7a48f61b52419691fdfdceffde48a9a7c5ed5c2a633d84732ba5cb2a84ad6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 KB (8551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7169f6898aed40beabfc0aeaf537dbd02ad6a808f7673edcf3a3b3fa16c04fc6`

```dockerfile
```

-	Layers:
	-	`sha256:0a442a3071463dbde8edaf572fd34cb061e3d8e1d7fda870f8aca02db0a426c6`  
		Last Modified: Sat, 20 Jan 2024 18:14:07 GMT  
		Size: 3.0 KB (2976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67458a838c7895e03f3f415cfb1c6cd11667c947945a823b0af1fd33d6af7dd6`  
		Last Modified: Sat, 20 Jan 2024 18:14:07 GMT  
		Size: 5.6 KB (5575 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:1.35.0-glibc`

```console
$ docker pull busybox@sha256:ba3d9c56716804e60357233fed1f5df28da28e3804253d27652c173d0429373a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `busybox:1.35.0-glibc` - linux; amd64

```console
$ docker pull busybox@sha256:462231a4068d238616e330a49aa4c0896a61c4003adde5cbe6879caa7f1992de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c00acac9c2794adfa8bb7b13ef38504300b505a043bf68dff7a00068dcc732b`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2354422721e449fa3fa83b84465b9d5bb65ac5415ec93c06f598854312e8957e`  
		Last Modified: Thu, 18 Jan 2024 23:03:25 GMT  
		Size: 2.2 MB (2212939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:ce63139305fd383ca8e320211f874a624b8b4a2e05307b9c18f37f69d0d98913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 KB (8551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ce1c047b16326ce720cd6e2d12a9189050c9306cb350864a132f836b56280c`

```dockerfile
```

-	Layers:
	-	`sha256:25c6d85b554105b1eb62bf541d8ba40745768e287fe13dd71a9fc2fe9680197d`  
		Last Modified: Thu, 18 Jan 2024 23:03:25 GMT  
		Size: 3.0 KB (2976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81c7c2a7711e2add234a2694186a75c0c1ceb5c852a72c96af466f4f24e41c69`  
		Last Modified: Thu, 18 Jan 2024 23:03:25 GMT  
		Size: 5.6 KB (5575 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35.0-glibc` - linux; arm variant v5

```console
$ docker pull busybox@sha256:3cb1d74becebf3031646d8d4822728973482e2e56b73a6669243a52aaf1544ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1772716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f419b164f0f391706417345127f8bbf8d7b747e24283b6a5ee48a348d5c157a`
-	Default Command: `["sh"]`

```dockerfile
# Sun, 26 Dec 2021 16:56:57 GMT
RUN BusyBox 1.35.0 (glibc), Debian 12
```

-	Layers:
	-	`sha256:b59bb812a84f8d3e6554de2334ce709ce2ddd45b2122f4243d195d8311296290`  
		Last Modified: Wed, 06 Mar 2024 00:08:14 GMT  
		Size: 1.8 MB (1772716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0-glibc` - linux; arm variant v7

```console
$ docker pull busybox@sha256:9ad13fde87c1a28d0f81f25851b9bbf442691310607311ec8c563e2103536e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1550275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d335b8de554e790e78e0b1a84e0b148c3ac7ada67f91b0c22b34b3c3dd946b8e`
-	Default Command: `["sh"]`

```dockerfile
# Sun, 26 Dec 2021 16:56:57 GMT
RUN BusyBox 1.35.0 (glibc), Debian 12
```

-	Layers:
	-	`sha256:bbcae909f65630db46bda0bbbbdca543c71fec5233df65620405f8e11b831d9f`  
		Last Modified: Wed, 06 Mar 2024 00:10:56 GMT  
		Size: 1.6 MB (1550275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0-glibc` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:05d019b284f629eddedf2d63b6a62c084bcadc1d7b1deaabdc76c66b609f6c9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1913311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcedb5826f9d4e187e358214a4a1d503c33448d15b57eacc882aa8da640b19c`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:37dfde395fb0e71c422335995f1b44064442171f53b0979f11f6bf919fbdda28`  
		Last Modified: Fri, 19 Jan 2024 01:52:11 GMT  
		Size: 1.9 MB (1913311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:c0c7478f2d9213e1550dcd040149b1cecb49b771a73ab320568fc79c47f403ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 KB (8571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5ed5d452b1f21eb43710dbeda0fbf5d6570d6856fb028961604f050f45a22a`

```dockerfile
```

-	Layers:
	-	`sha256:5595c6eb9287ff73c8d8e69d0e880190d4fe189a94f52a032784aafcec3aa238`  
		Last Modified: Fri, 19 Jan 2024 01:52:11 GMT  
		Size: 3.0 KB (2986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a430708e41abcad94463dce7ba8976703febec19dae1e6ae1918639864896b0c`  
		Last Modified: Fri, 19 Jan 2024 01:52:11 GMT  
		Size: 5.6 KB (5585 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35.0-glibc` - linux; 386

```console
$ docker pull busybox@sha256:acb951a45cc2407d4a7bc8af187d477254694faf7590b9396fdda5fd04c90c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2264085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72caec8a3c0377d18f5f695b63ead89d34e3768907d63c7060bbba98d000993`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:18964fea37a7ba3237684b9f0850daecc248d4422709cdc7f495301c3f2025f4`  
		Last Modified: Thu, 18 Jan 2024 23:03:32 GMT  
		Size: 2.3 MB (2264085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:022caa5a29959876efc12343dbd422bffdf80b800c5c47b7a84ed71881eea784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 KB (8505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ad2f8aea767ef2e9d2b36fb3c8b0b69913679e4cef86d70109bad47e06b7b6`

```dockerfile
```

-	Layers:
	-	`sha256:a17e8c3966826c87cdb35d0a9249aa1ae7e7d867e28fe07bdec612fb21334a6b`  
		Last Modified: Thu, 18 Jan 2024 23:03:32 GMT  
		Size: 3.0 KB (2953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40844810caa868ad53fa21b45e474a7f3e3f71d1702ff917265abbcdc22d69ca`  
		Last Modified: Thu, 18 Jan 2024 23:03:32 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35.0-glibc` - linux; mips64le

```console
$ docker pull busybox@sha256:4f42e99c852996a8f560b737046a8501fb714664914b9aab6c08796739497195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2072932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0905a181f6a06656547a117e6ddf579ddc6706a18ec7334c91af5d737b9b6c3a`
-	Default Command: `["sh"]`

```dockerfile
# Sun, 26 Dec 2021 16:56:57 GMT
RUN BusyBox 1.35.0 (glibc), Debian 12
```

-	Layers:
	-	`sha256:bde827b12c95d1ece79ad25f0839a526e44b3fe4e8148f21957b007c3b8e5488`  
		Last Modified: Wed, 06 Mar 2024 00:09:28 GMT  
		Size: 2.1 MB (2072932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0-glibc` - linux; ppc64le

```console
$ docker pull busybox@sha256:d2b10a11ed4117229cb399588b887956ff05a9541577a825c3ef12390a29a00e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2523465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64849f6b691d998aef552e64ed2aa7d2428421b3cbffaf6530bc0cfe78231aa7`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:de183f91e330998a45a7ce3945ce6cb95565b808920d4f702326d757519d7a0d`  
		Last Modified: Fri, 19 Jan 2024 01:38:22 GMT  
		Size: 2.5 MB (2523465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:869d38b81c849a53e15d3bcce944e075cc69be0be325d5978187bae28778df09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 KB (8611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac98edb286e659de67f172339c6d2609921c484ead187c9a9b47b2382e6272a`

```dockerfile
```

-	Layers:
	-	`sha256:a9bba9b2a154c8acc57919e4ae0fca4a9c4f8ef796580ce577e66f0c6d30697f`  
		Last Modified: Fri, 19 Jan 2024 01:38:22 GMT  
		Size: 3.0 KB (3004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b743576ba60eaebb52475f473cf8e9c8250aaf3ad0e1467e6f6e9c4de23943`  
		Last Modified: Fri, 19 Jan 2024 01:38:22 GMT  
		Size: 5.6 KB (5607 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35.0-glibc` - linux; s390x

```console
$ docker pull busybox@sha256:09940308e5ef4ce1f6b5d387a8cbb44d1804f070abfe81bf55a3af042b8910c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1922049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef688f9f4132329a7ff47e9c1cc1f05cfb1f36837810f4f63c81d2be575224b1`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:adc2171e0b3598572ea7d01d4357650afd9ae4738448d7a0e0026f1515534596`  
		Last Modified: Sat, 20 Jan 2024 18:14:07 GMT  
		Size: 1.9 MB (1922049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:8f7a48f61b52419691fdfdceffde48a9a7c5ed5c2a633d84732ba5cb2a84ad6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 KB (8551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7169f6898aed40beabfc0aeaf537dbd02ad6a808f7673edcf3a3b3fa16c04fc6`

```dockerfile
```

-	Layers:
	-	`sha256:0a442a3071463dbde8edaf572fd34cb061e3d8e1d7fda870f8aca02db0a426c6`  
		Last Modified: Sat, 20 Jan 2024 18:14:07 GMT  
		Size: 3.0 KB (2976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67458a838c7895e03f3f415cfb1c6cd11667c947945a823b0af1fd33d6af7dd6`  
		Last Modified: Sat, 20 Jan 2024 18:14:07 GMT  
		Size: 5.6 KB (5575 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:1.35.0-musl`

```console
$ docker pull busybox@sha256:e9058ccf9dd60cb6f036f180d9a80305cf51bd9ab6b599fedd382b36d6026da4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `busybox:1.35.0-musl` - linux; amd64

```console
$ docker pull busybox@sha256:7fdca99f8229ad55e0a648308d50bd57f702b101f2376464c42d61987d20cffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.1 KB (875117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e491ab50c8a13432fd590754deddbe140eeef8e168236cbd059d40316be5d0d`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7f1728eb6f84b32300bdb38048b4382c6345a43b0ff86015bcad473c716b71e7`  
		Last Modified: Thu, 18 Jan 2024 23:03:29 GMT  
		Size: 875.1 KB (875117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:d6fe6e87c9b601a2e371b4ddbcba9c37156ee863e9723067b122ad1af105cd4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 KB (7347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe88d4b1313eef327248160f2b38c3d0696063587c30a247f915c2a78199439`

```dockerfile
```

-	Layers:
	-	`sha256:9ba329d343ecfa06ec1f9208af38a0c95f6b2bc103a70c6e2114c806fd0a03fc`  
		Last Modified: Thu, 18 Jan 2024 23:03:29 GMT  
		Size: 2.4 KB (2376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60ea2dc67ba2a041c8abc3dbab5c710f74decbee703454db58f9ebd841e8e1d3`  
		Last Modified: Thu, 18 Jan 2024 23:03:29 GMT  
		Size: 5.0 KB (4971 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35.0-musl` - linux; arm variant v6

```console
$ docker pull busybox@sha256:c7f19b2a99f29f55049763f30c63c47c9bdca74f1eb58129c90cb200565cbafd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.2 KB (982203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eeabca632d8676e6d6c1acf9811e4bccda69f8182c70709058b96af9e30c520`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:eb75023da78324fbaccf28f5cfe7d06a00358e27f865593f058b0c72c1c47131`  
		Last Modified: Fri, 19 Jan 2024 00:06:15 GMT  
		Size: 982.2 KB (982203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:d89dc84838ba45e53a43defc1f4b6c61fe74afeb9ef4200e12427dd1767e0c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 KB (5392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50180279f5b44900fd416af7735026eba4b77c710780d7c9e30c5ec845699577`

```dockerfile
```

-	Layers:
	-	`sha256:9606dc24cdf8f1271dcc65fa1f9a3b1484d93e64d07de2986fc9b512532257e8`  
		Last Modified: Fri, 19 Jan 2024 00:06:14 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35.0-musl` - linux; arm variant v7

```console
$ docker pull busybox@sha256:b3b36963e5429889ca5dce40d4a861fc29a82367e9ba15b5f59e8f8bb99e6520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.4 KB (840429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcb8e8a21628e66f548247868e3165ab6a60464c4ff9b4a0e29b04af369aec4`
-	Default Command: `["sh"]`

```dockerfile
# Sun, 26 Dec 2021 16:56:57 GMT
RUN BusyBox 1.35.0 (musl), Alpine 3.19.1
```

-	Layers:
	-	`sha256:029b6487ed7f95712a2317b02fd31472ed9d382733b25df1c71c777208b5057b`  
		Last Modified: Wed, 06 Mar 2024 00:11:25 GMT  
		Size: 840.4 KB (840429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0-musl` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:b64cf69654e04e01c19e3886a2ef189f6eaffe92fab50852f1fc208fd50ad694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **916.7 KB (916712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a0a9c5d45e7d3c6221ee1a243aeceb3343ce8f85726528cb00334d88f1d0cb`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:21d07345bea875bf0be1c1b74ddee035dde4f480d8fc75095a52b6211b01d5a7`  
		Last Modified: Fri, 19 Jan 2024 02:41:06 GMT  
		Size: 916.7 KB (916712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:797346742db20df832edc1b731e1052b75c2f11fc244fe9d37a7dbe5af4a2fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 KB (7359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be58d86e7b4a2687802aa503a66b0766b8b554c6410dfe00de04324e06fde2af`

```dockerfile
```

-	Layers:
	-	`sha256:832407fdb33401d33901161bf6f9f1b18696a3b053502d6bee6a0dfdbffad732`  
		Last Modified: Fri, 19 Jan 2024 02:41:06 GMT  
		Size: 2.4 KB (2382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e162294a58a5703b4243d9dae5184390c0d742553bae041014108711cc1e237e`  
		Last Modified: Fri, 19 Jan 2024 02:41:06 GMT  
		Size: 5.0 KB (4977 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35.0-musl` - linux; 386

```console
$ docker pull busybox@sha256:9cc63fc991901dd3b16eb689b51589899afb47239e27172f5af96804730eff76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **870.8 KB (870838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b19ff4d06c974c384a4a0d1e734436fc9c23ac7070c1dd4a15899824868476a`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:b3a8068e19de6b6a1cdcf1c86727a2943522e32ba84f7ad5bf70375aaa5e271e`  
		Last Modified: Thu, 18 Jan 2024 23:03:29 GMT  
		Size: 870.8 KB (870838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:788f41ab09b68d5990162c843cb0a0b56987914473ca9bfe4e19cffa18ab7ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 KB (7321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2804ba03e92c5bf796ba12073f89cf19f74b1d347e6f261729a19977b207f40e`

```dockerfile
```

-	Layers:
	-	`sha256:fe10b08719796b49403b967fa5bf96efb123deff08307efe13ca26dde7d94c96`  
		Last Modified: Thu, 18 Jan 2024 23:03:28 GMT  
		Size: 2.4 KB (2363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8461c6c04734fa524664be72c646359dd883a587e0dd8c6de63337f2e5ea2c43`  
		Last Modified: Thu, 18 Jan 2024 23:03:29 GMT  
		Size: 5.0 KB (4958 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35.0-musl` - linux; ppc64le

```console
$ docker pull busybox@sha256:5f542805890190cfde0a3ca951b6d91742aa985029f9aa6c3da31b0505f1f8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **962.4 KB (962431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19a44cfb0217719948f2a746c334963c3307afb8099dd1a345b09f21de52ec8`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:51673f3dc3d728d27086c5e9fdbb36b13522ff7386083a957880b1e827361124`  
		Last Modified: Fri, 19 Jan 2024 01:39:39 GMT  
		Size: 962.4 KB (962431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:45e2246eb4bef0b69b69f89d48a76afc2285dacb02394beca8b4c80805378e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 KB (7383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af9bd8c6fb28d03eb4c20f6dbad203b085106a4462d14e3e0f45d2518c6f79b`

```dockerfile
```

-	Layers:
	-	`sha256:636e89bc10d1ae01c93df2e01943123d3344a0de34deac2e0eb196fa73a76aca`  
		Last Modified: Fri, 19 Jan 2024 01:39:39 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8b3a1baba5ba53d1bf50717954c9e488072dfb0d6f8d02e0062c927d8d9e748`  
		Last Modified: Fri, 19 Jan 2024 01:39:39 GMT  
		Size: 5.0 KB (4991 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35.0-musl` - linux; s390x

```console
$ docker pull busybox@sha256:3db0ce1ab0adcc77156eed3e90af31afdf2e1c92cc364a78d6b2cc94208bae7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **935.6 KB (935603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc46a864d450d1fc19132dfd7a6f95c31121ac8e769c4bcbb38cb6f95e12ff8f`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:84ca1d5a2d4d3fa6b50b5a299c612c49fbdd10f943b4da57fd050990059cd2f4`  
		Last Modified: Sat, 20 Jan 2024 18:16:44 GMT  
		Size: 935.6 KB (935603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:c3490fb2b6c2de4d9deb64b0acddf5678231e7dd840aa2d1677588581d831f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 KB (7347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efca67582df92ac6fc8411dbf3368b5e89d2756a2933e4a0042133965ab26324`

```dockerfile
```

-	Layers:
	-	`sha256:92d34425a64bb0c15a14200e7f6bc0354f89c3da9f05b3a5b4715c6ec557389f`  
		Last Modified: Sat, 20 Jan 2024 18:16:44 GMT  
		Size: 2.4 KB (2376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55f022a45f40f554098e298f83f75c4b152b4596cb03278d7bef4a078c0387d3`  
		Last Modified: Sat, 20 Jan 2024 18:16:44 GMT  
		Size: 5.0 KB (4971 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:1.35.0-uclibc`

```console
$ docker pull busybox@sha256:f8c1d34481f6f0984c4c4acd3a35465bbb05d32772019802b146045af1c678fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; riscv64
	-	unknown; unknown

### `busybox:1.35.0-uclibc` - linux; amd64

```console
$ docker pull busybox@sha256:acbb3f26329f0a965e70bb008bbee0e343f1696539661c86567dec773cb1cf78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **778.0 KB (778023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a718d91a1fd2bc0258ad5bebd7fb76b6f3e48a75522e46765ecd57ebfcd86d1a`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c71ea4fbb52b203d1a1656e4360a35b09d0a8e726cbfeb2aeb455639b2bdc36f`  
		Last Modified: Thu, 18 Jan 2024 23:03:38 GMT  
		Size: 778.0 KB (778023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:d25fa1adc91178d832a246eb483f1e6af4432bb2667deb461bb9ce944d7c8bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 KB (7369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e80ebe025235b99a478b21e8904d146580f271c042162ca041160dc4752359e`

```dockerfile
```

-	Layers:
	-	`sha256:d1ae6abc4db8f6f3bf4f2d7b7c72e4d51467ff1074b74f857bb43b99c73264a6`  
		Last Modified: Thu, 18 Jan 2024 23:03:38 GMT  
		Size: 2.4 KB (2384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01ea378a620c1f27274d8c5a36723ef41a85b0271d203771c4c7a0bed28d16c2`  
		Last Modified: Thu, 18 Jan 2024 23:03:38 GMT  
		Size: 5.0 KB (4985 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35.0-uclibc` - linux; arm variant v5

```console
$ docker pull busybox@sha256:3bb1b0a88048e60fe19936f65786af4b21cabb00fbfe0ac7b382829bf5aeddc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **740.2 KB (740233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8334aa380a491218db8cf437a7ced14fb21d249c6bdefe7ed942313e4eafc1b6`
-	Default Command: `["sh"]`

```dockerfile
# Sun, 26 Dec 2021 16:56:57 GMT
RUN BusyBox 1.35.0 (uclibc), Buildroot 2023.11.1, Debian 12
```

-	Layers:
	-	`sha256:061baea95096df67af0fc29e9937847ed58ccc1d56acea395b67771e7f4986ae`  
		Last Modified: Wed, 06 Mar 2024 00:08:30 GMT  
		Size: 740.2 KB (740233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0-uclibc` - linux; arm variant v7

```console
$ docker pull busybox@sha256:22257afa60fc1528c2c6ad730e22ef2f6ba2cbcf71b48a9b0e90ec3f23fc20de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.7 KB (705698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7438374a62f6706adaa7ad9d221598dbb30cd4c2b075b3d121d386c0d00e06`
-	Default Command: `["sh"]`

```dockerfile
# Sun, 26 Dec 2021 16:56:57 GMT
RUN BusyBox 1.35.0 (uclibc), Buildroot 2023.11.1, Debian 12
```

-	Layers:
	-	`sha256:392ca4c865185a559f72a503e3ce6c18b19ef690b40f3b95aff438547165abf3`  
		Last Modified: Wed, 06 Mar 2024 00:11:10 GMT  
		Size: 705.7 KB (705698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0-uclibc` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:27d4ba64accf0014cb911a27a897bbc00fa5e2016bd8645ffc6574e6915f5867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **833.5 KB (833500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbdb38e89580db8f50fb544140206cd99df16e27ab126cd2fde506ce23e72960`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fafc658f82bac17e0166814952a32fc7d5cc966e74021f5b0a80ed22a2dcadc0`  
		Last Modified: Fri, 19 Jan 2024 02:28:37 GMT  
		Size: 833.5 KB (833500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:964f27751362808974dc8e093bbdafe4abf2abc052f96f28e341371de54ba586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 KB (7381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7978fb78b8bb38ad16e4ee3af13b3ff1a0cd8315f5d071d1b34ce2e1e6eac7a`

```dockerfile
```

-	Layers:
	-	`sha256:7956df5b59b8ecf364039b2f31cd8402b67fe73aa6766cc8b03302b74b093102`  
		Last Modified: Fri, 19 Jan 2024 02:28:37 GMT  
		Size: 2.4 KB (2390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3ba3ac29866c0bc27810969f16a1de3711a8f9708bd07222f7d0081d0ebd510`  
		Last Modified: Fri, 19 Jan 2024 02:28:37 GMT  
		Size: 5.0 KB (4991 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35.0-uclibc` - linux; 386

```console
$ docker pull busybox@sha256:1481cfb16dab22e60956f77bd115496225f33a105456cd1343cf0ac3efda8d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.2 KB (742193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8662e56a995d2ed22d171b46a9f53ac72b5d437e7ccb5a719e0079f59955a7`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8e125412f16939f8b61ee9ae53850beca915b7ac4c17f513250c115c5ae15fc8`  
		Last Modified: Thu, 18 Jan 2024 23:03:37 GMT  
		Size: 742.2 KB (742193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:2fb625106c3daec0c3f1022e9abb5510f3baa6cb2482b7c8e5785ce670cc4dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 KB (7343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d181eca6ed16c05b75fc1661e73b940a23536061c37a36566702d653d330cf3`

```dockerfile
```

-	Layers:
	-	`sha256:7bfd870d605cdd3cf51a69a0cca7ec591f1ac0bf3d21970588d688437b75ac6a`  
		Last Modified: Thu, 18 Jan 2024 23:03:37 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d21bd876b22da57b0a668775b7d1a85f6b5de13c883f72a0e62c255388233af1`  
		Last Modified: Thu, 18 Jan 2024 23:03:37 GMT  
		Size: 5.0 KB (4972 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.35.0-uclibc` - linux; mips64le

```console
$ docker pull busybox@sha256:2c8059e4a59bdbca443286b089d5e12e4933de22278bf25095ed8610892bb863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.2 KB (944244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b3dd53233406d5fe45807a5a057343e53001147aa5ab2669c4400cee324242`
-	Default Command: `["sh"]`

```dockerfile
# Sun, 26 Dec 2021 16:56:57 GMT
RUN BusyBox 1.35.0 (uclibc), Buildroot 2023.11.1, Debian 12
```

-	Layers:
	-	`sha256:6bec3ab929b6ce9fd0f9128cfae9a2190c7e094102488b7f34cfffa80e2e44cc`  
		Last Modified: Wed, 06 Mar 2024 00:09:53 GMT  
		Size: 944.2 KB (944244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0-uclibc` - linux; riscv64

```console
$ docker pull busybox@sha256:9acc76dacdcf324e5349d8bb516f93a6bd51c3dd056b1e54f84ed232d7218663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **911.2 KB (911232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adeffaa38ccdb1bbf3208a6a7cda3c5e4befe92ff57391761f07be40f5aac113`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:429ffc68429126516047bcf0f37ad1d12806c4e3f8cf5892c65772562d564ee8`  
		Last Modified: Thu, 18 Jan 2024 23:07:04 GMT  
		Size: 911.2 KB (911232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.35.0-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:a4b903347f20af97e226ac6c5553192e6e0563286ca0dc467ce5a94c4a035aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 KB (8620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36435b18a0c8b949ad5fce71f28a40615a5331bd80583e1ffd0d09a9c3b9e684`

```dockerfile
```

-	Layers:
	-	`sha256:2d0c8c4ab41c1ccc8b6646d553eb938c137550644dd90942b5bcc77bcd65a72b`  
		Last Modified: Thu, 18 Jan 2024 23:07:04 GMT  
		Size: 3.0 KB (3008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:226dff263f3c0631e353a897768994cd9ebc5e40aaf34f2adcf22a6a0f8f6482`  
		Last Modified: Thu, 18 Jan 2024 23:07:04 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:1.36`

```console
$ docker pull busybox@sha256:acdc29f25f9c5d678b264007f6f0ea63f12756dcef1cdb043f3fd2a13ba735c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 17
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `busybox:1.36` - linux; amd64

```console
$ docker pull busybox@sha256:538721340ded10875f4710cad688c70e5d0ecb4dcd5e7d0c161f301f36f79414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2220094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f57d9401f8d42f986df300f0c69192fc41da28ccc8d797829467780db3dd741`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9ad63333ebc97e32b987ae66aa3cff81300e4c2e6d2f2395cef8a3ae18b249fe`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 2.2 MB (2220094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36` - unknown; unknown

```console
$ docker pull busybox@sha256:253eb45864243efd740aa87ba169151e4d165538b168d77284396469217ee5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 KB (12149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9095a17baa618e6b1b5b3da6493f78682688b3c18f07a524e30bd47a404d4cb`

```dockerfile
```

-	Layers:
	-	`sha256:e1104929ee0cb0e8ea3d2c3b4024ce9f852364d233aabe800ea7789df99cfc23`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 4.8 KB (4778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d186640ac3f58c681ac3bc3aa314992df65409336eccb7e94bd7c4b8174a2b`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 7.4 KB (7371 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36` - linux; arm variant v5

```console
$ docker pull busybox@sha256:491e28080f41a345b794a1528e23525f67f8693d8c541b9ef8f4990f6af501f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1776853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6578b94d614adfa46696754ab33bdd8b8b70ac8adea2fb6061d90e2b01f90e3`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:e209cc4af23c3ed4ac3e8cf58f8e9ea90d51fe28fcfca3ad91d91e74aabca274`  
		Last Modified: Wed, 06 Mar 2024 00:07:47 GMT  
		Size: 1.8 MB (1776853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36` - linux; arm variant v6

```console
$ docker pull busybox@sha256:b64a6a9cff5d2916ce4e5ab52254faa487ae93d9028c157c10d444aa3b5b7e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.6 KB (987570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5059e5cce9929da538b30d11caea9231836d6b937083115b4058ae4649341b74`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd544bbcb8b286d4a58e2b02357bb516d089d281fc87ae2b375921b8d2389923`  
		Last Modified: Thu, 18 Jan 2024 23:58:56 GMT  
		Size: 987.6 KB (987570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36` - unknown; unknown

```console
$ docker pull busybox@sha256:0c1556654c58755833235ba840bb04258b5cf8d3e1771be01a2c48e38c266c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e96145e5c30a04c819cb052df4fa049365de24673fc3afdc9d5305cc2999a8`

```dockerfile
```

-	Layers:
	-	`sha256:1bbd274efa1896b02a475d573d66e47cc60d67dfb2334eef4aefc1d23763fe11`  
		Last Modified: Thu, 18 Jan 2024 23:58:56 GMT  
		Size: 7.2 KB (7231 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36` - linux; arm variant v7

```console
$ docker pull busybox@sha256:8a4415fb43600953cbdac6ec03c2d96d900bb21f8d78964837dad7f73b9afcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1554425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9903cc888814e8feef24381cdb6d29d8598385dcb109a9908a4a98e1ab021532`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:a7cbd68a76a020b8b283c940bc267cd88a66013dcb160cad746344483dfc4b52`  
		Last Modified: Wed, 06 Mar 2024 00:10:11 GMT  
		Size: 1.6 MB (1554425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:8f03917912ea995c637b6c0295846aaff5665f06ac82a29b421fba4c379494e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1916607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4fd538a9a0b729be05707cf805388be2fb701cfd5d44c6542f1988e8aef6e3`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c2bf9493c1bf786e95e3eac7d406c20aa1b8a2d40916756e891627e9e8f8d119`  
		Last Modified: Fri, 19 Jan 2024 00:32:32 GMT  
		Size: 1.9 MB (1916607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36` - unknown; unknown

```console
$ docker pull busybox@sha256:a69e011a60760aba5dd1209f91c05980c6fab54d8b25ae169291e63377f51cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 KB (12193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd1ff0b19ae0f0339dfa452087f6e62d3885ac4cd6d87c8b93b3893fa44b0b6`

```dockerfile
```

-	Layers:
	-	`sha256:24ccf6b7ae0e49578be9c4155a809a71d3e4b9c5486ce7c4086d68e3d1acd22f`  
		Last Modified: Fri, 19 Jan 2024 00:32:31 GMT  
		Size: 4.8 KB (4800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53a196fbf5767399864392abcd4b090e16c2f74821ac8b44d3f139986875dae`  
		Last Modified: Fri, 19 Jan 2024 00:32:31 GMT  
		Size: 7.4 KB (7393 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36` - linux; 386

```console
$ docker pull busybox@sha256:99eabec0f153fb38feb80682492123326c994a6857f7ef9b73d46eecd8b81684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2268883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a422f55b78a61a0acf17d1ad4cea56c7542f1a09e6a256def15b8787d41ad7a`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:b6f95b873e20279fb8550d2d0b30bff9e72de3fe85f2ff4cfbf5f8f8aa6dabf4`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 2.3 MB (2268883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36` - unknown; unknown

```console
$ docker pull busybox@sha256:deb0f17418ba410fceb230e48f01a2056732cba642d66a812901fa3d039c7e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 KB (12043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e79a31fa88e6a7c031f212bf2849dfb712003711e72dcae4abf34405846cdcf`

```dockerfile
```

-	Layers:
	-	`sha256:347076177c54f21c7c7fd98a9a45a717898d8441f14a94c5248a682a00008516`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 4.7 KB (4725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcf8fff8866352521d3aef70307e34f73f9951524290a8b4b36ffb75b6e6c138`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 7.3 KB (7318 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36` - linux; mips64le

```console
$ docker pull busybox@sha256:8c4284fa9cc28d0b9455f84527de8b58d5d4df00abcd18e47f2f1dc4e89f7ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2077641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c67790aa14859c61c94e0b7e727a8c50a5e246783c252e080ae41187e8ec52`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:b9f2f1866e3467e8735b90ecad932b7c1f122f80426b5beda6fb8a4c87f45757`  
		Last Modified: Wed, 06 Mar 2024 00:08:46 GMT  
		Size: 2.1 MB (2077641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36` - linux; ppc64le

```console
$ docker pull busybox@sha256:4b36905f6e9385ec2234f41dbb9d67ccd99ee2b50ef225c08746b2276991bb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb40c4cff2a5d1551f5a9e79b6fac3cf2d655f702041d0ae8d670e027645bd9`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1e329ff3bf1d3bf69d13da2954652acf3457a6fbd276780a232bb5254c915148`  
		Last Modified: Fri, 19 Jan 2024 00:42:12 GMT  
		Size: 2.5 MB (2528609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36` - unknown; unknown

```console
$ docker pull busybox@sha256:17110abebf0882f7e23b68ea936ab719a49047e1b4a8e0ab0118ff0abff0066d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 KB (12281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48490b9b70ffd6de2941a4f2dbecc81750fe06d0c527e787a94fff4504c7721`

```dockerfile
```

-	Layers:
	-	`sha256:07f1bfa21dee33589c5658c47aa84655e024d44ef684cbd102571f1fdaa89c48`  
		Last Modified: Fri, 19 Jan 2024 00:42:12 GMT  
		Size: 4.8 KB (4842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f2fcbb930547c7a7fa4783062b75854e39e225a8dc9dbf51df1bcb5b2580c4`  
		Last Modified: Fri, 19 Jan 2024 00:42:11 GMT  
		Size: 7.4 KB (7439 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36` - linux; riscv64

```console
$ docker pull busybox@sha256:41af629cfa908c7ed7550db6a260c79d6dd55fe4996d7481595e3d547ab829c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.3 KB (914275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9673ad33efcd24dfd28f0415f23ee1c42d743140691e10781669692ef3af1ba6`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:917dbba7e6e14feb5914ca2711ff13b50b1f9a2b0b8315b79bbceabde34d11c2`  
		Last Modified: Thu, 18 Jan 2024 23:05:50 GMT  
		Size: 914.3 KB (914275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36` - unknown; unknown

```console
$ docker pull busybox@sha256:126af02605028b8076a4a47fe1c707c795ce58c66a266c67b447519ebf1f3b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 KB (12303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa149c79ad9040800185662b3a226758c08cd6d612ca2a1abf6ebf0d9716f32`

```dockerfile
```

-	Layers:
	-	`sha256:1acfa35c63c5a80ca903c34528318a0b6b614a7060738be73b2b8424004473b1`  
		Last Modified: Thu, 18 Jan 2024 23:05:50 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97288386ab763b23aa899ebcfaa85d4b1708c86df318569f03865c7fb2b7ad4f`  
		Last Modified: Thu, 18 Jan 2024 23:05:51 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36` - linux; s390x

```console
$ docker pull busybox@sha256:df5506ae24620e67cb668f0137869babd6305cf4912190ee7de781c412b9bad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1926831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a46af96236bcedbc5591856e442999857d24fd51f5ff2135ede6486c79e2e7`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:230db3ea6af07ccf4b5f3ad6164f90d07967b83607909a587631245cc7c84ef4`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 1.9 MB (1926831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36` - unknown; unknown

```console
$ docker pull busybox@sha256:b2a97dca77d5ae1e0ddef0cbfba271b5f0597c9ea7b8cb8127b397c7c9d03dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 KB (12149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e23940337a50804f81942abe24849f22423565ad3dabdfeefa3ee5cc61fd96`

```dockerfile
```

-	Layers:
	-	`sha256:5f4fdc6f7194500531229dc2d7aa2b54119cdf908b5e842b6ae1bfbf57487b79`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 4.8 KB (4778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ad8320e0617081f2bb73e6289f33979e1ee192d12ef3459b3bfe278084c075c`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 7.4 KB (7371 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:1.36-glibc`

```console
$ docker pull busybox@sha256:eba7ad4cfa554dd96910090a41fa8eee6d4231f92bf5587dbd05a4badfeec2cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `busybox:1.36-glibc` - linux; amd64

```console
$ docker pull busybox@sha256:538721340ded10875f4710cad688c70e5d0ecb4dcd5e7d0c161f301f36f79414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2220094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f57d9401f8d42f986df300f0c69192fc41da28ccc8d797829467780db3dd741`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9ad63333ebc97e32b987ae66aa3cff81300e4c2e6d2f2395cef8a3ae18b249fe`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 2.2 MB (2220094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:253eb45864243efd740aa87ba169151e4d165538b168d77284396469217ee5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 KB (12149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9095a17baa618e6b1b5b3da6493f78682688b3c18f07a524e30bd47a404d4cb`

```dockerfile
```

-	Layers:
	-	`sha256:e1104929ee0cb0e8ea3d2c3b4024ce9f852364d233aabe800ea7789df99cfc23`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 4.8 KB (4778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d186640ac3f58c681ac3bc3aa314992df65409336eccb7e94bd7c4b8174a2b`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 7.4 KB (7371 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36-glibc` - linux; arm variant v5

```console
$ docker pull busybox@sha256:491e28080f41a345b794a1528e23525f67f8693d8c541b9ef8f4990f6af501f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1776853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6578b94d614adfa46696754ab33bdd8b8b70ac8adea2fb6061d90e2b01f90e3`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:e209cc4af23c3ed4ac3e8cf58f8e9ea90d51fe28fcfca3ad91d91e74aabca274`  
		Last Modified: Wed, 06 Mar 2024 00:07:47 GMT  
		Size: 1.8 MB (1776853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36-glibc` - linux; arm variant v7

```console
$ docker pull busybox@sha256:8a4415fb43600953cbdac6ec03c2d96d900bb21f8d78964837dad7f73b9afcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1554425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9903cc888814e8feef24381cdb6d29d8598385dcb109a9908a4a98e1ab021532`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:a7cbd68a76a020b8b283c940bc267cd88a66013dcb160cad746344483dfc4b52`  
		Last Modified: Wed, 06 Mar 2024 00:10:11 GMT  
		Size: 1.6 MB (1554425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36-glibc` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:8f03917912ea995c637b6c0295846aaff5665f06ac82a29b421fba4c379494e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1916607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4fd538a9a0b729be05707cf805388be2fb701cfd5d44c6542f1988e8aef6e3`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c2bf9493c1bf786e95e3eac7d406c20aa1b8a2d40916756e891627e9e8f8d119`  
		Last Modified: Fri, 19 Jan 2024 00:32:32 GMT  
		Size: 1.9 MB (1916607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:a69e011a60760aba5dd1209f91c05980c6fab54d8b25ae169291e63377f51cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 KB (12193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd1ff0b19ae0f0339dfa452087f6e62d3885ac4cd6d87c8b93b3893fa44b0b6`

```dockerfile
```

-	Layers:
	-	`sha256:24ccf6b7ae0e49578be9c4155a809a71d3e4b9c5486ce7c4086d68e3d1acd22f`  
		Last Modified: Fri, 19 Jan 2024 00:32:31 GMT  
		Size: 4.8 KB (4800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53a196fbf5767399864392abcd4b090e16c2f74821ac8b44d3f139986875dae`  
		Last Modified: Fri, 19 Jan 2024 00:32:31 GMT  
		Size: 7.4 KB (7393 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36-glibc` - linux; 386

```console
$ docker pull busybox@sha256:99eabec0f153fb38feb80682492123326c994a6857f7ef9b73d46eecd8b81684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2268883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a422f55b78a61a0acf17d1ad4cea56c7542f1a09e6a256def15b8787d41ad7a`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:b6f95b873e20279fb8550d2d0b30bff9e72de3fe85f2ff4cfbf5f8f8aa6dabf4`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 2.3 MB (2268883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:deb0f17418ba410fceb230e48f01a2056732cba642d66a812901fa3d039c7e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 KB (12043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e79a31fa88e6a7c031f212bf2849dfb712003711e72dcae4abf34405846cdcf`

```dockerfile
```

-	Layers:
	-	`sha256:347076177c54f21c7c7fd98a9a45a717898d8441f14a94c5248a682a00008516`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 4.7 KB (4725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcf8fff8866352521d3aef70307e34f73f9951524290a8b4b36ffb75b6e6c138`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 7.3 KB (7318 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36-glibc` - linux; mips64le

```console
$ docker pull busybox@sha256:8c4284fa9cc28d0b9455f84527de8b58d5d4df00abcd18e47f2f1dc4e89f7ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2077641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c67790aa14859c61c94e0b7e727a8c50a5e246783c252e080ae41187e8ec52`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:b9f2f1866e3467e8735b90ecad932b7c1f122f80426b5beda6fb8a4c87f45757`  
		Last Modified: Wed, 06 Mar 2024 00:08:46 GMT  
		Size: 2.1 MB (2077641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36-glibc` - linux; ppc64le

```console
$ docker pull busybox@sha256:4b36905f6e9385ec2234f41dbb9d67ccd99ee2b50ef225c08746b2276991bb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb40c4cff2a5d1551f5a9e79b6fac3cf2d655f702041d0ae8d670e027645bd9`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1e329ff3bf1d3bf69d13da2954652acf3457a6fbd276780a232bb5254c915148`  
		Last Modified: Fri, 19 Jan 2024 00:42:12 GMT  
		Size: 2.5 MB (2528609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:17110abebf0882f7e23b68ea936ab719a49047e1b4a8e0ab0118ff0abff0066d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 KB (12281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48490b9b70ffd6de2941a4f2dbecc81750fe06d0c527e787a94fff4504c7721`

```dockerfile
```

-	Layers:
	-	`sha256:07f1bfa21dee33589c5658c47aa84655e024d44ef684cbd102571f1fdaa89c48`  
		Last Modified: Fri, 19 Jan 2024 00:42:12 GMT  
		Size: 4.8 KB (4842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f2fcbb930547c7a7fa4783062b75854e39e225a8dc9dbf51df1bcb5b2580c4`  
		Last Modified: Fri, 19 Jan 2024 00:42:11 GMT  
		Size: 7.4 KB (7439 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36-glibc` - linux; s390x

```console
$ docker pull busybox@sha256:df5506ae24620e67cb668f0137869babd6305cf4912190ee7de781c412b9bad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1926831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a46af96236bcedbc5591856e442999857d24fd51f5ff2135ede6486c79e2e7`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:230db3ea6af07ccf4b5f3ad6164f90d07967b83607909a587631245cc7c84ef4`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 1.9 MB (1926831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:b2a97dca77d5ae1e0ddef0cbfba271b5f0597c9ea7b8cb8127b397c7c9d03dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 KB (12149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e23940337a50804f81942abe24849f22423565ad3dabdfeefa3ee5cc61fd96`

```dockerfile
```

-	Layers:
	-	`sha256:5f4fdc6f7194500531229dc2d7aa2b54119cdf908b5e842b6ae1bfbf57487b79`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 4.8 KB (4778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ad8320e0617081f2bb73e6289f33979e1ee192d12ef3459b3bfe278084c075c`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 7.4 KB (7371 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:1.36-musl`

```console
$ docker pull busybox@sha256:9a7f0d2407780a98013e227ddc43f87bf5fbe626fb59f98280efd591c75ccdec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `busybox:1.36-musl` - linux; amd64

```console
$ docker pull busybox@sha256:d4707523ce6e12afdbe9a3be5ad69027150a834870ca0933baf7516dd1fe0f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **878.7 KB (878681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59888ccc9e6510deabb10bb0452f184f40cec7064c0fc522a01924f66c7fdfd8`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8dfc70c9a1cfc61f5873aed748e446239a5cb27faddd51d118180665010c02b7`  
		Last Modified: Thu, 18 Jan 2024 23:03:35 GMT  
		Size: 878.7 KB (878681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:864e79c6eb0056047a68c6c717ee53d548519ee307dec471696a5e6d0fab0a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c89e5c4f095b960e7a950b75e8f1386f0c1d1d43c108818b9b3922c803c1f1d`

```dockerfile
```

-	Layers:
	-	`sha256:aa7db50a9fdf0d3338cc08bc515695143e4aaf3e3e4b276f5f6d6d3bba5cca05`  
		Last Modified: Thu, 18 Jan 2024 23:03:35 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce0dddc950954bfb91430621087a12e68a552255f8c49ff243c27b22fbc6280`  
		Last Modified: Thu, 18 Jan 2024 23:03:35 GMT  
		Size: 5.9 KB (5871 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36-musl` - linux; arm variant v6

```console
$ docker pull busybox@sha256:b64a6a9cff5d2916ce4e5ab52254faa487ae93d9028c157c10d444aa3b5b7e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.6 KB (987570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5059e5cce9929da538b30d11caea9231836d6b937083115b4058ae4649341b74`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd544bbcb8b286d4a58e2b02357bb516d089d281fc87ae2b375921b8d2389923`  
		Last Modified: Thu, 18 Jan 2024 23:58:56 GMT  
		Size: 987.6 KB (987570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:0c1556654c58755833235ba840bb04258b5cf8d3e1771be01a2c48e38c266c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e96145e5c30a04c819cb052df4fa049365de24673fc3afdc9d5305cc2999a8`

```dockerfile
```

-	Layers:
	-	`sha256:1bbd274efa1896b02a475d573d66e47cc60d67dfb2334eef4aefc1d23763fe11`  
		Last Modified: Thu, 18 Jan 2024 23:58:56 GMT  
		Size: 7.2 KB (7231 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36-musl` - linux; arm variant v7

```console
$ docker pull busybox@sha256:f2939eb0b529af5706172c10db02a0894949c461b81ed4282ff4df5bf18c14d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.6 KB (843648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855943b02ba3319e1345d803a557c4a88bfd0c18954db6869f2ac791e17c4ae3`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (musl), Alpine 3.19.1
```

-	Layers:
	-	`sha256:83dc776fdc81b19e8a0c134d8eecfc7793d00ca52c1cc4292e973750e3684712`  
		Last Modified: Wed, 06 Mar 2024 00:10:38 GMT  
		Size: 843.6 KB (843648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36-musl` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:fed6b26ea319254ef0d6bae87482b5ab58b85250a7cc46d14c533e1f5c2556db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.0 KB (920992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f13cdcd8df2876053fd8dc5d01363344a92ea4d6537bd78625b9209e988edf`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d997961b9429e6c49b53a709a914c6578f5ff5ba7166ee52de62d1ac94887c1e`  
		Last Modified: Fri, 19 Jan 2024 01:36:22 GMT  
		Size: 921.0 KB (920992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:1cbd2ff89d7ff09ec11e246f3a887f3a914ab78b5d7445c43487b8c6fbed88cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83f629b0163590a531f21a762bb0cbaa263d937678e8f68d96a31c90ef4a07b`

```dockerfile
```

-	Layers:
	-	`sha256:3c2685448006e438049a85838a6b8137f2e8454a9bc20b249241ff956b520505`  
		Last Modified: Fri, 19 Jan 2024 01:36:22 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6177450e2c462aaedbb8f947886eb918cc00046a7fdc55ccca512c51f9243ee4`  
		Last Modified: Fri, 19 Jan 2024 01:36:22 GMT  
		Size: 5.9 KB (5883 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36-musl` - linux; 386

```console
$ docker pull busybox@sha256:b6678a8456f13554d339f393c4bcf798b3730a4f1662f6d9842129cbeeb5c665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.5 KB (875482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e9971e1ff6c5b5940f3f82628fe182aead284575c0ae4a798ed91e15ef08d7`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:769db000cf23b44ad2664168ee3886ca8883b18f32581f08cd06ce00f41ff872`  
		Last Modified: Thu, 18 Jan 2024 23:03:39 GMT  
		Size: 875.5 KB (875482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:fcc65e203ef7a06b3c9852b25de034cc8472405e5d7f033e818752a15778a758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa92905283639dceabeee0502770622fc73c4856e769907a58b011d8c5ea776f`

```dockerfile
```

-	Layers:
	-	`sha256:9020223ee3ca8d6d37dab73b397baddf426d3d408db20f63d02b1e9d2faff9d6`  
		Last Modified: Thu, 18 Jan 2024 23:03:39 GMT  
		Size: 3.3 KB (3254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6eae553040cde89419e4a177c32658f1d867ec25cf9a30b7655184d189a9439`  
		Last Modified: Thu, 18 Jan 2024 23:03:39 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36-musl` - linux; ppc64le

```console
$ docker pull busybox@sha256:74dfdbf9d13a59af2f6aa61ad738fa1fdade6dfd0d6f687eb3b0d53ffc8b5623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **967.1 KB (967138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f646f514a9f9bafe5483609c8bb0c3c64f9628f35d9beffda459a7fc992d9fe0`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:e4d8791bb918bc69b870f21a553724ec9b2812219040885317ce57b6eb4e6ab3`  
		Last Modified: Fri, 19 Jan 2024 01:03:30 GMT  
		Size: 967.1 KB (967138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:832836469bae4830469c6b70aa0ca4cf84181eb2a11484479ea37d6ce6143846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376ae5066f35abd2be10b0eacfecd79b91086e268f707d436e7b8798c411fcf9`

```dockerfile
```

-	Layers:
	-	`sha256:1ecc1159b446640a86f9969f010bbc8178567a5b46e779b2ce340b9229dac07e`  
		Last Modified: Fri, 19 Jan 2024 01:03:30 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a8411155c9d98fe9609d4ca6e64859296085c39baa2e804ebae951ab5b80b8`  
		Last Modified: Fri, 19 Jan 2024 01:03:30 GMT  
		Size: 5.9 KB (5909 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36-musl` - linux; s390x

```console
$ docker pull busybox@sha256:e7e0969b47c05409c0fa5c909e006a620f845d5b119869c8346e4f3cb93f8c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **940.3 KB (940326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774f60d2b6d3daa542d524858ddb90ae71c4b3cc014a0235132a36c51e1d4515`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:48e10ecef46b18109935c897c4fb6ba3b06fea3fc7b54588e2aef37a9ecc7db9`  
		Last Modified: Sat, 20 Jan 2024 17:54:57 GMT  
		Size: 940.3 KB (940326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:6ac7f239a3bffeaff764ae1948e58f80497ce3fe2d2bdfb42b7c9899ac58270e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2deb03e82c885a1c5de5b9ffc72f3b12beb43f880ffec52862abecf85ba22e4`

```dockerfile
```

-	Layers:
	-	`sha256:72517eef4c47c126a39ac1b293ba0bcfcb63a31962064a4a8bc3907115262d23`  
		Last Modified: Sat, 20 Jan 2024 17:54:57 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:990936cff923ba93c536c3d8f4ba7db950b54f638d8ca2d0b278ed1e0110f3b9`  
		Last Modified: Sat, 20 Jan 2024 17:54:57 GMT  
		Size: 5.9 KB (5871 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:1.36-uclibc`

```console
$ docker pull busybox@sha256:61651f1730187bbbfaa01e81d31eb082a1853a14118255c7dff5f1365d0ca3e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; riscv64
	-	unknown; unknown

### `busybox:1.36-uclibc` - linux; amd64

```console
$ docker pull busybox@sha256:21de0dff31b277e0d37fe21f6e89e461f5c07415719d225235121c144287dc17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **783.2 KB (783164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e537aeebf5260fe6cb054017b3af5862945ab73f5a7091cd6e2127cdfdd5a14`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cff2761077a7b33f0ac06f806d159087b8c79413afc45167a232c5b9394615f1`  
		Last Modified: Thu, 18 Jan 2024 23:03:48 GMT  
		Size: 783.2 KB (783164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:385fe86cbfdf640c4538befe889e1e9bf93fa21eeb9955f7ea076e6d874a2d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7796465a33cc98caddbb8bc190b367eaeb431320484f406887f0d1c8578327c`

```dockerfile
```

-	Layers:
	-	`sha256:165aad5817a1de48ec8d7d517f5332a81840adf0cc4836a6c3f4aad1ac31e128`  
		Last Modified: Thu, 18 Jan 2024 23:03:51 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f647335cce5641a56b28c17896a32f125e7d6823621a542398ee88b0754d863`  
		Last Modified: Thu, 18 Jan 2024 23:03:48 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36-uclibc` - linux; arm variant v5

```console
$ docker pull busybox@sha256:2e2d13aea845763e5152bb8116738d5179f67b79fc6fde83bf813896829d4bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.2 KB (744233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be06eb6ec3aaf1ca11f443876561f4e75e1dd0ceb407c1880033d7ff6328b3e`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (uclibc), Buildroot 2023.11.1, Debian 12
```

-	Layers:
	-	`sha256:120231968b7db68bb2d25cd765a3eee8fe0ec5be354a4306354fdd9606bd7774`  
		Last Modified: Wed, 06 Mar 2024 00:08:00 GMT  
		Size: 744.2 KB (744233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36-uclibc` - linux; arm variant v7

```console
$ docker pull busybox@sha256:b87edd76d8d0b9e848a0059a3014d87dabf763bc6cfcb9df52d13f4523a3d371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.9 KB (708929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2858fb01eb20e8b8f27c5d3108e9df3065a5c3196a170111aabbf09b81d4bf9`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (uclibc), Buildroot 2023.11.1, Debian 12
```

-	Layers:
	-	`sha256:19210f7552436b95fa7de660fcbf9e9425a0813bfccb850b3fcd053709caf443`  
		Last Modified: Wed, 06 Mar 2024 00:10:24 GMT  
		Size: 708.9 KB (708929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36-uclibc` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:b8879bdf897086348b8048b0a5ae3d85addc583ed20050328ec7146858e847e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **836.8 KB (836843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80467bacead9d1b091a5648f067f735716b201eba3fd71a4fb44e13f5341f0cd`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cea42dbd04d75d2786e9fef4399413709452debd69b417e4c200743b4b844c00`  
		Last Modified: Fri, 19 Jan 2024 00:57:12 GMT  
		Size: 836.8 KB (836843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:d872e2c2932c6bd7821197d583a23869fdb68bf056a7d7dac8a97e20e62bd6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a42e696a19934cb4621a011849c38a5b99a99a7db2a5f5914af4bd5c886b3f4`

```dockerfile
```

-	Layers:
	-	`sha256:4f836af667398f1a6feb5e25980960f902daf9096ca799ab436dba129c2c8698`  
		Last Modified: Fri, 19 Jan 2024 00:57:11 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:880e28375df06f638d5045451a8dda0fc51cc28429dba1387275de009fd5d3b3`  
		Last Modified: Fri, 19 Jan 2024 00:57:11 GMT  
		Size: 5.9 KB (5909 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36-uclibc` - linux; 386

```console
$ docker pull busybox@sha256:b805bdb43c275243e31c549abcc71d98c1323a225598b74e5a9b9dc91fdf4073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **747.9 KB (747949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992d7e8ad26e67c26250373ac39142b725403b68173a52edacc7c191cf5f097a`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d6a6d95c0da603317dbc3d49423910ecb730bb5d4219de536cfd7120bd1d792e`  
		Last Modified: Thu, 18 Jan 2024 23:03:27 GMT  
		Size: 747.9 KB (747949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:3cb35ce2ebff606afe19b8965ea3f0fe093bbbfc9fabc67a3158c7f4cd146068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c6ca91c6552ef25e52903cad76d996d7b60375a160b4205a35c7b060549a35`

```dockerfile
```

-	Layers:
	-	`sha256:cd8b24a6892d4af4db2582c4db92db552c251baa708fd3d249742144a1f06c65`  
		Last Modified: Thu, 18 Jan 2024 23:03:27 GMT  
		Size: 3.3 KB (3274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3117b42969c2d3cfbd84681cccff735d766b482184839bd402d14f12180792ad`  
		Last Modified: Thu, 18 Jan 2024 23:03:27 GMT  
		Size: 5.9 KB (5868 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36-uclibc` - linux; mips64le

```console
$ docker pull busybox@sha256:388eed10bf5614e88ae1e2b2c1d237cbef877a07858125415556e3d9edff526d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **948.9 KB (948864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd60f88674723ffdec05a32d2bee1157f95e335ced9c3efea5686b9b15cd1416`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (uclibc), Buildroot 2023.11.1, Debian 12
```

-	Layers:
	-	`sha256:16b2225af5a2181079c894731b1031c046d90aca99349dd3487cfc6d6702d0e3`  
		Last Modified: Wed, 06 Mar 2024 00:09:07 GMT  
		Size: 948.9 KB (948864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36-uclibc` - linux; riscv64

```console
$ docker pull busybox@sha256:41af629cfa908c7ed7550db6a260c79d6dd55fe4996d7481595e3d547ab829c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.3 KB (914275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9673ad33efcd24dfd28f0415f23ee1c42d743140691e10781669692ef3af1ba6`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:917dbba7e6e14feb5914ca2711ff13b50b1f9a2b0b8315b79bbceabde34d11c2`  
		Last Modified: Thu, 18 Jan 2024 23:05:50 GMT  
		Size: 914.3 KB (914275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:126af02605028b8076a4a47fe1c707c795ce58c66a266c67b447519ebf1f3b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 KB (12303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa149c79ad9040800185662b3a226758c08cd6d612ca2a1abf6ebf0d9716f32`

```dockerfile
```

-	Layers:
	-	`sha256:1acfa35c63c5a80ca903c34528318a0b6b614a7060738be73b2b8424004473b1`  
		Last Modified: Thu, 18 Jan 2024 23:05:50 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97288386ab763b23aa899ebcfaa85d4b1708c86df318569f03865c7fb2b7ad4f`  
		Last Modified: Thu, 18 Jan 2024 23:05:51 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:1.36.1`

```console
$ docker pull busybox@sha256:acdc29f25f9c5d678b264007f6f0ea63f12756dcef1cdb043f3fd2a13ba735c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 17
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `busybox:1.36.1` - linux; amd64

```console
$ docker pull busybox@sha256:538721340ded10875f4710cad688c70e5d0ecb4dcd5e7d0c161f301f36f79414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2220094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f57d9401f8d42f986df300f0c69192fc41da28ccc8d797829467780db3dd741`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9ad63333ebc97e32b987ae66aa3cff81300e4c2e6d2f2395cef8a3ae18b249fe`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 2.2 MB (2220094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1` - unknown; unknown

```console
$ docker pull busybox@sha256:253eb45864243efd740aa87ba169151e4d165538b168d77284396469217ee5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 KB (12149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9095a17baa618e6b1b5b3da6493f78682688b3c18f07a524e30bd47a404d4cb`

```dockerfile
```

-	Layers:
	-	`sha256:e1104929ee0cb0e8ea3d2c3b4024ce9f852364d233aabe800ea7789df99cfc23`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 4.8 KB (4778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d186640ac3f58c681ac3bc3aa314992df65409336eccb7e94bd7c4b8174a2b`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 7.4 KB (7371 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36.1` - linux; arm variant v5

```console
$ docker pull busybox@sha256:491e28080f41a345b794a1528e23525f67f8693d8c541b9ef8f4990f6af501f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1776853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6578b94d614adfa46696754ab33bdd8b8b70ac8adea2fb6061d90e2b01f90e3`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:e209cc4af23c3ed4ac3e8cf58f8e9ea90d51fe28fcfca3ad91d91e74aabca274`  
		Last Modified: Wed, 06 Mar 2024 00:07:47 GMT  
		Size: 1.8 MB (1776853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1` - linux; arm variant v6

```console
$ docker pull busybox@sha256:b64a6a9cff5d2916ce4e5ab52254faa487ae93d9028c157c10d444aa3b5b7e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.6 KB (987570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5059e5cce9929da538b30d11caea9231836d6b937083115b4058ae4649341b74`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd544bbcb8b286d4a58e2b02357bb516d089d281fc87ae2b375921b8d2389923`  
		Last Modified: Thu, 18 Jan 2024 23:58:56 GMT  
		Size: 987.6 KB (987570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1` - unknown; unknown

```console
$ docker pull busybox@sha256:0c1556654c58755833235ba840bb04258b5cf8d3e1771be01a2c48e38c266c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e96145e5c30a04c819cb052df4fa049365de24673fc3afdc9d5305cc2999a8`

```dockerfile
```

-	Layers:
	-	`sha256:1bbd274efa1896b02a475d573d66e47cc60d67dfb2334eef4aefc1d23763fe11`  
		Last Modified: Thu, 18 Jan 2024 23:58:56 GMT  
		Size: 7.2 KB (7231 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36.1` - linux; arm variant v7

```console
$ docker pull busybox@sha256:8a4415fb43600953cbdac6ec03c2d96d900bb21f8d78964837dad7f73b9afcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1554425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9903cc888814e8feef24381cdb6d29d8598385dcb109a9908a4a98e1ab021532`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:a7cbd68a76a020b8b283c940bc267cd88a66013dcb160cad746344483dfc4b52`  
		Last Modified: Wed, 06 Mar 2024 00:10:11 GMT  
		Size: 1.6 MB (1554425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:8f03917912ea995c637b6c0295846aaff5665f06ac82a29b421fba4c379494e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1916607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4fd538a9a0b729be05707cf805388be2fb701cfd5d44c6542f1988e8aef6e3`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c2bf9493c1bf786e95e3eac7d406c20aa1b8a2d40916756e891627e9e8f8d119`  
		Last Modified: Fri, 19 Jan 2024 00:32:32 GMT  
		Size: 1.9 MB (1916607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1` - unknown; unknown

```console
$ docker pull busybox@sha256:a69e011a60760aba5dd1209f91c05980c6fab54d8b25ae169291e63377f51cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 KB (12193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd1ff0b19ae0f0339dfa452087f6e62d3885ac4cd6d87c8b93b3893fa44b0b6`

```dockerfile
```

-	Layers:
	-	`sha256:24ccf6b7ae0e49578be9c4155a809a71d3e4b9c5486ce7c4086d68e3d1acd22f`  
		Last Modified: Fri, 19 Jan 2024 00:32:31 GMT  
		Size: 4.8 KB (4800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53a196fbf5767399864392abcd4b090e16c2f74821ac8b44d3f139986875dae`  
		Last Modified: Fri, 19 Jan 2024 00:32:31 GMT  
		Size: 7.4 KB (7393 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36.1` - linux; 386

```console
$ docker pull busybox@sha256:99eabec0f153fb38feb80682492123326c994a6857f7ef9b73d46eecd8b81684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2268883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a422f55b78a61a0acf17d1ad4cea56c7542f1a09e6a256def15b8787d41ad7a`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:b6f95b873e20279fb8550d2d0b30bff9e72de3fe85f2ff4cfbf5f8f8aa6dabf4`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 2.3 MB (2268883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1` - unknown; unknown

```console
$ docker pull busybox@sha256:deb0f17418ba410fceb230e48f01a2056732cba642d66a812901fa3d039c7e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 KB (12043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e79a31fa88e6a7c031f212bf2849dfb712003711e72dcae4abf34405846cdcf`

```dockerfile
```

-	Layers:
	-	`sha256:347076177c54f21c7c7fd98a9a45a717898d8441f14a94c5248a682a00008516`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 4.7 KB (4725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcf8fff8866352521d3aef70307e34f73f9951524290a8b4b36ffb75b6e6c138`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 7.3 KB (7318 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36.1` - linux; mips64le

```console
$ docker pull busybox@sha256:8c4284fa9cc28d0b9455f84527de8b58d5d4df00abcd18e47f2f1dc4e89f7ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2077641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c67790aa14859c61c94e0b7e727a8c50a5e246783c252e080ae41187e8ec52`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:b9f2f1866e3467e8735b90ecad932b7c1f122f80426b5beda6fb8a4c87f45757`  
		Last Modified: Wed, 06 Mar 2024 00:08:46 GMT  
		Size: 2.1 MB (2077641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1` - linux; ppc64le

```console
$ docker pull busybox@sha256:4b36905f6e9385ec2234f41dbb9d67ccd99ee2b50ef225c08746b2276991bb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb40c4cff2a5d1551f5a9e79b6fac3cf2d655f702041d0ae8d670e027645bd9`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1e329ff3bf1d3bf69d13da2954652acf3457a6fbd276780a232bb5254c915148`  
		Last Modified: Fri, 19 Jan 2024 00:42:12 GMT  
		Size: 2.5 MB (2528609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1` - unknown; unknown

```console
$ docker pull busybox@sha256:17110abebf0882f7e23b68ea936ab719a49047e1b4a8e0ab0118ff0abff0066d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 KB (12281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48490b9b70ffd6de2941a4f2dbecc81750fe06d0c527e787a94fff4504c7721`

```dockerfile
```

-	Layers:
	-	`sha256:07f1bfa21dee33589c5658c47aa84655e024d44ef684cbd102571f1fdaa89c48`  
		Last Modified: Fri, 19 Jan 2024 00:42:12 GMT  
		Size: 4.8 KB (4842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f2fcbb930547c7a7fa4783062b75854e39e225a8dc9dbf51df1bcb5b2580c4`  
		Last Modified: Fri, 19 Jan 2024 00:42:11 GMT  
		Size: 7.4 KB (7439 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36.1` - linux; riscv64

```console
$ docker pull busybox@sha256:41af629cfa908c7ed7550db6a260c79d6dd55fe4996d7481595e3d547ab829c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.3 KB (914275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9673ad33efcd24dfd28f0415f23ee1c42d743140691e10781669692ef3af1ba6`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:917dbba7e6e14feb5914ca2711ff13b50b1f9a2b0b8315b79bbceabde34d11c2`  
		Last Modified: Thu, 18 Jan 2024 23:05:50 GMT  
		Size: 914.3 KB (914275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1` - unknown; unknown

```console
$ docker pull busybox@sha256:126af02605028b8076a4a47fe1c707c795ce58c66a266c67b447519ebf1f3b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 KB (12303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa149c79ad9040800185662b3a226758c08cd6d612ca2a1abf6ebf0d9716f32`

```dockerfile
```

-	Layers:
	-	`sha256:1acfa35c63c5a80ca903c34528318a0b6b614a7060738be73b2b8424004473b1`  
		Last Modified: Thu, 18 Jan 2024 23:05:50 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97288386ab763b23aa899ebcfaa85d4b1708c86df318569f03865c7fb2b7ad4f`  
		Last Modified: Thu, 18 Jan 2024 23:05:51 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36.1` - linux; s390x

```console
$ docker pull busybox@sha256:df5506ae24620e67cb668f0137869babd6305cf4912190ee7de781c412b9bad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1926831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a46af96236bcedbc5591856e442999857d24fd51f5ff2135ede6486c79e2e7`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:230db3ea6af07ccf4b5f3ad6164f90d07967b83607909a587631245cc7c84ef4`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 1.9 MB (1926831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1` - unknown; unknown

```console
$ docker pull busybox@sha256:b2a97dca77d5ae1e0ddef0cbfba271b5f0597c9ea7b8cb8127b397c7c9d03dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 KB (12149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e23940337a50804f81942abe24849f22423565ad3dabdfeefa3ee5cc61fd96`

```dockerfile
```

-	Layers:
	-	`sha256:5f4fdc6f7194500531229dc2d7aa2b54119cdf908b5e842b6ae1bfbf57487b79`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 4.8 KB (4778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ad8320e0617081f2bb73e6289f33979e1ee192d12ef3459b3bfe278084c075c`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 7.4 KB (7371 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:1.36.1-glibc`

```console
$ docker pull busybox@sha256:eba7ad4cfa554dd96910090a41fa8eee6d4231f92bf5587dbd05a4badfeec2cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `busybox:1.36.1-glibc` - linux; amd64

```console
$ docker pull busybox@sha256:538721340ded10875f4710cad688c70e5d0ecb4dcd5e7d0c161f301f36f79414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2220094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f57d9401f8d42f986df300f0c69192fc41da28ccc8d797829467780db3dd741`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9ad63333ebc97e32b987ae66aa3cff81300e4c2e6d2f2395cef8a3ae18b249fe`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 2.2 MB (2220094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:253eb45864243efd740aa87ba169151e4d165538b168d77284396469217ee5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 KB (12149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9095a17baa618e6b1b5b3da6493f78682688b3c18f07a524e30bd47a404d4cb`

```dockerfile
```

-	Layers:
	-	`sha256:e1104929ee0cb0e8ea3d2c3b4024ce9f852364d233aabe800ea7789df99cfc23`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 4.8 KB (4778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d186640ac3f58c681ac3bc3aa314992df65409336eccb7e94bd7c4b8174a2b`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 7.4 KB (7371 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36.1-glibc` - linux; arm variant v5

```console
$ docker pull busybox@sha256:491e28080f41a345b794a1528e23525f67f8693d8c541b9ef8f4990f6af501f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1776853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6578b94d614adfa46696754ab33bdd8b8b70ac8adea2fb6061d90e2b01f90e3`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:e209cc4af23c3ed4ac3e8cf58f8e9ea90d51fe28fcfca3ad91d91e74aabca274`  
		Last Modified: Wed, 06 Mar 2024 00:07:47 GMT  
		Size: 1.8 MB (1776853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1-glibc` - linux; arm variant v7

```console
$ docker pull busybox@sha256:8a4415fb43600953cbdac6ec03c2d96d900bb21f8d78964837dad7f73b9afcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1554425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9903cc888814e8feef24381cdb6d29d8598385dcb109a9908a4a98e1ab021532`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:a7cbd68a76a020b8b283c940bc267cd88a66013dcb160cad746344483dfc4b52`  
		Last Modified: Wed, 06 Mar 2024 00:10:11 GMT  
		Size: 1.6 MB (1554425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1-glibc` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:8f03917912ea995c637b6c0295846aaff5665f06ac82a29b421fba4c379494e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1916607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4fd538a9a0b729be05707cf805388be2fb701cfd5d44c6542f1988e8aef6e3`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c2bf9493c1bf786e95e3eac7d406c20aa1b8a2d40916756e891627e9e8f8d119`  
		Last Modified: Fri, 19 Jan 2024 00:32:32 GMT  
		Size: 1.9 MB (1916607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:a69e011a60760aba5dd1209f91c05980c6fab54d8b25ae169291e63377f51cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 KB (12193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd1ff0b19ae0f0339dfa452087f6e62d3885ac4cd6d87c8b93b3893fa44b0b6`

```dockerfile
```

-	Layers:
	-	`sha256:24ccf6b7ae0e49578be9c4155a809a71d3e4b9c5486ce7c4086d68e3d1acd22f`  
		Last Modified: Fri, 19 Jan 2024 00:32:31 GMT  
		Size: 4.8 KB (4800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53a196fbf5767399864392abcd4b090e16c2f74821ac8b44d3f139986875dae`  
		Last Modified: Fri, 19 Jan 2024 00:32:31 GMT  
		Size: 7.4 KB (7393 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36.1-glibc` - linux; 386

```console
$ docker pull busybox@sha256:99eabec0f153fb38feb80682492123326c994a6857f7ef9b73d46eecd8b81684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2268883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a422f55b78a61a0acf17d1ad4cea56c7542f1a09e6a256def15b8787d41ad7a`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:b6f95b873e20279fb8550d2d0b30bff9e72de3fe85f2ff4cfbf5f8f8aa6dabf4`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 2.3 MB (2268883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:deb0f17418ba410fceb230e48f01a2056732cba642d66a812901fa3d039c7e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 KB (12043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e79a31fa88e6a7c031f212bf2849dfb712003711e72dcae4abf34405846cdcf`

```dockerfile
```

-	Layers:
	-	`sha256:347076177c54f21c7c7fd98a9a45a717898d8441f14a94c5248a682a00008516`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 4.7 KB (4725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcf8fff8866352521d3aef70307e34f73f9951524290a8b4b36ffb75b6e6c138`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 7.3 KB (7318 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36.1-glibc` - linux; mips64le

```console
$ docker pull busybox@sha256:8c4284fa9cc28d0b9455f84527de8b58d5d4df00abcd18e47f2f1dc4e89f7ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2077641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c67790aa14859c61c94e0b7e727a8c50a5e246783c252e080ae41187e8ec52`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:b9f2f1866e3467e8735b90ecad932b7c1f122f80426b5beda6fb8a4c87f45757`  
		Last Modified: Wed, 06 Mar 2024 00:08:46 GMT  
		Size: 2.1 MB (2077641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1-glibc` - linux; ppc64le

```console
$ docker pull busybox@sha256:4b36905f6e9385ec2234f41dbb9d67ccd99ee2b50ef225c08746b2276991bb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb40c4cff2a5d1551f5a9e79b6fac3cf2d655f702041d0ae8d670e027645bd9`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1e329ff3bf1d3bf69d13da2954652acf3457a6fbd276780a232bb5254c915148`  
		Last Modified: Fri, 19 Jan 2024 00:42:12 GMT  
		Size: 2.5 MB (2528609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:17110abebf0882f7e23b68ea936ab719a49047e1b4a8e0ab0118ff0abff0066d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 KB (12281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48490b9b70ffd6de2941a4f2dbecc81750fe06d0c527e787a94fff4504c7721`

```dockerfile
```

-	Layers:
	-	`sha256:07f1bfa21dee33589c5658c47aa84655e024d44ef684cbd102571f1fdaa89c48`  
		Last Modified: Fri, 19 Jan 2024 00:42:12 GMT  
		Size: 4.8 KB (4842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f2fcbb930547c7a7fa4783062b75854e39e225a8dc9dbf51df1bcb5b2580c4`  
		Last Modified: Fri, 19 Jan 2024 00:42:11 GMT  
		Size: 7.4 KB (7439 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36.1-glibc` - linux; s390x

```console
$ docker pull busybox@sha256:df5506ae24620e67cb668f0137869babd6305cf4912190ee7de781c412b9bad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1926831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a46af96236bcedbc5591856e442999857d24fd51f5ff2135ede6486c79e2e7`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:230db3ea6af07ccf4b5f3ad6164f90d07967b83607909a587631245cc7c84ef4`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 1.9 MB (1926831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:b2a97dca77d5ae1e0ddef0cbfba271b5f0597c9ea7b8cb8127b397c7c9d03dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 KB (12149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e23940337a50804f81942abe24849f22423565ad3dabdfeefa3ee5cc61fd96`

```dockerfile
```

-	Layers:
	-	`sha256:5f4fdc6f7194500531229dc2d7aa2b54119cdf908b5e842b6ae1bfbf57487b79`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 4.8 KB (4778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ad8320e0617081f2bb73e6289f33979e1ee192d12ef3459b3bfe278084c075c`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 7.4 KB (7371 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:1.36.1-musl`

```console
$ docker pull busybox@sha256:9a7f0d2407780a98013e227ddc43f87bf5fbe626fb59f98280efd591c75ccdec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `busybox:1.36.1-musl` - linux; amd64

```console
$ docker pull busybox@sha256:d4707523ce6e12afdbe9a3be5ad69027150a834870ca0933baf7516dd1fe0f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **878.7 KB (878681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59888ccc9e6510deabb10bb0452f184f40cec7064c0fc522a01924f66c7fdfd8`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8dfc70c9a1cfc61f5873aed748e446239a5cb27faddd51d118180665010c02b7`  
		Last Modified: Thu, 18 Jan 2024 23:03:35 GMT  
		Size: 878.7 KB (878681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:864e79c6eb0056047a68c6c717ee53d548519ee307dec471696a5e6d0fab0a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c89e5c4f095b960e7a950b75e8f1386f0c1d1d43c108818b9b3922c803c1f1d`

```dockerfile
```

-	Layers:
	-	`sha256:aa7db50a9fdf0d3338cc08bc515695143e4aaf3e3e4b276f5f6d6d3bba5cca05`  
		Last Modified: Thu, 18 Jan 2024 23:03:35 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce0dddc950954bfb91430621087a12e68a552255f8c49ff243c27b22fbc6280`  
		Last Modified: Thu, 18 Jan 2024 23:03:35 GMT  
		Size: 5.9 KB (5871 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36.1-musl` - linux; arm variant v6

```console
$ docker pull busybox@sha256:b64a6a9cff5d2916ce4e5ab52254faa487ae93d9028c157c10d444aa3b5b7e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.6 KB (987570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5059e5cce9929da538b30d11caea9231836d6b937083115b4058ae4649341b74`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd544bbcb8b286d4a58e2b02357bb516d089d281fc87ae2b375921b8d2389923`  
		Last Modified: Thu, 18 Jan 2024 23:58:56 GMT  
		Size: 987.6 KB (987570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:0c1556654c58755833235ba840bb04258b5cf8d3e1771be01a2c48e38c266c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e96145e5c30a04c819cb052df4fa049365de24673fc3afdc9d5305cc2999a8`

```dockerfile
```

-	Layers:
	-	`sha256:1bbd274efa1896b02a475d573d66e47cc60d67dfb2334eef4aefc1d23763fe11`  
		Last Modified: Thu, 18 Jan 2024 23:58:56 GMT  
		Size: 7.2 KB (7231 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36.1-musl` - linux; arm variant v7

```console
$ docker pull busybox@sha256:f2939eb0b529af5706172c10db02a0894949c461b81ed4282ff4df5bf18c14d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.6 KB (843648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855943b02ba3319e1345d803a557c4a88bfd0c18954db6869f2ac791e17c4ae3`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (musl), Alpine 3.19.1
```

-	Layers:
	-	`sha256:83dc776fdc81b19e8a0c134d8eecfc7793d00ca52c1cc4292e973750e3684712`  
		Last Modified: Wed, 06 Mar 2024 00:10:38 GMT  
		Size: 843.6 KB (843648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1-musl` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:fed6b26ea319254ef0d6bae87482b5ab58b85250a7cc46d14c533e1f5c2556db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.0 KB (920992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f13cdcd8df2876053fd8dc5d01363344a92ea4d6537bd78625b9209e988edf`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d997961b9429e6c49b53a709a914c6578f5ff5ba7166ee52de62d1ac94887c1e`  
		Last Modified: Fri, 19 Jan 2024 01:36:22 GMT  
		Size: 921.0 KB (920992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:1cbd2ff89d7ff09ec11e246f3a887f3a914ab78b5d7445c43487b8c6fbed88cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83f629b0163590a531f21a762bb0cbaa263d937678e8f68d96a31c90ef4a07b`

```dockerfile
```

-	Layers:
	-	`sha256:3c2685448006e438049a85838a6b8137f2e8454a9bc20b249241ff956b520505`  
		Last Modified: Fri, 19 Jan 2024 01:36:22 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6177450e2c462aaedbb8f947886eb918cc00046a7fdc55ccca512c51f9243ee4`  
		Last Modified: Fri, 19 Jan 2024 01:36:22 GMT  
		Size: 5.9 KB (5883 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36.1-musl` - linux; 386

```console
$ docker pull busybox@sha256:b6678a8456f13554d339f393c4bcf798b3730a4f1662f6d9842129cbeeb5c665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.5 KB (875482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e9971e1ff6c5b5940f3f82628fe182aead284575c0ae4a798ed91e15ef08d7`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:769db000cf23b44ad2664168ee3886ca8883b18f32581f08cd06ce00f41ff872`  
		Last Modified: Thu, 18 Jan 2024 23:03:39 GMT  
		Size: 875.5 KB (875482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:fcc65e203ef7a06b3c9852b25de034cc8472405e5d7f033e818752a15778a758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa92905283639dceabeee0502770622fc73c4856e769907a58b011d8c5ea776f`

```dockerfile
```

-	Layers:
	-	`sha256:9020223ee3ca8d6d37dab73b397baddf426d3d408db20f63d02b1e9d2faff9d6`  
		Last Modified: Thu, 18 Jan 2024 23:03:39 GMT  
		Size: 3.3 KB (3254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6eae553040cde89419e4a177c32658f1d867ec25cf9a30b7655184d189a9439`  
		Last Modified: Thu, 18 Jan 2024 23:03:39 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36.1-musl` - linux; ppc64le

```console
$ docker pull busybox@sha256:74dfdbf9d13a59af2f6aa61ad738fa1fdade6dfd0d6f687eb3b0d53ffc8b5623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **967.1 KB (967138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f646f514a9f9bafe5483609c8bb0c3c64f9628f35d9beffda459a7fc992d9fe0`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:e4d8791bb918bc69b870f21a553724ec9b2812219040885317ce57b6eb4e6ab3`  
		Last Modified: Fri, 19 Jan 2024 01:03:30 GMT  
		Size: 967.1 KB (967138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:832836469bae4830469c6b70aa0ca4cf84181eb2a11484479ea37d6ce6143846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376ae5066f35abd2be10b0eacfecd79b91086e268f707d436e7b8798c411fcf9`

```dockerfile
```

-	Layers:
	-	`sha256:1ecc1159b446640a86f9969f010bbc8178567a5b46e779b2ce340b9229dac07e`  
		Last Modified: Fri, 19 Jan 2024 01:03:30 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a8411155c9d98fe9609d4ca6e64859296085c39baa2e804ebae951ab5b80b8`  
		Last Modified: Fri, 19 Jan 2024 01:03:30 GMT  
		Size: 5.9 KB (5909 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36.1-musl` - linux; s390x

```console
$ docker pull busybox@sha256:e7e0969b47c05409c0fa5c909e006a620f845d5b119869c8346e4f3cb93f8c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **940.3 KB (940326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774f60d2b6d3daa542d524858ddb90ae71c4b3cc014a0235132a36c51e1d4515`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:48e10ecef46b18109935c897c4fb6ba3b06fea3fc7b54588e2aef37a9ecc7db9`  
		Last Modified: Sat, 20 Jan 2024 17:54:57 GMT  
		Size: 940.3 KB (940326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:6ac7f239a3bffeaff764ae1948e58f80497ce3fe2d2bdfb42b7c9899ac58270e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2deb03e82c885a1c5de5b9ffc72f3b12beb43f880ffec52862abecf85ba22e4`

```dockerfile
```

-	Layers:
	-	`sha256:72517eef4c47c126a39ac1b293ba0bcfcb63a31962064a4a8bc3907115262d23`  
		Last Modified: Sat, 20 Jan 2024 17:54:57 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:990936cff923ba93c536c3d8f4ba7db950b54f638d8ca2d0b278ed1e0110f3b9`  
		Last Modified: Sat, 20 Jan 2024 17:54:57 GMT  
		Size: 5.9 KB (5871 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:1.36.1-uclibc`

```console
$ docker pull busybox@sha256:61651f1730187bbbfaa01e81d31eb082a1853a14118255c7dff5f1365d0ca3e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; riscv64
	-	unknown; unknown

### `busybox:1.36.1-uclibc` - linux; amd64

```console
$ docker pull busybox@sha256:21de0dff31b277e0d37fe21f6e89e461f5c07415719d225235121c144287dc17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **783.2 KB (783164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e537aeebf5260fe6cb054017b3af5862945ab73f5a7091cd6e2127cdfdd5a14`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cff2761077a7b33f0ac06f806d159087b8c79413afc45167a232c5b9394615f1`  
		Last Modified: Thu, 18 Jan 2024 23:03:48 GMT  
		Size: 783.2 KB (783164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:385fe86cbfdf640c4538befe889e1e9bf93fa21eeb9955f7ea076e6d874a2d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7796465a33cc98caddbb8bc190b367eaeb431320484f406887f0d1c8578327c`

```dockerfile
```

-	Layers:
	-	`sha256:165aad5817a1de48ec8d7d517f5332a81840adf0cc4836a6c3f4aad1ac31e128`  
		Last Modified: Thu, 18 Jan 2024 23:03:51 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f647335cce5641a56b28c17896a32f125e7d6823621a542398ee88b0754d863`  
		Last Modified: Thu, 18 Jan 2024 23:03:48 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36.1-uclibc` - linux; arm variant v5

```console
$ docker pull busybox@sha256:2e2d13aea845763e5152bb8116738d5179f67b79fc6fde83bf813896829d4bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.2 KB (744233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be06eb6ec3aaf1ca11f443876561f4e75e1dd0ceb407c1880033d7ff6328b3e`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (uclibc), Buildroot 2023.11.1, Debian 12
```

-	Layers:
	-	`sha256:120231968b7db68bb2d25cd765a3eee8fe0ec5be354a4306354fdd9606bd7774`  
		Last Modified: Wed, 06 Mar 2024 00:08:00 GMT  
		Size: 744.2 KB (744233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1-uclibc` - linux; arm variant v7

```console
$ docker pull busybox@sha256:b87edd76d8d0b9e848a0059a3014d87dabf763bc6cfcb9df52d13f4523a3d371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.9 KB (708929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2858fb01eb20e8b8f27c5d3108e9df3065a5c3196a170111aabbf09b81d4bf9`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (uclibc), Buildroot 2023.11.1, Debian 12
```

-	Layers:
	-	`sha256:19210f7552436b95fa7de660fcbf9e9425a0813bfccb850b3fcd053709caf443`  
		Last Modified: Wed, 06 Mar 2024 00:10:24 GMT  
		Size: 708.9 KB (708929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1-uclibc` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:b8879bdf897086348b8048b0a5ae3d85addc583ed20050328ec7146858e847e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **836.8 KB (836843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80467bacead9d1b091a5648f067f735716b201eba3fd71a4fb44e13f5341f0cd`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cea42dbd04d75d2786e9fef4399413709452debd69b417e4c200743b4b844c00`  
		Last Modified: Fri, 19 Jan 2024 00:57:12 GMT  
		Size: 836.8 KB (836843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:d872e2c2932c6bd7821197d583a23869fdb68bf056a7d7dac8a97e20e62bd6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a42e696a19934cb4621a011849c38a5b99a99a7db2a5f5914af4bd5c886b3f4`

```dockerfile
```

-	Layers:
	-	`sha256:4f836af667398f1a6feb5e25980960f902daf9096ca799ab436dba129c2c8698`  
		Last Modified: Fri, 19 Jan 2024 00:57:11 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:880e28375df06f638d5045451a8dda0fc51cc28429dba1387275de009fd5d3b3`  
		Last Modified: Fri, 19 Jan 2024 00:57:11 GMT  
		Size: 5.9 KB (5909 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36.1-uclibc` - linux; 386

```console
$ docker pull busybox@sha256:b805bdb43c275243e31c549abcc71d98c1323a225598b74e5a9b9dc91fdf4073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **747.9 KB (747949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992d7e8ad26e67c26250373ac39142b725403b68173a52edacc7c191cf5f097a`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d6a6d95c0da603317dbc3d49423910ecb730bb5d4219de536cfd7120bd1d792e`  
		Last Modified: Thu, 18 Jan 2024 23:03:27 GMT  
		Size: 747.9 KB (747949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:3cb35ce2ebff606afe19b8965ea3f0fe093bbbfc9fabc67a3158c7f4cd146068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c6ca91c6552ef25e52903cad76d996d7b60375a160b4205a35c7b060549a35`

```dockerfile
```

-	Layers:
	-	`sha256:cd8b24a6892d4af4db2582c4db92db552c251baa708fd3d249742144a1f06c65`  
		Last Modified: Thu, 18 Jan 2024 23:03:27 GMT  
		Size: 3.3 KB (3274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3117b42969c2d3cfbd84681cccff735d766b482184839bd402d14f12180792ad`  
		Last Modified: Thu, 18 Jan 2024 23:03:27 GMT  
		Size: 5.9 KB (5868 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:1.36.1-uclibc` - linux; mips64le

```console
$ docker pull busybox@sha256:388eed10bf5614e88ae1e2b2c1d237cbef877a07858125415556e3d9edff526d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **948.9 KB (948864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd60f88674723ffdec05a32d2bee1157f95e335ced9c3efea5686b9b15cd1416`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (uclibc), Buildroot 2023.11.1, Debian 12
```

-	Layers:
	-	`sha256:16b2225af5a2181079c894731b1031c046d90aca99349dd3487cfc6d6702d0e3`  
		Last Modified: Wed, 06 Mar 2024 00:09:07 GMT  
		Size: 948.9 KB (948864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1-uclibc` - linux; riscv64

```console
$ docker pull busybox@sha256:41af629cfa908c7ed7550db6a260c79d6dd55fe4996d7481595e3d547ab829c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.3 KB (914275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9673ad33efcd24dfd28f0415f23ee1c42d743140691e10781669692ef3af1ba6`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:917dbba7e6e14feb5914ca2711ff13b50b1f9a2b0b8315b79bbceabde34d11c2`  
		Last Modified: Thu, 18 Jan 2024 23:05:50 GMT  
		Size: 914.3 KB (914275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:1.36.1-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:126af02605028b8076a4a47fe1c707c795ce58c66a266c67b447519ebf1f3b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 KB (12303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa149c79ad9040800185662b3a226758c08cd6d612ca2a1abf6ebf0d9716f32`

```dockerfile
```

-	Layers:
	-	`sha256:1acfa35c63c5a80ca903c34528318a0b6b614a7060738be73b2b8424004473b1`  
		Last Modified: Thu, 18 Jan 2024 23:05:50 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97288386ab763b23aa899ebcfaa85d4b1708c86df318569f03865c7fb2b7ad4f`  
		Last Modified: Thu, 18 Jan 2024 23:05:51 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:glibc`

```console
$ docker pull busybox@sha256:eba7ad4cfa554dd96910090a41fa8eee6d4231f92bf5587dbd05a4badfeec2cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `busybox:glibc` - linux; amd64

```console
$ docker pull busybox@sha256:538721340ded10875f4710cad688c70e5d0ecb4dcd5e7d0c161f301f36f79414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2220094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f57d9401f8d42f986df300f0c69192fc41da28ccc8d797829467780db3dd741`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9ad63333ebc97e32b987ae66aa3cff81300e4c2e6d2f2395cef8a3ae18b249fe`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 2.2 MB (2220094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:253eb45864243efd740aa87ba169151e4d165538b168d77284396469217ee5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 KB (12149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9095a17baa618e6b1b5b3da6493f78682688b3c18f07a524e30bd47a404d4cb`

```dockerfile
```

-	Layers:
	-	`sha256:e1104929ee0cb0e8ea3d2c3b4024ce9f852364d233aabe800ea7789df99cfc23`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 4.8 KB (4778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d186640ac3f58c681ac3bc3aa314992df65409336eccb7e94bd7c4b8174a2b`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 7.4 KB (7371 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:glibc` - linux; arm variant v5

```console
$ docker pull busybox@sha256:491e28080f41a345b794a1528e23525f67f8693d8c541b9ef8f4990f6af501f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1776853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6578b94d614adfa46696754ab33bdd8b8b70ac8adea2fb6061d90e2b01f90e3`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:e209cc4af23c3ed4ac3e8cf58f8e9ea90d51fe28fcfca3ad91d91e74aabca274`  
		Last Modified: Wed, 06 Mar 2024 00:07:47 GMT  
		Size: 1.8 MB (1776853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:glibc` - linux; arm variant v7

```console
$ docker pull busybox@sha256:8a4415fb43600953cbdac6ec03c2d96d900bb21f8d78964837dad7f73b9afcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1554425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9903cc888814e8feef24381cdb6d29d8598385dcb109a9908a4a98e1ab021532`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:a7cbd68a76a020b8b283c940bc267cd88a66013dcb160cad746344483dfc4b52`  
		Last Modified: Wed, 06 Mar 2024 00:10:11 GMT  
		Size: 1.6 MB (1554425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:glibc` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:8f03917912ea995c637b6c0295846aaff5665f06ac82a29b421fba4c379494e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1916607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4fd538a9a0b729be05707cf805388be2fb701cfd5d44c6542f1988e8aef6e3`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c2bf9493c1bf786e95e3eac7d406c20aa1b8a2d40916756e891627e9e8f8d119`  
		Last Modified: Fri, 19 Jan 2024 00:32:32 GMT  
		Size: 1.9 MB (1916607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:a69e011a60760aba5dd1209f91c05980c6fab54d8b25ae169291e63377f51cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 KB (12193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd1ff0b19ae0f0339dfa452087f6e62d3885ac4cd6d87c8b93b3893fa44b0b6`

```dockerfile
```

-	Layers:
	-	`sha256:24ccf6b7ae0e49578be9c4155a809a71d3e4b9c5486ce7c4086d68e3d1acd22f`  
		Last Modified: Fri, 19 Jan 2024 00:32:31 GMT  
		Size: 4.8 KB (4800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53a196fbf5767399864392abcd4b090e16c2f74821ac8b44d3f139986875dae`  
		Last Modified: Fri, 19 Jan 2024 00:32:31 GMT  
		Size: 7.4 KB (7393 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:glibc` - linux; 386

```console
$ docker pull busybox@sha256:99eabec0f153fb38feb80682492123326c994a6857f7ef9b73d46eecd8b81684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2268883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a422f55b78a61a0acf17d1ad4cea56c7542f1a09e6a256def15b8787d41ad7a`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:b6f95b873e20279fb8550d2d0b30bff9e72de3fe85f2ff4cfbf5f8f8aa6dabf4`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 2.3 MB (2268883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:deb0f17418ba410fceb230e48f01a2056732cba642d66a812901fa3d039c7e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 KB (12043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e79a31fa88e6a7c031f212bf2849dfb712003711e72dcae4abf34405846cdcf`

```dockerfile
```

-	Layers:
	-	`sha256:347076177c54f21c7c7fd98a9a45a717898d8441f14a94c5248a682a00008516`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 4.7 KB (4725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcf8fff8866352521d3aef70307e34f73f9951524290a8b4b36ffb75b6e6c138`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 7.3 KB (7318 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:glibc` - linux; mips64le

```console
$ docker pull busybox@sha256:8c4284fa9cc28d0b9455f84527de8b58d5d4df00abcd18e47f2f1dc4e89f7ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2077641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c67790aa14859c61c94e0b7e727a8c50a5e246783c252e080ae41187e8ec52`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:b9f2f1866e3467e8735b90ecad932b7c1f122f80426b5beda6fb8a4c87f45757`  
		Last Modified: Wed, 06 Mar 2024 00:08:46 GMT  
		Size: 2.1 MB (2077641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:glibc` - linux; ppc64le

```console
$ docker pull busybox@sha256:4b36905f6e9385ec2234f41dbb9d67ccd99ee2b50ef225c08746b2276991bb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb40c4cff2a5d1551f5a9e79b6fac3cf2d655f702041d0ae8d670e027645bd9`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1e329ff3bf1d3bf69d13da2954652acf3457a6fbd276780a232bb5254c915148`  
		Last Modified: Fri, 19 Jan 2024 00:42:12 GMT  
		Size: 2.5 MB (2528609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:17110abebf0882f7e23b68ea936ab719a49047e1b4a8e0ab0118ff0abff0066d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 KB (12281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48490b9b70ffd6de2941a4f2dbecc81750fe06d0c527e787a94fff4504c7721`

```dockerfile
```

-	Layers:
	-	`sha256:07f1bfa21dee33589c5658c47aa84655e024d44ef684cbd102571f1fdaa89c48`  
		Last Modified: Fri, 19 Jan 2024 00:42:12 GMT  
		Size: 4.8 KB (4842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f2fcbb930547c7a7fa4783062b75854e39e225a8dc9dbf51df1bcb5b2580c4`  
		Last Modified: Fri, 19 Jan 2024 00:42:11 GMT  
		Size: 7.4 KB (7439 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:glibc` - linux; s390x

```console
$ docker pull busybox@sha256:df5506ae24620e67cb668f0137869babd6305cf4912190ee7de781c412b9bad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1926831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a46af96236bcedbc5591856e442999857d24fd51f5ff2135ede6486c79e2e7`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:230db3ea6af07ccf4b5f3ad6164f90d07967b83607909a587631245cc7c84ef4`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 1.9 MB (1926831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:b2a97dca77d5ae1e0ddef0cbfba271b5f0597c9ea7b8cb8127b397c7c9d03dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 KB (12149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e23940337a50804f81942abe24849f22423565ad3dabdfeefa3ee5cc61fd96`

```dockerfile
```

-	Layers:
	-	`sha256:5f4fdc6f7194500531229dc2d7aa2b54119cdf908b5e842b6ae1bfbf57487b79`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 4.8 KB (4778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ad8320e0617081f2bb73e6289f33979e1ee192d12ef3459b3bfe278084c075c`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 7.4 KB (7371 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:latest`

```console
$ docker pull busybox@sha256:acdc29f25f9c5d678b264007f6f0ea63f12756dcef1cdb043f3fd2a13ba735c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 17
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `busybox:latest` - linux; amd64

```console
$ docker pull busybox@sha256:538721340ded10875f4710cad688c70e5d0ecb4dcd5e7d0c161f301f36f79414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2220094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f57d9401f8d42f986df300f0c69192fc41da28ccc8d797829467780db3dd741`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9ad63333ebc97e32b987ae66aa3cff81300e4c2e6d2f2395cef8a3ae18b249fe`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 2.2 MB (2220094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:latest` - unknown; unknown

```console
$ docker pull busybox@sha256:253eb45864243efd740aa87ba169151e4d165538b168d77284396469217ee5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 KB (12149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9095a17baa618e6b1b5b3da6493f78682688b3c18f07a524e30bd47a404d4cb`

```dockerfile
```

-	Layers:
	-	`sha256:e1104929ee0cb0e8ea3d2c3b4024ce9f852364d233aabe800ea7789df99cfc23`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 4.8 KB (4778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d186640ac3f58c681ac3bc3aa314992df65409336eccb7e94bd7c4b8174a2b`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 7.4 KB (7371 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:latest` - linux; arm variant v5

```console
$ docker pull busybox@sha256:491e28080f41a345b794a1528e23525f67f8693d8c541b9ef8f4990f6af501f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1776853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6578b94d614adfa46696754ab33bdd8b8b70ac8adea2fb6061d90e2b01f90e3`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:e209cc4af23c3ed4ac3e8cf58f8e9ea90d51fe28fcfca3ad91d91e74aabca274`  
		Last Modified: Wed, 06 Mar 2024 00:07:47 GMT  
		Size: 1.8 MB (1776853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:latest` - linux; arm variant v6

```console
$ docker pull busybox@sha256:b64a6a9cff5d2916ce4e5ab52254faa487ae93d9028c157c10d444aa3b5b7e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.6 KB (987570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5059e5cce9929da538b30d11caea9231836d6b937083115b4058ae4649341b74`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd544bbcb8b286d4a58e2b02357bb516d089d281fc87ae2b375921b8d2389923`  
		Last Modified: Thu, 18 Jan 2024 23:58:56 GMT  
		Size: 987.6 KB (987570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:latest` - unknown; unknown

```console
$ docker pull busybox@sha256:0c1556654c58755833235ba840bb04258b5cf8d3e1771be01a2c48e38c266c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e96145e5c30a04c819cb052df4fa049365de24673fc3afdc9d5305cc2999a8`

```dockerfile
```

-	Layers:
	-	`sha256:1bbd274efa1896b02a475d573d66e47cc60d67dfb2334eef4aefc1d23763fe11`  
		Last Modified: Thu, 18 Jan 2024 23:58:56 GMT  
		Size: 7.2 KB (7231 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:latest` - linux; arm variant v7

```console
$ docker pull busybox@sha256:8a4415fb43600953cbdac6ec03c2d96d900bb21f8d78964837dad7f73b9afcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1554425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9903cc888814e8feef24381cdb6d29d8598385dcb109a9908a4a98e1ab021532`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:a7cbd68a76a020b8b283c940bc267cd88a66013dcb160cad746344483dfc4b52`  
		Last Modified: Wed, 06 Mar 2024 00:10:11 GMT  
		Size: 1.6 MB (1554425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:latest` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:8f03917912ea995c637b6c0295846aaff5665f06ac82a29b421fba4c379494e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1916607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4fd538a9a0b729be05707cf805388be2fb701cfd5d44c6542f1988e8aef6e3`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c2bf9493c1bf786e95e3eac7d406c20aa1b8a2d40916756e891627e9e8f8d119`  
		Last Modified: Fri, 19 Jan 2024 00:32:32 GMT  
		Size: 1.9 MB (1916607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:latest` - unknown; unknown

```console
$ docker pull busybox@sha256:a69e011a60760aba5dd1209f91c05980c6fab54d8b25ae169291e63377f51cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 KB (12193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd1ff0b19ae0f0339dfa452087f6e62d3885ac4cd6d87c8b93b3893fa44b0b6`

```dockerfile
```

-	Layers:
	-	`sha256:24ccf6b7ae0e49578be9c4155a809a71d3e4b9c5486ce7c4086d68e3d1acd22f`  
		Last Modified: Fri, 19 Jan 2024 00:32:31 GMT  
		Size: 4.8 KB (4800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53a196fbf5767399864392abcd4b090e16c2f74821ac8b44d3f139986875dae`  
		Last Modified: Fri, 19 Jan 2024 00:32:31 GMT  
		Size: 7.4 KB (7393 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:latest` - linux; 386

```console
$ docker pull busybox@sha256:99eabec0f153fb38feb80682492123326c994a6857f7ef9b73d46eecd8b81684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2268883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a422f55b78a61a0acf17d1ad4cea56c7542f1a09e6a256def15b8787d41ad7a`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:b6f95b873e20279fb8550d2d0b30bff9e72de3fe85f2ff4cfbf5f8f8aa6dabf4`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 2.3 MB (2268883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:latest` - unknown; unknown

```console
$ docker pull busybox@sha256:deb0f17418ba410fceb230e48f01a2056732cba642d66a812901fa3d039c7e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 KB (12043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e79a31fa88e6a7c031f212bf2849dfb712003711e72dcae4abf34405846cdcf`

```dockerfile
```

-	Layers:
	-	`sha256:347076177c54f21c7c7fd98a9a45a717898d8441f14a94c5248a682a00008516`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 4.7 KB (4725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcf8fff8866352521d3aef70307e34f73f9951524290a8b4b36ffb75b6e6c138`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 7.3 KB (7318 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:latest` - linux; mips64le

```console
$ docker pull busybox@sha256:8c4284fa9cc28d0b9455f84527de8b58d5d4df00abcd18e47f2f1dc4e89f7ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2077641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c67790aa14859c61c94e0b7e727a8c50a5e246783c252e080ae41187e8ec52`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:b9f2f1866e3467e8735b90ecad932b7c1f122f80426b5beda6fb8a4c87f45757`  
		Last Modified: Wed, 06 Mar 2024 00:08:46 GMT  
		Size: 2.1 MB (2077641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:latest` - linux; ppc64le

```console
$ docker pull busybox@sha256:4b36905f6e9385ec2234f41dbb9d67ccd99ee2b50ef225c08746b2276991bb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb40c4cff2a5d1551f5a9e79b6fac3cf2d655f702041d0ae8d670e027645bd9`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1e329ff3bf1d3bf69d13da2954652acf3457a6fbd276780a232bb5254c915148`  
		Last Modified: Fri, 19 Jan 2024 00:42:12 GMT  
		Size: 2.5 MB (2528609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:latest` - unknown; unknown

```console
$ docker pull busybox@sha256:17110abebf0882f7e23b68ea936ab719a49047e1b4a8e0ab0118ff0abff0066d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 KB (12281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48490b9b70ffd6de2941a4f2dbecc81750fe06d0c527e787a94fff4504c7721`

```dockerfile
```

-	Layers:
	-	`sha256:07f1bfa21dee33589c5658c47aa84655e024d44ef684cbd102571f1fdaa89c48`  
		Last Modified: Fri, 19 Jan 2024 00:42:12 GMT  
		Size: 4.8 KB (4842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f2fcbb930547c7a7fa4783062b75854e39e225a8dc9dbf51df1bcb5b2580c4`  
		Last Modified: Fri, 19 Jan 2024 00:42:11 GMT  
		Size: 7.4 KB (7439 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:latest` - linux; riscv64

```console
$ docker pull busybox@sha256:41af629cfa908c7ed7550db6a260c79d6dd55fe4996d7481595e3d547ab829c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.3 KB (914275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9673ad33efcd24dfd28f0415f23ee1c42d743140691e10781669692ef3af1ba6`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:917dbba7e6e14feb5914ca2711ff13b50b1f9a2b0b8315b79bbceabde34d11c2`  
		Last Modified: Thu, 18 Jan 2024 23:05:50 GMT  
		Size: 914.3 KB (914275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:latest` - unknown; unknown

```console
$ docker pull busybox@sha256:126af02605028b8076a4a47fe1c707c795ce58c66a266c67b447519ebf1f3b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 KB (12303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa149c79ad9040800185662b3a226758c08cd6d612ca2a1abf6ebf0d9716f32`

```dockerfile
```

-	Layers:
	-	`sha256:1acfa35c63c5a80ca903c34528318a0b6b614a7060738be73b2b8424004473b1`  
		Last Modified: Thu, 18 Jan 2024 23:05:50 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97288386ab763b23aa899ebcfaa85d4b1708c86df318569f03865c7fb2b7ad4f`  
		Last Modified: Thu, 18 Jan 2024 23:05:51 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:latest` - linux; s390x

```console
$ docker pull busybox@sha256:df5506ae24620e67cb668f0137869babd6305cf4912190ee7de781c412b9bad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1926831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a46af96236bcedbc5591856e442999857d24fd51f5ff2135ede6486c79e2e7`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:230db3ea6af07ccf4b5f3ad6164f90d07967b83607909a587631245cc7c84ef4`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 1.9 MB (1926831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:latest` - unknown; unknown

```console
$ docker pull busybox@sha256:b2a97dca77d5ae1e0ddef0cbfba271b5f0597c9ea7b8cb8127b397c7c9d03dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 KB (12149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e23940337a50804f81942abe24849f22423565ad3dabdfeefa3ee5cc61fd96`

```dockerfile
```

-	Layers:
	-	`sha256:5f4fdc6f7194500531229dc2d7aa2b54119cdf908b5e842b6ae1bfbf57487b79`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 4.8 KB (4778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ad8320e0617081f2bb73e6289f33979e1ee192d12ef3459b3bfe278084c075c`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 7.4 KB (7371 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:musl`

```console
$ docker pull busybox@sha256:9a7f0d2407780a98013e227ddc43f87bf5fbe626fb59f98280efd591c75ccdec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `busybox:musl` - linux; amd64

```console
$ docker pull busybox@sha256:d4707523ce6e12afdbe9a3be5ad69027150a834870ca0933baf7516dd1fe0f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **878.7 KB (878681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59888ccc9e6510deabb10bb0452f184f40cec7064c0fc522a01924f66c7fdfd8`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8dfc70c9a1cfc61f5873aed748e446239a5cb27faddd51d118180665010c02b7`  
		Last Modified: Thu, 18 Jan 2024 23:03:35 GMT  
		Size: 878.7 KB (878681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:musl` - unknown; unknown

```console
$ docker pull busybox@sha256:864e79c6eb0056047a68c6c717ee53d548519ee307dec471696a5e6d0fab0a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c89e5c4f095b960e7a950b75e8f1386f0c1d1d43c108818b9b3922c803c1f1d`

```dockerfile
```

-	Layers:
	-	`sha256:aa7db50a9fdf0d3338cc08bc515695143e4aaf3e3e4b276f5f6d6d3bba5cca05`  
		Last Modified: Thu, 18 Jan 2024 23:03:35 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce0dddc950954bfb91430621087a12e68a552255f8c49ff243c27b22fbc6280`  
		Last Modified: Thu, 18 Jan 2024 23:03:35 GMT  
		Size: 5.9 KB (5871 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:musl` - linux; arm variant v6

```console
$ docker pull busybox@sha256:b64a6a9cff5d2916ce4e5ab52254faa487ae93d9028c157c10d444aa3b5b7e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.6 KB (987570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5059e5cce9929da538b30d11caea9231836d6b937083115b4058ae4649341b74`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd544bbcb8b286d4a58e2b02357bb516d089d281fc87ae2b375921b8d2389923`  
		Last Modified: Thu, 18 Jan 2024 23:58:56 GMT  
		Size: 987.6 KB (987570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:musl` - unknown; unknown

```console
$ docker pull busybox@sha256:0c1556654c58755833235ba840bb04258b5cf8d3e1771be01a2c48e38c266c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e96145e5c30a04c819cb052df4fa049365de24673fc3afdc9d5305cc2999a8`

```dockerfile
```

-	Layers:
	-	`sha256:1bbd274efa1896b02a475d573d66e47cc60d67dfb2334eef4aefc1d23763fe11`  
		Last Modified: Thu, 18 Jan 2024 23:58:56 GMT  
		Size: 7.2 KB (7231 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:musl` - linux; arm variant v7

```console
$ docker pull busybox@sha256:f2939eb0b529af5706172c10db02a0894949c461b81ed4282ff4df5bf18c14d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.6 KB (843648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855943b02ba3319e1345d803a557c4a88bfd0c18954db6869f2ac791e17c4ae3`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (musl), Alpine 3.19.1
```

-	Layers:
	-	`sha256:83dc776fdc81b19e8a0c134d8eecfc7793d00ca52c1cc4292e973750e3684712`  
		Last Modified: Wed, 06 Mar 2024 00:10:38 GMT  
		Size: 843.6 KB (843648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:musl` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:fed6b26ea319254ef0d6bae87482b5ab58b85250a7cc46d14c533e1f5c2556db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.0 KB (920992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f13cdcd8df2876053fd8dc5d01363344a92ea4d6537bd78625b9209e988edf`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d997961b9429e6c49b53a709a914c6578f5ff5ba7166ee52de62d1ac94887c1e`  
		Last Modified: Fri, 19 Jan 2024 01:36:22 GMT  
		Size: 921.0 KB (920992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:musl` - unknown; unknown

```console
$ docker pull busybox@sha256:1cbd2ff89d7ff09ec11e246f3a887f3a914ab78b5d7445c43487b8c6fbed88cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83f629b0163590a531f21a762bb0cbaa263d937678e8f68d96a31c90ef4a07b`

```dockerfile
```

-	Layers:
	-	`sha256:3c2685448006e438049a85838a6b8137f2e8454a9bc20b249241ff956b520505`  
		Last Modified: Fri, 19 Jan 2024 01:36:22 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6177450e2c462aaedbb8f947886eb918cc00046a7fdc55ccca512c51f9243ee4`  
		Last Modified: Fri, 19 Jan 2024 01:36:22 GMT  
		Size: 5.9 KB (5883 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:musl` - linux; 386

```console
$ docker pull busybox@sha256:b6678a8456f13554d339f393c4bcf798b3730a4f1662f6d9842129cbeeb5c665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.5 KB (875482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e9971e1ff6c5b5940f3f82628fe182aead284575c0ae4a798ed91e15ef08d7`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:769db000cf23b44ad2664168ee3886ca8883b18f32581f08cd06ce00f41ff872`  
		Last Modified: Thu, 18 Jan 2024 23:03:39 GMT  
		Size: 875.5 KB (875482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:musl` - unknown; unknown

```console
$ docker pull busybox@sha256:fcc65e203ef7a06b3c9852b25de034cc8472405e5d7f033e818752a15778a758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa92905283639dceabeee0502770622fc73c4856e769907a58b011d8c5ea776f`

```dockerfile
```

-	Layers:
	-	`sha256:9020223ee3ca8d6d37dab73b397baddf426d3d408db20f63d02b1e9d2faff9d6`  
		Last Modified: Thu, 18 Jan 2024 23:03:39 GMT  
		Size: 3.3 KB (3254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6eae553040cde89419e4a177c32658f1d867ec25cf9a30b7655184d189a9439`  
		Last Modified: Thu, 18 Jan 2024 23:03:39 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:musl` - linux; ppc64le

```console
$ docker pull busybox@sha256:74dfdbf9d13a59af2f6aa61ad738fa1fdade6dfd0d6f687eb3b0d53ffc8b5623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **967.1 KB (967138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f646f514a9f9bafe5483609c8bb0c3c64f9628f35d9beffda459a7fc992d9fe0`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:e4d8791bb918bc69b870f21a553724ec9b2812219040885317ce57b6eb4e6ab3`  
		Last Modified: Fri, 19 Jan 2024 01:03:30 GMT  
		Size: 967.1 KB (967138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:musl` - unknown; unknown

```console
$ docker pull busybox@sha256:832836469bae4830469c6b70aa0ca4cf84181eb2a11484479ea37d6ce6143846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376ae5066f35abd2be10b0eacfecd79b91086e268f707d436e7b8798c411fcf9`

```dockerfile
```

-	Layers:
	-	`sha256:1ecc1159b446640a86f9969f010bbc8178567a5b46e779b2ce340b9229dac07e`  
		Last Modified: Fri, 19 Jan 2024 01:03:30 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a8411155c9d98fe9609d4ca6e64859296085c39baa2e804ebae951ab5b80b8`  
		Last Modified: Fri, 19 Jan 2024 01:03:30 GMT  
		Size: 5.9 KB (5909 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:musl` - linux; s390x

```console
$ docker pull busybox@sha256:e7e0969b47c05409c0fa5c909e006a620f845d5b119869c8346e4f3cb93f8c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **940.3 KB (940326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774f60d2b6d3daa542d524858ddb90ae71c4b3cc014a0235132a36c51e1d4515`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:48e10ecef46b18109935c897c4fb6ba3b06fea3fc7b54588e2aef37a9ecc7db9`  
		Last Modified: Sat, 20 Jan 2024 17:54:57 GMT  
		Size: 940.3 KB (940326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:musl` - unknown; unknown

```console
$ docker pull busybox@sha256:6ac7f239a3bffeaff764ae1948e58f80497ce3fe2d2bdfb42b7c9899ac58270e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2deb03e82c885a1c5de5b9ffc72f3b12beb43f880ffec52862abecf85ba22e4`

```dockerfile
```

-	Layers:
	-	`sha256:72517eef4c47c126a39ac1b293ba0bcfcb63a31962064a4a8bc3907115262d23`  
		Last Modified: Sat, 20 Jan 2024 17:54:57 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:990936cff923ba93c536c3d8f4ba7db950b54f638d8ca2d0b278ed1e0110f3b9`  
		Last Modified: Sat, 20 Jan 2024 17:54:57 GMT  
		Size: 5.9 KB (5871 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:stable`

```console
$ docker pull busybox@sha256:acdc29f25f9c5d678b264007f6f0ea63f12756dcef1cdb043f3fd2a13ba735c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 17
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `busybox:stable` - linux; amd64

```console
$ docker pull busybox@sha256:538721340ded10875f4710cad688c70e5d0ecb4dcd5e7d0c161f301f36f79414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2220094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f57d9401f8d42f986df300f0c69192fc41da28ccc8d797829467780db3dd741`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9ad63333ebc97e32b987ae66aa3cff81300e4c2e6d2f2395cef8a3ae18b249fe`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 2.2 MB (2220094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable` - unknown; unknown

```console
$ docker pull busybox@sha256:253eb45864243efd740aa87ba169151e4d165538b168d77284396469217ee5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 KB (12149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9095a17baa618e6b1b5b3da6493f78682688b3c18f07a524e30bd47a404d4cb`

```dockerfile
```

-	Layers:
	-	`sha256:e1104929ee0cb0e8ea3d2c3b4024ce9f852364d233aabe800ea7789df99cfc23`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 4.8 KB (4778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d186640ac3f58c681ac3bc3aa314992df65409336eccb7e94bd7c4b8174a2b`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 7.4 KB (7371 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:stable` - linux; arm variant v5

```console
$ docker pull busybox@sha256:491e28080f41a345b794a1528e23525f67f8693d8c541b9ef8f4990f6af501f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1776853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6578b94d614adfa46696754ab33bdd8b8b70ac8adea2fb6061d90e2b01f90e3`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:e209cc4af23c3ed4ac3e8cf58f8e9ea90d51fe28fcfca3ad91d91e74aabca274`  
		Last Modified: Wed, 06 Mar 2024 00:07:47 GMT  
		Size: 1.8 MB (1776853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable` - linux; arm variant v6

```console
$ docker pull busybox@sha256:b64a6a9cff5d2916ce4e5ab52254faa487ae93d9028c157c10d444aa3b5b7e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.6 KB (987570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5059e5cce9929da538b30d11caea9231836d6b937083115b4058ae4649341b74`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd544bbcb8b286d4a58e2b02357bb516d089d281fc87ae2b375921b8d2389923`  
		Last Modified: Thu, 18 Jan 2024 23:58:56 GMT  
		Size: 987.6 KB (987570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable` - unknown; unknown

```console
$ docker pull busybox@sha256:0c1556654c58755833235ba840bb04258b5cf8d3e1771be01a2c48e38c266c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e96145e5c30a04c819cb052df4fa049365de24673fc3afdc9d5305cc2999a8`

```dockerfile
```

-	Layers:
	-	`sha256:1bbd274efa1896b02a475d573d66e47cc60d67dfb2334eef4aefc1d23763fe11`  
		Last Modified: Thu, 18 Jan 2024 23:58:56 GMT  
		Size: 7.2 KB (7231 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:stable` - linux; arm variant v7

```console
$ docker pull busybox@sha256:8a4415fb43600953cbdac6ec03c2d96d900bb21f8d78964837dad7f73b9afcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1554425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9903cc888814e8feef24381cdb6d29d8598385dcb109a9908a4a98e1ab021532`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:a7cbd68a76a020b8b283c940bc267cd88a66013dcb160cad746344483dfc4b52`  
		Last Modified: Wed, 06 Mar 2024 00:10:11 GMT  
		Size: 1.6 MB (1554425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:8f03917912ea995c637b6c0295846aaff5665f06ac82a29b421fba4c379494e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1916607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4fd538a9a0b729be05707cf805388be2fb701cfd5d44c6542f1988e8aef6e3`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c2bf9493c1bf786e95e3eac7d406c20aa1b8a2d40916756e891627e9e8f8d119`  
		Last Modified: Fri, 19 Jan 2024 00:32:32 GMT  
		Size: 1.9 MB (1916607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable` - unknown; unknown

```console
$ docker pull busybox@sha256:a69e011a60760aba5dd1209f91c05980c6fab54d8b25ae169291e63377f51cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 KB (12193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd1ff0b19ae0f0339dfa452087f6e62d3885ac4cd6d87c8b93b3893fa44b0b6`

```dockerfile
```

-	Layers:
	-	`sha256:24ccf6b7ae0e49578be9c4155a809a71d3e4b9c5486ce7c4086d68e3d1acd22f`  
		Last Modified: Fri, 19 Jan 2024 00:32:31 GMT  
		Size: 4.8 KB (4800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53a196fbf5767399864392abcd4b090e16c2f74821ac8b44d3f139986875dae`  
		Last Modified: Fri, 19 Jan 2024 00:32:31 GMT  
		Size: 7.4 KB (7393 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:stable` - linux; 386

```console
$ docker pull busybox@sha256:99eabec0f153fb38feb80682492123326c994a6857f7ef9b73d46eecd8b81684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2268883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a422f55b78a61a0acf17d1ad4cea56c7542f1a09e6a256def15b8787d41ad7a`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:b6f95b873e20279fb8550d2d0b30bff9e72de3fe85f2ff4cfbf5f8f8aa6dabf4`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 2.3 MB (2268883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable` - unknown; unknown

```console
$ docker pull busybox@sha256:deb0f17418ba410fceb230e48f01a2056732cba642d66a812901fa3d039c7e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 KB (12043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e79a31fa88e6a7c031f212bf2849dfb712003711e72dcae4abf34405846cdcf`

```dockerfile
```

-	Layers:
	-	`sha256:347076177c54f21c7c7fd98a9a45a717898d8441f14a94c5248a682a00008516`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 4.7 KB (4725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcf8fff8866352521d3aef70307e34f73f9951524290a8b4b36ffb75b6e6c138`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 7.3 KB (7318 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:stable` - linux; mips64le

```console
$ docker pull busybox@sha256:8c4284fa9cc28d0b9455f84527de8b58d5d4df00abcd18e47f2f1dc4e89f7ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2077641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c67790aa14859c61c94e0b7e727a8c50a5e246783c252e080ae41187e8ec52`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:b9f2f1866e3467e8735b90ecad932b7c1f122f80426b5beda6fb8a4c87f45757`  
		Last Modified: Wed, 06 Mar 2024 00:08:46 GMT  
		Size: 2.1 MB (2077641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable` - linux; ppc64le

```console
$ docker pull busybox@sha256:4b36905f6e9385ec2234f41dbb9d67ccd99ee2b50ef225c08746b2276991bb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb40c4cff2a5d1551f5a9e79b6fac3cf2d655f702041d0ae8d670e027645bd9`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1e329ff3bf1d3bf69d13da2954652acf3457a6fbd276780a232bb5254c915148`  
		Last Modified: Fri, 19 Jan 2024 00:42:12 GMT  
		Size: 2.5 MB (2528609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable` - unknown; unknown

```console
$ docker pull busybox@sha256:17110abebf0882f7e23b68ea936ab719a49047e1b4a8e0ab0118ff0abff0066d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 KB (12281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48490b9b70ffd6de2941a4f2dbecc81750fe06d0c527e787a94fff4504c7721`

```dockerfile
```

-	Layers:
	-	`sha256:07f1bfa21dee33589c5658c47aa84655e024d44ef684cbd102571f1fdaa89c48`  
		Last Modified: Fri, 19 Jan 2024 00:42:12 GMT  
		Size: 4.8 KB (4842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f2fcbb930547c7a7fa4783062b75854e39e225a8dc9dbf51df1bcb5b2580c4`  
		Last Modified: Fri, 19 Jan 2024 00:42:11 GMT  
		Size: 7.4 KB (7439 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:stable` - linux; riscv64

```console
$ docker pull busybox@sha256:41af629cfa908c7ed7550db6a260c79d6dd55fe4996d7481595e3d547ab829c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.3 KB (914275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9673ad33efcd24dfd28f0415f23ee1c42d743140691e10781669692ef3af1ba6`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:917dbba7e6e14feb5914ca2711ff13b50b1f9a2b0b8315b79bbceabde34d11c2`  
		Last Modified: Thu, 18 Jan 2024 23:05:50 GMT  
		Size: 914.3 KB (914275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable` - unknown; unknown

```console
$ docker pull busybox@sha256:126af02605028b8076a4a47fe1c707c795ce58c66a266c67b447519ebf1f3b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 KB (12303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa149c79ad9040800185662b3a226758c08cd6d612ca2a1abf6ebf0d9716f32`

```dockerfile
```

-	Layers:
	-	`sha256:1acfa35c63c5a80ca903c34528318a0b6b614a7060738be73b2b8424004473b1`  
		Last Modified: Thu, 18 Jan 2024 23:05:50 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97288386ab763b23aa899ebcfaa85d4b1708c86df318569f03865c7fb2b7ad4f`  
		Last Modified: Thu, 18 Jan 2024 23:05:51 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:stable` - linux; s390x

```console
$ docker pull busybox@sha256:df5506ae24620e67cb668f0137869babd6305cf4912190ee7de781c412b9bad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1926831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a46af96236bcedbc5591856e442999857d24fd51f5ff2135ede6486c79e2e7`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:230db3ea6af07ccf4b5f3ad6164f90d07967b83607909a587631245cc7c84ef4`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 1.9 MB (1926831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable` - unknown; unknown

```console
$ docker pull busybox@sha256:b2a97dca77d5ae1e0ddef0cbfba271b5f0597c9ea7b8cb8127b397c7c9d03dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 KB (12149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e23940337a50804f81942abe24849f22423565ad3dabdfeefa3ee5cc61fd96`

```dockerfile
```

-	Layers:
	-	`sha256:5f4fdc6f7194500531229dc2d7aa2b54119cdf908b5e842b6ae1bfbf57487b79`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 4.8 KB (4778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ad8320e0617081f2bb73e6289f33979e1ee192d12ef3459b3bfe278084c075c`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 7.4 KB (7371 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:stable-glibc`

```console
$ docker pull busybox@sha256:eba7ad4cfa554dd96910090a41fa8eee6d4231f92bf5587dbd05a4badfeec2cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `busybox:stable-glibc` - linux; amd64

```console
$ docker pull busybox@sha256:538721340ded10875f4710cad688c70e5d0ecb4dcd5e7d0c161f301f36f79414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2220094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f57d9401f8d42f986df300f0c69192fc41da28ccc8d797829467780db3dd741`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9ad63333ebc97e32b987ae66aa3cff81300e4c2e6d2f2395cef8a3ae18b249fe`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 2.2 MB (2220094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:253eb45864243efd740aa87ba169151e4d165538b168d77284396469217ee5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 KB (12149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9095a17baa618e6b1b5b3da6493f78682688b3c18f07a524e30bd47a404d4cb`

```dockerfile
```

-	Layers:
	-	`sha256:e1104929ee0cb0e8ea3d2c3b4024ce9f852364d233aabe800ea7789df99cfc23`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 4.8 KB (4778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d186640ac3f58c681ac3bc3aa314992df65409336eccb7e94bd7c4b8174a2b`  
		Last Modified: Thu, 18 Jan 2024 23:03:21 GMT  
		Size: 7.4 KB (7371 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:stable-glibc` - linux; arm variant v5

```console
$ docker pull busybox@sha256:491e28080f41a345b794a1528e23525f67f8693d8c541b9ef8f4990f6af501f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1776853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6578b94d614adfa46696754ab33bdd8b8b70ac8adea2fb6061d90e2b01f90e3`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:e209cc4af23c3ed4ac3e8cf58f8e9ea90d51fe28fcfca3ad91d91e74aabca274`  
		Last Modified: Wed, 06 Mar 2024 00:07:47 GMT  
		Size: 1.8 MB (1776853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable-glibc` - linux; arm variant v7

```console
$ docker pull busybox@sha256:8a4415fb43600953cbdac6ec03c2d96d900bb21f8d78964837dad7f73b9afcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1554425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9903cc888814e8feef24381cdb6d29d8598385dcb109a9908a4a98e1ab021532`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:a7cbd68a76a020b8b283c940bc267cd88a66013dcb160cad746344483dfc4b52`  
		Last Modified: Wed, 06 Mar 2024 00:10:11 GMT  
		Size: 1.6 MB (1554425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable-glibc` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:8f03917912ea995c637b6c0295846aaff5665f06ac82a29b421fba4c379494e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1916607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4fd538a9a0b729be05707cf805388be2fb701cfd5d44c6542f1988e8aef6e3`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c2bf9493c1bf786e95e3eac7d406c20aa1b8a2d40916756e891627e9e8f8d119`  
		Last Modified: Fri, 19 Jan 2024 00:32:32 GMT  
		Size: 1.9 MB (1916607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:a69e011a60760aba5dd1209f91c05980c6fab54d8b25ae169291e63377f51cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 KB (12193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd1ff0b19ae0f0339dfa452087f6e62d3885ac4cd6d87c8b93b3893fa44b0b6`

```dockerfile
```

-	Layers:
	-	`sha256:24ccf6b7ae0e49578be9c4155a809a71d3e4b9c5486ce7c4086d68e3d1acd22f`  
		Last Modified: Fri, 19 Jan 2024 00:32:31 GMT  
		Size: 4.8 KB (4800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53a196fbf5767399864392abcd4b090e16c2f74821ac8b44d3f139986875dae`  
		Last Modified: Fri, 19 Jan 2024 00:32:31 GMT  
		Size: 7.4 KB (7393 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:stable-glibc` - linux; 386

```console
$ docker pull busybox@sha256:99eabec0f153fb38feb80682492123326c994a6857f7ef9b73d46eecd8b81684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2268883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a422f55b78a61a0acf17d1ad4cea56c7542f1a09e6a256def15b8787d41ad7a`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:b6f95b873e20279fb8550d2d0b30bff9e72de3fe85f2ff4cfbf5f8f8aa6dabf4`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 2.3 MB (2268883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:deb0f17418ba410fceb230e48f01a2056732cba642d66a812901fa3d039c7e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 KB (12043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e79a31fa88e6a7c031f212bf2849dfb712003711e72dcae4abf34405846cdcf`

```dockerfile
```

-	Layers:
	-	`sha256:347076177c54f21c7c7fd98a9a45a717898d8441f14a94c5248a682a00008516`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 4.7 KB (4725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcf8fff8866352521d3aef70307e34f73f9951524290a8b4b36ffb75b6e6c138`  
		Last Modified: Thu, 18 Jan 2024 23:03:24 GMT  
		Size: 7.3 KB (7318 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:stable-glibc` - linux; mips64le

```console
$ docker pull busybox@sha256:8c4284fa9cc28d0b9455f84527de8b58d5d4df00abcd18e47f2f1dc4e89f7ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2077641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c67790aa14859c61c94e0b7e727a8c50a5e246783c252e080ae41187e8ec52`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (glibc), Debian 12
```

-	Layers:
	-	`sha256:b9f2f1866e3467e8735b90ecad932b7c1f122f80426b5beda6fb8a4c87f45757`  
		Last Modified: Wed, 06 Mar 2024 00:08:46 GMT  
		Size: 2.1 MB (2077641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable-glibc` - linux; ppc64le

```console
$ docker pull busybox@sha256:4b36905f6e9385ec2234f41dbb9d67ccd99ee2b50ef225c08746b2276991bb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb40c4cff2a5d1551f5a9e79b6fac3cf2d655f702041d0ae8d670e027645bd9`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1e329ff3bf1d3bf69d13da2954652acf3457a6fbd276780a232bb5254c915148`  
		Last Modified: Fri, 19 Jan 2024 00:42:12 GMT  
		Size: 2.5 MB (2528609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:17110abebf0882f7e23b68ea936ab719a49047e1b4a8e0ab0118ff0abff0066d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 KB (12281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48490b9b70ffd6de2941a4f2dbecc81750fe06d0c527e787a94fff4504c7721`

```dockerfile
```

-	Layers:
	-	`sha256:07f1bfa21dee33589c5658c47aa84655e024d44ef684cbd102571f1fdaa89c48`  
		Last Modified: Fri, 19 Jan 2024 00:42:12 GMT  
		Size: 4.8 KB (4842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f2fcbb930547c7a7fa4783062b75854e39e225a8dc9dbf51df1bcb5b2580c4`  
		Last Modified: Fri, 19 Jan 2024 00:42:11 GMT  
		Size: 7.4 KB (7439 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:stable-glibc` - linux; s390x

```console
$ docker pull busybox@sha256:df5506ae24620e67cb668f0137869babd6305cf4912190ee7de781c412b9bad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1926831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a46af96236bcedbc5591856e442999857d24fd51f5ff2135ede6486c79e2e7`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:230db3ea6af07ccf4b5f3ad6164f90d07967b83607909a587631245cc7c84ef4`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 1.9 MB (1926831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable-glibc` - unknown; unknown

```console
$ docker pull busybox@sha256:b2a97dca77d5ae1e0ddef0cbfba271b5f0597c9ea7b8cb8127b397c7c9d03dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 KB (12149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e23940337a50804f81942abe24849f22423565ad3dabdfeefa3ee5cc61fd96`

```dockerfile
```

-	Layers:
	-	`sha256:5f4fdc6f7194500531229dc2d7aa2b54119cdf908b5e842b6ae1bfbf57487b79`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 4.8 KB (4778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ad8320e0617081f2bb73e6289f33979e1ee192d12ef3459b3bfe278084c075c`  
		Last Modified: Sat, 20 Jan 2024 17:28:03 GMT  
		Size: 7.4 KB (7371 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:stable-musl`

```console
$ docker pull busybox@sha256:9a7f0d2407780a98013e227ddc43f87bf5fbe626fb59f98280efd591c75ccdec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `busybox:stable-musl` - linux; amd64

```console
$ docker pull busybox@sha256:d4707523ce6e12afdbe9a3be5ad69027150a834870ca0933baf7516dd1fe0f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **878.7 KB (878681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59888ccc9e6510deabb10bb0452f184f40cec7064c0fc522a01924f66c7fdfd8`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8dfc70c9a1cfc61f5873aed748e446239a5cb27faddd51d118180665010c02b7`  
		Last Modified: Thu, 18 Jan 2024 23:03:35 GMT  
		Size: 878.7 KB (878681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:864e79c6eb0056047a68c6c717ee53d548519ee307dec471696a5e6d0fab0a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c89e5c4f095b960e7a950b75e8f1386f0c1d1d43c108818b9b3922c803c1f1d`

```dockerfile
```

-	Layers:
	-	`sha256:aa7db50a9fdf0d3338cc08bc515695143e4aaf3e3e4b276f5f6d6d3bba5cca05`  
		Last Modified: Thu, 18 Jan 2024 23:03:35 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce0dddc950954bfb91430621087a12e68a552255f8c49ff243c27b22fbc6280`  
		Last Modified: Thu, 18 Jan 2024 23:03:35 GMT  
		Size: 5.9 KB (5871 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:stable-musl` - linux; arm variant v6

```console
$ docker pull busybox@sha256:b64a6a9cff5d2916ce4e5ab52254faa487ae93d9028c157c10d444aa3b5b7e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.6 KB (987570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5059e5cce9929da538b30d11caea9231836d6b937083115b4058ae4649341b74`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd544bbcb8b286d4a58e2b02357bb516d089d281fc87ae2b375921b8d2389923`  
		Last Modified: Thu, 18 Jan 2024 23:58:56 GMT  
		Size: 987.6 KB (987570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:0c1556654c58755833235ba840bb04258b5cf8d3e1771be01a2c48e38c266c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e96145e5c30a04c819cb052df4fa049365de24673fc3afdc9d5305cc2999a8`

```dockerfile
```

-	Layers:
	-	`sha256:1bbd274efa1896b02a475d573d66e47cc60d67dfb2334eef4aefc1d23763fe11`  
		Last Modified: Thu, 18 Jan 2024 23:58:56 GMT  
		Size: 7.2 KB (7231 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:stable-musl` - linux; arm variant v7

```console
$ docker pull busybox@sha256:f2939eb0b529af5706172c10db02a0894949c461b81ed4282ff4df5bf18c14d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.6 KB (843648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855943b02ba3319e1345d803a557c4a88bfd0c18954db6869f2ac791e17c4ae3`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (musl), Alpine 3.19.1
```

-	Layers:
	-	`sha256:83dc776fdc81b19e8a0c134d8eecfc7793d00ca52c1cc4292e973750e3684712`  
		Last Modified: Wed, 06 Mar 2024 00:10:38 GMT  
		Size: 843.6 KB (843648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable-musl` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:fed6b26ea319254ef0d6bae87482b5ab58b85250a7cc46d14c533e1f5c2556db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.0 KB (920992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f13cdcd8df2876053fd8dc5d01363344a92ea4d6537bd78625b9209e988edf`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d997961b9429e6c49b53a709a914c6578f5ff5ba7166ee52de62d1ac94887c1e`  
		Last Modified: Fri, 19 Jan 2024 01:36:22 GMT  
		Size: 921.0 KB (920992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:1cbd2ff89d7ff09ec11e246f3a887f3a914ab78b5d7445c43487b8c6fbed88cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83f629b0163590a531f21a762bb0cbaa263d937678e8f68d96a31c90ef4a07b`

```dockerfile
```

-	Layers:
	-	`sha256:3c2685448006e438049a85838a6b8137f2e8454a9bc20b249241ff956b520505`  
		Last Modified: Fri, 19 Jan 2024 01:36:22 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6177450e2c462aaedbb8f947886eb918cc00046a7fdc55ccca512c51f9243ee4`  
		Last Modified: Fri, 19 Jan 2024 01:36:22 GMT  
		Size: 5.9 KB (5883 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:stable-musl` - linux; 386

```console
$ docker pull busybox@sha256:b6678a8456f13554d339f393c4bcf798b3730a4f1662f6d9842129cbeeb5c665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.5 KB (875482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e9971e1ff6c5b5940f3f82628fe182aead284575c0ae4a798ed91e15ef08d7`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:769db000cf23b44ad2664168ee3886ca8883b18f32581f08cd06ce00f41ff872`  
		Last Modified: Thu, 18 Jan 2024 23:03:39 GMT  
		Size: 875.5 KB (875482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:fcc65e203ef7a06b3c9852b25de034cc8472405e5d7f033e818752a15778a758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa92905283639dceabeee0502770622fc73c4856e769907a58b011d8c5ea776f`

```dockerfile
```

-	Layers:
	-	`sha256:9020223ee3ca8d6d37dab73b397baddf426d3d408db20f63d02b1e9d2faff9d6`  
		Last Modified: Thu, 18 Jan 2024 23:03:39 GMT  
		Size: 3.3 KB (3254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6eae553040cde89419e4a177c32658f1d867ec25cf9a30b7655184d189a9439`  
		Last Modified: Thu, 18 Jan 2024 23:03:39 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:stable-musl` - linux; ppc64le

```console
$ docker pull busybox@sha256:74dfdbf9d13a59af2f6aa61ad738fa1fdade6dfd0d6f687eb3b0d53ffc8b5623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **967.1 KB (967138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f646f514a9f9bafe5483609c8bb0c3c64f9628f35d9beffda459a7fc992d9fe0`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:e4d8791bb918bc69b870f21a553724ec9b2812219040885317ce57b6eb4e6ab3`  
		Last Modified: Fri, 19 Jan 2024 01:03:30 GMT  
		Size: 967.1 KB (967138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:832836469bae4830469c6b70aa0ca4cf84181eb2a11484479ea37d6ce6143846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376ae5066f35abd2be10b0eacfecd79b91086e268f707d436e7b8798c411fcf9`

```dockerfile
```

-	Layers:
	-	`sha256:1ecc1159b446640a86f9969f010bbc8178567a5b46e779b2ce340b9229dac07e`  
		Last Modified: Fri, 19 Jan 2024 01:03:30 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a8411155c9d98fe9609d4ca6e64859296085c39baa2e804ebae951ab5b80b8`  
		Last Modified: Fri, 19 Jan 2024 01:03:30 GMT  
		Size: 5.9 KB (5909 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:stable-musl` - linux; s390x

```console
$ docker pull busybox@sha256:e7e0969b47c05409c0fa5c909e006a620f845d5b119869c8346e4f3cb93f8c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **940.3 KB (940326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774f60d2b6d3daa542d524858ddb90ae71c4b3cc014a0235132a36c51e1d4515`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:48e10ecef46b18109935c897c4fb6ba3b06fea3fc7b54588e2aef37a9ecc7db9`  
		Last Modified: Sat, 20 Jan 2024 17:54:57 GMT  
		Size: 940.3 KB (940326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable-musl` - unknown; unknown

```console
$ docker pull busybox@sha256:6ac7f239a3bffeaff764ae1948e58f80497ce3fe2d2bdfb42b7c9899ac58270e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2deb03e82c885a1c5de5b9ffc72f3b12beb43f880ffec52862abecf85ba22e4`

```dockerfile
```

-	Layers:
	-	`sha256:72517eef4c47c126a39ac1b293ba0bcfcb63a31962064a4a8bc3907115262d23`  
		Last Modified: Sat, 20 Jan 2024 17:54:57 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:990936cff923ba93c536c3d8f4ba7db950b54f638d8ca2d0b278ed1e0110f3b9`  
		Last Modified: Sat, 20 Jan 2024 17:54:57 GMT  
		Size: 5.9 KB (5871 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:stable-uclibc`

```console
$ docker pull busybox@sha256:61651f1730187bbbfaa01e81d31eb082a1853a14118255c7dff5f1365d0ca3e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; riscv64
	-	unknown; unknown

### `busybox:stable-uclibc` - linux; amd64

```console
$ docker pull busybox@sha256:21de0dff31b277e0d37fe21f6e89e461f5c07415719d225235121c144287dc17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **783.2 KB (783164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e537aeebf5260fe6cb054017b3af5862945ab73f5a7091cd6e2127cdfdd5a14`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cff2761077a7b33f0ac06f806d159087b8c79413afc45167a232c5b9394615f1`  
		Last Modified: Thu, 18 Jan 2024 23:03:48 GMT  
		Size: 783.2 KB (783164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:385fe86cbfdf640c4538befe889e1e9bf93fa21eeb9955f7ea076e6d874a2d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7796465a33cc98caddbb8bc190b367eaeb431320484f406887f0d1c8578327c`

```dockerfile
```

-	Layers:
	-	`sha256:165aad5817a1de48ec8d7d517f5332a81840adf0cc4836a6c3f4aad1ac31e128`  
		Last Modified: Thu, 18 Jan 2024 23:03:51 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f647335cce5641a56b28c17896a32f125e7d6823621a542398ee88b0754d863`  
		Last Modified: Thu, 18 Jan 2024 23:03:48 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:stable-uclibc` - linux; arm variant v5

```console
$ docker pull busybox@sha256:2e2d13aea845763e5152bb8116738d5179f67b79fc6fde83bf813896829d4bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.2 KB (744233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be06eb6ec3aaf1ca11f443876561f4e75e1dd0ceb407c1880033d7ff6328b3e`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (uclibc), Buildroot 2023.11.1, Debian 12
```

-	Layers:
	-	`sha256:120231968b7db68bb2d25cd765a3eee8fe0ec5be354a4306354fdd9606bd7774`  
		Last Modified: Wed, 06 Mar 2024 00:08:00 GMT  
		Size: 744.2 KB (744233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable-uclibc` - linux; arm variant v7

```console
$ docker pull busybox@sha256:b87edd76d8d0b9e848a0059a3014d87dabf763bc6cfcb9df52d13f4523a3d371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.9 KB (708929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2858fb01eb20e8b8f27c5d3108e9df3065a5c3196a170111aabbf09b81d4bf9`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (uclibc), Buildroot 2023.11.1, Debian 12
```

-	Layers:
	-	`sha256:19210f7552436b95fa7de660fcbf9e9425a0813bfccb850b3fcd053709caf443`  
		Last Modified: Wed, 06 Mar 2024 00:10:24 GMT  
		Size: 708.9 KB (708929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable-uclibc` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:b8879bdf897086348b8048b0a5ae3d85addc583ed20050328ec7146858e847e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **836.8 KB (836843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80467bacead9d1b091a5648f067f735716b201eba3fd71a4fb44e13f5341f0cd`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cea42dbd04d75d2786e9fef4399413709452debd69b417e4c200743b4b844c00`  
		Last Modified: Fri, 19 Jan 2024 00:57:12 GMT  
		Size: 836.8 KB (836843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:d872e2c2932c6bd7821197d583a23869fdb68bf056a7d7dac8a97e20e62bd6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a42e696a19934cb4621a011849c38a5b99a99a7db2a5f5914af4bd5c886b3f4`

```dockerfile
```

-	Layers:
	-	`sha256:4f836af667398f1a6feb5e25980960f902daf9096ca799ab436dba129c2c8698`  
		Last Modified: Fri, 19 Jan 2024 00:57:11 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:880e28375df06f638d5045451a8dda0fc51cc28429dba1387275de009fd5d3b3`  
		Last Modified: Fri, 19 Jan 2024 00:57:11 GMT  
		Size: 5.9 KB (5909 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:stable-uclibc` - linux; 386

```console
$ docker pull busybox@sha256:b805bdb43c275243e31c549abcc71d98c1323a225598b74e5a9b9dc91fdf4073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **747.9 KB (747949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992d7e8ad26e67c26250373ac39142b725403b68173a52edacc7c191cf5f097a`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d6a6d95c0da603317dbc3d49423910ecb730bb5d4219de536cfd7120bd1d792e`  
		Last Modified: Thu, 18 Jan 2024 23:03:27 GMT  
		Size: 747.9 KB (747949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:3cb35ce2ebff606afe19b8965ea3f0fe093bbbfc9fabc67a3158c7f4cd146068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c6ca91c6552ef25e52903cad76d996d7b60375a160b4205a35c7b060549a35`

```dockerfile
```

-	Layers:
	-	`sha256:cd8b24a6892d4af4db2582c4db92db552c251baa708fd3d249742144a1f06c65`  
		Last Modified: Thu, 18 Jan 2024 23:03:27 GMT  
		Size: 3.3 KB (3274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3117b42969c2d3cfbd84681cccff735d766b482184839bd402d14f12180792ad`  
		Last Modified: Thu, 18 Jan 2024 23:03:27 GMT  
		Size: 5.9 KB (5868 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:stable-uclibc` - linux; mips64le

```console
$ docker pull busybox@sha256:388eed10bf5614e88ae1e2b2c1d237cbef877a07858125415556e3d9edff526d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **948.9 KB (948864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd60f88674723ffdec05a32d2bee1157f95e335ced9c3efea5686b9b15cd1416`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (uclibc), Buildroot 2023.11.1, Debian 12
```

-	Layers:
	-	`sha256:16b2225af5a2181079c894731b1031c046d90aca99349dd3487cfc6d6702d0e3`  
		Last Modified: Wed, 06 Mar 2024 00:09:07 GMT  
		Size: 948.9 KB (948864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable-uclibc` - linux; riscv64

```console
$ docker pull busybox@sha256:41af629cfa908c7ed7550db6a260c79d6dd55fe4996d7481595e3d547ab829c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.3 KB (914275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9673ad33efcd24dfd28f0415f23ee1c42d743140691e10781669692ef3af1ba6`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:917dbba7e6e14feb5914ca2711ff13b50b1f9a2b0b8315b79bbceabde34d11c2`  
		Last Modified: Thu, 18 Jan 2024 23:05:50 GMT  
		Size: 914.3 KB (914275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:stable-uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:126af02605028b8076a4a47fe1c707c795ce58c66a266c67b447519ebf1f3b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 KB (12303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa149c79ad9040800185662b3a226758c08cd6d612ca2a1abf6ebf0d9716f32`

```dockerfile
```

-	Layers:
	-	`sha256:1acfa35c63c5a80ca903c34528318a0b6b614a7060738be73b2b8424004473b1`  
		Last Modified: Thu, 18 Jan 2024 23:05:50 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97288386ab763b23aa899ebcfaa85d4b1708c86df318569f03865c7fb2b7ad4f`  
		Last Modified: Thu, 18 Jan 2024 23:05:51 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.in-toto+json

## `busybox:uclibc`

```console
$ docker pull busybox@sha256:61651f1730187bbbfaa01e81d31eb082a1853a14118255c7dff5f1365d0ca3e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; riscv64
	-	unknown; unknown

### `busybox:uclibc` - linux; amd64

```console
$ docker pull busybox@sha256:21de0dff31b277e0d37fe21f6e89e461f5c07415719d225235121c144287dc17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **783.2 KB (783164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e537aeebf5260fe6cb054017b3af5862945ab73f5a7091cd6e2127cdfdd5a14`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cff2761077a7b33f0ac06f806d159087b8c79413afc45167a232c5b9394615f1`  
		Last Modified: Thu, 18 Jan 2024 23:03:48 GMT  
		Size: 783.2 KB (783164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:385fe86cbfdf640c4538befe889e1e9bf93fa21eeb9955f7ea076e6d874a2d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7796465a33cc98caddbb8bc190b367eaeb431320484f406887f0d1c8578327c`

```dockerfile
```

-	Layers:
	-	`sha256:165aad5817a1de48ec8d7d517f5332a81840adf0cc4836a6c3f4aad1ac31e128`  
		Last Modified: Thu, 18 Jan 2024 23:03:51 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f647335cce5641a56b28c17896a32f125e7d6823621a542398ee88b0754d863`  
		Last Modified: Thu, 18 Jan 2024 23:03:48 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:uclibc` - linux; arm variant v5

```console
$ docker pull busybox@sha256:2e2d13aea845763e5152bb8116738d5179f67b79fc6fde83bf813896829d4bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.2 KB (744233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be06eb6ec3aaf1ca11f443876561f4e75e1dd0ceb407c1880033d7ff6328b3e`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (uclibc), Buildroot 2023.11.1, Debian 12
```

-	Layers:
	-	`sha256:120231968b7db68bb2d25cd765a3eee8fe0ec5be354a4306354fdd9606bd7774`  
		Last Modified: Wed, 06 Mar 2024 00:08:00 GMT  
		Size: 744.2 KB (744233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:uclibc` - linux; arm variant v7

```console
$ docker pull busybox@sha256:b87edd76d8d0b9e848a0059a3014d87dabf763bc6cfcb9df52d13f4523a3d371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.9 KB (708929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2858fb01eb20e8b8f27c5d3108e9df3065a5c3196a170111aabbf09b81d4bf9`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (uclibc), Buildroot 2023.11.1, Debian 12
```

-	Layers:
	-	`sha256:19210f7552436b95fa7de660fcbf9e9425a0813bfccb850b3fcd053709caf443`  
		Last Modified: Wed, 06 Mar 2024 00:10:24 GMT  
		Size: 708.9 KB (708929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:uclibc` - linux; arm64 variant v8

```console
$ docker pull busybox@sha256:b8879bdf897086348b8048b0a5ae3d85addc583ed20050328ec7146858e847e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **836.8 KB (836843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80467bacead9d1b091a5648f067f735716b201eba3fd71a4fb44e13f5341f0cd`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cea42dbd04d75d2786e9fef4399413709452debd69b417e4c200743b4b844c00`  
		Last Modified: Fri, 19 Jan 2024 00:57:12 GMT  
		Size: 836.8 KB (836843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:d872e2c2932c6bd7821197d583a23869fdb68bf056a7d7dac8a97e20e62bd6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a42e696a19934cb4621a011849c38a5b99a99a7db2a5f5914af4bd5c886b3f4`

```dockerfile
```

-	Layers:
	-	`sha256:4f836af667398f1a6feb5e25980960f902daf9096ca799ab436dba129c2c8698`  
		Last Modified: Fri, 19 Jan 2024 00:57:11 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:880e28375df06f638d5045451a8dda0fc51cc28429dba1387275de009fd5d3b3`  
		Last Modified: Fri, 19 Jan 2024 00:57:11 GMT  
		Size: 5.9 KB (5909 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:uclibc` - linux; 386

```console
$ docker pull busybox@sha256:b805bdb43c275243e31c549abcc71d98c1323a225598b74e5a9b9dc91fdf4073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **747.9 KB (747949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992d7e8ad26e67c26250373ac39142b725403b68173a52edacc7c191cf5f097a`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d6a6d95c0da603317dbc3d49423910ecb730bb5d4219de536cfd7120bd1d792e`  
		Last Modified: Thu, 18 Jan 2024 23:03:27 GMT  
		Size: 747.9 KB (747949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:3cb35ce2ebff606afe19b8965ea3f0fe093bbbfc9fabc67a3158c7f4cd146068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c6ca91c6552ef25e52903cad76d996d7b60375a160b4205a35c7b060549a35`

```dockerfile
```

-	Layers:
	-	`sha256:cd8b24a6892d4af4db2582c4db92db552c251baa708fd3d249742144a1f06c65`  
		Last Modified: Thu, 18 Jan 2024 23:03:27 GMT  
		Size: 3.3 KB (3274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3117b42969c2d3cfbd84681cccff735d766b482184839bd402d14f12180792ad`  
		Last Modified: Thu, 18 Jan 2024 23:03:27 GMT  
		Size: 5.9 KB (5868 bytes)  
		MIME: application/vnd.in-toto+json

### `busybox:uclibc` - linux; mips64le

```console
$ docker pull busybox@sha256:388eed10bf5614e88ae1e2b2c1d237cbef877a07858125415556e3d9edff526d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **948.9 KB (948864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd60f88674723ffdec05a32d2bee1157f95e335ced9c3efea5686b9b15cd1416`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 May 2023 22:34:17 GMT
RUN BusyBox 1.36.1 (uclibc), Buildroot 2023.11.1, Debian 12
```

-	Layers:
	-	`sha256:16b2225af5a2181079c894731b1031c046d90aca99349dd3487cfc6d6702d0e3`  
		Last Modified: Wed, 06 Mar 2024 00:09:07 GMT  
		Size: 948.9 KB (948864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:uclibc` - linux; riscv64

```console
$ docker pull busybox@sha256:41af629cfa908c7ed7550db6a260c79d6dd55fe4996d7481595e3d547ab829c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.3 KB (914275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9673ad33efcd24dfd28f0415f23ee1c42d743140691e10781669692ef3af1ba6`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Jan 2024 21:49:12 GMT
ADD busybox.tar.xz / # buildkit
# Wed, 17 Jan 2024 21:49:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:917dbba7e6e14feb5914ca2711ff13b50b1f9a2b0b8315b79bbceabde34d11c2`  
		Last Modified: Thu, 18 Jan 2024 23:05:50 GMT  
		Size: 914.3 KB (914275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `busybox:uclibc` - unknown; unknown

```console
$ docker pull busybox@sha256:126af02605028b8076a4a47fe1c707c795ce58c66a266c67b447519ebf1f3b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 KB (12303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa149c79ad9040800185662b3a226758c08cd6d612ca2a1abf6ebf0d9716f32`

```dockerfile
```

-	Layers:
	-	`sha256:1acfa35c63c5a80ca903c34528318a0b6b614a7060738be73b2b8424004473b1`  
		Last Modified: Thu, 18 Jan 2024 23:05:50 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97288386ab763b23aa899ebcfaa85d4b1708c86df318569f03865c7fb2b7ad4f`  
		Last Modified: Thu, 18 Jan 2024 23:05:51 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.in-toto+json
