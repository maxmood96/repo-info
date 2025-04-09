## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:431352b2855feeb5654db0155f58f3401396c02584d2260c14023a3d11a518ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7009; amd64

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

### `hello-world:nanoserver` - windows version 10.0.20348.3453; amd64

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

### `hello-world:nanoserver` - windows version 10.0.17763.7009; amd64

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
