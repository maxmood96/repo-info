## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:f1890db4fe349a9b4466c44405a205361379f91286c2bf94920d664e4945db2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull traefik@sha256:2f402caa1a995240930664c12d8f2a3df3f2d21f1847f10bc057b750b0220a29
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166008115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d128f301aed47d2a80440be5218f59a325eadde037b10b52dd2c1fe8b7e249`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 10 Oct 2024 00:04:57 GMT
RUN cmd /S /C #(nop) COPY file:87da60a6562645605cbb404b52701410b8e4984fc45db4db6cfbe2ecbdde699c in \ 
# Thu, 10 Oct 2024 00:05:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 10 Oct 2024 00:05:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 10 Oct 2024 00:05:01 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cdbd2c31f5063dc6e557a1216024a0578a91a2a5f630830372d91f0dd2dac67`  
		Last Modified: Thu, 10 Oct 2024 00:05:13 GMT  
		Size: 45.5 MB (45494026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157ea08483e2a4e36adcc8865650833af938f434045837cf2a216646f8a6cf9c`  
		Last Modified: Thu, 10 Oct 2024 00:05:03 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2762f65e5d3ac6c0871a1a8ea5e7f1eca514c4cb045ed593aa8754ad47e7c6af`  
		Last Modified: Thu, 10 Oct 2024 00:05:03 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e13769a13749d8098426a82b57724ff092d3018fa1c7e5fa1e63586649244f`  
		Last Modified: Thu, 10 Oct 2024 00:05:03 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
