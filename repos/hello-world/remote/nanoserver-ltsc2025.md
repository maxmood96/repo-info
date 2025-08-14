## `hello-world:nanoserver-ltsc2025`

```console
$ docker pull hello-world@sha256:61eb53c21e3e4da751d3a6d25bc67de3e8f9541d0d5a8f2f4414ff011b33040b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `hello-world:nanoserver-ltsc2025` - windows version 10.0.26100.4946; amd64

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
