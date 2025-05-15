## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:920a3ced101dd37bf5dc0c9cd7cee3af10eba165f2bf245d78c69cabcfe8ce75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull hello-world@sha256:9632aada1d9006d557750664378d6c48f35da02c6382c95f75323b1580e73982
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.8 MB (108783529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0cd77ce30ab6bda35b16c3085e8f7356f2220d3c180584f3d54fd76d663141`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 20:50:04 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Wed, 14 May 2025 20:50:06 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Thu, 15 May 2025 19:27:12 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0268197ef922fcfd42d9e5b07fbc3cf689d92e7cf15265760b248c621893b8c7`  
		Last Modified: Thu, 15 May 2025 19:27:04 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19c8856cb6aa883b67f7102b0304f59a5c6acd51506b2de38c7330b9ae25824`  
		Last Modified: Thu, 15 May 2025 19:27:04 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
