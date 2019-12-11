## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:f79d26474b02aa9d105a36cee22c2515111844df37163f6822b41d279f7cee83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull hello-world@sha256:351e40a9ab7ca6818dfbf9c967d1dd15599438edc41189e3d4d87eeffba5b8bf
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101108700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16464c76a19c8d421eb399abf70ec009d94df8f7817f7a3410c46d9b3e3ab98d`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Tue, 10 Dec 2019 22:10:28 GMT
RUN cmd /S /C #(nop) COPY file:0afaffc2fa64462107b7178b2ae7d20404ff12f637eabe3a8046192b9d9a0338 in C: 
# Tue, 10 Dec 2019 22:10:29 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:1951f408509ba9ddcf240ef5d838c72c5596f97a05b063446508f2ba15d510f2`  
		Size: 101.1 MB (101106116 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b0b355a12b28eb47202572e0a6ee477c93ab4be3be2e0e88790927f6f9e0e87d`  
		Last Modified: Tue, 10 Dec 2019 22:10:46 GMT  
		Size: 1.7 KB (1664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1cd8096f0f3963947727f23bcbb892d31702fd3bcb7b0a32aa8518f2b9bfdc`  
		Last Modified: Tue, 10 Dec 2019 22:10:45 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
