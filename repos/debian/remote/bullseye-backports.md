## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:45df5f1a1c19ba0ca7120337b318b9259b5b59274de50189665fb83439c266d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:b3b98b935436f43f45688579b7556fada5236bc490b86e940c887386ed9bfb42
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54923058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8030c757eff9d640044497b9cf7501904afe56015412672eec200c2f53c1c2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 04:03:51 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d07f66a00daa6ae24d23d34a13309054ca97c8aeac682be4dbc2bcdc9eedab`  
		Last Modified: Thu, 17 Mar 2022 04:09:53 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:50c0a4db5f92764f9b253dba5a70837434005a1444f825ad923d68be01fa2485
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52470477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832100f8694aeced8508d4ffabd4b4f07b81c26e41f8fd13da82f884df9d87ff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 05:19:10 GMT
ADD file:711abc0c0a502fe727f811a82e7e6175c753593bc9f6d477a47b889fc3fe8ff6 in / 
# Thu, 17 Mar 2022 05:19:11 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 05:19:27 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f6db9b0909e16205c253a4a6e736ed382b68f85839d7822d22d5ddd35fd2fda4`  
		Last Modified: Thu, 17 Mar 2022 05:34:11 GMT  
		Size: 52.5 MB (52470250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07906ecb1340a3334b761d9d168956bf82e0ecc9a614020d0af2851e67a3f8f0`  
		Last Modified: Thu, 17 Mar 2022 05:34:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:0dd58b1b891fe5d46ac2923d47ae70f98006dc39af91d0628f1e8829b055dd68
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50122479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9305fc6626ee992b4372ce53770d0c1d87a81bc3d2a84b877a80764fc112f04`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 09:30:27 GMT
ADD file:a76bfdf79974fef637725f4c4d8afd998baacd9f3852ac94ce4db52fd65edd8c in / 
# Thu, 17 Mar 2022 09:30:28 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 09:30:44 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4a0c373b7fd878320ee1d0810692c38f8079bd0783a53740b236b67ccd6eab4f`  
		Last Modified: Thu, 17 Mar 2022 09:45:54 GMT  
		Size: 50.1 MB (50122251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b6688870d26d090b09c3b0dc4b261a9b55608386f58676e670ea06933a4199`  
		Last Modified: Thu, 17 Mar 2022 09:46:18 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:2d22169ba6c4b5f10228d592ee2f7ab9c765a24fce0d759c4bc0a739dee5e9d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53616533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f522b03791ac15534712e07df5d95d4374fcb4b3ad9a74e2ddce2c8514134e41`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:41 GMT
ADD file:5effc7e0ab7312f14a7ee81c06c71400aae31219d477ebe1a4f7a9156797c42a in / 
# Thu, 17 Mar 2022 03:21:42 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 03:21:49 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:260ad8146ed2447d5587608b10fed4f80de80cdc559e619f3a235d3ba09eaf7b`  
		Last Modified: Thu, 17 Mar 2022 03:28:04 GMT  
		Size: 53.6 MB (53616308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e79573b742949caa26c03c051a018305fd251f648c0bee22cc41fca918296a`  
		Last Modified: Thu, 17 Mar 2022 03:28:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:e2e78c67e181ad4883cd23a608124097326b91431fc82c68f62de7a027454b4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55942637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33260a02ff642f3deb041d81b9234871e1617df21fc7f561a07f701dc66946df`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:15:32 GMT
ADD file:db8b3d2a46fd5f7f175e96ecfedbb16788e0232263c4d22fd79f2c997c6dc9d5 in / 
# Thu, 17 Mar 2022 08:15:32 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:15:39 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c46f89774ba16a64f47622b4e0890ea7dfdf72f98f9c0fe3a99b594f399ce289`  
		Last Modified: Thu, 17 Mar 2022 08:23:24 GMT  
		Size: 55.9 MB (55942412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5897cc728920a776e7ca61122e64767cb710b3e763283cedda7d98317a4223`  
		Last Modified: Thu, 17 Mar 2022 08:23:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:dc800ce44a6d492c01ba0750d554cf4a180ed89c79e2224a81c33e90d0885cab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53180203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac5ac9fdac387677652099b4f79a85b58ee32f61654159bbdcbbca97de64c41`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:18 GMT
ADD file:5beac822d8ef6913f5cda32d2e19a31978679cd0a8f51793343f0616de081608 in / 
# Tue, 01 Mar 2022 02:02:19 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:02:26 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b9a7ad0f3cddab5c27fc342066cc786b37353dfb853deb360bb79e8256fffac3`  
		Last Modified: Tue, 01 Mar 2022 02:11:43 GMT  
		Size: 53.2 MB (53179977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1977023ed4c4123f364d0e16eb5940e35e594bc741a9982cfb04dfc0e0f12e`  
		Last Modified: Tue, 01 Mar 2022 02:12:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:b209bd22e291996830400b13fa0ca7cccf7eb5ffc32ef5805ad16fd42293d958
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58834343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0a0d9c07e7e2f0b83327bbd253322c4ee01391414eb9fcc66566ac9ddd06ea`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:04:22 GMT
ADD file:00554eaeb433a7cc43c22f2544d800896f451a2e5a7895863c4651ed425b8c36 in / 
# Tue, 01 Mar 2022 02:04:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:04:51 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9ff352265b4a055377b95db6dddea03717bbefbc7f30fbacf493764d617ae85e`  
		Last Modified: Tue, 01 Mar 2022 02:14:41 GMT  
		Size: 58.8 MB (58834115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f55afb944092afeb1402d0004dbf7825bb7b6309d8a190f2888de2627dc672b`  
		Last Modified: Tue, 01 Mar 2022 02:15:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:7045f9b96c34e3584baaad174f5b3e682f49c7a62279a77592d1af2a5e8efaaf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53217752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691a5362eec68ee7847d675634e46826cfcd0bda272ae6f30b748e25c01c34a8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:06:38 GMT
ADD file:75b45e65d2ec2c6822b1ddc46ff159dd10ac56bf9dff8b0996ac589a1ede22ff in / 
# Thu, 17 Mar 2022 03:06:42 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 03:06:49 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ae9f1a186a2633be1ad71c317c2f195b221cef89502f9edc510b3a2049723758`  
		Last Modified: Thu, 17 Mar 2022 03:12:26 GMT  
		Size: 53.2 MB (53217527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d2a13dc9534faa54a2fc10c5779eecea53da4c61e4b071be1b9e2a4d357238`  
		Last Modified: Thu, 17 Mar 2022 03:12:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
