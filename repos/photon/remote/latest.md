## `photon:latest`

```console
$ docker pull photon@sha256:777bfe878bb8f0590907f817676f7485a302e70da2cbabb03612b3bcdaf4671f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:739541f7d58063594de905b4063cf7a577d6a27e7816202b3a9a2fbeaf4f6511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16313797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d267adf76c4ff7fba1b8b087b0f1ebd1b7f9d1a10fa99dbab71e2f6fd0ba403e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 27 Apr 2025 10:48:53 GMT
ADD photon-rootfs-5.0-b3da2fa72.x86_64.tar.gz / # buildkit
# Sun, 27 Apr 2025 10:48:53 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20250427
# Sun, 27 Apr 2025 10:48:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:259e20632a8931bea69b741f75472610b0cba464dad95d1b0854009e22751382`  
		Last Modified: Mon, 28 Apr 2025 17:57:50 GMT  
		Size: 16.3 MB (16313797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:d1e3e5488fb7ae8021b72a81a218e5b5678c901f28fa69ef3a8fac15f2bc2aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.7 KB (362711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf3942a43aab3a78eb21d154ae00dae111408bcbbe5df1267a62b4d0a2f5d1a`

```dockerfile
```

-	Layers:
	-	`sha256:7a3848a0e549a92ffb6125e756f178e266818eab50d23f150d66df6ac45edad1`  
		Last Modified: Mon, 28 Apr 2025 17:57:49 GMT  
		Size: 357.2 KB (357161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:490375f9f763856ddf96c51b0c171860703b5fd2a2ec58f47fb5c5dd18059d69`  
		Last Modified: Mon, 28 Apr 2025 17:57:49 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.in-toto+json

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:5027c1fceeccccff429ea6612ee2fd6603e3af4ce4a0a75fa6a6e9788926b684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15308155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7b6bc170089ea8e58055bc58bb70e57704198351937bd3f302f8032f462c57`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 27 Apr 2025 10:49:07 GMT
ADD photon-rootfs-5.0-b3da2fa72.aarch64.tar.gz / # buildkit
# Sun, 27 Apr 2025 10:49:07 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20250427
# Sun, 27 Apr 2025 10:49:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:30fac09f4eb23a2e8db97eece77947f5aa1cededdf827ab2ce3be4e8c7e5a61e`  
		Last Modified: Mon, 28 Apr 2025 18:22:39 GMT  
		Size: 15.3 MB (15308155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:d5378d694255ed7f9e57bad2f9a56ee8a94dcbee2ef6b3cda0ff73cdf435e3e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 KB (361019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318087eeb6ae44e0284cb50ef1869d1f330a7a90dbf5effb277db7e0d32f51e9`

```dockerfile
```

-	Layers:
	-	`sha256:ec9cfc174689b4bf44a7995ef7747772f34344e260029b8cfd9f0b6467dd1a7e`  
		Last Modified: Mon, 28 Apr 2025 18:22:39 GMT  
		Size: 355.4 KB (355414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da629e230019bb1037033dd98bf3fba49e1a91f22f0e2dc77fed36f67d04911`  
		Last Modified: Mon, 28 Apr 2025 18:22:38 GMT  
		Size: 5.6 KB (5605 bytes)  
		MIME: application/vnd.in-toto+json
