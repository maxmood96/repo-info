## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:2ad489c2c9c7e95ea1186df52f3c5ba600676f9f71ad155483d1e1a855bcdcbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:4ded7f26758b04052f307160ba83a445fa286ddcc45e47eb5851539c5199a030
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68835200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08a937e02b1a6f949658edb4aea1c6ee917dd8d0021a50df2abf37fe1ef64e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 15 Apr 2024 17:50:14 GMT
ADD file:cc60085a9a5adc2fde18aad73a7434d0674f04a1394934851efedc8f1269f4eb in / 
# Mon, 15 Apr 2024 17:50:15 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 15 Apr 2024 17:50:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:16b7c468d9877baba670768f000b8778d9dc8f7fa4a1983a63db483db9abb1ac`  
		Last Modified: Mon, 15 Apr 2024 17:50:33 GMT  
		Size: 68.8 MB (68834986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6e82aa03d2e0017e9f6737f26e8fcbca5c12d5f9162492241ae87f253c3cf3`  
		Last Modified: Mon, 15 Apr 2024 17:50:24 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
