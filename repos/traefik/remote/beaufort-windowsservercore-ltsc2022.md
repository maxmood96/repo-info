## `traefik:beaufort-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:0084d4bb9d9b219532a0c7a49fd1438552a0689ae3c72d164e98cf248656d731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `traefik:beaufort-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull traefik@sha256:4d4b9dfbd3f20864adb35cdfcd62f2ca4e516ec1fa96c31d050ed32c00459241
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1942021057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebbbdfd3595247cbe68a2b6ad81bfafb420be2d9c6a1f160f3983b12062f999`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 02:55:28 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta5/traefik_v3.0.0-beta5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Jan 2024 02:55:29 GMT
EXPOSE 80
# Thu, 11 Jan 2024 02:55:30 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Jan 2024 02:55:31 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddb0a528ee25f289459dfa0d84bac9a14b9127f771882f0b60425ffaab79933`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e15c3c989998bebef01e6f171e9fb5b99f55348a3879ed15b6daabff0aafb3`  
		Last Modified: Thu, 11 Jan 2024 03:02:00 GMT  
		Size: 41.8 MB (41803194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7c5c08c03f3a3058bd365dd03f1ca2060bbdf3565509f2ba85ef99d94048f1`  
		Last Modified: Thu, 11 Jan 2024 03:01:50 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a307677f611cfb82606d5fa26ca3281533fbbc379b98c4097015b614ab2d7d`  
		Last Modified: Thu, 11 Jan 2024 03:01:50 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fad3662942fc37b68b55707e5f6535567f16dd002fc3a19f491db73b04e7c3b`  
		Last Modified: Thu, 11 Jan 2024 03:01:50 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
