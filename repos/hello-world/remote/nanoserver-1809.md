## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:c9531f9a0fa8c7656281ddc9d6c2696f99fd32c2438f1a31b4b64b7196246bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull hello-world@sha256:c891ad98d505abb8c9618868fc43c74aa94d08f1d7afe37d19647c0030905cae
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101342589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50cc4261fc3da9e119d9ee9ca03452dfee57916d8b02808ad721ef3dc7419482`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 13:21:04 GMT
RUN cmd /S /C #(nop) COPY file:0afaffc2fa64462107b7178b2ae7d20404ff12f637eabe3a8046192b9d9a0338 in C: 
# Wed, 13 Jan 2021 13:21:05 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f2ad3c79fcc2a8a5f82e2bbb42507e565c567e98be7d9812443f76181071faf5`  
		Last Modified: Wed, 13 Jan 2021 13:21:18 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4350ef4c31e7e01a3c0d88e6ff7b338036b113d132865ef81a3415443f5656f8`  
		Last Modified: Wed, 13 Jan 2021 13:21:18 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
