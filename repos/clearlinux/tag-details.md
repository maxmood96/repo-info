<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:404543ccf358219e304925043bf38e03d4334ebf155f9c31e962f588d7c950cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:06458b40c0e4f642690e7f2af6c97748cbe18cfd3337d2aefa040782e78731e8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71778667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0176f79d7125153725a9470ca6d8c31983f3679ac474a580346c09fbbb1a7aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 05 Aug 2024 19:19:35 GMT
ADD file:5e0a336629e27065af378a10ffa2d4f1b48ce2991cfc69a9ab7ae9ed6ad92d36 in / 
# Mon, 05 Aug 2024 19:19:36 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 05 Aug 2024 19:19:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a6ec584ab5467172fcc0874ba614dcd4f41ecc2ab7519513eddc3f2c8d0456ac`  
		Last Modified: Mon, 05 Aug 2024 19:19:52 GMT  
		Size: 71.8 MB (71778453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc13da4e8260aac264a81dac543eda0799849ab212834e4c28b7ee92d5b2495`  
		Last Modified: Mon, 05 Aug 2024 19:19:44 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:404543ccf358219e304925043bf38e03d4334ebf155f9c31e962f588d7c950cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:06458b40c0e4f642690e7f2af6c97748cbe18cfd3337d2aefa040782e78731e8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71778667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0176f79d7125153725a9470ca6d8c31983f3679ac474a580346c09fbbb1a7aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 05 Aug 2024 19:19:35 GMT
ADD file:5e0a336629e27065af378a10ffa2d4f1b48ce2991cfc69a9ab7ae9ed6ad92d36 in / 
# Mon, 05 Aug 2024 19:19:36 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 05 Aug 2024 19:19:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a6ec584ab5467172fcc0874ba614dcd4f41ecc2ab7519513eddc3f2c8d0456ac`  
		Last Modified: Mon, 05 Aug 2024 19:19:52 GMT  
		Size: 71.8 MB (71778453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc13da4e8260aac264a81dac543eda0799849ab212834e4c28b7ee92d5b2495`  
		Last Modified: Mon, 05 Aug 2024 19:19:44 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
