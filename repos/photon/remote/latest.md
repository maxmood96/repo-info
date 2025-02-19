## `photon:latest`

```console
$ docker pull photon@sha256:df32a2bcf3f7e7ae03b6810656d9d8a3e1ea117f4f25ddaaf2a47ade8fbc424d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:a709bb2c7235186bd8da66fe587260bbd151a8646523a9e0f6f22b274ef93179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16262328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be1c5c448995c31edf9045395d40bd567216737e3310cf346de95817427006b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 02 Feb 2025 10:44:02 GMT
ADD photon-rootfs-5.0-d07f841c8.x86_64.tar.gz / # buildkit
# Sun, 02 Feb 2025 10:44:02 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20250202
# Sun, 02 Feb 2025 10:44:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:58794d7d7d5c2227b0b44830e5fc66bd2e9ebb86bdd20e034f6bf59334067033`  
		Last Modified: Tue, 04 Feb 2025 00:34:00 GMT  
		Size: 16.3 MB (16262328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:470400906db09758722f15b510602884a32d3634d6e99c75d7aa007cf6b8def9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.5 KB (362458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ad5dcfac0e2637a6e353bd1f007c70704820edfd121ab96fec06cefa0abf23`

```dockerfile
```

-	Layers:
	-	`sha256:4f51544930a201471d6cbdbf853bc9cd5eeca879c958039e43ccc2adbed52bfb`  
		Last Modified: Mon, 10 Feb 2025 15:06:42 GMT  
		Size: 356.9 KB (356908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:208ad07471bc0fa019a321f64b5fa8baf0d8819946b9ef7f0737c1bed8ad3b02`  
		Last Modified: Wed, 19 Feb 2025 16:03:20 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.in-toto+json

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:67f6448f89c0034200b89e5230467efa6744a53543cd1fae4103c279a7bd8539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15259785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed5338c92ef326c12ff10fb2be14d61d682a02a1916f8ec68dff1ddc3098ff8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 02 Feb 2025 10:44:09 GMT
ADD photon-rootfs-5.0-e50ad5cb8.aarch64.tar.gz / # buildkit
# Sun, 02 Feb 2025 10:44:09 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20250202
# Sun, 02 Feb 2025 10:44:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a3f00d2ae8330f1334296f54d298d3a2bcd1cb13233f7ab6c12132619f7fda55`  
		Last Modified: Tue, 04 Feb 2025 20:26:14 GMT  
		Size: 15.3 MB (15259785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:bfc934958557fad9de03c230f90a06ed525ec31fbf9f7351cad8c975934646c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 KB (361015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b9754f38c82cb3ecfe8ea217fd08b54d5e355d620034d781e0d39386144069`

```dockerfile
```

-	Layers:
	-	`sha256:080bc321c06bb2f150e6faf19afd733839e4045241b35a7828780ec6539f5f83`  
		Last Modified: Wed, 19 Feb 2025 16:03:20 GMT  
		Size: 355.4 KB (355409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a1aa96ffb35fff568fa76317dec622797561ced7e3cb05f1410f5bc79862c06`  
		Last Modified: Wed, 19 Feb 2025 16:03:20 GMT  
		Size: 5.6 KB (5606 bytes)  
		MIME: application/vnd.in-toto+json
