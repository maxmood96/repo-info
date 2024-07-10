## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:2d9529d294cf53211e0a1f7db0db6a55383ca9b37eba529904e84ebf555548a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull hello-world@sha256:3681aa9aed8e441153021bcd4f1253c48d99c9b43b6252748353ab64a4ff46a3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155084166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9ff65226108f6f5e77ef09257c7712c4a95c7c153be3753141ae40b64676d0`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 16:57:58 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Wed, 10 Jul 2024 16:57:59 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c0e19ca80c2db57e31044041879a883a547ec1486f02c5c21c083fc956b9c3`  
		Last Modified: Wed, 10 Jul 2024 16:58:01 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86583d90fccb184a9b0a8f066c760cbbb2ba106954fc59085225287f72282e5`  
		Last Modified: Wed, 10 Jul 2024 16:58:01 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
