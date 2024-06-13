## `debian:experimental-20240612`

```console
$ docker pull debian@sha256:5fbac6733f137686cfea56e6d5e030992424d121dbae1f4d87ef0545959bf23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; arm variant v5
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x

### `debian:experimental-20240612` - linux; arm variant v5

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

### `debian:experimental-20240612` - linux; arm64 variant v8

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

### `debian:experimental-20240612` - linux; 386

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

### `debian:experimental-20240612` - linux; s390x

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
