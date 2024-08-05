## `photon:latest`

```console
$ docker pull photon@sha256:9102e211a9d7ef59f2910bb746e3ff5e9f352a268c4796abf582c18bdff3ccf5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:d2014a11893140a54754e399423288c52f7218b0b857c05e28cdc8489e11679e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16136734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b99940652c1e0da2967b654f88f9da38b17454b4d0d3cf4b29d1609a0b1d16`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 04 Aug 2024 10:44:02 GMT
ADD photon-rootfs-5.0-8ac51553c.x86_64.tar.gz / # buildkit
# Sun, 04 Aug 2024 10:44:02 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20240804
# Sun, 04 Aug 2024 10:44:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4d59cc894b0497391fb9fb15701bc970b075710b9561ebd7e902d580cb1796ef`  
		Last Modified: Mon, 05 Aug 2024 19:07:23 GMT  
		Size: 16.1 MB (16136734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:013c57a558d3fbce23d0015315bab78cf8b51e28f4f14c06b6949374cbba8151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.9 KB (352882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c02cec5bf947f7d9dd0913f53201cd4c32f7009223b13a3cc8b271c17b456f0`

```dockerfile
```

-	Layers:
	-	`sha256:977e671914d0e4fdca064f8760e7b77d5ee786aa3264a75243b135f414bded65`  
		Last Modified: Mon, 05 Aug 2024 19:07:22 GMT  
		Size: 347.4 KB (347366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39840e76f47e61a3be1376be904c44a92af56ecaece270305267c69fcab58c19`  
		Last Modified: Mon, 05 Aug 2024 19:07:22 GMT  
		Size: 5.5 KB (5516 bytes)  
		MIME: application/vnd.in-toto+json

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:27f2730a26973357290a294832e4e89a4336557088479f32fa820c667ef6d199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15140651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e32f83090e22ff0bf223f4f6a568aef7b6b602de98e68f0333aa34390fe5b8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 04 Aug 2024 10:45:35 GMT
ADD photon-rootfs-5.0-8ac51553c.aarch64.tar.gz / # buildkit
# Sun, 04 Aug 2024 10:45:35 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20240804
# Sun, 04 Aug 2024 10:45:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c562e71ba6a70e059d0f4f891ec79b5354ce8189127018ee0c5bef6453cee8ea`  
		Last Modified: Mon, 05 Aug 2024 19:20:59 GMT  
		Size: 15.1 MB (15140651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:a639707ad675ecf9e4009e00c5729aba6353549ffb428e284bf1aca258b9f70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.4 KB (351434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b82b5bc1aa06a615d70d746f73626af25044f7852ac9ec2a444115c04aab664`

```dockerfile
```

-	Layers:
	-	`sha256:aae469873a51aa81352c72827edd5b38339ca8fa7ca75f6d22e849beb08f7969`  
		Last Modified: Mon, 05 Aug 2024 19:20:58 GMT  
		Size: 345.9 KB (345865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:465ea2e7b8e9b0372162b797b08085198a998e2ce0f2da85d9b1ed881ea0acc9`  
		Last Modified: Mon, 05 Aug 2024 19:20:58 GMT  
		Size: 5.6 KB (5569 bytes)  
		MIME: application/vnd.in-toto+json
