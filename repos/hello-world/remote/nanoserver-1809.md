## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:54ec70d49446b2b7ab19fcde27890771a1751e602c5de8fb4e3b5448e3b63725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.2452; amd64

```console
$ docker pull hello-world@sha256:2ace993493fbbae9a0e44cff1c09589f59a8306fae084fbf3cf82dbef8b28442
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (103034109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b495126e307c8153b13ca3ff8f0d854ceb4b3e779afb30f9df8ec58368cf050`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 13:11:45 GMT
RUN cmd /S /C #(nop) COPY file:dbb4e437ca342a79d5980fcb71c065abfe00353f696b1b54084e7c09d32ec085 in C: 
# Wed, 12 Jan 2022 13:11:46 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:3a78847ea829208edc2d7b320b7e602b9d12e47689499d5180a9cc7790dec4d7`  
		Size: 103.0 MB (103031066 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:052260bdedd93c210cd755ce8367fb93014f5178e3c65d330bc5de62629951a4`  
		Last Modified: Wed, 12 Jan 2022 13:12:08 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a64f8bebcb262827cf0b7f78ccd2fc98cff78e782d7db1d76f5ba344e73841`  
		Last Modified: Wed, 12 Jan 2022 13:12:07 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
