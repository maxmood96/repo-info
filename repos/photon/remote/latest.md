## `photon:latest`

```console
$ docker pull photon@sha256:82e5913640242fd2655bf756c3bc4e755bcaee70c77002dd3494154e9a910582
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:dab0b3ff59cbb85eaabad2840ec6c5b1297b2c54bacb7fa2f5d3edec9dbab1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16313866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf10f6abe77acdfc248ce0012347506c61cb0563c8f3b124bda64aa31a4af1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 23 Mar 2025 10:44:17 GMT
ADD photon-rootfs-5.0-3b8af0aeb.x86_64.tar.gz / # buildkit
# Sun, 23 Mar 2025 10:44:17 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20250323
# Sun, 23 Mar 2025 10:44:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:274a2d247d4118e8249481be4cef37050e57241aad3898926059a0750cc9f5ab`  
		Last Modified: Mon, 24 Mar 2025 17:02:15 GMT  
		Size: 16.3 MB (16313866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:e6f85d889bb912a51ed5b1dfd70234d6c9a50f7bcb4edb595039cfb36302a671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.5 KB (362462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e1109c5e3a212e4db80d90e90ece65d154142f588f22b09780cac83a08b820`

```dockerfile
```

-	Layers:
	-	`sha256:c257ff0c0221f2e0c25053909a922060d476068dea6a095cb6f0afbad631e7ab`  
		Last Modified: Mon, 24 Mar 2025 17:02:15 GMT  
		Size: 356.9 KB (356912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86129cd1438103a23eac3c81ab4c692a63610e2a2508a1ab7c7de8e6277e984d`  
		Last Modified: Mon, 24 Mar 2025 17:02:15 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.in-toto+json

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:913c68ccf3d3bab187343c0d8b1b9690dd1ef2947517c74e334f6bed08079ce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15308269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8dbdf1a14cffeacc0c685ad77fb17bc64232aab8b269dff033217b02a81061`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 23 Mar 2025 10:44:34 GMT
ADD photon-rootfs-5.0-415e664fc.aarch64.tar.gz / # buildkit
# Sun, 23 Mar 2025 10:44:34 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20250323
# Sun, 23 Mar 2025 10:44:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:190e655885747f64ca58dbc1ee8e15f78dc97dba89eea7bd1ed86f6a24336636`  
		Last Modified: Mon, 24 Mar 2025 17:32:35 GMT  
		Size: 15.3 MB (15308269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:497e5b2594155c9f96a26a06366aa45b8c0cb8f9e90fbdc822ebe5d9ec5323de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 KB (361019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c07b49de00c9c5d03a69c6ae3ad1ab0c27d970bda291b8dfc523313fa9da884`

```dockerfile
```

-	Layers:
	-	`sha256:553a6bd825ae0c9213e0b0aef42c0320cd1523b191e5ab1306dc5bb7e4b44b81`  
		Last Modified: Mon, 24 Mar 2025 17:32:35 GMT  
		Size: 355.4 KB (355413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4488683fa1afe129f6d4ba9ba43e1c42f2b61ce33a9119ae9d19c879568eefcb`  
		Last Modified: Mon, 24 Mar 2025 17:32:34 GMT  
		Size: 5.6 KB (5606 bytes)  
		MIME: application/vnd.in-toto+json
