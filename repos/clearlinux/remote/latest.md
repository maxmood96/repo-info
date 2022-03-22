## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:007427b70fcfb1327155b0744764307ab6c8035146a33a2c4ce5b9201b539ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:8698875c60428bd08d0c4a3374f0bc1347f54e5b727d296482270f21c9a1c252
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88050958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6a261b53924a19c5c3a69aef3b6750835c5c11f5681c0a57b1bd2f16540d88`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 21 Mar 2022 21:23:32 GMT
ADD file:173e83d701e1e131a1ad5e6722b44040997055cdcfc0cb28979b0ae2bd6fb770 in / 
# Mon, 21 Mar 2022 21:23:34 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 21 Mar 2022 21:23:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:161f45ff1e758810fc1254beeeec4da27fb7b6efa6421218c2da5902c25c6fd6`  
		Last Modified: Mon, 21 Mar 2022 21:23:57 GMT  
		Size: 88.1 MB (88050740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ba0e27c71cb9a5f10124cb87abbc14843d9b9024561b06df1e41985faf0568`  
		Last Modified: Mon, 21 Mar 2022 21:23:45 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
