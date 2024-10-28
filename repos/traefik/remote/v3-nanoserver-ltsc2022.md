## `traefik:v3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:d825761006cc50c51331d7f1c32ccd6428b7467f573c8883f286c43334e7b27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull traefik@sha256:bccfaee4d7d2cbc0be614f2aa5b53a72a06e5f947309dc5eb1b2007935fdd901
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168671067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa79f0454ca908c6344323c8f9eecbff52a466a31d666969b562226f5dd8934`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Mon, 28 Oct 2024 18:57:15 GMT
RUN cmd /S /C #(nop) COPY file:7df0f422a82ce5e59bd5bd682fd7b457028b9b5f0d6f84e4afddd8cda3586dec in \ 
# Mon, 28 Oct 2024 18:57:18 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 28 Oct 2024 18:57:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 28 Oct 2024 18:57:19 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab2b44ebb223fccc3726d3ca3748cffe34b1337fb36a9c22b7cab43957fbe73`  
		Last Modified: Mon, 28 Oct 2024 18:57:28 GMT  
		Size: 48.2 MB (48156982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44502a9a47a0bf5fe212ee1f6f7a98619068ff29be0eaaa75c9896159feed30`  
		Last Modified: Mon, 28 Oct 2024 18:57:22 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22f8e7bec925b3d8c2a4d1054d7002d9dd5e3b3912ecbc4243c81216e715459`  
		Last Modified: Mon, 28 Oct 2024 18:57:22 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4ba72d8a354ef6525d73110cafdb6f6bb0fa6361bbce84d3936cc648de439e`  
		Last Modified: Mon, 28 Oct 2024 18:57:22 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
