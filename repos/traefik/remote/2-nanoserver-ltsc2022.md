## `traefik:2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:4c2c190287785b4874df6494a247350e55c0acab6f134b6e62ae44455eb96949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull traefik@sha256:300838d28c9e53e3b05413b26d970ac16a840d8ab9d04d179b9ddc13b55f5be8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172429513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa668e1a183e20018c4002876dcebce53a5cdf799252f054ebc8e2fc794b0d8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Wed, 09 Apr 2025 03:22:22 GMT
RUN cmd /S /C #(nop) COPY file:62490611dce40fce94a4eecc9994c657b13d11646d516ee0c3e68fb0881f46a3 in \ 
# Wed, 09 Apr 2025 03:22:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 09 Apr 2025 03:22:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 09 Apr 2025 03:22:28 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.22 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d228da5ee1447510c49289a560de8dceaa416df0493da4813ce7d5eb9f631d47`  
		Last Modified: Wed, 09 Apr 2025 03:22:37 GMT  
		Size: 51.7 MB (51690082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16b37be9bd26d04323ba1ede12c88adc0ce87f1181acbe2a733ca12edd2d922`  
		Last Modified: Wed, 09 Apr 2025 03:22:31 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9dbd9601026f7a6dd6380db1740cc7c75327f4fe3343bedda607acc8c6ea59`  
		Last Modified: Wed, 09 Apr 2025 03:22:31 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81940c11ba5dcd4372878cddc1b0f1c5b1fb5158a5953301781e81e8031dd461`  
		Last Modified: Wed, 09 Apr 2025 03:22:30 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
