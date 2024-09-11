## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:f36c7a50afd42041f37aa29ae608237b318355d06c1fcc92c70376998cd23002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull hello-world@sha256:a1af7a92f4bc620316446bb698d9dfc4c7ac674bed81dc701576aaf058b4d467
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155083735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c428bd95495a1932f855a62cf2d3c5ca0f6de31dfa844fe5597702f611cc3b7c`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Tue, 10 Sep 2024 23:59:01 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Tue, 10 Sep 2024 23:59:02 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8134cfe881fbcde4d0f26f176fc21ac562c9b1a98546bfb9639dd269006855`  
		Last Modified: Tue, 10 Sep 2024 23:59:06 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ab774784fad4f54979172f7b36dc306c47e8d6b146e969c344e4655cd43795`  
		Last Modified: Tue, 10 Sep 2024 23:59:06 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
