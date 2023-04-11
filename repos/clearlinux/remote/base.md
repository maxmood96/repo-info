## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:3d8341ec4a037267ec69bd319699d80c2e9c06ed392e5e7a126c2f7ead11eb91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:dfa43c4fee09c1182a1156f6aa5d22ce102805dab6a0460f13ede08570d21e86
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88621004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9b02e74a21a52046db939694ce08e2146f59161df1ad29b8abfd18a81c54b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 11 Apr 2023 19:21:38 GMT
ADD file:5adf3f0084a33bcdf189eb5ce988c199f3f82fe6c129c69643122de69198a6ed in / 
# Tue, 11 Apr 2023 19:21:39 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Tue, 11 Apr 2023 19:21:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0b9bd3080a471d8a7958cecadb8873c684a622b83b43e6a831444817fef5f53c`  
		Last Modified: Tue, 11 Apr 2023 19:21:59 GMT  
		Size: 88.6 MB (88620786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4ed07688bb61d2ac7423cc9b91e14a233cf27d1da648c52e2c521faa7f449b`  
		Last Modified: Tue, 11 Apr 2023 19:21:48 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
