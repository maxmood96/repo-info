## `oraclelinux:9-slim`

```console
$ docker pull oraclelinux@sha256:52d76e4f81dc1ffc0e42e1ef25610d6f8b570d68d607dade2b2264f8611cdb8f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `oraclelinux:9-slim` - linux; amd64

```console
$ docker pull oraclelinux@sha256:14fa7a6b315cd42bbd1d0e502f7bedf467001d9d9203fd1126e36b523c0b3e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49239252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98bcee69ff15ab5066b0c0bb90f208e3d40a49286a83eab1b41abf03ebd67519`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 09 Sep 2024 20:34:59 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 09 Sep 2024 20:34:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5e407bf3af905fb1f6edf271f870052697e79b018f921119921615cd25365fdb`  
		Last Modified: Tue, 10 Sep 2024 01:02:42 GMT  
		Size: 49.2 MB (49239252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:9-slim` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:8e951e571b0b3481a6417866d993767abf81225881d6472888149b5bf179e1b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06759a4a6ae840ec5cdb911e52640c729afe8a1aca14a81b3d6b6cb7b195ad4f`

```dockerfile
```

-	Layers:
	-	`sha256:fd1d0ccd3b553f658a3d73109cca70ba1a474e6854d93de7f1ba9e6803cdf8c1`  
		Last Modified: Tue, 10 Sep 2024 01:02:42 GMT  
		Size: 2.2 MB (2180701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a4d4c706245b149268538524736358064e1d1d2bd6417f6bbe76d99ee8a82cf`  
		Last Modified: Tue, 10 Sep 2024 01:02:42 GMT  
		Size: 4.8 KB (4847 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:9-slim` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:18ad107671d8f9a1810c3e1c58880b4979c207b813d2870602e2f541a60ee1c1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47912074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b514e22c48256383a20d3788b3d020b0c00d9661f8aa0e70abe89e72ad5937e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 09 Sep 2024 21:41:19 GMT
ADD file:5fa82731318ffec42020c16dfb1b8cc899182c7fbbde89801b30c3b184c022e9 in / 
# Mon, 09 Sep 2024 21:41:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:058f612f6a59bf8f9c1c3d4cd9901435e619af32c108cfbadb5c9ca26461b9ec`  
		Last Modified: Mon, 09 Sep 2024 21:42:16 GMT  
		Size: 47.9 MB (47912074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
