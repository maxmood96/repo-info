## `archlinux:base-devel-20230528.0.154326`

```console
$ docker pull archlinux@sha256:4b5f5c31a5a04caf428c8d9a175a87dbecbb9e3a892ba78abac8126603ce1784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20230528.0.154326` - linux; amd64

```console
$ docker pull archlinux@sha256:3317d3adc1a1f4b85e81155b46c1e367bb9b085bbaa1ca87e4640cd2e5fd8cca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252919851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819b57250da9b69d039a563491c13407eec79cf6d620faab7a1d9c4bd341d781`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 20:20:53 GMT
COPY dir:44daec227b53dff21531675eb39198acc99b78db7d8bbad351395eeb4ec096dc in / 
# Tue, 30 May 2023 20:20:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Tue, 30 May 2023 20:20:56 GMT
ENV LANG=C.UTF-8
# Tue, 30 May 2023 20:20:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:45ff414ffddb9107ed6633f3e3b38d498f0389de57fb0e9f523624790b937b12`  
		Last Modified: Tue, 30 May 2023 20:22:09 GMT  
		Size: 252.9 MB (252911130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43212488f1a732a4a7904dfc536c8069682e42e2392388c4035620e77d8949d`  
		Last Modified: Tue, 30 May 2023 20:21:36 GMT  
		Size: 8.7 KB (8721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
