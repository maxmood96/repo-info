## `photon:latest`

```console
$ docker pull photon@sha256:1e42d4117e8134a68751d0081628c86ad31895577f2a6f7154479a44cec54ed1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:b5dd8cae68e561faf40c07adf47ef56f94f7fe4d966cc3fa2e49f96f76b02a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16139943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7b02944ccae062c57fbbf4bf430f602baa0af6172004f592007b3e33a5c9d1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 15 Sep 2024 10:49:44 GMT
ADD photon-rootfs-5.0-edfd98556.x86_64.tar.gz / # buildkit
# Sun, 15 Sep 2024 10:49:44 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20240915
# Sun, 15 Sep 2024 10:49:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6be373a05078c30d1aa5d1ea9024b0c5a29d86e1c7673628fa9c5599a369687b`  
		Last Modified: Mon, 16 Sep 2024 19:01:44 GMT  
		Size: 16.1 MB (16139943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:cfa71f422d1bdcf230e8b47dc65b25ac055c9b30d4b01d80dfe3255a6c78435c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.9 KB (352882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feaf60b06e394156d4aa0c8b38603aa4df2c54a709f1f7d6d38f585fff24967`

```dockerfile
```

-	Layers:
	-	`sha256:fc38e91e1b2c6d65b6b7cd23200641069553b51aeb84d7c84d4551f9f6649872`  
		Last Modified: Mon, 16 Sep 2024 19:01:43 GMT  
		Size: 347.4 KB (347366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05c70969035fd701c0f7c81a9ea4dfdf77ad0b6535d940768d632557b7d42d0f`  
		Last Modified: Mon, 16 Sep 2024 19:01:43 GMT  
		Size: 5.5 KB (5516 bytes)  
		MIME: application/vnd.in-toto+json

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:54b4d7b4fc47b13d571b1da786ed85800faf81dbf5ec7d6d50e5daa6256bfc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15142912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e14e4ce8976c9124808100bdf2c15483df8a0a649064b0fd08e7aafe59ba65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 15 Sep 2024 10:51:17 GMT
ADD photon-rootfs-5.0-edfd98556.aarch64.tar.gz / # buildkit
# Sun, 15 Sep 2024 10:51:17 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20240915
# Sun, 15 Sep 2024 10:51:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5c21fe01eb16109a15183b71ce1153ef6d2e45a5efd69f0d625086fbc652cab0`  
		Last Modified: Mon, 16 Sep 2024 19:05:50 GMT  
		Size: 15.1 MB (15142912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:b3c13b66d2fea9d097f7e977fe6178667097535205f4db5c67de48c9d51b2729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.4 KB (351437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a50afe04169ebfb681501ce37739ca07a04ee1a3beb392ed687a3fc0c390d0`

```dockerfile
```

-	Layers:
	-	`sha256:7a72227695f693e51a312e300b2f8cd477805b50fb1aee7129f8b7455dc3a260`  
		Last Modified: Mon, 16 Sep 2024 19:05:50 GMT  
		Size: 345.9 KB (345865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4c8fc478c31f5cdc0edfef36571c3df06b792037aeccd9be853818ed63a6adc`  
		Last Modified: Mon, 16 Sep 2024 19:05:49 GMT  
		Size: 5.6 KB (5572 bytes)  
		MIME: application/vnd.in-toto+json
