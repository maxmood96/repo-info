## `oraclelinux:7-slim-fips`

```console
$ docker pull oraclelinux@sha256:c0c16a5ada2fccd01e5ae63479f655723f3ceff9fec64d46f319664ffa5923da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `oraclelinux:7-slim-fips` - linux; amd64

```console
$ docker pull oraclelinux@sha256:33cf6c83fc484d1fde3b780c34ab0c58e3c343dbb585dce9522de27c1f4aafc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76263977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595f0708062825c94839dd91435ce10a8858f481555252982a0e6367e56198e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 09 Sep 2024 20:34:59 GMT
ADD oraclelinux-7-slim-fips-amd64-rootfs.tar.xz / # buildkit
# Mon, 09 Sep 2024 20:34:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3f26774cd96a70dbb894d5f8fb9556ef19021819c38387b6ccbe641457f7910f`  
		Last Modified: Tue, 10 Sep 2024 01:04:06 GMT  
		Size: 76.3 MB (76263977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:7-slim-fips` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:65341a4eb11cf724a8ef65e6101ffed9eaeb060607e5790603a134956bd36add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0967b31ed8e73b6be139bbc2ccd7c0c54a9ee46f7c4261dd53e303eb9cf6cb`

```dockerfile
```

-	Layers:
	-	`sha256:7600d74e8b43077776261aebb4303c98fb87dc4f4cd34cc07bdb6ce0e3e1fcf3`  
		Last Modified: Tue, 10 Sep 2024 01:04:04 GMT  
		Size: 5.1 MB (5117897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c322bfda09ba1be2a41765e64542b2b49571305da47f8fffe61b89977a1f81fe`  
		Last Modified: Tue, 10 Sep 2024 01:04:03 GMT  
		Size: 4.9 KB (4885 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:7-slim-fips` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:b4d6f8e5b82e0b3943bec950123eea9102ea1357ee85cf6f2f8f7b71b4464aef
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77913019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c378915f57a1979821006e5e3e74c772f98b885c8f814cde21b022f7a71eb80b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 23:44:27 GMT
ADD file:2e8e371560149a4087a382054e509b66a90a2bab9801c294de4e855900e9a062 in / 
# Fri, 07 Jun 2024 23:44:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5531b67e7bea45ed18210b916734e755fbb37d78f65772df7457f5bffdd9d5cb`  
		Last Modified: Fri, 07 Jun 2024 23:45:20 GMT  
		Size: 77.9 MB (77913019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
