## `alt:latest`

```console
$ docker pull alt@sha256:7e4727efeb6cbf10575622256de51852278cb41b5fe6a73ed33c44cb187bf753
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `alt:latest` - linux; amd64

```console
$ docker pull alt@sha256:972c11aa6503b15245a410c087dd79560e3cf14457546f2df4a0e4b6743d218a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47325626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea43cfc79fff28924b868d618a6c6031086c4d58fabcbd16065e805a37c41f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Mar 2025 10:20:09 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Mon, 31 Mar 2025 10:20:09 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Mon, 31 Mar 2025 10:20:09 GMT
ADD alt-p10-x86_64.tar.xz / # buildkit
# Mon, 31 Mar 2025 10:20:09 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Mon, 31 Mar 2025 10:20:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5d2ed51eaaacac5cdd45c8df69bd5c9a0839624fd27710bfd17a4fa0bdfa392f`  
		Last Modified: Thu, 08 May 2025 23:53:31 GMT  
		Size: 47.3 MB (47325435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909fa0bd5676c6e92a645c81304f666f05f7784ff92293b3c8318ef1067c1fe2`  
		Last Modified: Thu, 08 May 2025 23:53:27 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:685dbd4d17bf3887ba84613c32aa6f4af0ba1f786f8a4e0893c62a7899b17b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2586130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3fc1729229c4a3bf4a330f141edd55a3abeb1550f407ab44f255e35400b57a`

```dockerfile
```

-	Layers:
	-	`sha256:bfb39c1be9d4b237e76ad8ca0ea659a8f59c1a0cf6644f43eac058d2c4230a17`  
		Last Modified: Tue, 03 Jun 2025 19:29:06 GMT  
		Size: 2.6 MB (2579910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e428f7bac8d25fae0a54716946f38b348886e76ab0559c5e7cd86a783f2ce4f6`  
		Last Modified: Tue, 03 Jun 2025 19:29:07 GMT  
		Size: 6.2 KB (6220 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:latest` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:f31125e153872b608dff1fb0c2ec4a1027ba8ddc720f74850957500a25bb7177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46497928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326437b80bd404563787b5d41fd9c35a39c40168aa37b8ce9eb851d192ec552c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Mar 2025 10:20:09 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Mon, 31 Mar 2025 10:20:09 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Mon, 31 Mar 2025 10:20:09 GMT
ADD alt-p10-aarch64.tar.xz / # buildkit
# Mon, 31 Mar 2025 10:20:09 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Mon, 31 Mar 2025 10:20:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bf548d9c98b536ab8509157300f0cf56b89adf17fed5c19121f6e62ed25e3f88`  
		Last Modified: Fri, 09 May 2025 16:17:21 GMT  
		Size: 46.5 MB (46497737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45806454953c68d3f4d9f40f2d1dbae84a1d4fe2b8a5ebab2fa29de9d9cf16f0`  
		Last Modified: Fri, 09 May 2025 16:17:02 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:eb05417b147bb9fc7f5d614aa8ea11385c799a571bac8f271f28034da5048e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf325613a55b2c131b1d5457bcf89a4b977c18fe5c68f2b18cffd9a4636b41da`

```dockerfile
```

-	Layers:
	-	`sha256:12c23add15a1f8bbe968a4b3e9c5af2539a2e23f6b08c4ebd672d0418f5767c6`  
		Last Modified: Mon, 31 Mar 2025 17:22:20 GMT  
		Size: 2.6 MB (2578563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25046bb77d156592f6d851cfc242afaab52d2f1e26673140ec6005f01d0556e9`  
		Last Modified: Mon, 31 Mar 2025 17:22:20 GMT  
		Size: 6.3 KB (6278 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:latest` - linux; 386

```console
$ docker pull alt@sha256:6023e4fd917d0b639a5448b1fb3bfe83452e43c5941cf84d7edc053de80f9bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48062698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef05ca38e9e33c4a92e361a4c3bf925abbfe61fc329ef250b86b8736601fc576`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Mar 2025 10:20:09 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Mon, 31 Mar 2025 10:20:09 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Mon, 31 Mar 2025 10:20:09 GMT
ADD alt-p10-i586.tar.xz / # buildkit
# Mon, 31 Mar 2025 10:20:09 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Mon, 31 Mar 2025 10:20:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0915c2bd92806a19beceb23e719a36d27a0d4568f4a994aecbe3f40e8e85cffd`  
		Last Modified: Wed, 11 Jun 2025 16:54:17 GMT  
		Size: 48.1 MB (48062506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40849c10a4e575dcfc1903e58fbbe02f3060d85b3c5e2494784ba7f6bea65605`  
		Last Modified: Wed, 11 Jun 2025 16:54:10 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:3c6bf643c18a069773958db1fa3b90cce428575f1a2078d7b2abe06d9a6d7ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2587946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4f6da13dd4ac401efa0d2a1a0eee406d2d53546b341fef4e59da67c510a90d`

```dockerfile
```

-	Layers:
	-	`sha256:160cf6d69d2eac555eac32a8b1e53f4e4cc964d1f7f4cbdbf843c145a7b65d88`  
		Last Modified: Mon, 31 Mar 2025 17:15:12 GMT  
		Size: 2.6 MB (2581753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2777b2be4380b4ef3944d2d3b3987b213b0d6460217942db390668231da93864`  
		Last Modified: Mon, 31 Mar 2025 17:15:12 GMT  
		Size: 6.2 KB (6193 bytes)  
		MIME: application/vnd.in-toto+json
