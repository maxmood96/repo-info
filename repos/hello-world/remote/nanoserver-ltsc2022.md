## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:ffbfb68544e0db31a5fa05392a9919faf6f806c31b47d3da90a0c36e7d63aa71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.2322; amd64

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
