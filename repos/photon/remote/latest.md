## `photon:latest`

```console
$ docker pull photon@sha256:3ec73ee1937f998b1cecb38c31d7ec955c613f6bc6bf1de682245d9489c48f2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:b9b66bb1f4901c79483627133cdb7a896a502611b4afa6c1f21f9304745b669f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16124945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f925e90ff1207456b47819c958efd805ea70821add6eba878d5730e6aa75d55`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 16 Jun 2024 10:53:48 GMT
ADD photon-rootfs-5.0-4a43fc53f.x86_64.tar.gz / # buildkit
# Sun, 16 Jun 2024 10:53:48 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20240616
# Sun, 16 Jun 2024 10:53:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f1a2e4d95c941ab21f2804ac3b850a1aa3ebfd1d80231397c25d68efdb1b09dc`  
		Last Modified: Mon, 17 Jun 2024 17:57:55 GMT  
		Size: 16.1 MB (16124945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:791330d49344bec325dcc0b16cd16d108c9788ff66a191d623f15afbc10e68fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 KB (344854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e00d15cef2ac7b4212b621d76cd573a44628b9bd360570edb70ab564fcc7141`

```dockerfile
```

-	Layers:
	-	`sha256:b236e4bcd68ed6c35d794ef4beda7002a9319ca866baca6679300c90a6709dbf`  
		Last Modified: Mon, 17 Jun 2024 17:57:54 GMT  
		Size: 339.3 KB (339338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca2b5df7431af9eb5cb15b311d0a64a33761a362e207267c30a338efcc40ddb6`  
		Last Modified: Mon, 17 Jun 2024 17:57:54 GMT  
		Size: 5.5 KB (5516 bytes)  
		MIME: application/vnd.in-toto+json

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:7aa0e85ae3dc147abe91698dba497c319901fd1d0a234dab10f74b7ae8719172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15127129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c094e244cc6395f770d8787791dfcd32c3b0c3be1869b721197697f80128af80`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 16 Jun 2024 10:55:32 GMT
ADD photon-rootfs-5.0-97686ea0c.aarch64.tar.gz / # buildkit
# Sun, 16 Jun 2024 10:55:32 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20240616
# Sun, 16 Jun 2024 10:55:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:941f696ab5d4e77f57ca26626e248a2c22333d4e7d26ff754d8e7d54dd08ef23`  
		Last Modified: Mon, 17 Jun 2024 18:24:26 GMT  
		Size: 15.1 MB (15127129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:026e2dd2c0b32cb48565e11c33d14c67be2386a0e144b42b462fdad7af568ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.4 KB (343409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c73dfd19be469000f162b7c463720e36d0a329de5d9da8384ac881da46cb25`

```dockerfile
```

-	Layers:
	-	`sha256:de201a055f12315a8df4ba4d6afbfdf0ba8e0eb94a6a7200da22e8bbaf92a005`  
		Last Modified: Mon, 17 Jun 2024 18:24:26 GMT  
		Size: 337.8 KB (337837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e24c56f135e6888981a5dde103d820caa9d1457f57e8c7eed44f8c6c06b42ece`  
		Last Modified: Mon, 17 Jun 2024 18:24:25 GMT  
		Size: 5.6 KB (5572 bytes)  
		MIME: application/vnd.in-toto+json
