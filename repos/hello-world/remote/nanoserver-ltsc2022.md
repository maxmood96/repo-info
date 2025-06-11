## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:16b3b71a3ae3a9ab9f1ce794402e87f417d1e335739764fdbd552039f85b05e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull hello-world@sha256:77f823d3e4c6d59edabc743e5252bc7b10cf682c606053298c417ac7012eef03
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122543294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687a18b7dabe4ab0513a71318a992a25b54bd82840c438bc16e91a84d53d753a`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 21:22:23 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Tue, 10 Jun 2025 21:22:24 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9a11e39bfc356e63862aff94c72702f6d7c5decf6e80bade65b27ee1ee5511`  
		Last Modified: Tue, 10 Jun 2025 21:23:15 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d490386a7abbb4c1d12af7af2de73b9c8e472043a8b46373fb209adc6ad0f32`  
		Last Modified: Tue, 10 Jun 2025 21:23:15 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
