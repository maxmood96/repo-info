## `photon:latest`

```console
$ docker pull photon@sha256:9600048133c54966e3123654850eaaca734d0548a37b3a0b51d5df9bbe145194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:5506ca3673bf732d3cdd075033c50b6fe1b93f80d1697cc2ae2b5c2a53b1bb77
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116ff90daf9ccc6facfd2c4e748885f7105bc23a234672860392d76e9aa2f033`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Aug 2020 00:22:05 GMT
ADD file:1b767ed4282a2e4a563cbcb9e9e9e18df73ea32ef38f1434278c5f1f4eac04ee in / 
# Sat, 15 Aug 2020 00:22:06 GMT
LABEL name=Photon OS x86_64/3.0 Base Image vendor=VMware build-date=20200814
# Sat, 15 Aug 2020 00:22:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e3cba4ca50b7b4ed92044c363c81ea65c038f2d553308c70b5b824868349f33c`  
		Last Modified: Sat, 15 Aug 2020 00:22:30 GMT  
		Size: 15.2 MB (15198977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:dd1b61361a20402166c9028274813c89d8ba7fbe12f62a3ed2897c9fc187782e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12985878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9e69351fd8dcb2c612ca9b64077ccb75797911ee281024c306ba10e379b3eb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Aug 2020 23:48:05 GMT
ADD file:7d4f60dd1e522af618a283eb3db5236fb9be72d0eb10a554d67a6a7d3e5ea8f4 in / 
# Fri, 14 Aug 2020 23:48:06 GMT
LABEL name=Photon OS aarch64/3.0 Base Image vendor=VMware build-date=20200814
# Fri, 14 Aug 2020 23:48:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:874a83eab31334d9f462133cb047cc5cf1d6a9912054eb76c1915812d13a6f8a`  
		Last Modified: Fri, 14 Aug 2020 23:48:25 GMT  
		Size: 13.0 MB (12985878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
