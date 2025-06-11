## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:87327a5eddc9875b2b387cb5c78ea8c1f0e2525b8736870884a4a0bdf99b1536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `hello-world:nanoserver` - windows version 10.0.26100.4349; amd64

```console
$ docker pull hello-world@sha256:30b0574fdcc5ce053d745e06047760b52ba620fbea36f75b3584f900c185b8e4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192085340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18112e9afa06a9c48a1f7f8bd1cfb96920f65e6bcaa5291792dc8f2822df7033`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Tue, 10 Jun 2025 21:22:45 GMT
RUN cmd /S /C #(nop) COPY file:1ae3735b36d6b3fc6ef1fd1d2d12badf8f42ad5660d983c9a406cb560633ed37 in C: 
# Tue, 10 Jun 2025 21:22:45 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415f42efd98cb879a94c93eda49f1adb2ff4da299c2de65eaa5038e7b90e3b5b`  
		Last Modified: Tue, 10 Jun 2025 21:23:15 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70a94b48ef9594a3b5dc2bed53013f188529750b5d70acd6d776b5f05f1b28d`  
		Last Modified: Tue, 10 Jun 2025 21:23:16 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.20348.3807; amd64

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
