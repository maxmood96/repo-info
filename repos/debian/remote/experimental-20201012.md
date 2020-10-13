## `debian:experimental-20201012`

```console
$ docker pull debian@sha256:4cebaa63c508946246ce1c6c2e01336cb5e7af77f0a38b62e1c46d0d28c13131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v7
	-	linux; mips64le

### `debian:experimental-20201012` - linux; arm variant v7

```console
$ docker pull debian@sha256:8263854f033586482bbf1e3fe86e19b99c99f8e94d32f759ee1fd41f17c0f2f8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48255891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fae46badbb5cdec8c4a1c5542fc5430292ad01612cf2b49e784a4727e3e068f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:05:47 GMT
ADD file:ea1110e2401cede9711b75a4d4c1feec66cbe3535cb9941b1a1aaece5c327c2b in / 
# Tue, 13 Oct 2020 01:05:49 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:06:19 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:bcedefd617c8ee8154342bdaa838939a994328a8ce30443a7d435855fc723cf4`  
		Last Modified: Tue, 13 Oct 2020 01:14:07 GMT  
		Size: 48.3 MB (48255667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c01f1036b934f706de44f0a71184b133abaa9f6caef2e635df61fb53692632e`  
		Last Modified: Tue, 13 Oct 2020 01:14:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20201012` - linux; mips64le

```console
$ docker pull debian@sha256:b1657e4abd3ab75c7e9f0da3108a3e26c6c36de3de7591f4f3985a2da83e26f1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51292419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0892627de2728561d08ba1c8e8e8fa65829ade5ca0708d9cbc9ce394807eeae`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:12:59 GMT
ADD file:201f399be78aabaf334ffe1beefe5ff3ba4adc0eced617f7764c64dfbfcac7e6 in / 
# Tue, 13 Oct 2020 01:13:00 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:13:28 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:f75dd32b36549bf5eea6afd3648636a312f27cb0d3a3a3c68c94b3ec0ec9df43`  
		Last Modified: Tue, 13 Oct 2020 01:21:22 GMT  
		Size: 51.3 MB (51292196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f412f638215cbc25e8525e424dbd40e4b1f320477e83186878e4df8669e7bc`  
		Last Modified: Tue, 13 Oct 2020 01:22:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
