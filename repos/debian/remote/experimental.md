## `debian:experimental`

```console
$ docker pull debian@sha256:f9cea4fed52c7fedefd3ee9d334b738f6df7eb4e340868645912f8f06fe54ebc
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
$ docker pull debian@sha256:4c9c619e44b7a16292bdc8104d2775e2e03f20d27da33a1d0e3bf2feaabcbb74
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (55984906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290aa9f7164dcbd86090e3f8d271fd4eb322ca5b3c4acff90935fe53ee76ca0b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:07:22 GMT
ADD file:bc3c9015bb239dcb67cf197fec1fd39931d41dd23ce1b8eff8b79bd424ea3762 in / 
# Thu, 17 Mar 2022 04:07:23 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 04:07:35 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2398521c41656e9b327837382b28fdcd3d0f605580556b0ecbb0ea21b69542d5`  
		Last Modified: Thu, 17 Mar 2022 04:15:04 GMT  
		Size: 56.0 MB (55984685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f094ea90483cd4c70a8260478f53667444af33b6a89710b2b25756542b32e5`  
		Last Modified: Thu, 17 Mar 2022 04:15:28 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:304ab36e89f022f1077f4e60e7255ebcf9b2a87773de12124b1d933cf74374d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53393704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4ba745ba1887e8c52c8feaf3e49acff93a5b91b1b6b103f201db58a26459bd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 05:26:43 GMT
ADD file:366f6307e2968600cdd85e905108bdf6903b1a09ca23945442214bdd85343763 in / 
# Thu, 17 Mar 2022 05:26:44 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 05:27:16 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:4ae1258dcec2b7a026a3807ea7d8516d5c816756d875afa47104d5d57cf62f6f`  
		Last Modified: Thu, 17 Mar 2022 05:44:54 GMT  
		Size: 53.4 MB (53393480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ae372e3a7ec0d79a091e1430fd0942ff4a683e1f8de732b64dc5600d524e30`  
		Last Modified: Thu, 17 Mar 2022 05:45:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:5299b4db362c0c50536ae37647abb32f050a9c61522f75364323013acb0bbd2a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51008335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b3c19fc48faae9a0d2a31217b3d2734b7421a88323f6eb786a3ee823990fd1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 09:38:32 GMT
ADD file:0e937512039da7e535dd1d9cb3dcc393ebdbd3c6f6ab174605715710e14d2492 in / 
# Thu, 17 Mar 2022 09:38:33 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 09:39:07 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:4cf093cf4be0e22f96681812b720a75157146b64fb090429d2f599aa0d504510`  
		Last Modified: Thu, 17 Mar 2022 09:55:34 GMT  
		Size: 51.0 MB (51008113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b8b4627b34d1bb31e0a12197bdb046c4c5dd36db4eeb51595822521c52d17c`  
		Last Modified: Thu, 17 Mar 2022 09:56:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4f88d9d2a85acc2b24d060a313c6f40ec9571f5d0d24b4cdc753130a14a19c24
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54917067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f2fd8bf4201d2bb6331d4c07f3032950783dc2612e3b744721f98a4b8f143c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:24:51 GMT
ADD file:bcc84755136e92419c0af0bfefc5de949afc5c59b2a4d4486d938994b6c5d7dc in / 
# Thu, 17 Mar 2022 03:24:52 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 03:25:07 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b86204abdc203120a866b579efb1ef69c5d47c3a0dfed61e847416f1259f1d97`  
		Last Modified: Thu, 17 Mar 2022 03:34:04 GMT  
		Size: 54.9 MB (54916843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef446e0be008f14f8adfc62ddae7033d640e938a155b766e9c308542bfcc79d`  
		Last Modified: Thu, 17 Mar 2022 03:34:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:6ba61825419238c35edc1a0b9189a27cb7ada5bb79b75123610fbe1763d8b1ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57031588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed6fb54a82fa690e234ce0daf3b9fcb85de731daeed73e02501705d9e03b275`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:19:40 GMT
ADD file:21e7c1e2d49f672557c19eb3465b89ec6ecf7cc7aafcac2b57bd9c968e04fc26 in / 
# Thu, 17 Mar 2022 08:19:40 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:19:57 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:111e10a77536effca910373723babfc3d3f5218cdc5797258e39c63555895485`  
		Last Modified: Thu, 17 Mar 2022 08:30:07 GMT  
		Size: 57.0 MB (57031367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871d256939b900f784839840e2820ca4d5ee65ac21be255e949e6e0b9481ff02`  
		Last Modified: Thu, 17 Mar 2022 08:30:36 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:80b4691da848c6ac96c2aca500f7d4f8c2360cb0aa092a51ecf73c811f7345a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54637075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6aebb2dc833f8a89c2db87865f54a15a28aadc59ad335d4d2781be33dc1888a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:59:04 GMT
ADD file:2478a4b21d6dc18e72f68cbd786bc6d5dc08915244ebed49ca04b0224d950380 in / 
# Thu, 17 Mar 2022 08:59:08 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:59:43 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c63f4c2724bcd37207b20ea95bf1cf9e98a67bfc02b309a3a308abea52dc7156`  
		Last Modified: Thu, 17 Mar 2022 10:50:20 GMT  
		Size: 54.6 MB (54636852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22877f115b31225cabfc4704be1182d64a16464b59fb16038c3529214b8612ba`  
		Last Modified: Thu, 17 Mar 2022 10:50:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:e964d68a41ad5b3cd13c9d2715f950fea5935f9e48412d34cc489ff15f26d704
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60406493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8344d6cb68dab0c76665c186eef760b114e6cfdac0152377652fcd6986bf6fe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 11:23:02 GMT
ADD file:bcebbd2c7c59a465c708216c96b82d4c94ba73f017ef8a5dd1b60b44b18bd788 in / 
# Thu, 17 Mar 2022 11:23:08 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 11:23:51 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:94a163b2e6f9ece0c9483ec0b0e5dc84879ef092f8008580b7f105d55ffe6d50`  
		Last Modified: Thu, 17 Mar 2022 11:33:04 GMT  
		Size: 60.4 MB (60406268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5836f2c31bb300884ea1065aa32f088f05f73bdc9fcb91ec474590cc75378f19`  
		Last Modified: Thu, 17 Mar 2022 11:33:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:37316c0f909830b5efe4dbb58666894c4005f08e6685bf2344ea8521a5ac6a8e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51661326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9588d3734b6ae66e8b31d62e16a2e3e929223468be161b85f2000fa6acef4438`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 01:18:48 GMT
ADD file:4c626b63b204e5b380c4353fba76c9209898643fc24714a7402d674240b7f135 in / 
# Thu, 17 Mar 2022 01:18:50 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 01:22:32 GMT
RUN echo 'deb http://deb.debian.org/debian-ports experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:6b90dc0fb7a457616d51b32f63c1e124b99d9706125517451c463c0d7342659e`  
		Last Modified: Thu, 17 Mar 2022 01:37:34 GMT  
		Size: 51.7 MB (51661098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e057dd15b886a293ed89588ef54cad4a4bd09a8d38fab67dab235e70c74382e`  
		Last Modified: Thu, 17 Mar 2022 01:40:47 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:e8883e987663e06408af13e0084b66ec7c422e87997682d72621cd993fd8fba1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54246877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772e073abc1808bee9f5ba32d400481c4dc647cf3736abd7d1b4276bac9beb42`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:09:36 GMT
ADD file:b88d00d93fbe7e21fdc29185cf31013d7e28197d4fcca9afbc15296e05e9ba54 in / 
# Thu, 17 Mar 2022 03:09:40 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 03:09:58 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:65932861d151b420a25002631af42473ebf8e4d463cea3d66ae0a10eb1728680`  
		Last Modified: Thu, 17 Mar 2022 03:15:18 GMT  
		Size: 54.2 MB (54246655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e95f4f0f7d055d91e76cd8497fab67473bd6c738613b9a5f0c283eecd479c5f`  
		Last Modified: Thu, 17 Mar 2022 03:15:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
