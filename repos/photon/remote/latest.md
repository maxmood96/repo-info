## `photon:latest`

```console
$ docker pull photon@sha256:70a98ddaccd30239b3951a1fbcda7fc3a948325429702253950cdb432fd5684a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:04fe66b1faf59ae62f07d2bf78ad633a07a9bc6b8e9edc2971d0bc6ae06dba91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16142218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e88b6d4f58a450490d526b34da5d19838f7897bd31a099256c04fbbd0aedcb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 19:50:41 GMT
ADD photon-rootfs-5.0-dac118894.x86_64.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:50:41 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20241016
# Wed, 16 Oct 2024 19:50:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d667db074125b5eaca53e565f0c28b11e145cce7aa1e40fda327ba6165b433d6`  
		Last Modified: Wed, 16 Oct 2024 23:10:27 GMT  
		Size: 16.1 MB (16142218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:4b5833aa4a911ba9ad0112de8455b77876f4a6fc04b7bea56ac93044c0423162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.9 KB (352933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617d42a8b2936accf70cff6ee04cb34b6259b3d0c60ba473d1fc7aabbb25163e`

```dockerfile
```

-	Layers:
	-	`sha256:1c6544ac11a3efe3d3156375d3bdbedd6ac6aa3c3affee5267b51064515498e3`  
		Last Modified: Wed, 16 Oct 2024 23:10:27 GMT  
		Size: 347.4 KB (347379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72ed076441a2562c192930e6901f021f458c5ddd6f6f89640fe61c0fa552afe8`  
		Last Modified: Wed, 16 Oct 2024 23:10:26 GMT  
		Size: 5.6 KB (5554 bytes)  
		MIME: application/vnd.in-toto+json

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:265890ac2b04e9503e24e57b13b4014f78840742c4161310dff48f19978b1986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15143026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a43539a1d2d799952ea113cd004376c8810d19fc1323ba54ee903b1b50a28f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 19:51:00 GMT
ADD photon-rootfs-5.0-d459a9f79.aarch64.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:51:00 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20241016
# Wed, 16 Oct 2024 19:51:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f00452fd8a794839ce1fe02ebbabb59d72834f01f2d8ee8bfd2509ef9299df16`  
		Last Modified: Thu, 17 Oct 2024 01:05:21 GMT  
		Size: 15.1 MB (15143026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:ca409b7f7741dd9496f4f1d13e54d96cf13b4e417a3a80f96f8d421da646ca84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 KB (351488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e82c8a7edf3bd447572eb3dcf5c65f4c7447f4ad03c42eb6b1ec3ba8cd00fde`

```dockerfile
```

-	Layers:
	-	`sha256:4750d8c0beb1f39a42471c8c5e4f2bc6549dc549116f489d3404d3d217e57319`  
		Last Modified: Thu, 17 Oct 2024 01:05:20 GMT  
		Size: 345.9 KB (345878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cac0789f9600c8d9d0c5a1779e78dfe14fbefeb380470bc6abd4130a469cb0e`  
		Last Modified: Thu, 17 Oct 2024 01:05:20 GMT  
		Size: 5.6 KB (5610 bytes)  
		MIME: application/vnd.in-toto+json
