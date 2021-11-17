## `debian:stretch-backports`

```console
$ docker pull debian@sha256:15cd80462228e0ddc237e2890ef3111d70ebb130d2769608f6594c503755e493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:stretch-backports` - linux; amd64

```console
$ docker pull debian@sha256:548c41c70872c618c0b675c41b47de1fc1815ec6df921e2354605132d4f90255
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45380665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083e21a8f2a7c9c2e0432e1d7a259c6633a26e2d0f2d6ea28b198ac692f56dfa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:22:28 GMT
ADD file:d7365dd9cf34b10ca189f85c95c21a0c33e44092f85ffb5884d5e737fb0b9be1 in / 
# Wed, 17 Nov 2021 02:22:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:22:32 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:200cae5c9d88bb9cf1dd3fcfb831d671403f078d2310416fa3b304337d8279c0`  
		Last Modified: Wed, 17 Nov 2021 02:29:09 GMT  
		Size: 45.4 MB (45380444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f54e01827d8e94188e47a454ee3cfc4c35991a75e866eda70c07e717257bce9`  
		Last Modified: Wed, 17 Nov 2021 02:29:23 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:1105e6f97d10f16d8577c28562fbdf2680651fe14d0a9271465f8da69914aad5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44091603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c788c320b4b1d7de55e92a031a349f458e7eee92bf6223875749f607bbc656df`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:55:43 GMT
ADD file:a8b0f40ff55722f4bb2e3ac65c3fefe9acaa513f89b73ed81ec04585058e58ba in / 
# Wed, 17 Nov 2021 02:55:45 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:55:59 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ec68ab8028a430064eed52d9b833f1a135dcce543b02666ee5acd73962b79070`  
		Last Modified: Wed, 17 Nov 2021 03:13:32 GMT  
		Size: 44.1 MB (44091379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223bbcda290abdf4a569960d4972eec20a6eea5a6fc6e34e5867907660c4c6bf`  
		Last Modified: Wed, 17 Nov 2021 03:13:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a9780d74a1fd954fa25160ce85876afc392fd4b73a97255d62c73e1dc523d135
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42117091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c152949883b1df7964bdeda015e14838286c784556d1821f72d56d1daea0634`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:04:57 GMT
ADD file:61da3fcef3aea99b4927189cfcb823a65b0e911a3f4436e44ea84a57a7919ff3 in / 
# Wed, 17 Nov 2021 02:04:58 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:05:14 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e4d54b576c2fcdd259e57bac14c4e1a2623f6e5dc9a0b1facaed7fe59d891e86`  
		Last Modified: Wed, 17 Nov 2021 02:22:03 GMT  
		Size: 42.1 MB (42116868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0863f9d3618f76a3e2652e9cd24aba6bd6ab604d9f02e4b392a7512536e610f`  
		Last Modified: Wed, 17 Nov 2021 02:22:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:af26827a27bc09d7cd71161319d6a6eba1700194c180b6cc7d81dfe4bf20cc9d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43174702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8f1701705027ba87c0a6af67888a318e98d809f6a1ec5d67fc275967f7246f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:33 GMT
ADD file:3225671be4edc3599e29ebd06516b95573246e68bf29649c402ed87c03c109b5 in / 
# Wed, 17 Nov 2021 02:42:34 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:42:40 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c64a4bafe4ad6fc05fcc6d76d2a06f168f331ffbc87e518fb4ca4ea22e75527e`  
		Last Modified: Wed, 17 Nov 2021 02:51:11 GMT  
		Size: 43.2 MB (43174478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a690cd9aa3033cb40ab740972092e393663ef9cb10a5ba27aa278b4f24d3d8f4`  
		Last Modified: Wed, 17 Nov 2021 02:51:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:08f56a672a3be4918c737a684a245f177f5728a099de26aab0663741c84edf11
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46097424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7af8d6205985b858dc9b036fb0eb8257654bd126ad51cea98724a859b29c27`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:21 GMT
ADD file:8e57eaeffee1cd4c93865af9d6370c68bddae095016766191b1338ae675f131c in / 
# Wed, 17 Nov 2021 02:42:22 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:42:29 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:24fc2b60c45394a399438249c8e7f92f6fa415f9c477524d5af3ab4782d51519`  
		Last Modified: Wed, 17 Nov 2021 02:52:15 GMT  
		Size: 46.1 MB (46097202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cafbbbfa23d42895791cf343cd8e71cc3e89946dde5df1af9beb9c2061bec6f`  
		Last Modified: Wed, 17 Nov 2021 02:52:36 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
