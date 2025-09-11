## `hello-world:nanoserver-ltsc2025`

```console
$ docker pull hello-world@sha256:1b11ba01aabdfa656e408bc1cb461a4d2f593056c37cf59240d259e3958202f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `hello-world:nanoserver-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull hello-world@sha256:bf2f6cded1837e43cd52fc6476d8ada11a22c482382919f427d80e8ec60b255f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193553751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad056272374477ce63e81ea05f73394d280fd83db6836582570e71366b5e6c75`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sat, 06 Sep 2025 02:12:39 GMT
RUN Apply image 10.0.26100.6584
# Wed, 10 Sep 2025 21:45:19 GMT
RUN cmd /S /C #(nop) COPY file:22c7ae19fd4cf03d26e9cf1357869206bf69101c4233df05ad5f8fa29b73cde4 in C: 
# Wed, 10 Sep 2025 21:45:21 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:a75a4ab04983f989d9a1442633d6c3952b863719a00dd77cf160f7055beaded9`  
		Last Modified: Tue, 09 Sep 2025 22:28:08 GMT  
		Size: 193.6 MB (193550846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad7dfb98a979f5d6802db21d133bc25e4ebd15831b7d6caa4171658072d6ce0`  
		Last Modified: Wed, 10 Sep 2025 21:46:29 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2475a3fec3bd13431541ba9def7fabd4a0a280e70ad1f5d7ac20bdd25e0141cd`  
		Last Modified: Wed, 10 Sep 2025 21:46:29 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
