## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:7b5a5f9ae3b67ea6500f0487535a25624dcf6fc6654bdd55168539718372aaa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull traefik@sha256:6c7c4e626ef275c4b21311636e3fd76123fa202a754fff105363eaf5e2eab07d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2172588654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a987ba6edd2cd67f70012641a96a73331329dfd61655e8a3ed930ffc5687e1`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Thu, 04 Jun 2026 18:08:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Jun 2026 18:29:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.48/traefik_v2.11.48_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 04 Jun 2026 18:29:27 GMT
EXPOSE 80
# Thu, 04 Jun 2026 18:29:28 GMT
ENTRYPOINT ["/traefik"]
# Thu, 04 Jun 2026 18:29:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.48 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cbff79e4cfab3735574b59b5e2a50633baa6542fe7250c4f43ca083fea2c5af`  
		Last Modified: Thu, 04 Jun 2026 18:10:38 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1d3cfbe848742a0193c5a9190e9607dd6ca747716c9d58b054fb539fdce257`  
		Last Modified: Thu, 04 Jun 2026 18:30:18 GMT  
		Size: 50.2 MB (50162753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb4e76c34025daff9a25f715dc5f58a5b9b33d401a438b7a4f74586857f4b7d`  
		Last Modified: Thu, 04 Jun 2026 18:29:34 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ef5e709ff7d06d7e288e7aee7b957aa530c31b175cdfe1abfe83b55d2a9471`  
		Last Modified: Thu, 04 Jun 2026 18:29:34 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a5086b5b3779f74bc60f654b8cad93c4b82ede25456a9e01d73a18fb224e74`  
		Last Modified: Thu, 04 Jun 2026 18:29:34 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
