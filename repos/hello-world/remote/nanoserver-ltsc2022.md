## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:388a14360767e45761ce5b7ce2cd2da18a1143a290e70fc3687447c8d901f362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull hello-world@sha256:3d622dcc0bef7fe6deec02dcdacc4017d2f63709d723823cae18a7266d2d33b8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127041640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195412cfe3aa24d0604ad85077b2e6f461ede18d7d01c834d65efa65c1e82404`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 12 May 2026 23:35:41 GMT
RUN cmd /S /C #(nop) COPY file:9fca1d3c77d0758894ceeb7952e49e3b465b238dc4943832e9436b0ce84d8ae0 in C: 
# Tue, 12 May 2026 23:35:42 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb6786a52e7d2cb487c3804086bfc193e8e78a7fb4db5586c3e06ff0009cb6e`  
		Last Modified: Tue, 12 May 2026 23:35:46 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544487f26c954c95689e2675e4d655e7b83b1ec105376a894363ebf70f3dae7a`  
		Last Modified: Tue, 12 May 2026 23:35:46 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
