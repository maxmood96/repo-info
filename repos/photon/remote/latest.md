## `photon:latest`

```console
$ docker pull photon@sha256:78bda000e685333f76711f1fc283aafb457de5761b42c2cce12f614ea2a9b19c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:3880d6327d3b44e1f77684319e2e0601fc1e8ec17daa2c240402bf3b7b4c4fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16313808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb0232658b7798b6d0bc93f5d30ee71c572441556f5c1edc437308a4d9cc953`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 29 Jun 2025 10:58:03 GMT
ADD photon-rootfs-5.0-c8c2e9315.x86_64.tar.gz / # buildkit
# Sun, 29 Jun 2025 10:58:03 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20250629
# Sun, 29 Jun 2025 10:58:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8448683fd5fb8663180725e71cd89bd3542d6a07b7400b3f77ca146b9a3a96b5`  
		Last Modified: Mon, 30 Jun 2025 17:22:12 GMT  
		Size: 16.3 MB (16313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:397b0d38bf49027a47dd0670c813faa188e1533ca51ccfe6167a457c801abaa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.7 KB (365720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4bbc070e6ca7d6dee3396c7106a5113e0a8ba19121831bb89c1b4aad427a55`

```dockerfile
```

-	Layers:
	-	`sha256:c351bceb7911393c146b40e4532e0839a53f0730f3684dc37c90d212d556fcd5`  
		Last Modified: Mon, 30 Jun 2025 17:30:27 GMT  
		Size: 360.2 KB (360170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7681ea1c4d3de877b8419e1fba6f02a91a427cae21d0d297593ed517b40a874`  
		Last Modified: Mon, 30 Jun 2025 17:30:28 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.in-toto+json

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:c94691bbfff44b0a4a9a5d9b17b84b962370b0b8bfcfaa814ca12c0c6e64293f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15307957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c142a711e35096c9859f585a011a02de77ce3c5e9a58ce5ba4f3c4e44a61e4b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 29 Jun 2025 10:58:19 GMT
ADD photon-rootfs-5.0-a03694f0b.aarch64.tar.gz / # buildkit
# Sun, 29 Jun 2025 10:58:19 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20250629
# Sun, 29 Jun 2025 10:58:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:842492a7aec8b16c67dcc2d73e3f4a1c3f5e7f6ad885bc49e39c1860d02a1b1e`  
		Last Modified: Mon, 30 Jun 2025 17:26:54 GMT  
		Size: 15.3 MB (15307957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:01a3446e6e1b19804880f4ebf1bebcbf1c036cc9d3d765550b49a51ae345f7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.0 KB (364029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245f47be1842221d3ba808baa7732a44e756b3d119a93ed9ea7ed9eb1cc87632`

```dockerfile
```

-	Layers:
	-	`sha256:5b78e389c13c412247ca68def0cee8ee3582cbcd96e63b151ffadf524de43f64`  
		Last Modified: Mon, 30 Jun 2025 17:30:31 GMT  
		Size: 358.4 KB (358423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d51148a40286cecbf8da6eca52801f1b178668f264b0cb1661aa981e80d05aa5`  
		Last Modified: Mon, 30 Jun 2025 17:30:32 GMT  
		Size: 5.6 KB (5606 bytes)  
		MIME: application/vnd.in-toto+json
