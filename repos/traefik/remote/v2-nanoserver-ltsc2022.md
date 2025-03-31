## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:6e4aaf1ed5c2b0177cdbe7f0e1ce17eadd75c76e4b4ef1da4fc34fe2ac867704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull traefik@sha256:3428e833550b50a05fd9552806a30e138dd42fce4eb4622a1e3df81eb766926b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172388814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96083fdb6a9ea5be39f03a5fc4885d9bf6f75b51e975f6b0db20812942f448fd`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Mon, 31 Mar 2025 17:32:06 GMT
RUN cmd /S /C #(nop) COPY file:62490611dce40fce94a4eecc9994c657b13d11646d516ee0c3e68fb0881f46a3 in \ 
# Mon, 31 Mar 2025 17:32:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 31 Mar 2025 17:32:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 31 Mar 2025 17:32:11 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.22 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6aef715082cf70d11c85ab0dfeffe62861785c538d39c787845cca1e877a8cd`  
		Last Modified: Mon, 31 Mar 2025 17:32:22 GMT  
		Size: 51.7 MB (51690084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24c92f09098b4940b866a34d824491623f3a80f4267e7cec82fc6e843c4edd3`  
		Last Modified: Mon, 31 Mar 2025 17:32:15 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f46ad8385a1f16c788c3fba2f5e680755a15cb921777eb65a66833b938ae28`  
		Last Modified: Mon, 31 Mar 2025 17:32:15 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd4aa711a9173ebd2ec40a684ece9c16c795e99234975d895dc28004efe8f0c`  
		Last Modified: Mon, 31 Mar 2025 17:32:15 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
