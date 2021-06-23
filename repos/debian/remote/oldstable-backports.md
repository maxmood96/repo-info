## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:2c69ab4cc29c2bbf7a2be75bd9c43e273576e0b29c70fddcbddfcb5aa36ae688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:554a3ba630a8e0009535d82a5dd463429031a7cd0e039f6d63c8abc3b7669752
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45380240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4074363c08c392c59db6a03974a4a76f77749040cf07cb25c90aeed40c2359f6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:51 GMT
ADD file:792d3cc1cdb0bf89cb5a6468d9d014710786214b1a1927780b6eba9756f0dfa3 in / 
# Wed, 23 Jun 2021 00:20:52 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 00:20:56 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6afbb7eb25b12139ebd740fda842011fdf35e40c2a88a59038189647d3be526f`  
		Last Modified: Wed, 23 Jun 2021 00:26:00 GMT  
		Size: 45.4 MB (45380012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cacb8e3787ffbcae898fe641565ea14bab1dd896b88cb30552ecb427f9f5b61`  
		Last Modified: Wed, 23 Jun 2021 00:26:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:d110556b8cbe257b281b3cf8e06c1cf7c62547650204d56d8ee62ca45304d4f2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44092226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc357b9fa7e5ad0da3b494c7b429613bfbbec515e4c78a4c0a16b546d4b9e6c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 22 Jun 2021 23:50:33 GMT
ADD file:f29150372f5bb6d22715a0a561933920920ed3d56d508843a318769ea6d8a556 in / 
# Tue, 22 Jun 2021 23:50:34 GMT
CMD ["bash"]
# Tue, 22 Jun 2021 23:50:46 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3fd3f1b6ddf83f33579c6342d86f05d67d53e392360d7001d759b85c10a01d42`  
		Last Modified: Wed, 23 Jun 2021 00:02:32 GMT  
		Size: 44.1 MB (44091999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a7f36c54a8a2fed054b826dbebf0488325bb478e42d685ab12cf43f0baf9f5`  
		Last Modified: Wed, 23 Jun 2021 00:02:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:7cbdc1e6dd2fccc8ce4883045fec3a7056f496faa6c6750dd5d18773b6fb3214
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42120150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5802d8715cc453d6ddf900874c07e2f82a8d845ecfdc773fadf1d65590d9823e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:53 GMT
ADD file:6149df75ddf19d47690e962c672d889496581efd3f91c8de4a5035268d0f3c1a in / 
# Wed, 23 Jun 2021 00:20:54 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 00:21:06 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:26957e3a4db2d81be1b1d8cdb0f2c51181c416a7987c443f1be43fab133e5877`  
		Last Modified: Wed, 23 Jun 2021 00:32:35 GMT  
		Size: 42.1 MB (42119924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1468a6c089040bf5cb1d8944e42c7e25735b0f3cc95e5b909c78231cc8f4a1`  
		Last Modified: Wed, 23 Jun 2021 00:32:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6c90357aa624ce6f7b3e2ed48f584394022d63461e607a27c00449c3c52ba49b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43177702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce454fe743e501b1bb43db8342c9e2a1bb06aecac363a8306e543973750f389`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 22 Jun 2021 23:49:50 GMT
ADD file:0331982bf935eca8d3dcc09d3ca81439c8f2f5cf859ee570d19ecf612dd853e1 in / 
# Tue, 22 Jun 2021 23:49:51 GMT
CMD ["bash"]
# Tue, 22 Jun 2021 23:49:57 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ac82cf4a7d6519391c2c270363b89764f926e23ef9ccc0fb7ea2fccd81e669ce`  
		Last Modified: Tue, 22 Jun 2021 23:55:49 GMT  
		Size: 43.2 MB (43177477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35999692593c8537a0604e18adb5e528ddc5cbd62b005fca4479d1c22f1e0635`  
		Last Modified: Tue, 22 Jun 2021 23:56:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:ec87a8e9573504958c0cf2850c67eeb4b35a8e61be356e23cd866f455f6bd8cd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46097210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4453eac24c68a740ac2612779e0750e82fac3eef0cbe2f89cece1294b8df11`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 22 Jun 2021 23:39:48 GMT
ADD file:470acd7b77f6c2fb762b018ad9dbd7f4ca32d544ea3b95977f863b8003f53227 in / 
# Tue, 22 Jun 2021 23:39:49 GMT
CMD ["bash"]
# Tue, 22 Jun 2021 23:39:55 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:23818e00c7991d0a44bb1e736fbea96c5b2b25848703128323db8de5a4780983`  
		Last Modified: Tue, 22 Jun 2021 23:46:51 GMT  
		Size: 46.1 MB (46096984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033a69276a78d14f7ccfca6bdb709f909cc0bb0b5a7e555405b405ea5b25648b`  
		Last Modified: Tue, 22 Jun 2021 23:47:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
