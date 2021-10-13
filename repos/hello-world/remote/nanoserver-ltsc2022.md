## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:518cbbc52b868f23937ce44ec94a5ce5a884c3a1571e327f1ebd25dcd1832691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.288; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.288; amd64

```console
$ docker pull hello-world@sha256:31801872aacfc6245ba5277e07dc2c9a482a473c87d625f25c3e6d5de930b35d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116942543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e564d7360cfa5451bc1d616d8871f6a17f1b2f977a68462a7259bce110f8a754`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 07 Oct 2021 11:15:04 GMT
RUN Apply image ltsc2022-amd64
# Wed, 13 Oct 2021 12:20:37 GMT
RUN cmd /S /C #(nop) COPY file:55c009fa8b983e38026b41064e5367bc779dae76c0d404a11886c3cb19ec4509 in C: 
# Wed, 13 Oct 2021 12:20:37 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:91284e7e8fd4bd7ebcfa98544a3e4f59639f38281225c81c34b6fe22e0dba4e5`  
		Size: 116.9 MB (116939483 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:84f480fc2b679166f7d1340f9ee5ffc1ce7f860cea8e850365fef57631f1908f`  
		Last Modified: Wed, 13 Oct 2021 12:21:01 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f41bfcf238a5a974261c1f9ce6c039568585a03e2d8966083e273d7448d275`  
		Last Modified: Wed, 13 Oct 2021 12:21:02 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
