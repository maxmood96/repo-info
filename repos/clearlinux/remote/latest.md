## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:5365ead07fa02bb9ca6b974607321c7149fa16563b127594da811c6013b299d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:f97df561f33b5e9f82366336d03dd920b4f84ee9fde73eb8d7937c6db5e9dea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72737544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9233cf2909380a8dace2615f513f52dddabf0720b040fd2adff893e5551def`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 May 2025 22:26:34 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 01 May 2025 22:26:34 GMT
ADD base.tar.xz / # buildkit
# Thu, 01 May 2025 22:26:34 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 01 May 2025 22:26:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6fd3815e825c8fc87ad2a282229e74685349d97d875daab0802db86808af700`  
		Last Modified: Mon, 05 May 2025 17:13:27 GMT  
		Size: 72.7 MB (72737332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a930fecc2fb96c2f9e677a07858b43e2cd8c93fc1d07e83ccad437f5586a97`  
		Last Modified: Mon, 05 May 2025 17:13:26 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:latest` - unknown; unknown

```console
$ docker pull clearlinux@sha256:fe9fa14c6084f34ed493f9afa680fdd0673b3fc315b8430c10a3e9fdcc8c32a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb09bcab1195fcb3627c62d18a734e8cba5f2528fa14da896b6e8d7289758bcc`

```dockerfile
```

-	Layers:
	-	`sha256:9ac0056262842ea1db3511f17027b81b0691450b43d366620a846a3a6648c65b`  
		Last Modified: Mon, 05 May 2025 17:13:26 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json
