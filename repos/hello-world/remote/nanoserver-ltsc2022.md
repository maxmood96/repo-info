## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:d9a1e5a0f73a97924fdd9863a717a4e46c6ef7a9c6a769d0053df1b4afbeaae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull hello-world@sha256:2f19ce27632e6baf4ebb1b582960d68948e52902c8cfac10133da0058f1dab23
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120705489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4df9232a51a135a5445363e5812f099cb9aebac338cc04e857c09b50475d92`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Tue, 05 Mar 2024 19:20:30 GMT
RUN Apply image 10.0.20348.2340
# Tue, 12 Mar 2024 23:58:00 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Tue, 12 Mar 2024 23:58:01 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:94ec3b200bababb5c0b6605ad82c23779d8f918fbfe1ef5d1cf51be6f12fa749`  
		Last Modified: Tue, 12 Mar 2024 19:42:37 GMT  
		Size: 120.7 MB (120702694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96349c1d782fecae40700091dafe28fa8d14f366569fdd910fa187a63d65b580`  
		Last Modified: Tue, 12 Mar 2024 23:58:03 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0057fc59369cf17cd5e000c5cdcde520da9276c8478befe99d5d700a621dd21e`  
		Last Modified: Tue, 12 Mar 2024 23:58:03 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
