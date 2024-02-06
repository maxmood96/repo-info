## `photon:latest`

```console
$ docker pull photon@sha256:30f4d46136dac28dd6e96581e5cf49a08743b8138dc25b72331f2095576f20ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:6373b03ab4674c7248e32d19f331acf86eb695bcc41c08de4abfd8c26867d696
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15941845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c324f10b7679e5b8f9e115f589ef68a4dd2bc0681585369d71e939489e7f8c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jan 2024 19:52:12 GMT
ADD file:d51309b3b5c64082d243826c72cdf4b78bf4b793a3da49bdfc4b46c87be14a81 in / 
# Mon, 22 Jan 2024 19:52:13 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20240120
# Mon, 22 Jan 2024 19:52:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:19f31b017df611795c43d24474c2610ae9402d804aa7a53403e58279460da86c`  
		Last Modified: Mon, 22 Jan 2024 19:52:39 GMT  
		Size: 15.9 MB (15941845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:78401e8d1f4dad15870f06057c1e1d455a1dbf02ebeeb2fe3f90b19a7443523a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14939702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b69f3e527b6653014660f2b5a3052f514afa4692c0374548802cd51f52772b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Feb 2024 22:49:42 GMT
ADD file:5b5cd39362bf13190b259102c6de4d9790a17982eb5bad70378ae947050e6168 in / 
# Mon, 05 Feb 2024 22:49:42 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20240203
# Mon, 05 Feb 2024 22:49:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2fdc75bdb2739e697914aefa5b8b497cd7d7e7ddd74fd7c7a4cb3779a2b568f4`  
		Last Modified: Mon, 05 Feb 2024 22:50:03 GMT  
		Size: 14.9 MB (14939702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
