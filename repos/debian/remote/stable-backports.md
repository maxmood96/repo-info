## `debian:stable-backports`

```console
$ docker pull debian@sha256:31b27b5284d167f5ac2ebcb4bbbc82b666cc4382c2a6053f4e4dbf02639489ea
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
$ docker pull debian@sha256:be66163a49ace1f23b224d1d4451a228ccd67664a918b614e8824bec7e773482
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55029958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbed3c5188441a08ba51d0dc00a67d86bdfb3b4e19afa67234145e5dab4fc452`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 00:57:33 GMT
ADD file:57088f13d9b85537ab9ccd327018b098c2e57f2ee2e1356e79cefc0f2fdc2760 in / 
# Tue, 13 Sep 2022 00:57:34 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 00:57:37 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f1e379b15ae030f3314a89ab08091556b6908686b2c832074e178f3c24666e60`  
		Last Modified: Tue, 13 Sep 2022 01:02:41 GMT  
		Size: 55.0 MB (55029736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bcfd9c12dcbdba6e02a533812444e4825c6b433bca157e1f5f4a19d9a8bfb2`  
		Last Modified: Tue, 13 Sep 2022 01:02:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:0ce7d54f7461a0e16df1ead933956aca3902985f0ceb7cab86dfa28ff01b5de2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52532430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675beccbc352e917e7e1c45b52bed92fae8eed43fd2115891ddaf7cd51322efa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 00:54:36 GMT
ADD file:b64be57dd449eb3bd2e5319d0d46632d2c277352b68db8d4a9c45c96896b2de6 in / 
# Tue, 13 Sep 2022 00:54:37 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 00:54:45 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:43faf6de0705a21d8ef228cbcb7960b4e2a3bab50c1e4556ea52fc3f2cf9c214`  
		Last Modified: Tue, 13 Sep 2022 01:02:33 GMT  
		Size: 52.5 MB (52532206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836999b221109912811a01ed70ee8bb77cb0a0eb1f85bd4235521f0edcd22033`  
		Last Modified: Tue, 13 Sep 2022 01:02:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:deecbcb10478e113b2a301f914f1069465664dc03170713cfdd6c7913b8ee384
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50195780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f2d1e0d31b09f2250bb697b3930eeb3e6d7092f544ccf90d75c5a83c5fbeb4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 03:44:31 GMT
ADD file:c7bb448986da57380e213e5b028975c8a77c3fde515121b13289fb2f28067b23 in / 
# Tue, 13 Sep 2022 03:44:31 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:44:37 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c2390c1cc1dfb42197f7df435c60d2e98a44a4617ebc2660131537b80d1f2256`  
		Last Modified: Tue, 13 Sep 2022 03:52:50 GMT  
		Size: 50.2 MB (50195557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbb4654e3af1dd486ea150169281ef11fc2d6f675f920072c769401787f2306`  
		Last Modified: Tue, 13 Sep 2022 03:53:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:81999e9eb3255d77e034a49af5b24be70710dd0127db1e5f8b748802792f7a0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53691611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0fc581e274bd7cafd91f200e5d58b63e8628369dbb048af256abfa4b8602abe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 02:12:12 GMT
ADD file:468f196709424e5890038843fe0d700bea08323502b70651aea54a8a3ad21a45 in / 
# Tue, 13 Sep 2022 02:12:13 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 02:12:19 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fed3d8424be5b8e0a375b613df7969d63080daea3dbed2cb99a70335b2895a11`  
		Last Modified: Tue, 13 Sep 2022 02:18:44 GMT  
		Size: 53.7 MB (53691389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87115726926e2cda3b729f9fc459008c46afd5a375ba947699527e218b2999e4`  
		Last Modified: Tue, 13 Sep 2022 02:18:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:46c4c5595784007b9572670bd9230fac11e6a44c665c56f08e63bf617d112e66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56010004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a73d39cdee99e3cdd445c1aeef96cf82c111e61d7b5d851f1c5704b92d6097c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 01:41:09 GMT
ADD file:5c00ca16f61f466c3c73954b1baeccc3532a41ae751cc946995770573c8738af in / 
# Tue, 13 Sep 2022 01:41:09 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 01:41:15 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:39c83621f7eafd0bd2a7260ed203a9cd996fba73e867394ebbf5ba7984022083`  
		Last Modified: Tue, 13 Sep 2022 01:47:48 GMT  
		Size: 56.0 MB (56009779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9285aed4a4ce3074b1889fdb8db1b2163212ebf9f06664f6eb3b908d137320e`  
		Last Modified: Tue, 13 Sep 2022 01:47:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:bf40109b45c3399791f46204ceb5aecc7ad7670079d242bae256544ba91f5afc
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53252031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb1a13c95b6734b40985d11ed1156affc4f636456a45806674731c8d511140b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 01:12:33 GMT
ADD file:8bcff9bb21fa2aad7fbbe9aa53e57bb4eeacc0833fc2611f64b61b3f3b143ba4 in / 
# Tue, 13 Sep 2022 01:12:38 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 01:12:47 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:eff9867c61e40ebbe46d26d9e10f1bc80d58cc0459bcfb8d814f5188a49136ee`  
		Last Modified: Tue, 13 Sep 2022 01:20:46 GMT  
		Size: 53.3 MB (53251808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b90913470695c538781c983522d69a183da96aeefad166ef34f707dbc1744aa`  
		Last Modified: Tue, 13 Sep 2022 01:20:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:7d5795a3e3ef939039ac158cf6282d3784288c8fab4c8791b8cb95ce3bab167e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58902794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd2718201f6d3605d1417975a65b59857c157d382cc13786ad222dd19fb3264`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 02:08:46 GMT
ADD file:21e944dd2f9d22770a7829b1447f2325e72c41d33d10008b94a7cb3670dfa667 in / 
# Tue, 13 Sep 2022 02:08:50 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 02:08:56 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:31163694439c63b285bf43a7331d1a1330df93ee0fd2c274b99113a4c8530286`  
		Last Modified: Tue, 13 Sep 2022 02:14:56 GMT  
		Size: 58.9 MB (58902573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e565b16520de4675905dfe624d613bca796332bd36189ef646a1605a1fd23a26`  
		Last Modified: Tue, 13 Sep 2022 02:15:08 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:e8e297c7834c4d1948bb05548ccf06287969f3f6a8802937b9b8fcfb0b46fe20
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53265038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366792733fcf4497889b5c94a5079efdc85be55e8417ef26e5c7d8a60290c155`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 00:48:42 GMT
ADD file:10e04dedfed81a283cdd807d30be507c7e18a597e0b6e6046ae1ee607c85dc26 in / 
# Tue, 13 Sep 2022 00:48:45 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 00:48:51 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:65e855ca2ae8ffaac40847c62a164755b2fdb4cd855c7fc502c00c7c3ec746c7`  
		Last Modified: Tue, 13 Sep 2022 00:53:19 GMT  
		Size: 53.3 MB (53264817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3f45a0c6770ec197023bace2187f00c99749031c21b578d33102dec028bb0e`  
		Last Modified: Tue, 13 Sep 2022 00:53:26 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
