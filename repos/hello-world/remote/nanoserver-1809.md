## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:786221e5d24f1ec1d54e7d0a156db7937904a108ca344cff68a0354409f06845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull hello-world@sha256:f32848311348c2d248635c5f47c97e1409f7dbd1b08ddaca101fbb0af2f3ecfd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106910576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9edf19a2f34fa58b36f87e3efda161dc8ddb0bc6f6a19da8673cdda862148d`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Wed, 12 Mar 2025 18:43:22 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Wed, 12 Mar 2025 18:43:23 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361e37a862fe155b4a60b0ce1fb2c10a0233057a5dc3a8e6fc7ab0b869025a41`  
		Last Modified: Wed, 12 Mar 2025 18:43:26 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dedd9e64479a5d2444b4f4a7a2e9fdcc125e680c1625ad9c25329a19a56b744`  
		Last Modified: Wed, 12 Mar 2025 18:43:26 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
