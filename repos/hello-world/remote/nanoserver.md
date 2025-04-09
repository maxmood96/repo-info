## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:d51057fe1bcf1c5e471d6f64e612b41895997cd4f6bea686d248b0a218d5c681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.17763.7136; amd64

### `hello-world:nanoserver` - windows version 10.0.26100.3775; amd64

```console
$ docker pull hello-world@sha256:cd293bc776c27d1b3902b2649b46d336295f6cf72f9cc6a812610120330e510a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190116022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717e70a68e84478d16955e2fc0a03c9bc9516d2e77fb61ecfbb690f4fe38a711`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 00:36:07 GMT
RUN cmd /S /C #(nop) COPY file:1ae3735b36d6b3fc6ef1fd1d2d12badf8f42ad5660d983c9a406cb560633ed37 in C: 
# Wed, 09 Apr 2025 00:36:09 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79eff77174fd757c2eff747e1ca53f7e57b76165fcfd16d11efb442b5621f846`  
		Last Modified: Wed, 09 Apr 2025 00:36:12 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d230a332f307b4059fc7eca36a7144666aadebf72b66490b0c5b269b0d205491`  
		Last Modified: Wed, 09 Apr 2025 00:36:12 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.7136; amd64

```console
$ docker pull hello-world@sha256:d18b7b53d1c2a4da501471f75b7f3bb70ee94505c63b39e4800ee75b7841fc48
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106925269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa19d3e486541342f72a05d3d28f065de2f013356e13b1a33ae9ceb8dd27fdd`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Wed, 09 Apr 2025 00:36:09 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Wed, 09 Apr 2025 00:36:11 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b0179748b5f3bfbfbd7e0dacfb4311832e810d6c4891fc3dba1a80cadde425`  
		Last Modified: Wed, 09 Apr 2025 00:36:14 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb1eeda9417b1d38264e2adeeb3ccfc264d101c4b1c54f8acca99f9c675f555`  
		Last Modified: Wed, 09 Apr 2025 00:36:14 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
