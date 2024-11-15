## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:72ad20eec310e9592942e6502318ddfddbd46d9e3f2f181d5fcf316f37f525f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull hello-world@sha256:5e44bb920261355fb67c79f81f46618a7cf46ac8fd0a9cb27078f386e4a6bd14
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155217091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9013d329142713b1f80bf068d542c6912c9bcbfe02e32e08e00d7b284ada3974`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 20:05:00 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Thu, 14 Nov 2024 20:05:03 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40757cb76c467dfc3ee48a8ad0f10a6fd5167bbf5ca775aa2422ca4a6a9116a1`  
		Last Modified: Thu, 14 Nov 2024 20:05:08 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e41233fcb4d960d808a3ab3fba7665c75cdaea393e3944718a38ff73c3a9b2`  
		Last Modified: Thu, 14 Nov 2024 20:05:08 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
