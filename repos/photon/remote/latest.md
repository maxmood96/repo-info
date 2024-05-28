## `photon:latest`

```console
$ docker pull photon@sha256:006fd71198056abcff69d77c50c97ad227341d57e42c42db8c53686f0f3ea714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:adeae7db9c287f67aeb07c21790f2738f5840ac4048773c665b706a924b649c0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16025269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ca2589ecd78be02be9e55921f2adb2d7ecdae72050fb724e72474908db9f6e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 20:02:01 GMT
ADD file:254474a32079242b4e5dd61f062125d81669bfcbe9ef249fe3b7b2292418b3a9 in / 
# Tue, 28 May 2024 20:02:01 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20240526
# Tue, 28 May 2024 20:02:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2a715ab8d96eb980e74a015f299d9c14156ebfb94230c7355090d84a84043a29`  
		Last Modified: Tue, 28 May 2024 20:02:29 GMT  
		Size: 16.0 MB (16025269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:ce26f9cea3327035c6e696730e1644cdbde6fb5132e11a90c237e88ddadaed38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15014962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b17319b64e1a674787e2e5315ad6343d62f1619aff30331a005d6dff79cdc02d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 May 2024 17:51:15 GMT
ADD file:08e20929d503610b6f2bc1087711e4266799120ae9adabc99bf32b003a06227c in / 
# Mon, 20 May 2024 17:51:15 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20240519
# Mon, 20 May 2024 17:51:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:43c0594b204a6be956b4548741b596698d632e91c15dda5ba9ea0e2d00ddb22a`  
		Last Modified: Mon, 20 May 2024 17:51:33 GMT  
		Size: 15.0 MB (15014962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
