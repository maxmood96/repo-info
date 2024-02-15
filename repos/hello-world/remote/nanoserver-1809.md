## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:3dc2e43c94e7bad2d4352b1d19c9524f7be36697820c8a86f4c3d4c4319a92d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull hello-world@sha256:088bdbea94d5c8fe3eb9f3cec836c3f7ea82923e7d0d3a4f1146ef0f860f5a93
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104624406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20c2a9cc77ae3474b2738a6c3dc715f6429df9152f24d03e8734eae14a1ea5f`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 19:53:45 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Wed, 14 Feb 2024 19:53:47 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f352d04d1742a39c08c2e779e52ff242a2b6ca46c59050e9c87d6e2e8e87b8`  
		Last Modified: Wed, 14 Feb 2024 19:53:49 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75410b00abbb3512684efb518f31ecb314ef4a895364bfdaac13cc4eba4a5257`  
		Last Modified: Wed, 14 Feb 2024 19:53:49 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
