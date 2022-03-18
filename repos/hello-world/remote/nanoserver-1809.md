## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:6fa260a68bb4e00481ebf7eac698ff82be51fff06f3cd445752de303e8ca216b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull hello-world@sha256:acd65ed93903ec23468247a22d7ea0390f2e5e09b0ea3a93965a24b25b905c1b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103057541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756271127782036359622cdb5d32edc2671c44b15bfcf41d8e6d4792c3b4f4cf`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Fri, 18 Mar 2022 01:15:35 GMT
RUN cmd /S /C #(nop) COPY file:994f63bc3cea8285310afa5f4677df29bf99dd4cd1881c7e381100a9e794ba71 in C: 
# Fri, 18 Mar 2022 01:15:36 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:026225b3819b614d196f5b6b5b714cfa54e8501e187e15b4546af5bd30c6a767`  
		Last Modified: Fri, 18 Mar 2022 01:16:04 GMT  
		Size: 1.9 KB (1853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc6b8742d7233d05a39a305e944b3d1d118b53dff17f5117477a666ab5081db`  
		Last Modified: Fri, 18 Mar 2022 01:16:04 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
