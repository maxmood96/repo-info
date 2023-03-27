## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:9dfc83ea3cde120ed2ea60f373b51b3c5ffda2acc5a0bd192d638d2958206ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:ddbdfa6b038b56ca66620697069e69c1666f737bc580f093ef58b2d31de57bce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88271333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ae9a3af475a624aa575d571b44a5f272102429b4fc9c0eb2389b20a12d51d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 27 Mar 2023 20:22:48 GMT
ADD file:92950b884d1dc4d7cd9d1740cd5b5e2595cc27404d69b9d7ba59ba1a1058af6a in / 
# Mon, 27 Mar 2023 20:22:49 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 27 Mar 2023 20:22:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2a860cd0d66ce18a1fd369bdf977c40714c1849c25d16d6627654400aee3839e`  
		Last Modified: Mon, 27 Mar 2023 20:23:09 GMT  
		Size: 88.3 MB (88271117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ddfb3bef3c1aaa63ad453605ba9b925048838a77dbededec2975816d58debbe`  
		Last Modified: Mon, 27 Mar 2023 20:22:57 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
