## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:f1f582bf1ec4d153bf422ac33189747f5edb30c26055c6a9249a2b76525030f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:8b8051d7c014c29bd035e60d32b57c217c105a0fb08a372808393c0b2fd37810
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71950203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c98901ef922d1fd0fcfd1d14e584a538849073ed219bfb573b3b4787bdb0c77`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 01 Oct 2024 00:23:26 GMT
ADD file:98765c72a1af3ca9d3313299d22912c65be302b8f1a2daace70ae1fe5da38258 in / 
# Tue, 01 Oct 2024 00:23:27 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Tue, 01 Oct 2024 00:23:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:400279a4664b4a2629f86119cede10f948a2e576dc56cd87e5d98a861ab414b5`  
		Last Modified: Tue, 01 Oct 2024 00:23:43 GMT  
		Size: 71.9 MB (71949991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0288f1d802621636f5225db435b5612a26ea8f2ff8a40556f0b1f74ee43989`  
		Last Modified: Tue, 01 Oct 2024 00:23:34 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
