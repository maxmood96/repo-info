## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:4bdeb25efe512405d2fb80dcf1358174c9c766d86369b047d605a9363deb2885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull hello-world@sha256:156a2a7ccac3d9740f0ad1133ee43030c24ffcbe308ddc7ee55549dca201a626
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120739083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b86ba68e3fdd953ca03bcf259b772df314fa6de46142d96b78a614b013ed881`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Wed, 09 Apr 2025 01:13:23 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Wed, 09 Apr 2025 01:13:23 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223fa054cb85e977c4af57e22677013773065ef486dbc055647344471973004d`  
		Last Modified: Wed, 09 Apr 2025 01:13:25 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef60f9ad288f7c5bca41e36026b8330e8ee6aba1e25d22f2d0e690fd2b8b46a`  
		Last Modified: Wed, 09 Apr 2025 01:13:25 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
