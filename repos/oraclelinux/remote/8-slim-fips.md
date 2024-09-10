## `oraclelinux:8-slim-fips`

```console
$ docker pull oraclelinux@sha256:0a33fd8d913316db0593d1a3eaded9dde43c3a36ae5c49907eca2694f0488d50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `oraclelinux:8-slim-fips` - linux; amd64

```console
$ docker pull oraclelinux@sha256:9e17c61aa2fb80e1651d28dbc3fe3f72286dff60b6522f2b0303bb4ba1716b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51297449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ed2f69a8e2895c306022ffc212c40b3564886b90c45a1a7dad7715c725244e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 09 Sep 2024 20:34:59 GMT
ADD oraclelinux-8-slim-fips-amd64-rootfs.tar.xz / # buildkit
# Mon, 09 Sep 2024 20:34:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f707cedc286fa90baadfb4380892911d9ca05062bf42b007b4630c04aacdae24`  
		Last Modified: Tue, 10 Sep 2024 01:03:49 GMT  
		Size: 51.3 MB (51297449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:8-slim-fips` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:7ded2cedfabcf8ca3399fd6b212c652fc8ee6010e0ca6ea2c3fcbcc21d8f0603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2092263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52b3f4c496738f2edd6c50f3276e7e0e81ef79b5c1b8866c5e97d336c1ab837`

```dockerfile
```

-	Layers:
	-	`sha256:906c6e507b3ff3986baa1ca5253f5807fcd5eb4f72593759654f3e03764304b8`  
		Last Modified: Tue, 10 Sep 2024 01:03:48 GMT  
		Size: 2.1 MB (2087378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6c94f9ad4ddd6cd6fc12a498d606b963d8a80afa39bc39e4f6c91077c794ffc`  
		Last Modified: Tue, 10 Sep 2024 01:03:47 GMT  
		Size: 4.9 KB (4885 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:8-slim-fips` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:8b91a52621d83abbb6117fd7d0421a32653dd73374f89b0285bb62ad02774fc2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50004128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4212f57cd8a3c49c851a97bbf1f22597d434a3fb1f242fbe343061961370787f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Aug 2024 00:40:59 GMT
ADD file:ff80ca6218f47d70a025a51cfe44f0a82e3e744482ac5d6ea1aca83297e1f9b8 in / 
# Fri, 23 Aug 2024 00:40:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8a5f91c1d6206b74be7988ec6d04e5d6c036f5a7aca330a4935e739440b96d80`  
		Last Modified: Fri, 23 Aug 2024 00:42:35 GMT  
		Size: 50.0 MB (50004128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
