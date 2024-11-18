## `photon:latest`

```console
$ docker pull photon@sha256:415d23067dfd225a1c57280a51850bad332768110106976af6a8a004f6c02c3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:8a6b2b2c6ec8b631ca9b0a302c3cb01aff942bd3504857b885ff845c44b9907e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16169369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c036d08dc5c4bbf10b864b579a608f1796286d9f17f61ee2866647e24c1cb950`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 17 Nov 2024 10:41:45 GMT
ADD photon-rootfs-5.0-965ee10ac.x86_64.tar.gz / # buildkit
# Sun, 17 Nov 2024 10:41:45 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20241117
# Sun, 17 Nov 2024 10:41:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a89e0c7e6e6d08e37de45bc22fe29c16ad36e1ace916790a75e72ee2776cc8e7`  
		Last Modified: Mon, 18 Nov 2024 19:05:00 GMT  
		Size: 16.2 MB (16169369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:009937de401dcbbd1571012024141385a8a0c3d523a0725a7222a8fd271aee83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 KB (368274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce8e4aa18faca541b0d661b240e31f53985c4d985c922969c6c9ce85809b67b`

```dockerfile
```

-	Layers:
	-	`sha256:3163eaaf26605037e4c1b2678ce8b60db8c861ab632113dd2eb3740b6ffaedda`  
		Last Modified: Mon, 18 Nov 2024 19:04:59 GMT  
		Size: 362.7 KB (362724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3283d4c37ac57ac891e5546579353a50b2437fc1bc219eab8dec5acf39700aca`  
		Last Modified: Mon, 18 Nov 2024 19:04:59 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.in-toto+json

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:cbfdc000efab18b4d3567db1b942f1352525b6e6566ce1f5378fc26e5baef745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15163699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e01f2602fa2a13c0fe1ff504d83e3e424dc30d57f35d0d7128dfdfc05314682`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 17 Nov 2024 10:41:59 GMT
ADD photon-rootfs-5.0-965ee10ac.aarch64.tar.gz / # buildkit
# Sun, 17 Nov 2024 10:41:59 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20241117
# Sun, 17 Nov 2024 10:41:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9ed3d4a347e8b0bc4e890a5cb612a70034d456c7113b06a80a719782459284e7`  
		Last Modified: Mon, 18 Nov 2024 19:07:44 GMT  
		Size: 15.2 MB (15163699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:2352817e457895c64ee7044ab9c54a73357c0165a620fe63e5ccef540599a706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 KB (366828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b7e5b78670ad2fa11a90735e6d75365503e7996000778e613b69f08fde8a15f`

```dockerfile
```

-	Layers:
	-	`sha256:8f38bc47b42be06b47822cfceec7460d8ce67a48ef6d1c2f51e16d1cd52f9d6f`  
		Last Modified: Mon, 18 Nov 2024 19:07:43 GMT  
		Size: 361.2 KB (361223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:371b72e008f10fc72103e3207262bbcc1aa75f27a47e831c2a75656b92cf024a`  
		Last Modified: Mon, 18 Nov 2024 19:07:43 GMT  
		Size: 5.6 KB (5605 bytes)  
		MIME: application/vnd.in-toto+json
