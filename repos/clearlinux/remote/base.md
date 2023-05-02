## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:58f4efe01526442f14587a2d50971acd33660e05b43220a732be18e36b83d749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:85f60507f54e2bd8184a1fecfb3af2cb724f7db8becbd4a3354b4984513d2826
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89775127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc0bb00cfb0c65a479b88c1ea218ecfd87ced2d5251cd0a938b0675442157ff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 02 May 2023 20:29:19 GMT
ADD file:66b4f79041bd240d00f201f115219498d8d03081e9eea1468e75ad36e0f3ad93 in / 
# Tue, 02 May 2023 20:29:20 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Tue, 02 May 2023 20:29:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f0426e1cbfa2ed56a3c65768b5e1b37773f0333907a3ac4101dc47d18d387d42`  
		Last Modified: Tue, 02 May 2023 20:29:37 GMT  
		Size: 89.8 MB (89774910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1841d099d38394b658ab0eb242f74f301be77bd313f9d398a98554e0df4b85c6`  
		Last Modified: Tue, 02 May 2023 20:29:27 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
