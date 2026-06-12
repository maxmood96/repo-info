## `photon:latest`

```console
$ docker pull photon@sha256:6db86de5ffc11d5c55e59d23790ad526b68e5bca4f030cb6a94e6136280866dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:4a96607c4af23d317ad525a9ef0434034938fe7d27da88c3301ad0f31d410d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19392490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be83de0bace8cba7bee10164cb3e13dd12eb60ea3a7d8534ab7abf82a5b17638`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Jun 2026 23:40:39 GMT
ADD photon-rootfs-5.0-db2794147.x86_64.tar.gz / # buildkit
# Wed, 10 Jun 2026 23:40:39 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20260610
# Wed, 10 Jun 2026 23:40:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2d092b3896874b635240686e9fac05f0100ffdaafb60e67ce92bea5a630b3be8`  
		Last Modified: Wed, 10 Jun 2026 23:40:46 GMT  
		Size: 19.4 MB (19392490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:923dccbe13f6d2cf0df2a934191bbb8d3ba3314cb1ebcc102467318052b05929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 KB (367808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d83ba84d33ba00d7b09449a7d3da8c3256f2cfe1cecf29400912eb180323cec`

```dockerfile
```

-	Layers:
	-	`sha256:c9f3513a5718a40e2601a8f3ac0083af8d72f62802c0a5976a3cb817d1b90f87`  
		Last Modified: Wed, 10 Jun 2026 23:40:45 GMT  
		Size: 362.3 KB (362301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbb806af5bcafa405e7017c72b7cee6933940528d10b432578d9e78517355423`  
		Last Modified: Wed, 10 Jun 2026 23:40:45 GMT  
		Size: 5.5 KB (5507 bytes)  
		MIME: application/vnd.in-toto+json

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:8a79b2b149709fead353929f0c550e3bc4d5c67faeba48b4a85f241bee6ffae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c754fba5ac67da3aea5bba46d373b2f9bd7bd266ae74e2d84bcb909f0a6e79a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Mar 2026 18:51:57 GMT
ADD photon-rootfs-5.0-eb39da49f.aarch64.tar.gz / # buildkit
# Tue, 03 Mar 2026 18:51:57 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20260214
# Tue, 03 Mar 2026 18:51:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6bce6d1acc07cf4dd1447b647c0f437a91f0b27140176c996880367b79ee0b9b`  
		Last Modified: Tue, 03 Mar 2026 18:52:04 GMT  
		Size: 15.3 MB (15271128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:1ce409dbd6311a7ce83d514870be826e2a0a41d77ff0b776639708f29729f4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.4 KB (358405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b372ba629ed9d1575ae2f71be10139d10162b2c8531f1041b4f3033d8221bd0b`

```dockerfile
```

-	Layers:
	-	`sha256:36ec08d93aa4d6a7f8968ac987ff2c80a27e5200a1b51f2b4fc5d8f680b5cad3`  
		Last Modified: Tue, 03 Mar 2026 18:52:04 GMT  
		Size: 352.8 KB (352842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6093300bda44b4ce1593379a068f197fce936907488f0514b1824f6a2e659094`  
		Last Modified: Tue, 03 Mar 2026 18:52:04 GMT  
		Size: 5.6 KB (5563 bytes)  
		MIME: application/vnd.in-toto+json
