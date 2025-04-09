## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:92c836b3e3ef27b63591d5d7d74954302263f5b91e6354fc1deb4fb83680b52b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull traefik@sha256:597a5063c5cb9a3d899e4f86ddea7fbf046632209c5b8339da55598f9eb5fa81
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175276182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0052d8b7f72c0b75ec7c30de17f8cf620c2db450354e104bbff90c41186d10ca`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Wed, 09 Apr 2025 02:51:33 GMT
RUN cmd /S /C #(nop) COPY file:dfe80004f835b8291cb14f4bbf836cdb2eb74e5ef43da07179c6316ad9924547 in \ 
# Wed, 09 Apr 2025 02:51:37 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 09 Apr 2025 02:51:37 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 09 Apr 2025 02:51:38 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5784c0aff70950d05428741a7c76399476f8eaab1581c940c4efd77037266d13`  
		Last Modified: Wed, 09 Apr 2025 02:51:48 GMT  
		Size: 54.5 MB (54536783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2b751f5fb1d4e117c5fbe21015ffde920ff0e11dad6e34a2f1aa2fefe760d5`  
		Last Modified: Wed, 09 Apr 2025 02:51:40 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d384a7a3007266269d6e1be0fe1d36b2be2442754e0efd3a406dee9beff5bd0`  
		Last Modified: Wed, 09 Apr 2025 02:51:40 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb77485cc69ec1688f429c508a89da176e5c3803b190c22f1b27cee24fdcd5e8`  
		Last Modified: Wed, 09 Apr 2025 02:51:40 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
