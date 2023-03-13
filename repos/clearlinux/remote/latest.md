## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:3ff6d61808807d5b6f18165ed22b366f4c0e90afe119ef73cb05350f5c367f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:eea62ffd494cb3803e719b6b1446f321a11e0fcdb12ce3c844931934c846b0bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87808584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a24f82d8974f59c66f169bc708b57281ad3731687bd4dd1505dddece4eace5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 13 Mar 2023 20:24:12 GMT
ADD file:e80146d51a456f887185d36834014ff7c260fe5570ad1f504a70103438db850b in / 
# Mon, 13 Mar 2023 20:24:13 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 13 Mar 2023 20:24:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2339181c9005cecc1a361e85f5dc3c8cb5adc4c50c64e26ce0911541b76e2734`  
		Last Modified: Mon, 13 Mar 2023 20:24:34 GMT  
		Size: 87.8 MB (87808368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d35afbe15c5a3905fe930623b0ce426ebe4b5449f7f4598f3a80fc7108cbe8`  
		Last Modified: Mon, 13 Mar 2023 20:24:24 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
