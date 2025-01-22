## `hello-world:nanoserver-ltsc2025`

```console
$ docker pull hello-world@sha256:9fbd3697f9dfc5425b6282d729151e61c5bc5042f9353bf2101964da7068b940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `hello-world:nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull hello-world@sha256:3070452d117828a9eb91c87c71f7e71605ceb531598c0acd2575ac2a90b8791d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199057063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c690bbde374586e3022cf23491339d9925d92e728ce4f5020338ec3657aecdee`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 22 Jan 2025 02:28:04 GMT
RUN cmd /S /C #(nop) COPY file:1ae3735b36d6b3fc6ef1fd1d2d12badf8f42ad5660d983c9a406cb560633ed37 in C: 
# Wed, 22 Jan 2025 02:28:04 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a575af90262df1196a014105a8994708f234f7f3663b27c5be27508443c98d9e`  
		Last Modified: Wed, 22 Jan 2025 02:28:08 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6308f12cac64ca86e267b96ebe7b3a1a876e0e6f8874df3113c7f72b9dfa05b6`  
		Last Modified: Wed, 22 Jan 2025 02:28:08 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
