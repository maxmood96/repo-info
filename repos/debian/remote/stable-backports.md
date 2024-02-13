## `debian:stable-backports`

```console
$ docker pull debian@sha256:30feae6d417b812d6a1cfc385b1f22e17365d9b6ab152d99a75d0dd53b6ae2af
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
$ docker pull debian@sha256:0eaa097bc73bc1822caa49ad337e09c36811da75435ad0f5bc48b18b9db546b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45153824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3c3664663a5a1fb191e61440a560690b58bf113baddb362b13a35006978165`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:23:00 GMT
ADD file:e3439a4810952ae06cf3fe7fdd79da280e631ee6dc095c998336ebcbd59b8194 in / 
# Tue, 13 Feb 2024 01:23:00 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:23:07 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:32e242ecc0526eb5f277f21daae9bc92ff14010eba6be449bd732c97c23deed2`  
		Last Modified: Tue, 13 Feb 2024 01:30:30 GMT  
		Size: 45.2 MB (45153600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d56652aa459c5c86c9bd0ceb0ad9d73141055ef15d527e6e9edb3a502126f3`  
		Last Modified: Tue, 13 Feb 2024 01:30:42 GMT  
		Size: 224.0 B  
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
$ docker pull debian@sha256:f18ccb0a80d8bf0717c7b341b009683a6058adf85d5f9d204964291a3aa54191
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49563387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41efdad266d478103569500c9d20c5f9f0e008f3fd5922d618416068e36100c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:08:22 GMT
ADD file:7bc0dcf4427df06751aba610176a833cc61f3bf48d6ffd0882213d0f3ff2bff6 in / 
# Tue, 13 Feb 2024 02:08:28 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:08:43 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9675d1c424b57ebf1257b9f640c41ff5d4338d9ac5243254eddf6c1c266250cf`  
		Last Modified: Tue, 13 Feb 2024 02:19:54 GMT  
		Size: 49.6 MB (49563165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c4b1eced6ef00f4e0289f1d81fb723f0e4bd3e439befa1be263551ee3d2493`  
		Last Modified: Tue, 13 Feb 2024 02:20:04 GMT  
		Size: 222.0 B  
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
$ docker pull debian@sha256:a5a616786ec86c127c00048c7be82f46791939aaa8b48aa1b9dafb15687c6bad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47916512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35f538e58ac6690fb73eccdf1542e1fc99f286f2bfafef002a4175e82ddc4f0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:13:34 GMT
ADD file:add114ef27d64c9c20b57371c7f484cf88a012747c89bf71d9bdae6051991786 in / 
# Tue, 13 Feb 2024 01:13:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:14:42 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0a7ac0df0cc7ec87d2eff30fc519f1c7d8fc1ed80b4a5406f6a95c0aec9acea1`  
		Last Modified: Tue, 13 Feb 2024 01:31:53 GMT  
		Size: 47.9 MB (47916292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20573823f9a9dcc8196f13c6fb4de9948117d765dc2755de2aaec6eda8e72fec`  
		Last Modified: Tue, 13 Feb 2024 01:32:00 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
