## `photon:latest`

```console
$ docker pull photon@sha256:68c35196bac93790ea9bbdf6d98d2c23ceb5c199ce09c97f905a31106bd9d035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:61ec23b5ac98387223280c6ba22cf5275d68d30b4bd9489e4e86b75d99352595
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15776575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c6f2620d204c5d6634fa59e6ef4570686c5d13118b0ca1ac024ff3d43a9caf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 May 2021 04:49:04 GMT
ADD file:b2236583bd88a210a3dbe8d7f850f8f3f6a4292bf29633eba0db2ca8aa11bca2 in / 
# Sat, 01 May 2021 04:49:05 GMT
LABEL name=Photon OS x86_64/4.0 Base Image vendor=VMware build-date=20210430
# Sat, 01 May 2021 04:49:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:607a50127620f71e8148c16e7fe4824003bb605f8d9eb50b0d390219a43921d0`  
		Last Modified: Sat, 01 May 2021 04:50:02 GMT  
		Size: 15.8 MB (15776575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:5417f67f03b35ad87d3948cb9d52289fc03b27b14a81121354574bd89318dd15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14810085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab754418763113c2ee9527997a193c7ec82589733f11f294b8bc15979eb4e73`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 May 2021 02:35:55 GMT
ADD file:80c8828746f123b59ad371d4c98db58704074268f4b2baa770fc3f67406bc1ec in / 
# Sat, 01 May 2021 02:35:56 GMT
LABEL name=Photon OS aarch64/4.0 Base Image vendor=VMware build-date=20210430
# Sat, 01 May 2021 02:35:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:16f0ba435362c3d41d392fc53069cfa728aea93ad3730c962da9a8e51ac469aa`  
		Last Modified: Sat, 01 May 2021 02:36:34 GMT  
		Size: 14.8 MB (14810085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
