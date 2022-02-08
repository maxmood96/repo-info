## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:48ba652957093eaf8f916bf63d8e776ed7830627f2ce3dda733c47228795d285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:502c13d08b6c71e3e81174575db44ad2bd50e410f85c3153385709da702dfbb9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88932015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64989659c2de8e4601e5244d23d9d693f15c45a450abfefdeb0699690d9acf4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 07 Feb 2022 20:23:10 GMT
ADD file:f4d094d95d1fecee2c43314cafc51eef2b979e29bf7d7727bff9db88021b8e98 in / 
# Mon, 07 Feb 2022 20:23:11 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 07 Feb 2022 20:23:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aebdd183fbf55894a4c6c583fb76e16cab758da6bec832ac11e1df8d9e633b6c`  
		Last Modified: Mon, 07 Feb 2022 20:23:34 GMT  
		Size: 88.9 MB (88931798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d89951d4e5e672267ea9884fb3719bd8afecfa7584110e8f26f01f28392225`  
		Last Modified: Mon, 07 Feb 2022 20:23:22 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
