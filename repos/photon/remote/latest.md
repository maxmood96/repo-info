## `photon:latest`

```console
$ docker pull photon@sha256:1c4f1a00f97a3d5276c6a4f6e1fe1e4372e5b5c4107e813030f716666dd2fb5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:76d28dc460748d0621207b38fa4dc1950c21b33604e2ccabb78b46d7fcf1c784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16254702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f26a412a75360acef111338ec4005811ee6f1a66272d982892062eeaaee3a3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Mar 2026 18:45:13 GMT
ADD photon-rootfs-5.0-eb39da49f.x86_64.tar.gz / # buildkit
# Tue, 03 Mar 2026 18:45:13 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20260214
# Tue, 03 Mar 2026 18:45:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f32f037feefe20936642c5e340e8c64d93058451336cb65f19d013394bb72823`  
		Last Modified: Tue, 03 Mar 2026 18:45:20 GMT  
		Size: 16.3 MB (16254702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:e3bb8f51619bebe0115af04f0846495192ca37e79c5bc24a8ec9091bb2a23f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 KB (359848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531a75b7cf521b467d8a7e4aae2d50735fa7d1cf136279e27870244662912d43`

```dockerfile
```

-	Layers:
	-	`sha256:7da01baf9b5525dabc39f8473748b9dcb9262ca3975de657a2e9e1da10ffe494`  
		Last Modified: Tue, 03 Mar 2026 18:45:20 GMT  
		Size: 354.3 KB (354341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ce8cc827e222ef54414ada4709c58e872b3d47a9bb1014dd0bcec371df7ddc`  
		Last Modified: Tue, 03 Mar 2026 18:45:20 GMT  
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
