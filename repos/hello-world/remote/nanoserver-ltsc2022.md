## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:093fc43e7a89405133ed385553fa0416393ad32ac7876379c3c1d19719df9ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull hello-world@sha256:c8e4ce54c77ac4705db52649726ebe2ef595ab3676bc3475828ad75cd6c216eb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.5 MB (120513811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50dbe804073a38e5ae439aa8af010144dad6c988139aea999dc7d3177b0411fe`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Wed, 09 Oct 2024 22:57:37 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Wed, 09 Oct 2024 22:57:37 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba3e107b76561a5897c0f7fce3ad4a1f062629cfad42b394a36be296f15fa2c`  
		Last Modified: Wed, 09 Oct 2024 22:57:40 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7297a5c564d9416e6441f4588784b35df60e487fc17bf57724283644bed70f7c`  
		Last Modified: Wed, 09 Oct 2024 22:57:40 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
