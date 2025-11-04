## `debian:experimental-20251103`

```console
$ docker pull debian@sha256:2fb8288ec8f7b00b004643f56a58a386713ff515b4e7ae86ec7c53b0acf99774
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; riscv64
	-	unknown; unknown

### `debian:experimental-20251103` - linux; riscv64

```console
$ docker pull debian@sha256:dbc99e94eaf2916f4b07e620497663044f28cd329cd52bdcfb1c99c8cca083b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46794483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900d851b92f21bc27aba41df6a5c037631e5069dbbf5752c3936bce6d3afe30f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'unstable' '@1762202650'
# Tue, 04 Nov 2025 01:25:16 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:5ce854dd87e3899c0d57c1835e481664836dfe75977d3564c7675f6f1ba1ced9`  
		Last Modified: Tue, 04 Nov 2025 00:31:19 GMT  
		Size: 46.8 MB (46794263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961e6869944b29d41dab954188f29c3f15e94e9477d231a1d6eac2e602035cfe`  
		Last Modified: Tue, 04 Nov 2025 01:26:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20251103` - unknown; unknown

```console
$ docker pull debian@sha256:49a4a583a4dbba391386136b0bdac4d1bfe1544011d52cd17c789c330f11fbf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b6da0c16a8f6ac775eea9330c00cb029c8e0745fccf92537e43e9d697d6982`

```dockerfile
```

-	Layers:
	-	`sha256:9829ff021fac7e623a1c72c7711e52f5176a0c2ec8110731589160d5e2fef698`  
		Last Modified: Tue, 04 Nov 2025 07:27:53 GMT  
		Size: 3.1 MB (3122164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fd6cb624db078091ba0d61cfb54b87794f69e1e17d4a3984938fae73040f97f`  
		Last Modified: Tue, 04 Nov 2025 07:27:53 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.in-toto+json
