## `photon:latest`

```console
$ docker pull photon@sha256:a3d9d35fa8bfcb0859716465359c1d78a0eb92afda3f276510783de0041cbcfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:9160a1c73b3a51ec2e74555dea24b5864b0a2e426de581826e8a74bc26286d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16144384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd4e9716382ab3c12f03ca5ac07f55249a47d312fab8e0d29da7f10d27e687b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Oct 2024 03:45:40 GMT
ADD photon-rootfs-5.0-71381badc.x86_64.tar.gz / # buildkit
# Wed, 23 Oct 2024 03:45:40 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20241023
# Wed, 23 Oct 2024 03:45:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:69f3f4f936bbecace0dfa103edacf28c180057c701a00194302a0dd3d320cbb4`  
		Last Modified: Thu, 24 Oct 2024 00:05:08 GMT  
		Size: 16.1 MB (16144384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:2964cb234ebd63ff805d5f7429e9fe44bfd5ed4a8ca255b0b65de531c4b487a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.0 KB (353022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef834f8b28efea4ebaeb4572e99788dc74d8dcaf1090ee71de3d81e0ee220b4`

```dockerfile
```

-	Layers:
	-	`sha256:9fb796ff0046619a3672810888b589f2af49803991ce5db1215593b855991899`  
		Last Modified: Thu, 24 Oct 2024 00:05:08 GMT  
		Size: 347.5 KB (347472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5bee5a80faae9cb908940ba008f8b4165bfa924170ef5c82638f5fa246679f7`  
		Last Modified: Thu, 24 Oct 2024 00:05:07 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.in-toto+json

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:80297b3aa42b856df9d0ac0cf0b7b537af0ce2b76763bc86edfeabbd2a02b542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15144057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443e44cf88b1efda84b50ec38ce2401b020be9e9b8c9f80e84cca95155c5a1ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Oct 2024 03:45:48 GMT
ADD photon-rootfs-5.0-71381badc.aarch64.tar.gz / # buildkit
# Wed, 23 Oct 2024 03:45:48 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20241023
# Wed, 23 Oct 2024 03:45:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:df89ca073e9ba257e293843f5de182fe9a5c43b5bb1d91bb74afe320bb10f142`  
		Last Modified: Thu, 24 Oct 2024 00:02:19 GMT  
		Size: 15.1 MB (15144057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:0d89346791ccaaf03af905ddac595b4b1dda1b090babb250c4e686dc90632777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 KB (351577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be117a8df5a9f9faa6ed76a1575fddd20966b0fcf683f5a01d073dabdbef19f8`

```dockerfile
```

-	Layers:
	-	`sha256:ef0f45fe43ec22fd26563c3103dc94858cd3f25df0a6737b55d1c52db3a0ea44`  
		Last Modified: Thu, 24 Oct 2024 00:02:18 GMT  
		Size: 346.0 KB (345971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:964369aa9096d7ecf3612e236f994d466afc240c996efc04a34cc0ffdfe86d68`  
		Last Modified: Thu, 24 Oct 2024 00:02:18 GMT  
		Size: 5.6 KB (5606 bytes)  
		MIME: application/vnd.in-toto+json
