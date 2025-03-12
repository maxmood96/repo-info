## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:e18d99d918ab5df71a21edf86591cc6e8037f6dbdec710950219ae827869a87f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `hello-world:nanoserver` - windows version 10.0.26100.3476; amd64

```console
$ docker pull hello-world@sha256:8624e61fae32dc716d33d40f9c075b7245246180a1969c81f4f66b8a3b0c7a32
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206305038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee339c49b8580808010e086f1004ea95f2be73ed8081539a8f4165ed901f2602`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Wed, 12 Mar 2025 18:43:08 GMT
RUN cmd /S /C #(nop) COPY file:1ae3735b36d6b3fc6ef1fd1d2d12badf8f42ad5660d983c9a406cb560633ed37 in C: 
# Wed, 12 Mar 2025 18:43:09 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee25e6b4b5ae8dd36fe3e922969584cb067b792f3982c7c9bdb41e9f1e0bcfc5`  
		Last Modified: Wed, 12 Mar 2025 18:43:11 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd5076e2b282441244beee4e4a150361623dd814ad5c8d43a7768ebd2dc5e14`  
		Last Modified: Wed, 12 Mar 2025 18:43:11 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.20348.3328; amd64

```console
$ docker pull hello-world@sha256:5e98ef53f6ec1678c4fe3d4f8fe4a0e8308c1305bcad58944a2491f40ab8001b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120698349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1bd2628a13622d38f7ae22fc482430fe8ff538416b4bdc38e2d3de5c4a90c2`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 18:43:22 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Wed, 12 Mar 2025 18:43:22 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46da91e0662a661cee0e8653fb251ddf9ff8a7a79ea868baad10057ebb9e568`  
		Last Modified: Wed, 12 Mar 2025 18:43:26 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9c489d3fbaf869b98e6866d6f9f703c955de90da0dec6fb073b058254166e3`  
		Last Modified: Wed, 12 Mar 2025 18:43:26 GMT  
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
