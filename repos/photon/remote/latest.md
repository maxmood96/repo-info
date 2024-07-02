## `photon:latest`

```console
$ docker pull photon@sha256:82dfa43f0451dc82df79ed6d5ce4f272705ce86af02b6fd227ade41fef4f9c06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:dcf8d15fcdc36c6fafadae528597833250419a4f4cec99d8538623fc799ef9e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16133509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa24b7171d27d640e21ccf3afbcac2c8fc787f0f29cf1e50afcb869c96e7747f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 01 Jul 2024 22:53:29 GMT
ADD photon-rootfs-5.0-e750aa567.x86_64.tar.gz / # buildkit
# Mon, 01 Jul 2024 22:53:29 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20240701
# Mon, 01 Jul 2024 22:53:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b73a46d4c129568123ce69e30e9dd94d4c82621477ea07ebb8450eece5393722`  
		Last Modified: Tue, 02 Jul 2024 01:00:33 GMT  
		Size: 16.1 MB (16133509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:62585feb0ee1a1e69aa0dab66394ad0705d16c1d674b88ed154d3164d115b592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 KB (344853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62aa4d5022e03606e9d441ccc0905f3f0a667ddac13f7772534b61c153ff99ed`

```dockerfile
```

-	Layers:
	-	`sha256:871a0ead6c230eacb0dc3a183b654f204f8cad436c66abc3a9f104a2750a41d8`  
		Last Modified: Tue, 02 Jul 2024 01:00:33 GMT  
		Size: 339.3 KB (339339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:981f7303cf389896fca20deeaf84c88ace2303c94eeaaaaac6061af5852c2cf9`  
		Last Modified: Tue, 02 Jul 2024 01:00:33 GMT  
		Size: 5.5 KB (5514 bytes)  
		MIME: application/vnd.in-toto+json

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:d7858fdf51c493418d08d80bbf154399f52f207b56ff1fc6163d5f034bf50953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15127552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dccc09514c6fb22866596780a80ed46a647a64f0a5b70995da5e28638340385`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 01 Jul 2024 22:55:02 GMT
ADD photon-rootfs-5.0-9c5bae00a.aarch64.tar.gz / # buildkit
# Mon, 01 Jul 2024 22:55:02 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20240701
# Mon, 01 Jul 2024 22:55:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:55774fc7be79a8512e89ed7118b7055f963d5e4d809601afa1559ffe7d4c62d5`  
		Last Modified: Tue, 02 Jul 2024 08:56:03 GMT  
		Size: 15.1 MB (15127552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:27e839f957857ae4774e3c2ca01676cf226d4fe00901f175b38b00fcf104fa8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.4 KB (343410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748e9db0c668e988e72e9ac40df80c6a3af258bf08abe8f183534fadc184c22b`

```dockerfile
```

-	Layers:
	-	`sha256:5d4d30f7992a63f4399d46aedb371b65c6d2ef1b0edd3f38cd43cb0c58bd10f1`  
		Last Modified: Tue, 02 Jul 2024 08:56:02 GMT  
		Size: 337.8 KB (337838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9d0b399e696df0d8e62a3cb6f147792748a04ca41e0f575a084c339f81e4539`  
		Last Modified: Tue, 02 Jul 2024 08:56:02 GMT  
		Size: 5.6 KB (5572 bytes)  
		MIME: application/vnd.in-toto+json
