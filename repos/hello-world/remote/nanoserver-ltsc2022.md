## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:56c2790ee44b3defbd5876b45e5af8e96681ed7a74b656da544656db9119305e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.2582; amd64

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
