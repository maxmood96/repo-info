## `debian:rc-buggy`

```console
$ docker pull debian@sha256:f1255a4b069841ffaff64e7b7c7a6533e22eb2c6d2c29fec2bf9463bda8588e7
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:26d6c2f551867d36ae66a6e18d400ba005f119452d8a72cb2528bff522aa23d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52643120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856a16695b65099421f45c980066646ec3b403d59242eafbb13decaf6dec378b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:29:36 GMT
ADD file:b10a84e4e404c6ca6a1a6782f9040f24bb7bfbb95055e8cd39600ef22a4a9284 in / 
# Tue, 14 May 2024 01:29:36 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:31:19 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a79fdf356ad40501c2429368bf029e9f2414f18b03d6fa40ddac5cebf750f95c`  
		Last Modified: Tue, 14 May 2024 01:35:04 GMT  
		Size: 52.6 MB (52642897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8863a21ce3855d25aaba1071bd27a27e2882a8851058819aa6fc1205103c8a4c`  
		Last Modified: Tue, 14 May 2024 01:37:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:437a05582690857f772246ebfd3de6d2870c1b82c1372020f7391deca0b307dd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49497946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc029e4f8d7f42c6d214534eff606be468aef079f7cba130e622ac21925c4f4d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:12 GMT
ADD file:53c5bacab4479c2281acdc8e18c636052e6d20212a45337d8a17b19319ec5ca7 in / 
# Thu, 13 Jun 2024 00:49:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:50:26 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a884fb5df6a69e4609683ee45a6be09afed09564ce4f6b3902caeb9298054718`  
		Last Modified: Thu, 13 Jun 2024 00:53:18 GMT  
		Size: 49.5 MB (49497721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9457941bdc510c18240bb26412e2d2f9882cfc824263de522c15d3feae3f11`  
		Last Modified: Thu, 13 Jun 2024 00:55:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:8937d39823ee176dbd05a9e5fced55175109f66ae8a6628dbda9c1a0515b7d53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47253608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc9e5fa80ab7ca82c68ffab9a4239c9c446912f8c2e7332fd46bfdd171e7bc3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:10:01 GMT
ADD file:02154de0dc9450545487c68904a4e760ff1ce6b2170e0658abc5f63881b61f8e in / 
# Tue, 14 May 2024 01:10:01 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:11:26 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:bdb66c06bd7989a8ebc0daa12fd841f7fcee2541fcb911169e2813963f822a18`  
		Last Modified: Tue, 14 May 2024 01:15:24 GMT  
		Size: 47.3 MB (47253384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ad2ba7b2ba90faa3d8983dd192cde00cef1d80da8de45eed0d4bec91181282`  
		Last Modified: Tue, 14 May 2024 01:17:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f16227b16d2aaa702098548f280ba02df4e1cf0b6d896289242e4cf5460051f8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52683336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185b68d233c232b0279afa598c58c188c7983ad4845702e017e100458ea93a61`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:53 GMT
ADD file:0df3518c1c665e2879ed3c7b7c5961b53fc28709cc135a245b209411a275c037 in / 
# Thu, 13 Jun 2024 00:40:54 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:42:02 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:844667f4b2125bd419ff2157667c09ca5b8d442b399e2db99e62277881555d82`  
		Last Modified: Thu, 13 Jun 2024 00:45:41 GMT  
		Size: 52.7 MB (52683111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00409951a21660750abb92e98f000117f7959193ebea75167e844648fec9d6fc`  
		Last Modified: Thu, 13 Jun 2024 00:48:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:3cf0545f191b2b761bc401d7b9c19fbe6192bef887c5caf1fd9ac9cb830f5886
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53304522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074892903b5c56339cc771ad4d63c10242787bc44159cd1cf7116d88ec3374ed`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:29 GMT
ADD file:8452dc45806912ac27c72fbde099f24d3385b2fe336f125781076ac8fada56f2 in / 
# Thu, 13 Jun 2024 00:40:30 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:42:10 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:892c6905b91a2725baf7261577bc387b671ddd2ecf5bba2922a38096ad8e5eae`  
		Last Modified: Thu, 13 Jun 2024 00:46:12 GMT  
		Size: 53.3 MB (53304297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cadc92d0d6c50ee5664137483570a0378349f491d67518ce2cb90505a7df55d2`  
		Last Modified: Thu, 13 Jun 2024 00:49:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:e5b7faa399735179167c6702d83350c196098041832237bb82cf7745ff25576e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51536563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f28f2ba43c9947f1158446ae75d68e4154009765eb966f548f3a5185c543599`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:14:15 GMT
ADD file:33e0af2de2241c9212af2152c10bf302aa0352fa38eaae9fab1cb558d6a457a2 in / 
# Tue, 14 May 2024 01:14:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:20:15 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:69f45a8662462c65462de8a317ebc50b0eeacc442e8038f6212a37458ce29095`  
		Last Modified: Tue, 14 May 2024 01:25:45 GMT  
		Size: 51.5 MB (51536337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2075670e862575bc52c6741e77f63a8df38b306be2b78f3db16587b74bfe4c7e`  
		Last Modified: Tue, 14 May 2024 01:31:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:391b5decb6d73785a176f87c579111033db8936bb9d7855e392970e6a3078b8b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56538421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e94c681d251af8739aa5da4498f2cab3e1e00cf02784351253cc6ce259ca7f2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:21:02 GMT
ADD file:48cc1541210c6108c0251f6f008cd7e9eb30330f4f7a0e4ca8f13863de6afe2f in / 
# Tue, 14 May 2024 01:21:05 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:22:54 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:bae7d269c4dd7d40de29faa635851f1c684cc32fdc792af4ff32efd2461c744f`  
		Last Modified: Tue, 14 May 2024 01:25:52 GMT  
		Size: 56.5 MB (56538197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c883e19f86c534de4653949006ddadff2de0ff29b711fb08c4286f5618a9340`  
		Last Modified: Tue, 14 May 2024 01:28:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:221092afbc3eac75dcd0da4a490e52aa284571c50e884622aa59c5ef23d6433b
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50961650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11856d88d71b59d42945a98310dcf0e4c653c305c937df7af75d532835ea0898`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:08:59 GMT
ADD file:18cb19ec2784efee4339c923ec316987819836eb7aad9280180eeca7729ae78c in / 
# Tue, 14 May 2024 01:09:01 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:10:46 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e438edd6428d670b6cea990c6caad079c8929366cc17e63aaad3fad6d8aaa661`  
		Last Modified: Tue, 14 May 2024 01:11:42 GMT  
		Size: 51.0 MB (50961424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc8decc4df642f85c4d5d62e888dc310ffb88cb9adb4b25bc54ac955a8069df`  
		Last Modified: Tue, 14 May 2024 01:13:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:4b101188c3d2ca0321ae587e24db80c083cf422d2ee8747613c4cfbded210f6a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52054618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60cc407eb268d1273d523f879ea0f8364067bbead569d41c6e81b2fef8605a4c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:44:00 GMT
ADD file:48df1edc9b73475781ccac0eb967ca97c87c5a3132a7c9058519fad686260867 in / 
# Thu, 13 Jun 2024 00:44:02 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:46:24 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:f539c970b22ae85b0b82128798f27249002cae24f6d005cd8df7e2098a346a0d`  
		Last Modified: Thu, 13 Jun 2024 00:48:56 GMT  
		Size: 52.1 MB (52054394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1384f408901b63cfe39e82164e9e3a0ec827ce83bf571f138148f7db4ace2c37`  
		Last Modified: Thu, 13 Jun 2024 00:50:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
