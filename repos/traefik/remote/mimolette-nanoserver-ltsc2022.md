## `traefik:mimolette-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b858774fbd8dccaffd6c45065f5d5f7875c16df7210d03fb9535294e606e3b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `traefik:mimolette-nanoserver-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull traefik@sha256:4d0f0424002537c645b733015fc037d161df237d505715107c97975e043af70e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166775258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108dddf6aeebe90e5a0d56ee017a04e2160465348f9ade18b25744a1bacb09ff`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Sat, 02 Nov 2024 23:34:35 GMT
RUN Apply image 10.0.20348.2849
# Tue, 10 Dec 2024 21:08:02 GMT
RUN cmd /S /C #(nop) COPY file:87185b296a51c23ba51e7f85f6c018d23e49d0fe423b2b39373ae759fd25a245 in \ 
# Tue, 10 Dec 2024 21:08:05 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 10 Dec 2024 21:08:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 10 Dec 2024 21:08:06 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.15 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:815d6b7f925aef8327c34c34073ae54cc1c82120f1058682eac4c8c14ca21c70`  
		Last Modified: Tue, 12 Nov 2024 22:44:32 GMT  
		Size: 120.6 MB (120604951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c15df1ef9907639a8b91dc5fbe30684f8806a24c62172aa5da0c492a29bf0af`  
		Last Modified: Tue, 10 Dec 2024 21:08:14 GMT  
		Size: 46.2 MB (46167217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ced073a9ba820381826ea8fd4d90ace0ef82cc0e54bb2b426a1a700f942ac8`  
		Last Modified: Tue, 10 Dec 2024 21:08:08 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638bab646b2033eb143024723b63caab09664e5330debb705a0cd6a3c2d2aede`  
		Last Modified: Tue, 10 Dec 2024 21:08:08 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888c8c56c890def884bfcb3d4ad11952cd50ec10da68fcf748f7f9c12a77be26`  
		Last Modified: Tue, 10 Dec 2024 21:08:08 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
