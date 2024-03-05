## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:240e1b1f6b326576de6902fad1d182f00baec563c7358b5e22e1e5cfec5fdd8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:c517468089327f5843ed12020d5323efd5a66f52fa7e1b7de1cdfe258eff66ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65296831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9018d3df6c3b94831e8387d65f47d528e50648ec710e923d321026c1fe7000be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 05 Mar 2024 00:54:02 GMT
ADD file:0081106c535fdb373ce7945c1ade403ffbeb1b95a798da56ab3c3cae92be179a in / 
# Tue, 05 Mar 2024 00:54:03 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Tue, 05 Mar 2024 00:54:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b64952a1dc8e03458956afd1937f26cf385807862e85d1ca3558e1024b85bf66`  
		Last Modified: Tue, 05 Mar 2024 00:54:20 GMT  
		Size: 65.3 MB (65296620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5d46407ab46341c8ec97a6aa07f999afe24eb3014862f52a1c2f5a51480f3a`  
		Last Modified: Tue, 05 Mar 2024 00:54:12 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
