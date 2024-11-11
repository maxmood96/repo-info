## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:effb4315e9c7e27a39b3c2ef1b2ecc3018b57a4ccd9ca4aa1cb81e88b018294d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:ea4bd3ee9b96221a3bff7671d1683bd019fd982c39b14a9e8a2bff1aae9257d2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72129976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d669f441b445d592d6574aef20ce1a5927c41f8bad2585e8f4b11adc6d571e84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 11 Nov 2024 19:19:46 GMT
ADD file:0fb1415e3533ba9ae155bafe58d57ddbfedd50ff8886ae128dba62f154ccec1e in / 
# Mon, 11 Nov 2024 19:19:48 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 11 Nov 2024 19:19:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ec4a9d6644dbc3195c32c272329e24e62c2e7eca188cd32775e966d0910c8f58`  
		Last Modified: Mon, 11 Nov 2024 19:20:04 GMT  
		Size: 72.1 MB (72129763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bca16fd9592dace5b84fbe5ae38a23a712d7c4fe2d6a8739609b74369202280`  
		Last Modified: Mon, 11 Nov 2024 19:19:55 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
