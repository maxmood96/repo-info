## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:1103dcf9bcde12d0ef8d976e75c6c82ef8c730d8d38cae980a21f4da3ae1859d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `hello-world:nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull hello-world@sha256:3070452d117828a9eb91c87c71f7e71605ceb531598c0acd2575ac2a90b8791d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199057063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c690bbde374586e3022cf23491339d9925d92e728ce4f5020338ec3657aecdee`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 22 Jan 2025 02:28:04 GMT
RUN cmd /S /C #(nop) COPY file:1ae3735b36d6b3fc6ef1fd1d2d12badf8f42ad5660d983c9a406cb560633ed37 in C: 
# Wed, 22 Jan 2025 02:28:04 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a575af90262df1196a014105a8994708f234f7f3663b27c5be27508443c98d9e`  
		Last Modified: Wed, 22 Jan 2025 02:28:08 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6308f12cac64ca86e267b96ebe7b3a1a876e0e6f8874df3113c7f72b9dfa05b6`  
		Last Modified: Wed, 22 Jan 2025 02:28:08 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull hello-world@sha256:1e00e4b67c3ddb20d60a424b278fc96b267e5587675321dcecb19dc55624fea2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120664387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab66d561eefe99f1e8c49e193e656626a012b7c0681ff368d505c05559ee8b0`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Tue, 14 Jan 2025 23:27:06 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Tue, 14 Jan 2025 23:27:07 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acdba3e6d94cbe8f9640224a4985a26e5abca2e7c8be0b25a16d67d606fb42a6`  
		Last Modified: Tue, 14 Jan 2025 23:27:09 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47131ca3f892f33705ecc9a13bd4dafca6dd980be0f39f766c4cc86c9e8a8856`  
		Last Modified: Tue, 14 Jan 2025 23:27:09 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull hello-world@sha256:e5186c0a754b32be8905baa4935d2371f43e59000d334f1d3b8a017bb7a3c75d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155270326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74dd06ce00d942bd38f2f5c5ee520b093416d4b3e1f717d93fa687cc6eb25923`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Tue, 14 Jan 2025 23:27:06 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Tue, 14 Jan 2025 23:27:07 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992e0af2da997ef6a20c8c003eecd705504394b373c256dc6b162bdb2e450556`  
		Last Modified: Tue, 14 Jan 2025 23:27:11 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d68d49ea2f85f180af358314d9417884f460f54dcc746a380493a08f1d9716`  
		Last Modified: Tue, 14 Jan 2025 23:27:11 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
