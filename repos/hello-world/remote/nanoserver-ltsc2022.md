## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:f4f89322e0adadc510078a70ea6f114afd578b627eb1eb20de0ccdd9150a3212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2159; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.2159; amd64

```console
$ docker pull hello-world@sha256:44497cf9d4c0c84fc8a74cb823dbbc0a0e3a2a8fe6339dc8b0c56850d0b9a7d5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120760076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a33b06b1557f692c4ef4e52fee22e1af2f035d87c7b32f57e5d4fb5c4bf736d`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sat, 02 Dec 2023 12:14:23 GMT
RUN Apply image 10.0.20348.2159
# Wed, 13 Dec 2023 00:54:38 GMT
RUN cmd /S /C #(nop) COPY file:ac9f104fd739943f22886335a779468d86b20ac43fd3168171f6b23fc28882b9 in C: 
# Wed, 13 Dec 2023 00:54:39 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:075332bb10f7fc70c56f7c073dd753e05cacbc93a38c181c5576739a29f8a7e1`  
		Last Modified: Tue, 12 Dec 2023 21:35:16 GMT  
		Size: 120.8 MB (120757041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672777f62307c9af99da139b8f6d8285d7549f4342916f54c33c58b62b3ae771`  
		Last Modified: Wed, 13 Dec 2023 00:55:03 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647d048f809356c4d1cbb10aeaab6abbd2d1cd4165417283246faa28f12ae1e4`  
		Last Modified: Wed, 13 Dec 2023 00:55:03 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
