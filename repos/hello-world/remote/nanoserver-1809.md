## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:36dc72b47dfd3b50cd5df3c48b8a425c3f481ac43ddf88bacde80153e6374b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull hello-world@sha256:291a95443b8ce36665d849bebe20bc0a81df914476a51bedbeac1e69d241600f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104513151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bcf1cfa96f62162f8aed5bb719274b1a2a2c6b553a3f9056266bdd4375f0616`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Mon, 04 Dec 2023 10:54:04 GMT
RUN Apply image 10.0.17763.5206
# Wed, 13 Dec 2023 00:54:45 GMT
RUN cmd /S /C #(nop) COPY file:994f63bc3cea8285310afa5f4677df29bf99dd4cd1881c7e381100a9e794ba71 in C: 
# Wed, 13 Dec 2023 00:54:46 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:424f13a93a185a5defe848e7d270655e05233555f51328c0af24b9e70677d037`  
		Last Modified: Tue, 12 Dec 2023 20:02:40 GMT  
		Size: 104.5 MB (104510104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d14a814a29b887ed7cfa8dcd69acfa5b60b0f192163e1071fd6651cd65a1f7d`  
		Last Modified: Wed, 13 Dec 2023 00:55:10 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e19beab1e0a7da79a9ffea82c35707a32e10cb0bfcef3c675952104d7bfbd3a`  
		Last Modified: Wed, 13 Dec 2023 00:55:10 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
