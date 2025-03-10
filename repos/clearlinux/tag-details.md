<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:66a62d84777227e3ccfa7407e8217e47abbb53188b2d23b92f57fe6364645cc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:68020bcec356d512e01f673d8033200125390cf8a52fb48efe140b2323f80b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73765391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c25eee4999c75979d2303289e5daa30f1f2c802c426eec01e9adefbca159a41`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Mar 2025 19:30:36 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 06 Mar 2025 19:30:36 GMT
ADD base.tar.xz / # buildkit
# Thu, 06 Mar 2025 19:30:36 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 06 Mar 2025 19:30:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0d03b9053b8b871661032dcf3310280590ea14db57ae162e044bfd5d1b41978b`  
		Last Modified: Mon, 10 Mar 2025 17:41:05 GMT  
		Size: 73.8 MB (73765176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f6b17071a10611bd278ff91a67568eb64710baac1a9b700cba598d43813a99`  
		Last Modified: Mon, 10 Mar 2025 17:41:02 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:8907fffd69cfcada0e0f318c440e0454b1c78b5435a85fd4c4873a72a6ea3627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf210b796397d6a9290125ed0c1a2913fb60069b63eeb16468380de534c29ec3`

```dockerfile
```

-	Layers:
	-	`sha256:77cec87a67251c2eb9df7e141fad686a3049f95da76aa44eaee5a8375caa7ece`  
		Last Modified: Mon, 10 Mar 2025 17:41:02 GMT  
		Size: 6.3 KB (6271 bytes)  
		MIME: application/vnd.in-toto+json

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:66a62d84777227e3ccfa7407e8217e47abbb53188b2d23b92f57fe6364645cc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:68020bcec356d512e01f673d8033200125390cf8a52fb48efe140b2323f80b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73765391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c25eee4999c75979d2303289e5daa30f1f2c802c426eec01e9adefbca159a41`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Mar 2025 19:30:36 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 06 Mar 2025 19:30:36 GMT
ADD base.tar.xz / # buildkit
# Thu, 06 Mar 2025 19:30:36 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 06 Mar 2025 19:30:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0d03b9053b8b871661032dcf3310280590ea14db57ae162e044bfd5d1b41978b`  
		Last Modified: Mon, 10 Mar 2025 17:41:05 GMT  
		Size: 73.8 MB (73765176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f6b17071a10611bd278ff91a67568eb64710baac1a9b700cba598d43813a99`  
		Last Modified: Mon, 10 Mar 2025 17:41:02 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:latest` - unknown; unknown

```console
$ docker pull clearlinux@sha256:8907fffd69cfcada0e0f318c440e0454b1c78b5435a85fd4c4873a72a6ea3627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf210b796397d6a9290125ed0c1a2913fb60069b63eeb16468380de534c29ec3`

```dockerfile
```

-	Layers:
	-	`sha256:77cec87a67251c2eb9df7e141fad686a3049f95da76aa44eaee5a8375caa7ece`  
		Last Modified: Mon, 10 Mar 2025 17:41:02 GMT  
		Size: 6.3 KB (6271 bytes)  
		MIME: application/vnd.in-toto+json
