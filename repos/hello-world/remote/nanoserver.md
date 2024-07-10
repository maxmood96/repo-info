## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:a8f654357ec406244abf4090c3a9494b58d6af73b293eaad9c07f7949370d5fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.2582; amd64

```console
$ docker pull hello-world@sha256:321dfaa5b73ffd9004a10ad894512e3f190faf5468da6412b85e621d62bb72ec
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.5 MB (120493169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18d27310d48c58b99e34ef009ff20d20534c49717ea7658ca37791aeee8adf3`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Wed, 03 Jul 2024 09:30:07 GMT
RUN Apply image 10.0.20348.2582
# Wed, 10 Jul 2024 16:58:10 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Wed, 10 Jul 2024 16:58:11 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:652774a5d82a114642848f8b0b8d486ec1b4995f9dda56e36fe4ac7563429990`  
		Last Modified: Tue, 09 Jul 2024 20:33:26 GMT  
		Size: 120.5 MB (120490378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742af9981066c433d413d2620a0e996978ef4b46879d602ed5b1f5a3001bc1c9`  
		Last Modified: Wed, 10 Jul 2024 16:58:13 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8d60d4785db6a268a4cadb2814b781f108fb7fecb355bfcf9b50985013268a`  
		Last Modified: Wed, 10 Jul 2024 16:58:13 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.6054; amd64

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
