## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:726f486c9348f32a8294d134c554d4e3083f47e71ecd2582cb90b5e5b80f7910
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:0d349283cca5d9a30e6764a3f07cb82c8b1980b13fe0b87eaa98a4a0c9991fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72131949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d0f723560b8138a7fb861d9e3d0a7182ddb5bea96f34ecbc129ef21637fab4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 05 Nov 2024 04:32:21 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 05 Nov 2024 04:32:21 GMT
ADD base.tar.xz / # buildkit
# Tue, 05 Nov 2024 04:32:21 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Tue, 05 Nov 2024 04:32:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:08ca51b4ff2dfe74e9512483f23ac63a73272ddeec360c892108242123dc4cb2`  
		Last Modified: Tue, 12 Nov 2024 00:54:49 GMT  
		Size: 72.1 MB (72131736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e8449afa0982280756d80cfd998a837b543ce3489db4df6e8a207422cd5ab9`  
		Last Modified: Tue, 12 Nov 2024 00:54:48 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:4510c4206283b6051fa9bc83f7d1c580ed287d9f146d6644a5a35a2bef6cf87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01309640b10fb35129ad792c2b5c8425de6325fdfb21cd4d9d79278789859949`

```dockerfile
```

-	Layers:
	-	`sha256:cb8d5a817af6ac57f83927411049b49e309156cc9c008eaab0e0582829109bec`  
		Last Modified: Tue, 12 Nov 2024 00:54:48 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json
