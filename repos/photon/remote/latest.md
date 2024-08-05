## `photon:latest`

```console
$ docker pull photon@sha256:afec26ed45d78aaf2bac192fcd141126b5ece43381b51ffc36eb5d994c323c0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:eb41a11a06f1daf717b8b949fa8615e357e20f2e99c2f95e91fabb3851e37e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16136747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250cc68699ae9dd49b6c1f6d8146e6b97a6ef1df36ad9d7887a4759f52a09604`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 28 Jul 2024 10:40:57 GMT
ADD photon-rootfs-5.0-8cd84e090.x86_64.tar.gz / # buildkit
# Sun, 28 Jul 2024 10:40:57 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20240728
# Sun, 28 Jul 2024 10:40:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2d1bdc17f19a32707ce25502d7752ec2cefb8f7c28f6d746a6fb2376cb0decce`  
		Last Modified: Mon, 29 Jul 2024 18:59:39 GMT  
		Size: 16.1 MB (16136747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:da24c722b7258c404d1e5105f2ee36f90c3c57827348ae798863ac5a8a21bf78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.9 KB (352882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234170f19cdd932dd5e1c02b17602b59259cb30e638822533974dbb60afbe5c6`

```dockerfile
```

-	Layers:
	-	`sha256:cc4e939a6dd219de88b76f777e38222ee12ea5fe986e62e69a64805fc426e541`  
		Last Modified: Mon, 29 Jul 2024 18:59:38 GMT  
		Size: 347.4 KB (347366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f3b4d44acd8c9218c33812289979257b7142387b449778c62a5c3cd7bd0f44`  
		Last Modified: Mon, 29 Jul 2024 18:59:38 GMT  
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
