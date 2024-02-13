## `debian:stable-backports`

```console
$ docker pull debian@sha256:de8a86db40f91c13128353a20036f5237132bd35c5c02be7e580f07de0b388ea
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:870270f928668da71ab6f1a817810383417908becf43c7b8e13910316e7d7cad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49552789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e85b47aa9083ae6a98128fc63c047cd44aee9f9d5832f98cf14d5ae1f5fd0984`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:20 GMT
ADD file:2dde0a7e9ef53cd86819c867b4da97698b6b839967268fa80bd1cef2866c25a5 in / 
# Tue, 13 Feb 2024 00:39:21 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:39:25 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a736c84bec8e30d55ec61a8187f373cce1bd36d001fa0267ccb14868373eb4a8`  
		Last Modified: Tue, 13 Feb 2024 00:45:26 GMT  
		Size: 49.6 MB (49552569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c289f1de1c71b78d5abc211474634c7822d824902893842b8f97e10bee4758f9`  
		Last Modified: Tue, 13 Feb 2024 00:45:34 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:6269001fa1849d728b8fdecb3486fd5dc5185cc2a33080ee85da375bacb259d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47312046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8f68523ca449dcc6d0c9d22d5d79c19a7323cdd31b844c5bcd3ce097d22912`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:10:00 GMT
ADD file:1608126ed8a5c15f429c3b7b7cba45b1db7a19cc957134c77b113a8234a1af86 in / 
# Tue, 13 Feb 2024 01:10:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:10:07 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6edd61c543d6cd97475f744a3bca1bb6029be932c2566f1233274535a1700913`  
		Last Modified: Tue, 13 Feb 2024 01:16:01 GMT  
		Size: 47.3 MB (47311825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def66dd764c15e4557a9d2e019b790648b06466a595ae449ef5061e1001a44f3`  
		Last Modified: Tue, 13 Feb 2024 01:16:10 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:e017115cf7479237d8cbb8ffa16b10554b8f1126e13a41812ea827aa5d773f00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45178208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0408cb923b5299ea4e16c485bb2f1ccc11316a0168401c110c2016ceee85cab4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:19 GMT
ADD file:6f2e49ecd351621d072153d2ab7e35f14645e2ed4f6251af6aeb3a272edfc936 in / 
# Wed, 31 Jan 2024 22:46:21 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:46:25 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2e56c8cbe9126c438a883217ecb653a84f1d36c267a42c563926e93c01e44034`  
		Last Modified: Wed, 31 Jan 2024 22:52:16 GMT  
		Size: 45.2 MB (45177985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0030aabb3951fca4e0418a0b25bbd7384bfe09c670217a91594aed098422b4c`  
		Last Modified: Wed, 31 Jan 2024 22:52:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4d392b0d94f18801e057393f1a1b4a3c20d12d192f0f02db44910ae2a0481509
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49591140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db570ab482b49294d993bb7f3c21668b60bf6f064f2fc254573429ac221b19e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:42:38 GMT
ADD file:d85da3262f212b1e44608f762a88a7a575d1bcb6d1830b9d0f664685e2ff8f8b in / 
# Tue, 13 Feb 2024 00:42:39 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:42:41 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4c4ca193ef91833b89cca0efd7e812118a8d2959acd35887a258596db4ae8b27`  
		Last Modified: Tue, 13 Feb 2024 00:48:02 GMT  
		Size: 49.6 MB (49590919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45fa9b10efc2efd857922f941ad2657936afe978d89df3b03d6aa27452696d7e`  
		Last Modified: Tue, 13 Feb 2024 00:48:13 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:557bbef503af1c2c11667482e1c4e50e657cb6ec545bfc95ee5796ab1f7bec70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50582153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127dc8ea62a2dcadb6d0196f1e20c88b054ebc98d1e740604d9ed156195884c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:59 GMT
ADD file:7e8e5402b0205e490c190998a0f5567509ccc3ea2fb231221316fe6f9a63a384 in / 
# Tue, 13 Feb 2024 00:41:00 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:41:03 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c6aeeb26c7e0fd85a61f10fa03deb67731003e13a803f8c2aed336f075074546`  
		Last Modified: Tue, 13 Feb 2024 00:47:44 GMT  
		Size: 50.6 MB (50581931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af830e9c0af61a38d8bf68b3dc3f45990966454d1a7f21bda977e0976c238c2b`  
		Last Modified: Tue, 13 Feb 2024 00:47:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:a6262e97f8d0d2f7a3e9f8ce1b5122a616d17b49c124519c3e9d320713355f7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49574269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d1db487bfcc61515ba302f79f39fdf00e9db1f1c28dda7b5de9808d5ac8ce0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:31:27 GMT
ADD file:203306375592f1b8ef48799b70a073323b34e37dec1a891045e5026e2ce71e6a in / 
# Wed, 31 Jan 2024 22:31:33 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:31:48 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:01586de3973913eb5e048c706ff7156913506104dcca09966de5d521173a56eb`  
		Last Modified: Wed, 31 Jan 2024 22:42:55 GMT  
		Size: 49.6 MB (49574044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989bd2de4e73aee4b213b570e418f68b1d7cc4455d96f8de964dd275d282f046`  
		Last Modified: Wed, 31 Jan 2024 22:43:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:e5ba487877ae6d77280e144d42051d316dd2bdab14dbcdcdd47afaebf38d0757
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53556736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45379497d4e8d680850b3d9db073a89d5ef6b2cba08314b09628bd752b1e165`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:43 GMT
ADD file:262dc74a2600b45d07b56f461c516ffebde52186b68b95c615ff0932f8524745 in / 
# Tue, 13 Feb 2024 00:40:46 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:40:50 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:69e3ba92080aea86126240745aefee8ca4458480f819b9ee0266774a30636d75`  
		Last Modified: Tue, 13 Feb 2024 00:46:31 GMT  
		Size: 53.6 MB (53556514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61959e73e136969f993653be96c4aab5dc996ce051e0ce58f085cb2278d4846a`  
		Last Modified: Tue, 13 Feb 2024 00:46:42 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:a5d3943613ed690960440ec14c470bee286a9cc6d04d3404cd08d2ab345fa2c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47941009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b765a6de9d9505c50b24f58204c75ef1e12e166a2203498cc861be24cd6ffd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:10:40 GMT
ADD file:0f5ed8b62165f1914aa949b60fdb485e77a142aa953b815fb5f52182342d022f in / 
# Wed, 31 Jan 2024 23:10:44 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:11:57 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5b662a61845417f74a9f7ea4719726885b4f3ad7f9de803e35342bab13cd53bc`  
		Last Modified: Wed, 31 Jan 2024 23:30:45 GMT  
		Size: 47.9 MB (47940787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4351e40f6890f45f7b249c40758ecdac9f7af840973df028b827876a3eefe08`  
		Last Modified: Wed, 31 Jan 2024 23:30:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
