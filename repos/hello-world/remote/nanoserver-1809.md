## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:4628b9d6eca69bfc51a9d8f55149bcecbeba8459731a2d5de422d5b03d264ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull hello-world@sha256:741e985f49fc0777c7cb5d3a0018a303e6180b4b4a55b782906b716b24c8183d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104594159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5274654dc3e47cfb4314fdf6c0317c74bece1fd669987020e21b994b1dbcd658`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Wed, 10 Jan 2024 23:56:11 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Wed, 10 Jan 2024 23:56:14 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1304b27db90c80a187cd20ffe7f0976ccf18928e2fd1c9379825166b2cacd5`  
		Last Modified: Wed, 10 Jan 2024 23:56:18 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b7cb9bd34cc785c5cbd8b8e3924d8b027a9629a20e976f70008085100d6e01`  
		Last Modified: Wed, 10 Jan 2024 23:56:18 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
