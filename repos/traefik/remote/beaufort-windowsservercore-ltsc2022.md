## `traefik:beaufort-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:2731fcc0e30bc985ce0c7ea7292e00ac29a7374360d939a22d134a6fc7af7073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `traefik:beaufort-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull traefik@sha256:0cc6be686e4cb1c83f675319b07c000b1f2832b3c9c3e6c781a788c3650654ab
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2184640266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47556e60637a4cd51cb9ff801171f52cb7adfbf26ba6a18bc54693085b6fccc`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Wed, 10 Jul 2024 16:34:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 17:54:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.4/traefik_v3.0.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Jul 2024 17:54:43 GMT
EXPOSE 80
# Wed, 10 Jul 2024 17:54:43 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Jul 2024 17:54:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d9de6992053b5598e6e6ffdf2a54d935d71057f5cc79ff86d167df37475ed8`  
		Last Modified: Wed, 10 Jul 2024 17:24:53 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2b5b055c4c6eceb85109182fa377b86dc4e8af5c397525381a15b5a01b1da7`  
		Last Modified: Wed, 10 Jul 2024 17:59:59 GMT  
		Size: 45.0 MB (45034326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd08e9b8cfc0111eb3ede94766d56e14000e78b22f45205a05facc4e289c0666`  
		Last Modified: Wed, 10 Jul 2024 17:59:51 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b39e5dcb75d16719f73d89ab633040d46041a138b3b2583363d7e6493f6bb5`  
		Last Modified: Wed, 10 Jul 2024 17:59:51 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0321b3b7340040a12d0782babe7528e41b60c17660dd5c71799a703694e43d`  
		Last Modified: Wed, 10 Jul 2024 17:59:51 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
