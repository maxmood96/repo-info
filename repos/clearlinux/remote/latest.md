## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:d3dd73575d2eb9c6ffb635c82b266fa9266591db844ac9f41014c0af415992c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:f6c07db408755f2e3a9a81ffca8f16faa9b94aac6966ad94f6ee5441b1444b4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87155085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2e188037f42b8090bcab4a8d7f35ecb9fd15baaff4b6989626b3177ca5d435`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 21 Feb 2023 20:24:22 GMT
ADD file:af0ad203353babab0263e1793415c0f1c3993ec33c99a6cd842dccba66d76f46 in / 
# Tue, 21 Feb 2023 20:24:23 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Tue, 21 Feb 2023 20:24:23 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:436554c6b02d79f7b424b5bf4c88fea4c88bdd9839abe87f5ae3e3f4ececd6b4`  
		Last Modified: Tue, 21 Feb 2023 20:24:41 GMT  
		Size: 87.2 MB (87154868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2337eda6ab19f9ce87b8a0928fe67d127e278291b6757e0a99fc4784e99b00f`  
		Last Modified: Tue, 21 Feb 2023 20:24:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
