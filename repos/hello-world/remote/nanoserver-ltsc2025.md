## `hello-world:nanoserver-ltsc2025`

```console
$ docker pull hello-world@sha256:3596d2c819b280ab01210e9f9ed25c3f1b88abd8e533f58846240b1d1065dd29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `hello-world:nanoserver-ltsc2025` - windows version 10.0.26100.4349; amd64

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
