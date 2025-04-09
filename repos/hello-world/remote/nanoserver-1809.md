## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:62148e4ac11eb6a7e0628759db99ed96d1d1aa66c74f94b3ae73105808ffde82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.7136; amd64

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
