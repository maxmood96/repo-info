## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:5b6f4b574013a42c1f65c40cb98bd9020fbb2d8f69f2f78d351e186b03ddda80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull traefik@sha256:96688c2d1c951c3d1a90eaaa12a49344e11bafb6d0ab3184f85c9c02d85e0131
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2185469192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c43b70f0ab7a0fef37b2b5b3c2f72eb37931a9320b8f71c4451cff97970ce3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Wed, 10 Jul 2024 16:34:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Aug 2024 20:16:23 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.1.2/traefik_v3.1.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 06 Aug 2024 20:16:24 GMT
EXPOSE 80
# Tue, 06 Aug 2024 20:16:25 GMT
ENTRYPOINT ["/traefik"]
# Tue, 06 Aug 2024 20:16:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6ef58dc4393db0b8bdae6b4740abd835da62ca63605e0eb063ed3c586eddda05`  
		Last Modified: Tue, 06 Aug 2024 20:20:40 GMT  
		Size: 45.9 MB (45863572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97d8f4a05c6e16ded7c301b8f401f13aaca353b3cf0e769b15e7a515ec85231`  
		Last Modified: Tue, 06 Aug 2024 20:20:32 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1582ae6e5578c05ee0fcf47352e6530ed750dd0063aef11f4fa1da417dd9832`  
		Last Modified: Tue, 06 Aug 2024 20:20:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4954d07d756c85aa449cd7e6c07cb34c00ce02e3790768d8abd30737abf80bc`  
		Last Modified: Tue, 06 Aug 2024 20:20:32 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
