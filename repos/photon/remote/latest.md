## `photon:latest`

```console
$ docker pull photon@sha256:8cfda36e2f54754c6004f700eec49bcb458c73478a00347a19c4e3ee7a6010e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:2c9ad1739e409831bac3adc874e24cf749f07dd8cbb028699eb446b280d25217
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16083195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfe6fc63dcbb9175bf1a045f77030356aceb24fbd361be7dea4bcd78e599d63`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 Mar 2023 18:21:13 GMT
ADD file:f7d25cf520073cd15407eebf5f523e5d53cdb5f8a9bc7c10090920cec8d0e39f in / 
# Mon, 27 Mar 2023 18:21:14 GMT
LABEL name=Photon OS x86_64/4.0 Base Image vendor=VMware build-date=20230325
# Mon, 27 Mar 2023 18:21:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:59695153de0d280efefe0b529aef9246b7ac4a44281b609b854dee3abefc2401`  
		Last Modified: Mon, 27 Mar 2023 18:21:38 GMT  
		Size: 16.1 MB (16083195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:66d776e7d4c2ec3a2d0e7fc1ff4e9fdb73b7ef22b7b0fa2b55a64ad8cd23d6fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15186397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0606539330018eaa80819b6084cc9682462d1a82334fa0b46597eaebe70f9c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Apr 2023 18:04:03 GMT
ADD file:38e9b21938011d14252d6c640a0b30fc4b374b5177722c598ba81f57b592ad92 in / 
# Tue, 11 Apr 2023 18:04:04 GMT
LABEL name=Photon OS aarch64/4.0 Base Image vendor=VMware build-date=20230408
# Tue, 11 Apr 2023 18:04:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f0d0f52f837244d7759cfe1e09836ee25c6af3d3e2c51c736c6a881184ae652b`  
		Last Modified: Tue, 11 Apr 2023 18:04:21 GMT  
		Size: 15.2 MB (15186397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
