## `photon:latest`

```console
$ docker pull photon@sha256:cc23e20e813fbc192cd9b2002b66a08cfe95c929078688f9ea662427038aea75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:f320ff758dd7006e2b91026e0b21159389d3c204e41c53d86ca2ae9abe1790b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16024526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bcef500a4b98b88f91fc45d7f5a4ae6711b225b222afccaa64e1062542bac7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Apr 2024 17:34:50 GMT
ADD file:98cf4e2c66cbf4e7a14f8f76b2ee153c10144683633fe75320d46d8520c2dcfb in / 
# Mon, 22 Apr 2024 17:34:50 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20240421
# Mon, 22 Apr 2024 17:34:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:31e49bb6f64ff6c5e343c6a11550a645fae134b73aa42fafa44fe50521506a13`  
		Last Modified: Mon, 22 Apr 2024 17:35:11 GMT  
		Size: 16.0 MB (16024526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:15cc11af183b528f2b260d7bfc47a2940bf01cf3db0babdc6ae418051dd73a81
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15014807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acccd4c9ce9ed9529039121db2cf137546fb1182d1780416b9f672056b1d0073`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Apr 2024 17:50:22 GMT
ADD file:873bc88a94d3ea1e9e8f50b2f5f353a73e77fc3a6ba7711db3490f6a474d0c8d in / 
# Mon, 22 Apr 2024 17:50:23 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20240421
# Mon, 22 Apr 2024 17:50:23 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7adf2d38d20a708b0194de4baa446db33ed2319a1651037425c9f207903728aa`  
		Last Modified: Mon, 22 Apr 2024 17:50:40 GMT  
		Size: 15.0 MB (15014807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
