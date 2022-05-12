## `amazonlinux:devel-with-sources`

```console
$ docker pull amazonlinux@sha256:4c152e453fb99b4f2716d50ab2bc89563e1891db06135940131dd5e2fd1179ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:devel-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:698032efb39ccbab8dc9abc5dc3b57682f1da1b89aa8a60bed1e5fd24f87e7d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.3 MB (489262019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bacdbeb608c26f31936f6982745dade2ec6c8d386926a8d490da20af6de4a85`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 May 2022 23:19:33 GMT
ADD file:8938ca932860236a5478568502c523de28f6fdb1844554dff09a9073e58e2d64 in / 
# Mon, 02 May 2022 23:19:34 GMT
CMD ["/bin/bash"]
# Mon, 02 May 2022 23:19:54 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-30a96c4f6cb306f42c34e07a80efcfbe6980633a9ac34327014a87423221b673.tar.gz"  && echo "eb2de792ff0fb280db260db9b6f4c55b40e52059337fc4c1a293f79f2b4e45bf  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ea1ba8a91f0904c1d69fc8987dcf4d80e75a6f574e1b4a292e9be3e1b78f1def`  
		Last Modified: Mon, 02 May 2022 09:17:35 GMT  
		Size: 70.6 MB (70553888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39db4bfd73372833edec2c995c10e909ff279746b73b39bbb9a78a95ef9464a`  
		Last Modified: Mon, 02 May 2022 23:21:01 GMT  
		Size: 418.7 MB (418708131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:devel-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:db26696e2371b0e24bc72edf8c118bd9cb18821dfe4f2343495d33eb93aaf2fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.9 MB (487866967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7afbb6532b42550d7ce56e9d45b1a30eddbbdf33eef198e4ba4b1123cf9ae38`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 May 2022 22:03:11 GMT
ADD file:8406e9d49dfceecd7a1c2cbf960e61dfe58dc85ab0ec500fe43df4123ea56b54 in / 
# Thu, 12 May 2022 22:03:13 GMT
CMD ["/bin/bash"]
# Thu, 12 May 2022 22:03:35 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-505b05ef761a138f8860c413d1520f5756d3a4ea82c5f6052934f3c34a880580.tar.gz"  && echo "bcbcae8a56de8cd107a736a9032b166d5ae7a15c72dbc2e8029ec7ac75d4c5da  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:57916acdbf1d56e1afdf905446c5a93b04658842560d4e5c51a61a1881c5f8b4`  
		Last Modified: Thu, 12 May 2022 22:04:21 GMT  
		Size: 69.1 MB (69117442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f37a59badfcabe5a4ef65d9e6f67b552297ca000f896c8a7f5bffc17447a49`  
		Last Modified: Thu, 12 May 2022 22:05:01 GMT  
		Size: 418.7 MB (418749525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
