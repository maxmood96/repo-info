## `photon:latest`

```console
$ docker pull photon@sha256:36b6bbb4d5dff9b08540fcc1dc1bb4efc59ce81715531e2c7169c4b137bcaf4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:235dfa257770101d9ba0ba9ba444223edfab556c16a51737a0aa6f8b166dd273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16313091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56723aee74447711fb57d34641ed5350a152dcbfcfb0d6c9fadbeb2211d82aaa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 17 Jun 2025 18:17:41 GMT
ADD photon-rootfs-5.0-eec645d58.x86_64.tar.gz / # buildkit
# Tue, 17 Jun 2025 18:17:41 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20250617
# Tue, 17 Jun 2025 18:17:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8de8b1a79f2f7834cd543b66c8521b28f10c8c9ff828516a594b7e0f609dc009`  
		Last Modified: Tue, 17 Jun 2025 22:34:41 GMT  
		Size: 16.3 MB (16313091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:3e3659e0d3340d347b4ea4fde95296a6a64e49f080b57baecb5ca9f6781f185e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.7 KB (365720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ff8f8456820f10166db63f94720c2e49767aa7e286e9d17d79e8d1264de804`

```dockerfile
```

-	Layers:
	-	`sha256:9bd51927f587ff4dc4c5099b63f02dc989156c8007cbb5447d9f34880420717d`  
		Last Modified: Tue, 17 Jun 2025 23:30:23 GMT  
		Size: 360.2 KB (360170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d99e2a6d82e409c7582058927ebd830416e9ba749527731dddbbb16171997159`  
		Last Modified: Tue, 17 Jun 2025 23:30:24 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.in-toto+json

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:0828d76c23b23db827970e7e614bb9840eb7d28d79d6badbe4902f13c0527084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15308129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd0bfdc102b32f59b4ac04fb08508e8cad75dcf0a9427879c8835f424dcd87d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 17 Jun 2025 18:17:57 GMT
ADD photon-rootfs-5.0-eec645d58.aarch64.tar.gz / # buildkit
# Tue, 17 Jun 2025 18:17:57 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20250617
# Tue, 17 Jun 2025 18:17:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5eff22eb4f25702cc4a722a5f6afa1cb82bb6d817127e0a1208f02dc7f412086`  
		Last Modified: Tue, 17 Jun 2025 22:48:44 GMT  
		Size: 15.3 MB (15308129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:e2b8ea157b7883a8ade8c86cf0e694a50a7ec67b0f2d4bef1ce95d4ee895ea46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.0 KB (364029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b15283d46a85ab049a9596450ff4dd5cefe2bd95b05ce9eafa110428e5f293d`

```dockerfile
```

-	Layers:
	-	`sha256:c05c1ff16b7fa9513b69246e73358ef55fda75345313f698abf96e848bc0f3e3`  
		Last Modified: Tue, 17 Jun 2025 23:30:27 GMT  
		Size: 358.4 KB (358423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a67d704c3ae7ce74c980dd77260d3ab0e305b14eb9af371151c662c6d1f04d`  
		Last Modified: Tue, 17 Jun 2025 23:30:28 GMT  
		Size: 5.6 KB (5606 bytes)  
		MIME: application/vnd.in-toto+json
