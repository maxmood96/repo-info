## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:eeb2749be1c4ec10d0a0f226fc3912b003df90a3414df19a17e61858e9a652e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.2322; amd64

```console
$ docker pull hello-world@sha256:245fe15fbb8f72b1988e35debf9172dedde4ec794de307633c5fb38c96ded61a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120737890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb50c0b64d64f98523484e902524fbe1b9b8fd55bfce59782adb45aea96c920`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Wed, 07 Feb 2024 06:29:10 GMT
RUN Apply image 10.0.20348.2322
# Wed, 14 Feb 2024 19:53:30 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Wed, 14 Feb 2024 19:53:30 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:ccff18da882d371921351307d169380d3ac22ef981f2bb4f14fb2b332b395439`  
		Last Modified: Tue, 13 Feb 2024 23:39:47 GMT  
		Size: 120.7 MB (120735093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc83f25239a0a9775255b0430886b7b92bc439e8e10a02ae8720a4810fcb80a4`  
		Last Modified: Wed, 14 Feb 2024 19:53:34 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4294d6705ec18f5b7a53cf034e1a0f4336ef10692380c3dcec95640d874a4ee1`  
		Last Modified: Wed, 14 Feb 2024 19:53:34 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.5458; amd64

```console
$ docker pull hello-world@sha256:088bdbea94d5c8fe3eb9f3cec836c3f7ea82923e7d0d3a4f1146ef0f860f5a93
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104624406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20c2a9cc77ae3474b2738a6c3dc715f6429df9152f24d03e8734eae14a1ea5f`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 19:53:45 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Wed, 14 Feb 2024 19:53:47 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f352d04d1742a39c08c2e779e52ff242a2b6ca46c59050e9c87d6e2e8e87b8`  
		Last Modified: Wed, 14 Feb 2024 19:53:49 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75410b00abbb3512684efb518f31ecb314ef4a895364bfdaac13cc4eba4a5257`  
		Last Modified: Wed, 14 Feb 2024 19:53:49 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
