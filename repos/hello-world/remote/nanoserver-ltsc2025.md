## `hello-world:nanoserver-ltsc2025`

```console
$ docker pull hello-world@sha256:249fe13fc91f3eda5f112339fbe7d7254b299a1ce0a24e349980a7f6b39392f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `hello-world:nanoserver-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull hello-world@sha256:bc3dc9fa409cd846f9a3dd7ad524de79f770da545603c71628bf238dbc37c1f0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.7 MB (199741858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18556c02f8d357723ddb41c7acb7c5d4113dc235ba43d9fc74810334ad57e645`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Tue, 12 May 2026 23:35:33 GMT
RUN cmd /S /C #(nop) COPY file:22c7ae19fd4cf03d26e9cf1357869206bf69101c4233df05ad5f8fa29b73cde4 in C: 
# Tue, 12 May 2026 23:35:34 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b042f2ce1a910bd5f853aeebf3990275905612db0e907239522f6fcfeb4cbbe2`  
		Last Modified: Tue, 12 May 2026 23:35:38 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959104eb488e2c2e84496e8c2594623962c0a84029276ab61a503463a4d25374`  
		Last Modified: Tue, 12 May 2026 23:35:38 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
