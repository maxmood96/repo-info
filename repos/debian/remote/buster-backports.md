## `debian:buster-backports`

```console
$ docker pull debian@sha256:08124eee1a5aebcaa3177f41a90dad1e82f4525ed3f61ba21f9d8ecde4c0953f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:6efd2ae4c36aa57d2f225cd47c51bbc478695198820444ce38126fb5eb0ed8ef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50383152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8984c136ba7ac79be63792aec5c8ea9da7f6cf227887ecd57578c633ad0a8be`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:20:22 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ef6dbd517405e887c80ae5e3dc38151f7f651a17601dba0dfaaffe292b773d`  
		Last Modified: Thu, 23 Apr 2020 00:25:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:fcc5d7fbc9869244da5a02fa6771f98e3782e27b4b6fbb1ab95d4c073b63c094
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48096952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192c311d31f3aaac344cbdc49e51e477f5f1f377f65d0db9f34b32ca9fcb8609`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:51:56 GMT
ADD file:a26bfbb8e57afc6eec1fa313ae92d674fec87fc7a133fa2b9b9e6f009ce5117e in / 
# Thu, 23 Apr 2020 00:51:59 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:52:09 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:80d6a9f0f7670192b63eb185db46734407dead712759839bc8ab18d61d3d6368`  
		Last Modified: Thu, 23 Apr 2020 00:59:23 GMT  
		Size: 48.1 MB (48096727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78455089a72683d4ae3ab0c1d88a0f77e982098118c58c231df40a96492e7fe7`  
		Last Modified: Thu, 23 Apr 2020 00:59:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b6f93a498a4ab646063c1aaca6d892691083f0009d04ba752f0dde82fd5589dd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45864505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01404a5e44aef4c8c0a355201edcff6a9e37b2d5b27aadfbcc087e7083ae4f9e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:03:01 GMT
ADD file:67087d9a080132a9a5865637874fa3dab5059ac619630d071c563e75a7a5d977 in / 
# Thu, 23 Apr 2020 01:03:02 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:03:12 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cb6703531d2fa1d357cdd21991ae844400ecd207dba47fdd9afad54cdd9ce65a`  
		Last Modified: Thu, 23 Apr 2020 01:10:47 GMT  
		Size: 45.9 MB (45864280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b2d456b9685bb6f23681ddc403f74ee334928422701c072394bc882b595baf`  
		Last Modified: Thu, 23 Apr 2020 01:10:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:7e2f9e62b8cb9217992ef94c7de799c9b5f34fe759143f3951fe7d31b0c01844
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49169923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:079cb802085ded7c42b60deacbb80bc9d4fb96ff3ff3331d6f5c22b93fe43f6e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:54:22 GMT
ADD file:c49818672222185a0a985a8511744bd524fce453bddb137364d79a793dc5740f in / 
# Thu, 23 Apr 2020 00:54:26 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:54:35 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6243ff87266a170a3ad584d6c9c13f9b93c3aa84bded170c0040480f6c4e4170`  
		Last Modified: Thu, 23 Apr 2020 01:03:05 GMT  
		Size: 49.2 MB (49169698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d565de8b353c869571cbf5929ba8d80fa5a7eadac58b4f6531e759279c64ea0`  
		Last Modified: Thu, 23 Apr 2020 01:03:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:4c1752a580c0392750db6f75e1269cc195fc457ed1930f0debc27c7f233297a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51147265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b2aef1b82dfbe7edf99508ba75c670cc112f2dbae78e5a9d93782e24dc7190`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:39:21 GMT
ADD file:10751e25934ebcf54b529ebd800a690886012d472846a404b452a1b27dc97eed in / 
# Thu, 23 Apr 2020 00:39:22 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:39:27 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5ca4f2c0deeb8dae824229454aa24e8d27bb031c4d3229fbc5465ac18d0fc46b`  
		Last Modified: Thu, 23 Apr 2020 00:44:20 GMT  
		Size: 51.1 MB (51147043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c047a466c4abc798720bcb0887a84f4c41ba00bc4e16e85ad0ca4117fd8c528`  
		Last Modified: Thu, 23 Apr 2020 00:44:26 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; mips64le

```console
$ docker pull debian@sha256:cb836d44e37b3c8544d984795bfb62dbb23b11b801dcda1a0c2d149285ddff54
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49019384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c9856a411d457c6f70653490652d9e5c0ff105d586dbb3c9e8289ecaf80c7f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:09:25 GMT
ADD file:ef71e7285bfdea3942f5b4db577b5b14ba7dbc37538dfeda1886a6afcef86692 in / 
# Thu, 23 Apr 2020 00:09:26 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:09:32 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7754e26af5c07372dee067377cd032efd21a4266d2a432d0bfd78f25f8cb5e64`  
		Last Modified: Thu, 23 Apr 2020 00:17:03 GMT  
		Size: 49.0 MB (49019159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436e5b125c4940ce0f50e3fe7c2beb3eff8d65906a6fea6573c727694a8afb50`  
		Last Modified: Thu, 23 Apr 2020 00:17:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:f0082da120e79f0562e0fe0b9e11dd4ee5dfa4b6d2e2b9ec09f9463aa0c1a6b2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54139846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b6f16a80524af373e8e8b7f3568a85035a0cfd7fe11689c3c3127b0c329591`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:34:50 GMT
ADD file:31369dd617691a0d7181117a065290be8cd8c32814e443ef0a7c7adf7e9d800a in / 
# Thu, 23 Apr 2020 00:34:54 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:35:08 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6bf15800932473d1ca0a2cca9bfac073da118f1172b9027f7e78394850b02d05`  
		Last Modified: Thu, 23 Apr 2020 00:49:32 GMT  
		Size: 54.1 MB (54139621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022d57b0a4774e928bab4eaf761e4f77d73f3f6109a7e35a1b35d861232ac345`  
		Last Modified: Thu, 23 Apr 2020 00:49:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; s390x

```console
$ docker pull debian@sha256:9dbed9fd25bc4a4770926bfa2b545fd51f03ebbe8de6f8d1624c340b95bd5c78
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48960380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b3f5feef0c9df63747a1faa2821ec2fe3fdcb865cc9b3c780a03ce5840b0b8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:51:31 GMT
ADD file:ff6937c6922875bc0f7ac0b859b2943c2ac9f7b57ac747bae88cbf4e0d5d4848 in / 
# Thu, 23 Apr 2020 00:51:34 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:51:39 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:21544d2d1a0f1cb5666bb8ad68a1dd7dff9022d1f9e2e096808ab6ce5c4c9275`  
		Last Modified: Thu, 23 Apr 2020 00:55:45 GMT  
		Size: 49.0 MB (48960155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2e74d8982b629065e01cbeb16895dbff26e81b0ca034302dd750c7ca52c887`  
		Last Modified: Thu, 23 Apr 2020 00:55:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
