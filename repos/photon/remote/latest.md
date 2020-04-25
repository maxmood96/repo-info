## `photon:latest`

```console
$ docker pull photon@sha256:136c0f18a192f98f66e7dc2f68fb9642dfdb4e12e4ea37d915b52ad0ebb3ce6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:548ce0341d67ebcb5c04d4637ade56fc2f4d541eea6f3933b159586d6051f034
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15153485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e4136790791a9b682d1d9d067172c45f4e3599e1a2e7a73d63bd8f7a02a14f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 25 Apr 2020 01:14:02 GMT
ADD file:550cfabd9559e01ed022cd54653f543d6a371e23d105690df1e9f9cd0b9d8ed2 in / 
# Sat, 25 Apr 2020 01:14:02 GMT
LABEL name=Photon OS x86_64/3.0 Base Image vendor=VMware build-date=20200424
# Sat, 25 Apr 2020 01:14:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:31111373f494c87dd39610bffaed8e11e12372ceb89d21fe2a4e5515afa85b37`  
		Last Modified: Sat, 25 Apr 2020 01:14:47 GMT  
		Size: 15.2 MB (15153485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:d0ade0635328dd38fd194515e2208a4fef9d865e159e187e20d06a28e72c5213
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12950040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb908c938097d2ed25ce3fe3e41e04ead416e850144962e00b186d0fd172e85`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2020 21:50:15 GMT
ADD file:6b299b5287bb487a0ad64040c09d2d7ee59dbf1cb2a52615be82cfe28e1d16b0 in / 
# Fri, 24 Apr 2020 21:50:16 GMT
LABEL name=Photon OS aarch64/3.0 Base Image vendor=VMware build-date=20200424
# Fri, 24 Apr 2020 21:50:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:59afedc3dc3734938cfa1d8fd76b31e182d1fb41157c8f9d405c1a30bdd4397e`  
		Last Modified: Fri, 24 Apr 2020 21:50:43 GMT  
		Size: 13.0 MB (12950040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
