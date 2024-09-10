## `oraclelinux:7-slim`

```console
$ docker pull oraclelinux@sha256:7356f45b70d208cc3b526c2947bd7f38ec11f6b40492c9a8038dc35925a8f1ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `oraclelinux:7-slim` - linux; amd64

```console
$ docker pull oraclelinux@sha256:bb1f3786036e118a9831c0bd2109611a20bfae73d3165f204e8efa25c3b2ef5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50399909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0319563761f16d61164df91e65472d0876efab1f5898a7f9226f94654fd5be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 09 Sep 2024 20:34:59 GMT
ADD oraclelinux-7-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 09 Sep 2024 20:34:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2f8b6e621346440edc34024f5db08c1adfb53a1a33b61d626b838fdadd052d21`  
		Last Modified: Tue, 10 Sep 2024 01:03:39 GMT  
		Size: 50.4 MB (50399909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:7-slim` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:8da514dba3e4bca28c94c4bb32d23b3c8fbab35b8fd963ea0f770dd7c2b84f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4262003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687f279ea98f7e770a0051cc2c1e809ea14937525cabfd461060cda8f0e47bf9`

```dockerfile
```

-	Layers:
	-	`sha256:9336b8aa2f6d2fe25418cf970211ca18e429fb348a394180bac1b4a41d78912d`  
		Last Modified: Tue, 10 Sep 2024 01:03:38 GMT  
		Size: 4.3 MB (4257156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6e54543aa4280d209ed2c5c615b2a46ab07787a29b576d30be044b0014ea816`  
		Last Modified: Tue, 10 Sep 2024 01:03:38 GMT  
		Size: 4.8 KB (4847 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:7-slim` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:ce991a4f5e65b7ec519485f16ca31fd4bff8736c9b3343fd992d8688a9b36997
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51002219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff5bdd251fda3f42706f7defc34751e5b260adfe15ec7390c3c59e4eb3ac75a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 23:44:19 GMT
ADD file:8cec73244d2c9c86e2669bae9cdefcdc0b44e2d95ea94b54501de7d3b9b4910e in / 
# Fri, 07 Jun 2024 23:44:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:609f0fc083e15af05bce9c640e0a6e192c074a269fc7e1c4d0705e359c481e73`  
		Last Modified: Fri, 07 Jun 2024 23:45:06 GMT  
		Size: 51.0 MB (51002219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
