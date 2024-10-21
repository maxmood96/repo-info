## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:9fa4143694d956928d73af04aab65ffe6a02cd0e3d2e59dec2ed0c4dba5f6add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:3cf5924f041e3cf20a7a0a29daf84c2f28c48f0c7c6d52966fba472bd951d2b4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71984521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fa613333204360afa0819a3a7a9e55e515e8fa03999c32179c4c985dd123d9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 21 Oct 2024 18:19:35 GMT
ADD file:504c207cc6b21a663713923eb52300d2c2dca10a0636339277a9daf714444bc3 in / 
# Mon, 21 Oct 2024 18:19:36 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 21 Oct 2024 18:19:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:03e65fbc7302972a3ecce582cc0aa7d80ad9498bdf6d3736106172b95750b60f`  
		Last Modified: Mon, 21 Oct 2024 18:19:53 GMT  
		Size: 72.0 MB (71984308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66bf68d01e3b24e4960896a65874e4593396d5026bc085e58098162c198e8ce`  
		Last Modified: Mon, 21 Oct 2024 18:19:45 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
