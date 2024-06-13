## `debian:experimental`

```console
$ docker pull debian@sha256:e4e05eecb59e0eb7d2bada8d7f78623bcf71645acbec09c983d9d5b1775ec44a
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

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:e5b39eed4a5e7c1a0c77e394ce0405e95c00b427b0c59e8b3b64bda638c6172b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52429843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d296fc6b37718626b68d81efa6c1c0a07832acb87b655c3aa685a2b756fe8a4b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:23:55 GMT
ADD file:97038e10ef5b1dcac530c1eb1f457a998d419abea6085bbbe937116f2734da4f in / 
# Thu, 13 Jun 2024 01:23:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:24:09 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:8a16955337e68b0976cc5d012b5c3e3c48345581507a5671f69829c93d67d423`  
		Last Modified: Thu, 13 Jun 2024 01:30:11 GMT  
		Size: 52.4 MB (52429622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f501ae50f47db8b467c7e8397ad1d69a941760dfb21e29a15c34b6c1891c066e`  
		Last Modified: Thu, 13 Jun 2024 01:30:33 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:a6cbe8c8bca94e2330e859ca02621a21ec06d09a00f5c82b16b6b5c2bfa83511
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49497948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4f031361e79eaf6ff1ba91063be163ce6a7c131ec21be1abb7f4a02d9ba93d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:50:15 GMT
ADD file:8220399af7e4dac5b20511baf0f7e41ec5497bb049c252b12df487975c998ed0 in / 
# Thu, 13 Jun 2024 00:50:16 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:50:24 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:75707ab2c3205293345df9598e07e04ba5f0de0e27278a19483e6462d8a689d1`  
		Last Modified: Thu, 13 Jun 2024 00:55:24 GMT  
		Size: 49.5 MB (49497728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a474ea4f07a1f85d9d764988ddf925a842411286a4d9da80f8b6d15f5d3399`  
		Last Modified: Thu, 13 Jun 2024 00:55:44 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:e98a5c2748295103758b629be5309e908819f344f50015248dbdb16ba5c311dd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47007212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c83a6cd33875f4638c9b7ca75eb1d5b20bce9523c0a284141079ca3708a119b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:00:06 GMT
ADD file:c8576f01408268dccc2e6013e433b0ce1cc99a3c56cfd455bf0f8bd30a93f7e3 in / 
# Thu, 13 Jun 2024 01:00:07 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:00:17 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d9c4dfc4f55a75057804b71e78f004a12b235cc841655acf600155c3d5214e74`  
		Last Modified: Thu, 13 Jun 2024 01:06:25 GMT  
		Size: 47.0 MB (47006992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5dc8d5575aa6a69c54e3a84117ba799243c5a5b26f543cb8290776274a7d18`  
		Last Modified: Thu, 13 Jun 2024 01:06:44 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:fe4f90bc84e078ea54cf263e0053c8739bdc9f2367bd85104408c1ec2bbe5499
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52683338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9da6d6972f1500d319a7d6e43c47c3d5de70dc40b435e9ac521b8f0f779007`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:50 GMT
ADD file:e2515159d6b834a66909c60f24e550c86184ad739c792a452011306effdc8fd6 in / 
# Thu, 13 Jun 2024 00:41:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:42:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b6c619a1513a6517126a1a9da5e700e69d3542c73ba74f6fdb7d1148e7d04ae6`  
		Last Modified: Thu, 13 Jun 2024 00:47:36 GMT  
		Size: 52.7 MB (52683114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d62b9c95012152309a3cc31a4b9981600fd5045dd875addb566d1a7229c5730`  
		Last Modified: Thu, 13 Jun 2024 00:47:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:babd55a8cddb60e49b0647f731f4232900a52a63b2490369fcb678ba529f4416
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53304527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7c0f34ba69c775d4ff95c80590e695c5bef2984e5aa821262a8dbeaef69bf9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:54 GMT
ADD file:d1fdb0b9ed021eb7269ce6cfe09244166cc99a859401d9045ed096abe376a631 in / 
# Thu, 13 Jun 2024 00:41:55 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:42:08 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:0079983cf187ab06fc29ea2245b355e72b8261ccbcd555b98c457c2560f5bf18`  
		Last Modified: Thu, 13 Jun 2024 00:48:34 GMT  
		Size: 53.3 MB (53304306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320559339114c4bc10293d3902d93c365b2243096379e60a48b9229253376283`  
		Last Modified: Thu, 13 Jun 2024 00:48:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:14be8029d0a6d4ce2e82e491444846522a54b8bf80c5ab379d8f206a1f9cab43
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51279428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374f41c28748e85fc170a0c91256bd05785752e55d4fb7d1313b1570156fe4ba`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:18:44 GMT
ADD file:d5d3e02cac4443cadbda6b89811c5d054d1db9db3bcc1927947b232c06d0720f in / 
# Thu, 13 Jun 2024 01:18:50 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:19:34 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c7d43b9a5bb5053e2c3962b043f5a84589a756c4fd34f55d353670560e9d2f3c`  
		Last Modified: Thu, 13 Jun 2024 01:30:20 GMT  
		Size: 51.3 MB (51279206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10aba5e63281c08e3cec361df70037367097ed35cb675aa9c8102a20b61f73a`  
		Last Modified: Thu, 13 Jun 2024 01:31:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:d6c43947e566f3b89058b9149a8a5019b3fa6cc7dcf040c221706491f0f06931
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56297184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720f2421d1dd06e6abd964e714422b1d324a9b0c73df52a1f9bdfed627c2df0c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:19:50 GMT
ADD file:c0f742f5a573473fe32bd2303e208818bebfac551d2e724b46c7592fd23c03bb in / 
# Thu, 13 Jun 2024 01:19:53 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:20:08 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5a4f4bea5771f3cc7e0e3d3df946acfbe0781a7bbacf73a3dc2076694f16a928`  
		Last Modified: Thu, 13 Jun 2024 01:25:56 GMT  
		Size: 56.3 MB (56296961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d596c5a188a1fd4490a51ed76d1316e5f7d309a21b04bfde90f89330021ac30b`  
		Last Modified: Thu, 13 Jun 2024 01:26:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:d8564c043b96e14451bf5b27733a899f90960b5ae6513f3391ee4147f4769d43
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50715979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b059146f68a9320361e08ac2909e90ae292290c4f114d9677e3355af40d4bf34`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:33:36 GMT
ADD file:bd75ce513a1cd4e1dcf03472bc2246bef166b6cac30321e05001eb699626feeb in / 
# Thu, 13 Jun 2024 01:33:39 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:34:39 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:417bae7710696ae32abd510e3ba1f59f127a3be7dca2de95632b8dc9f4baf55a`  
		Last Modified: Thu, 13 Jun 2024 01:38:32 GMT  
		Size: 50.7 MB (50715756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c5224f3cc9a1ce6f8627fa691d3eb97c5163187da471d2befb01c4ecc14fe`  
		Last Modified: Thu, 13 Jun 2024 01:39:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:fe13dd9173997c3c635ab38e8b750447dc00470cb4f71b8566f5fd331aee7803
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52054625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96818ab0be8408472d1391e28d5696003b59d1e17fbdad2400807212687cbcae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:45:56 GMT
ADD file:1cbd288c9973cca24a784013268a6407731c6606f529134567c162da1d143fa4 in / 
# Thu, 13 Jun 2024 00:45:58 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:46:17 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a0759db133a573847da61ab8e01bdc49bfcfd141d195de276e707216b4f465b2`  
		Last Modified: Thu, 13 Jun 2024 00:50:35 GMT  
		Size: 52.1 MB (52054405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3daca2c4a7cf4dd9ebbbc3235af238e6141faa007561b6e9a450ff8eb02560c5`  
		Last Modified: Thu, 13 Jun 2024 00:50:51 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
