## `photon:latest`

```console
$ docker pull photon@sha256:29dc7685f02170f37c1922def3e33b7d645d0665b5b3db90bc1bf0d7f9a85ce3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:979188ca79b40ac6524fb60455ac1c2196748e0b8bc04d369a23f205e678c81e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16131498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9adee4ef95cfb54fb0aec907106e4ac7e714557ce6a97045ae7b7071f1566ab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 23 Jun 2024 10:50:38 GMT
ADD photon-rootfs-5.0-ec1a32159.x86_64.tar.gz / # buildkit
# Sun, 23 Jun 2024 10:50:38 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20240623
# Sun, 23 Jun 2024 10:50:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:935c28b7c7c0ffaab944d86ce34dc9ea9c8f0b33d47b2d0b3147cfd91d460acb`  
		Last Modified: Mon, 24 Jun 2024 18:01:19 GMT  
		Size: 16.1 MB (16131498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:7edefaddbf960e16c1a87a10193f047517b3b8e19a5ff80b908be88936f355e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 KB (344855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6148763b227a7420284273a87ac2fba0b635841183de78329e53d37d698a3d`

```dockerfile
```

-	Layers:
	-	`sha256:6a3e394c824836e29c29c0a422a5f493c3bc1c2e5a9af519e596bcbefa542c05`  
		Last Modified: Mon, 24 Jun 2024 18:01:19 GMT  
		Size: 339.3 KB (339339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f81d7551e9fecff57a32e09b0e9f38e54cc1150210e5a163c8b3a1e7f48f1372`  
		Last Modified: Mon, 24 Jun 2024 18:01:19 GMT  
		Size: 5.5 KB (5516 bytes)  
		MIME: application/vnd.in-toto+json

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:43d471ee00622d46954dad627850c127296611263163c76591e5ed6bc2f72b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15127254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbbbe9fa20b4b43d7905855abf44effa1a9b6842334b0e58a0afe7fafbd1fb1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 23 Jun 2024 10:52:05 GMT
ADD photon-rootfs-5.0-ec1a32159.aarch64.tar.gz / # buildkit
# Sun, 23 Jun 2024 10:52:05 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20240623
# Sun, 23 Jun 2024 10:52:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5dd4a90cf4e1e306560acef357d209ecfc06b0cd2e03b24d68aaf697a2945a63`  
		Last Modified: Mon, 24 Jun 2024 18:38:52 GMT  
		Size: 15.1 MB (15127254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:79d9f5db4b4036c4a64ae78da2eb8f502cbceb770cbe11e7fd62701405841188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.4 KB (343410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87133fe0341edefc9ba47e332ab2753ee1bef1342373615bf425c72d6a3fba8`

```dockerfile
```

-	Layers:
	-	`sha256:832117591a64c10c259d1f56f46c5ce61f4de1bb1f8ec3d08e137b2622a4d0a7`  
		Last Modified: Mon, 24 Jun 2024 18:38:51 GMT  
		Size: 337.8 KB (337838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82db7400f92e522a3249b4945d493006af25f6e7c389e86a7cd15a7b00f0b98d`  
		Last Modified: Mon, 24 Jun 2024 18:38:51 GMT  
		Size: 5.6 KB (5572 bytes)  
		MIME: application/vnd.in-toto+json
