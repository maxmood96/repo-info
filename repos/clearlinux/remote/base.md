## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:72782ecd07a3c773c5bafb1203c2d58e3f0eb66b281d19b96fb04f5853012404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:139338a813f27293ed5d8a552efc24d90cd10e533b2f79cd27046b03f496df0c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71936338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbd6ef29ff50e63abad683b5b68e7497934e2e72b593acfd50fa21ef822518c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 03 Sep 2024 20:19:48 GMT
ADD file:818d09a29a20492f7c505b61b1549046d40d80a056d5f4bb20c0322b9fc566d2 in / 
# Tue, 03 Sep 2024 20:19:49 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Tue, 03 Sep 2024 20:19:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:59d943a4296bee14c3c06b6ed71c77ebb445da07a15837f6fcd9647b9cecc1cf`  
		Last Modified: Tue, 03 Sep 2024 20:20:06 GMT  
		Size: 71.9 MB (71936127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe1b334aba598a560769c17df385f0feacc5e73ab2c5405dd5c6428cb8fb4a6`  
		Last Modified: Tue, 03 Sep 2024 20:19:57 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
