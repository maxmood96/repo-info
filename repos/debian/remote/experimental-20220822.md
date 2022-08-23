## `debian:experimental-20220822`

```console
$ docker pull debian@sha256:166c9b01ef446eef826e8fc89b613304d1ecb14aff2a0a27ea76e9e4cbbdfbb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; mips64le

### `debian:experimental-20220822` - linux; mips64le

```console
$ docker pull debian@sha256:7f1b884cbbffa5b3e0d22f887d427dbf8f9b7f7bae3e4085dd5aee0a0baab28b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53216875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7054f25de1425f072e88a81807a07f1e3f38fc2072c6807c4dd3a120cb230e4c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:15:27 GMT
ADD file:289ff967122b94852c18b08616d72bff729cc9d607c295c6c758bb8917ce5864 in / 
# Tue, 23 Aug 2022 00:15:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 00:16:13 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:10ecab1bdcec7f490bd4865c91fc25cfc0d3d5506b9673055d7740a86765bdea`  
		Last Modified: Tue, 23 Aug 2022 00:24:06 GMT  
		Size: 53.2 MB (53216652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8187526258e55e7a283249775de7fdac990d25e667fd1d930ae0538e05ef8d`  
		Last Modified: Tue, 23 Aug 2022 00:24:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
