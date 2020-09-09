## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:99dada0ce59ac709cd9159ed92194d99e1a768ce41cd18e0c460094a9d8fc1a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `hello-world:nanoserver` - windows version 10.0.17763.1457; amd64

```console
$ docker pull hello-world@sha256:afe8589c1b07df4af361d249739788deb4d76109795139aa5f710f5638f556f5
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101241587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441fbdc37c401e41789ccccba867ab85698b1ecbbc3de3d5afd71b19a4a6b93d`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Wed, 02 Sep 2020 12:08:18 GMT
RUN Apply image 1809-amd64
# Wed, 09 Sep 2020 12:13:02 GMT
RUN cmd /S /C #(nop) COPY file:0afaffc2fa64462107b7178b2ae7d20404ff12f637eabe3a8046192b9d9a0338 in C: 
# Wed, 09 Sep 2020 12:13:03 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:ecf9bb62dc6eedea9fd367628f8715dea75b7d2053afa4b5121e7809aa692139`  
		Size: 101.2 MB (101239122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5668db61405f34e33f9c14fbbb5fac410bfc2ec6c4cbf6c46854043a735796e3`  
		Last Modified: Wed, 09 Sep 2020 12:13:17 GMT  
		Size: 1.6 KB (1600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de05d96201d8f50fb09e37370d6da683bd9aa7b6a95d5e3db71045261320b6`  
		Last Modified: Wed, 09 Sep 2020 12:13:17 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
