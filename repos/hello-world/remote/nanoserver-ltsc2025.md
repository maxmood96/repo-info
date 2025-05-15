## `hello-world:nanoserver-ltsc2025`

```console
$ docker pull hello-world@sha256:cf8bf9bfcbc9434c03f1907a14084bee99611adab3fd10caf0af992a78142b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `hello-world:nanoserver-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull hello-world@sha256:45767087cbe67a8edbfcfc013026d1730c662cc14e4160f449d534b2d439603b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191414894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178248e4c7d3c52d4576c3b8a860ccc1f39cecd43dd7ed62bdf007ea5f390c5b`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Wed, 14 May 2025 20:50:27 GMT
RUN cmd /S /C #(nop) COPY file:1ae3735b36d6b3fc6ef1fd1d2d12badf8f42ad5660d983c9a406cb560633ed37 in C: 
# Wed, 14 May 2025 20:50:29 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Thu, 15 May 2025 20:15:30 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787a49ff64bad1bb68d7207522bc0701f0d3aad782397a83ef86c1992def81a3`  
		Last Modified: Wed, 14 May 2025 20:50:32 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd2b583015cbb38f3fa8ce3286b6d7e8733898535cbe6daf972acd760f33ffb`  
		Last Modified: Wed, 14 May 2025 20:50:32 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
