## `photon:latest`

```console
$ docker pull photon@sha256:b01c1e143bd8884a5022a0339c36b95e3d1d297452698d1d3f87389372e09905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:3acaa5a39fb1bad964664acc204273d57aaaa7d8a06204ce9b12139192703f22
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17541336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de4c154c8f5c12dd82fb963bf582ff52ef4bccedb4861b506fd07a9c6a3007a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Mar 2022 23:20:02 GMT
ADD file:4bb337ab7e5abc9e6a47909d70b21e070aef86f6e809ed27813ee64a9f652a0c in / 
# Fri, 11 Mar 2022 23:20:02 GMT
LABEL name=Photon OS x86_64/4.0 Base Image vendor=VMware build-date=20220311
# Fri, 11 Mar 2022 23:20:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6c964f3b879f03c1bb0ffd0e1b010a17fdd15faa2cd8d364f2222d0f4a490f9d`  
		Last Modified: Fri, 11 Mar 2022 23:20:37 GMT  
		Size: 17.5 MB (17541336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:b70e59d8510f261ac391c79c97347b3a1cd56dedcd02ab3bc9f169615da24bf1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16543827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e5a4087bd4cb8fd066f2960a2da908795180a4d3c752199e86e892095a495c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Mar 2022 23:40:14 GMT
ADD file:70c6ff093c42ce224ea85c3bfc3be6cd009f32a416376fec50510235bb568cc1 in / 
# Fri, 11 Mar 2022 23:40:15 GMT
LABEL name=Photon OS aarch64/4.0 Base Image vendor=VMware build-date=20220311
# Fri, 11 Mar 2022 23:40:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fbe286af82ad0f6c5c2a5eee5deeb66edc09d932a57942bb06fc67e88bd42336`  
		Last Modified: Fri, 11 Mar 2022 23:40:45 GMT  
		Size: 16.5 MB (16543827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
