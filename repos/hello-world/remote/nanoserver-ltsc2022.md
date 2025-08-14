## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:765aeb8dcea2b905e4d8d6c731c6a978c8a5bfc2267113baa9b5c120d9d39b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

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
