## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:c49a1aefb4b4f92d0ab90d5e2a6b017712755e1088967ced036c7c28c50eed9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull hello-world@sha256:011aff33508d4e1a9cd36b6324660eb123f29a8deb0180d75caf425121a98f71
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101267292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85b72bead12ef43b491e714e0b0f8c3a8572c6a91c3a0a7cad2dd61fd5ff7acf`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 13:13:28 GMT
RUN cmd /S /C #(nop) COPY file:0afaffc2fa64462107b7178b2ae7d20404ff12f637eabe3a8046192b9d9a0338 in C: 
# Wed, 09 Dec 2020 13:13:29 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8d3bdee7e2fc8a11dc506c26cb471d67e504db2ed7dd7b8fdb0b395f1786d698`  
		Last Modified: Wed, 09 Dec 2020 13:13:44 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3419bde20ae6a7a452cb6b9f68a85bb45431747b4cc2cca038e6f32dd0110d`  
		Last Modified: Wed, 09 Dec 2020 13:13:44 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
