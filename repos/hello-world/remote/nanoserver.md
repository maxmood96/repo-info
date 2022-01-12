## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:a23331fc11117e58e611ff577b9f5b06a4280a9fb5172a3c3f01640184ba43be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.469; amd64
	-	windows version 10.0.17763.2452; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.469; amd64

```console
$ docker pull hello-world@sha256:8ad7c869546021c7af55ebb2c376dca59c3829ea4588e7fd22a4a1c8f5bcb472
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117337353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9ca78832b1805382ef71ddc1b108b5a65f0e49e9e24b6f285cc537c5072c46`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 06 Jan 2022 03:34:42 GMT
RUN Apply image ltsc2022-amd64
# Tue, 11 Jan 2022 20:48:49 GMT
RUN cmd /S /C #(nop) COPY file:55c009fa8b983e38026b41064e5367bc779dae76c0d404a11886c3cb19ec4509 in C: 
# Tue, 11 Jan 2022 20:48:50 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:b2bb136f79c12b0a42720d7bb83469bce3f7bf2ca5c8bc68a36228796311fc6b`  
		Size: 117.3 MB (117334348 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1693f2bb3e1cc4eda5d0bd640e0efedc1778ecd9610aa18ab06fdf3dd46d6c35`  
		Last Modified: Tue, 11 Jan 2022 20:49:17 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698f7fae438e6cd3f9363993be625d0f68f81f160c816177da50be9acff80218`  
		Last Modified: Tue, 11 Jan 2022 20:49:17 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.2452; amd64

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
