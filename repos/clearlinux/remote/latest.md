## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:4451f0afe7c5914057d3b895fd951c60b4c2a0bf94e623b8dfaa1471f440c98c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:2dea0347901e9e16f5a858dc7a19e8f223f0a5988f561de644b0f722b55ccaa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72207364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a89ed99f6669106dfd283ff336d9070a05d0c10bcf6eed6c7ed4d19774c2cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 23 Jan 2025 23:49:45 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 23 Jan 2025 23:49:45 GMT
ADD base.tar.xz / # buildkit
# Thu, 23 Jan 2025 23:49:45 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 23 Jan 2025 23:49:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b8870ed492ce618b19a03e8eb2915eeb1350e91c2ffaa431124a31590168bfca`  
		Last Modified: Tue, 28 Jan 2025 01:28:02 GMT  
		Size: 72.2 MB (72207149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303b26c871ab9dbfe010d66859e93a03b15a34cc06dc8c392b21f0c6cbef2508`  
		Last Modified: Tue, 28 Jan 2025 01:28:01 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:latest` - unknown; unknown

```console
$ docker pull clearlinux@sha256:a2862fda6e1b52510d81d2cc414cf40a907e15c86280367ff65edde8d85458be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e503a6c043e8453ba2ee485540fe3502cc4d37aab44924e49b96709005d168b`

```dockerfile
```

-	Layers:
	-	`sha256:4e5d1d894ff8ae9f5922b46664a1dc4412dcf2e47c168364f08b3306213adb4e`  
		Last Modified: Tue, 28 Jan 2025 01:28:01 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json
