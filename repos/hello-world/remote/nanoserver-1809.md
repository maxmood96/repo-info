## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:8c4ce6bd3e746243ff284710ee95caf21d9a08e50e7a6f0c9dffe36cf681a7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull hello-world@sha256:22d2e99f3bd1c5f6706995d3d76aa53fe25c49d6cd1e4dbfdd452d37b8d93fe5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155085886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22694920b31fa7cbbbaaf903b97cfe62a4949caae00f4756ec673d6a329d008c`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:02:36 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Tue, 13 Aug 2024 20:02:37 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3888db953df238ded741089e208af46b29c213ce4d09ceeee40214d9047f22`  
		Last Modified: Tue, 13 Aug 2024 20:02:41 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab866df638435514bcf8a48e17dfe5f9cd1b591a8f6c509c4b566972b3605459`  
		Last Modified: Tue, 13 Aug 2024 20:02:41 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
