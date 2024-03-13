## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:21d300d8d72db35e94fd885be7873e66fdf9a50407378145a1e8c5df0ae6f1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:698b27fe2f1a7d910141455723932f32b8c7cb729830eb791a0b9bb9e1dfc37b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1999700334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac748ff26ef4b15d8858f826b681d177e9546e01c1809c76064e4595ef8f622`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:24:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:24:05 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:24:06 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:24:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3defa6c0936d429cc07a43d4c41e98fe9a563b22d6d47c2d4e8b26bb91fd09`  
		Last Modified: Wed, 13 Mar 2024 04:27:11 GMT  
		Size: 42.2 MB (42235665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90320aa66285218bea75d45b7a0ce6306af06d7590d55538d05bb2d86f92f8d`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff82c34f3abc3e251df983c86355fbe950801d6de486bdf2b7bc3ab052e92cce`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bffafb756604dddb7d508523e6b558dbb9907799b21e53718fda2e27125f2af`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
