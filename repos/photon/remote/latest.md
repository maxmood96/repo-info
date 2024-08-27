## `photon:latest`

```console
$ docker pull photon@sha256:a7bc396b1e7b1e119fd76e4fe1fb3bbd38ef89e10cf6a51170b085f3d924ed15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:f92e9fd26d7adaae450763f6b8956de1922d057607bc7d7550e13850e13b129a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16137278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2321516f14d6e6912d53f7de244a82e9b4168660b347ae12ab036c881957baae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Aug 2024 21:16:37 GMT
ADD photon-rootfs-5.0-cb551f076.x86_64.tar.gz / # buildkit
# Mon, 26 Aug 2024 21:16:37 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20240826
# Mon, 26 Aug 2024 21:16:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fce7e7b15de5f8e342b3278a1cb84b3368c7f6f9b1e839826fcd2158d2591133`  
		Last Modified: Mon, 26 Aug 2024 23:00:18 GMT  
		Size: 16.1 MB (16137278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:e8e5c3deb8c087aa28de91f62908edd581c29c59901476312f6c97b681356ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.9 KB (352882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d80d882e384c2319a31ebc25862b903bbf4e9d7af22377818c23c7f45dc15c`

```dockerfile
```

-	Layers:
	-	`sha256:f94383d5fd71a32d2dd18ac67c08a7b2e83361c7bc716c1d4636b3b229420a0a`  
		Last Modified: Mon, 26 Aug 2024 23:00:18 GMT  
		Size: 347.4 KB (347366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c41904afc1dac938624433481a66b4380983a76602410b5840cfb14cd4f3700`  
		Last Modified: Mon, 26 Aug 2024 23:00:18 GMT  
		Size: 5.5 KB (5516 bytes)  
		MIME: application/vnd.in-toto+json

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:9997eef7986ef4fcf259298c82b034e76803b961433fdfbe4208b7ed364727d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15142229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30810d0ddfc0e394f51943a21a6826c25b78a4cca84bb7a0f4bd074e1ad1e89b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Aug 2024 21:18:07 GMT
ADD photon-rootfs-5.0-cb551f076.aarch64.tar.gz / # buildkit
# Mon, 26 Aug 2024 21:18:07 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20240826
# Mon, 26 Aug 2024 21:18:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d06013a18cae865bc550d7bb103f1bb8d38e56eb20a9d3f80336761fd6415e5a`  
		Last Modified: Mon, 26 Aug 2024 23:04:11 GMT  
		Size: 15.1 MB (15142229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:9dd4354526fd8cf231755ac544834c6abe46c61745dde5666469181335346caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.4 KB (351436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeda116ade49325d670957b1d950c5426101643c68919498b66c91737b8c204e`

```dockerfile
```

-	Layers:
	-	`sha256:591fd340452b742deda0ecb65e2b4ba2c28e32a74c4c64389b9a128d0140feb3`  
		Last Modified: Mon, 26 Aug 2024 23:04:10 GMT  
		Size: 345.9 KB (345865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:facdb2602cb6124f910c507d901133009b1947aa87aa3d7fbd4743b2ead444be`  
		Last Modified: Mon, 26 Aug 2024 23:04:10 GMT  
		Size: 5.6 KB (5571 bytes)  
		MIME: application/vnd.in-toto+json
