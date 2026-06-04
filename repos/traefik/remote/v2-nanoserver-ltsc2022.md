## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:6ee255897d15f3a32a4ed6d2c315ba4da6dc1081281629caaa4f3bfa9166278f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull traefik@sha256:14604f20e6380ba326a639a306c60520ce2e14ade2b84ac3009cdc6b0ab15e6c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176569104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71152e627f2f7e0c4b586ea279e3b88a86288c28d431a6ab131417e96e61d22f`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Thu, 04 Jun 2026 19:19:40 GMT
RUN cmd /S /C #(nop) COPY file:63641df7acb522b60e0ab145ca4d300185943aa9e6e193307bfefbde751eade1 in \ 
# Thu, 04 Jun 2026 19:19:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 04 Jun 2026 19:19:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 04 Jun 2026 19:19:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.48 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25126e8ecf444dd77f702173b6943f095d532b3d44a078531de223e4eb760c4`  
		Last Modified: Thu, 04 Jun 2026 19:20:13 GMT  
		Size: 49.5 MB (49527138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a880930334abce589fe16c607cb2d4b435092c8595de3badf65107bf93d8b9`  
		Last Modified: Thu, 04 Jun 2026 19:19:46 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad83cd97fec6788ba07e95895d4a7161d27a76957f9d2b6b5a3347398c1e680`  
		Last Modified: Thu, 04 Jun 2026 19:19:46 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb3cd7d6c482a7d35df9094953e068882b1d97fcbcc1d98f33d136510af3d2c`  
		Last Modified: Thu, 04 Jun 2026 19:19:46 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
