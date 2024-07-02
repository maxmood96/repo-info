## `traefik:comte-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:fb272b42909d0c2997d6f694b16d5e0baa4a66169ac231d2fb90086627d4f819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `traefik:comte-nanoserver-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull traefik@sha256:1a66df510cf8eeddd32dfd39d5fb673d258d01e420af72ec1bac388aa45d9ca3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165895947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5559c4b092661433f7538fce978fcd934062ac919dff9781f0699ed3ab7bd2f1`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 19 Jun 2024 19:27:30 GMT
RUN Apply image 10.0.20348.2529
# Tue, 02 Jul 2024 22:18:49 GMT
RUN cmd /S /C #(nop) COPY file:987ddc38bdcbf05fc62f7bba70e854cd0031e97dfa83dd1102109eed532b2127 in \ 
# Tue, 02 Jul 2024 22:18:51 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 02 Jul 2024 22:18:52 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 02 Jul 2024 22:18:52 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a8c295c425a912de308ded279124ae45fec44d55a451843fe5877155417f453c`  
		Last Modified: Fri, 21 Jun 2024 02:24:34 GMT  
		Size: 120.5 MB (120499549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab55db9b0336a3f823534f14b034be8917a2cb738af67641511db116a2dc0004`  
		Last Modified: Tue, 02 Jul 2024 22:26:31 GMT  
		Size: 45.4 MB (45393259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893fd054fc088784f6435e1c5e59b534ba757b74e84dfff69a27c9972f1b7df9`  
		Last Modified: Tue, 02 Jul 2024 22:26:21 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a9dacbcdf7277d953e63821e656dda4f776a9da59a80115fdd9df775c8762a`  
		Last Modified: Tue, 02 Jul 2024 22:26:21 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d13d337d2d215f7f6fb97ccfc2dcbf0824e891e7ddce31197e64d4717d4a3c5`  
		Last Modified: Tue, 02 Jul 2024 22:26:21 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
