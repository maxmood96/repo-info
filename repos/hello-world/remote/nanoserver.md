## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:d93acf29645c198134420e57224ff82b41afe1e05f73ee69b64bdbc9cab998fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2159; amd64
	-	windows version 10.0.17763.5206; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.2159; amd64

```console
$ docker pull hello-world@sha256:44497cf9d4c0c84fc8a74cb823dbbc0a0e3a2a8fe6339dc8b0c56850d0b9a7d5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120760076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a33b06b1557f692c4ef4e52fee22e1af2f035d87c7b32f57e5d4fb5c4bf736d`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sat, 02 Dec 2023 12:14:23 GMT
RUN Apply image 10.0.20348.2159
# Wed, 13 Dec 2023 00:54:38 GMT
RUN cmd /S /C #(nop) COPY file:ac9f104fd739943f22886335a779468d86b20ac43fd3168171f6b23fc28882b9 in C: 
# Wed, 13 Dec 2023 00:54:39 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:075332bb10f7fc70c56f7c073dd753e05cacbc93a38c181c5576739a29f8a7e1`  
		Last Modified: Tue, 12 Dec 2023 21:35:16 GMT  
		Size: 120.8 MB (120757041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672777f62307c9af99da139b8f6d8285d7549f4342916f54c33c58b62b3ae771`  
		Last Modified: Wed, 13 Dec 2023 00:55:03 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647d048f809356c4d1cbb10aeaab6abbd2d1cd4165417283246faa28f12ae1e4`  
		Last Modified: Wed, 13 Dec 2023 00:55:03 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.5206; amd64

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
