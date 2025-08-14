## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:533cea5ed5c9a782b8099ecc6db24d00a493290cf3dc1eccab2fbbbe8472984b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `hello-world:nanoserver` - windows version 10.0.26100.4946; amd64

```console
$ docker pull hello-world@sha256:f50ee46444ef55bb677ee156456a7f9df25316d890d443548fff3d1f484714a3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193472226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f07e694075a85897485216e62aaae92cb7cb17c7f562223e14335d3e787d13c`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sun, 10 Aug 2025 02:44:20 GMT
RUN Apply image 10.0.26100.4946
# Tue, 12 Aug 2025 20:22:46 GMT
RUN cmd /S /C #(nop) COPY file:1ae3735b36d6b3fc6ef1fd1d2d12badf8f42ad5660d983c9a406cb560633ed37 in C: 
# Tue, 12 Aug 2025 20:22:47 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:6d63d98dae9e3419e8c965c24a11d30e40947cf35ee17c204c5d8b7bae7ff2ef`  
		Last Modified: Tue, 12 Aug 2025 21:13:38 GMT  
		Size: 193.5 MB (193469373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413e788cd5f721eb084057ef120e7a2145be7dbf68cb6a3f9ce109eddd1de349`  
		Last Modified: Tue, 12 Aug 2025 20:23:37 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8841065237d9e5774c234fc119b2044ac3ce1dece4aa971f9f49d0be68b508ca`  
		Last Modified: Tue, 12 Aug 2025 20:23:37 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull hello-world@sha256:1ea80daeeab481d4df055245fe34349d31c7409fa4e66d3506f3e31538855017
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122663107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7d754e2cf88cc106712a0449340a1487247c587abd840b7f931452985055a2`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:22:49 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Tue, 12 Aug 2025 20:22:49 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee6246e0cddf4df3c84bbccbf1f5b208533d84a743a376123e87b5bb0aa283b`  
		Last Modified: Tue, 12 Aug 2025 20:23:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8ee7fe4fb2104d1e612d99e73656c0ebc7d696b67654517450a9fb643966ad`  
		Last Modified: Tue, 12 Aug 2025 20:23:35 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
