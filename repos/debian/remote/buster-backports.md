## `debian:buster-backports`

```console
$ docker pull debian@sha256:ca903b9ebafdbcf363c5aa52f875328005c00461addd0c21d9c2d41bbb33b5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:046da921bffdf4a5eec601509d7952ebf4b8ef31b6034a66d6a675a45a55e616
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50499693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0381a8125017cb0ccbdb3dfd42afd58454229575503bce4a48b5f21220b2795`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 05:22:13 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468284df22e87f37190c2061d8d1609132a76308fca1c33cfe7c9347e50cc681`  
		Last Modified: Tue, 21 Nov 2023 05:27:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b6c70e145a58d84eca06af8882f2248a355684a780c8ec0a66e58b3c03e42bf6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45966534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b2cf67cd7b10d6d8424731ab620b951dcb61b9b690137345755114d91d775c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:58:12 GMT
ADD file:e69e944c7b28ca650586e3fa2bcb51c4c99491167bee97c4ab32982eeab66750 in / 
# Tue, 21 Nov 2023 03:58:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 03:58:16 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:859d411365ce23ca0a7fbddedc1babff0039e814c09756ad01c59527ebe62dc8`  
		Last Modified: Tue, 21 Nov 2023 04:02:56 GMT  
		Size: 46.0 MB (45966309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62db21155347660f4290e33e6572b395c7f099c20f9cff08a9e238a7284db2eb`  
		Last Modified: Tue, 21 Nov 2023 04:03:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:407c83338acc96eea08385cce267e6ed51d93ac8a0a328acb937ff2025e89787
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49291369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e853a16cfda8f73cd4673c0c5fdeca6921662f945ebea541f769cec74d3080`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:27:30 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94636a4be4146da57e0709ac95ee6011fbce0702bb6bcc820345cb33891d8f05`  
		Last Modified: Tue, 21 Nov 2023 06:31:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:4b77606913bc1d33e3a0f2ee23e2419caee3ad7b4c79d5856bbecb219fa9f10c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51256355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50ff3451597f834cfd122eda9ac1420ee89bb2f5f1abd908fef44a817b14f9f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:40:26 GMT
ADD file:3a91c3eed04829ed9d8801ae9da9d5dfb67139d59f8b98f87943131fc8953b49 in / 
# Tue, 21 Nov 2023 04:40:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:40:30 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d9ff368d73b50f922dcf47b179053552ad7a9257e80ae0ef12ba15c8ca86eb6f`  
		Last Modified: Tue, 21 Nov 2023 04:45:46 GMT  
		Size: 51.3 MB (51256132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4783eae5f635ec321510fb6e0fccf89335526bee7a495767433b744aa225b2fe`  
		Last Modified: Tue, 21 Nov 2023 04:45:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
