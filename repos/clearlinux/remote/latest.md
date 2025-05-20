## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:cf8d0d8707e5ff69ea0d69428ecd5ec3f0dd6e3cba60fa19fe4bf817034a54cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:153420abd1eeabeae673e9e8e8f032a99faa6f21c3393e67f94ca8c07ca19a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73021349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd7191057bb1394f50501fadb72d8070974592ab76d1c3b881942221fd372ab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 May 2025 16:14:40 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 15 May 2025 16:14:40 GMT
ADD base.tar.xz / # buildkit
# Thu, 15 May 2025 16:14:40 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 15 May 2025 16:14:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dbc924beb9cea03ab11baaa72b044a9060538e4564c6d4fc09b0b60961f321ed`  
		Last Modified: Mon, 19 May 2025 23:06:12 GMT  
		Size: 73.0 MB (73021135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc590ad57e0a27bd1918f0d9b95238ee6666a57a13d7a0e36b343dcd0e35ac7e`  
		Last Modified: Mon, 19 May 2025 23:05:47 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:latest` - unknown; unknown

```console
$ docker pull clearlinux@sha256:7c62f4144cd6e7b377446778575c9ff7632986b5b07bf9ebd8616aafa8a87e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0dee5d9c9a044d080409453cd74872797e7e97cf59badb056ee423b97a45da`

```dockerfile
```

-	Layers:
	-	`sha256:8447a9048951b2730dfa33aae8f0d41cbacc6d3d1d00a608ca4a3bfbda3f2151`  
		Last Modified: Tue, 20 May 2025 02:04:16 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json
