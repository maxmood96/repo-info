## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:9d1f74796e613311efaab208aacec0e0cecb6b9b897238dd4fe708b4ec181b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull hello-world@sha256:021ddc79e0783426193571ab98b68ba7d8cf9a01ea223db6ddb2fde955faa014
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155096375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44feca5fb350cebbc7ab8f46321be1a0d80d285cb6d99617fe1a98e21affec6a`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Wed, 09 Oct 2024 22:57:56 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Wed, 09 Oct 2024 22:57:58 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1ddae6505dea12aa52146b7471bbf898d8306947cb7064e3729d9d7685c1ca`  
		Last Modified: Wed, 09 Oct 2024 22:58:00 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2449acfe7797abcd8e2a04a169df0a4c64da9627c3e6b321ce88af5f5e7cd55b`  
		Last Modified: Wed, 09 Oct 2024 22:58:00 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
