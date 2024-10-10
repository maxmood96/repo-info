## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:5b662e7eecd1d840b46b7e1851e1a2d8216686f1bf31ecb2e1fb8f8f7466111b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.2762; amd64

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

### `hello-world:nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull hello-world@sha256:021ddc79e0783426193571ab98b68ba7d8cf9a01ea223db6ddb2fde955faa014
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155096375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44feca5fb350cebbc7ab8f46321be1a0d80d285cb6d99617fe1a98e21affec6a`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Wed, 09 Oct 2024 22:57:56 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Wed, 09 Oct 2024 22:57:58 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1ddae6505dea12aa52146b7471bbf898d8306947cb7064e3729d9d7685c1ca`  
		Last Modified: Wed, 09 Oct 2024 22:58:00 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2449acfe7797abcd8e2a04a169df0a4c64da9627c3e6b321ce88af5f5e7cd55b`  
		Last Modified: Wed, 09 Oct 2024 22:58:00 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
