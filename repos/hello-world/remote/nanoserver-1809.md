## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:9c478efbd2812038a3e3b421c56f08d0b47b3847f03669ac3ca3de2e038ac9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull hello-world@sha256:6f3e9cb5ba02b4607759878cab7a0e838580ac23e95ee5dad4410bfef2707182
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106918232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863268e13a654ebe7b16e038a9c68028f49d87079004a5b46914968fbbdda689`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 00:28:05 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Thu, 13 Feb 2025 00:28:07 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6ae2e93fcab86cfb343d0d766eeaa15086901ae9b5c8e2a468cd78bb4f6726`  
		Last Modified: Thu, 13 Feb 2025 00:28:42 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9fe1136a6ad1252569c0ac51fc15bb8f0bbc7b49d3016c9fdc7cb8b4299106c`  
		Last Modified: Thu, 13 Feb 2025 00:28:42 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
