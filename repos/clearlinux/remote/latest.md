## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:2598af0a167b8330b1e2d363e993945d5314da370dccaf69bb577f3a6ef7856b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:6a7fa57932a6a2d3700b5d850bd4de94d19ff4b4a9a71e813c2fb99670810e13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68080335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31355b39991dff09c90bbdd297d3cf41f379c9b94149601c25b163f0da6a6f7d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 26 Dec 2023 19:30:22 GMT
ADD file:7fdbf99f37c2902d45acde86d13deb894231604ce0b9eba0c5b4c37fa0a6c896 in / 
# Tue, 26 Dec 2023 19:30:23 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Tue, 26 Dec 2023 19:30:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e2979d62b0c338bc088eec92502a19d45010557bcd1b3eea15f91223e7323d45`  
		Last Modified: Tue, 26 Dec 2023 19:30:40 GMT  
		Size: 68.1 MB (68080124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa4f783650b39717a60fe37ddbdc2f3a2e794cb09b0657e35a3e481677dacb4`  
		Last Modified: Tue, 26 Dec 2023 19:30:32 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
