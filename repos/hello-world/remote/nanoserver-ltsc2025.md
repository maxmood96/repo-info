## `hello-world:nanoserver-ltsc2025`

```console
$ docker pull hello-world@sha256:8d0fff890b85ae2ffea0db1f94e6e0c9c576ff0699d8395bf342b638200dd24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `hello-world:nanoserver-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull hello-world@sha256:0b17a530fdd0e8684881b63c438df2aaeb46007b7e77c38849e4673f9788c4fb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196670941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59fdb5fdb01a6a77bdac2f7b50b0bb50f2d65de4bc7180f1c1964ecff8ee722`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Tue, 09 Jun 2026 22:09:47 GMT
RUN cmd /S /C #(nop) COPY file:22c7ae19fd4cf03d26e9cf1357869206bf69101c4233df05ad5f8fa29b73cde4 in C: 
# Tue, 09 Jun 2026 22:09:49 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c28e3c357614599fe7a4aeec98c41370f6590a1ff0604415a2f2f0ca95e1b18`  
		Last Modified: Tue, 09 Jun 2026 22:09:53 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2e4e8bbf2a44bb5dc18c759f1c7402625f81bca2e6d32480262ad66349fb69`  
		Last Modified: Tue, 09 Jun 2026 22:09:53 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
