## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:be5c3ce5d8e5a212b38839566ec43e3a7c8023567bdb292920c61c3a1c8137ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.3932; amd64

```console
$ docker pull traefik@sha256:dc41ddffa2a142fa15e4200a9b86928c3097fb22edac4068742937fa7cb5aa83
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.6 MB (178566565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbf75ba72c5c5fec1fc5933070bb9a4975bcc6db029da5d990c2386a017b30e`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Sat, 05 Jul 2025 05:15:23 GMT
RUN Apply image 10.0.20348.3932
# Wed, 09 Jul 2025 19:15:14 GMT
RUN cmd /S /C #(nop) COPY file:5083c222284b9f568262eb745ded73c4481e67481ebd9b42b3cbcbd98b9b25b9 in \ 
# Wed, 09 Jul 2025 19:15:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 09 Jul 2025 19:15:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 09 Jul 2025 19:15:19 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b1cf2c299ff70c52cb8ecf52e66d64d5068519867510919d8807ed2c58a54ba2`  
		Last Modified: Tue, 08 Jul 2025 21:55:51 GMT  
		Size: 122.6 MB (122630906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a037187eb2fa8fdac93f31ec2842c7d2062056a5e7f8034fca6b0add9f62b504`  
		Last Modified: Wed, 09 Jul 2025 19:15:53 GMT  
		Size: 55.9 MB (55932559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e780b4f8572e72720093f92b06965961cc02a790a7c5b710ebba3da3001377e`  
		Last Modified: Wed, 09 Jul 2025 19:15:42 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32a192a895df9d675f8e29b060ce4749fba5f05b255fbed6840c11e66cebd93`  
		Last Modified: Wed, 09 Jul 2025 19:15:42 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a922cf7c6a8d5218c4aca914382a7684da6c3809c003f437de2eeb6ac85800`  
		Last Modified: Wed, 09 Jul 2025 19:15:42 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
