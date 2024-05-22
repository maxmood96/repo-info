## `traefik:beaufort-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:b0dad9ccba259204f31641ee7991895e48460b22b2e7825e8788e899f8aad6ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `traefik:beaufort-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull traefik@sha256:d3eabe6c26aa986431f49a2e9efbbd877cfad97afc5584f3fdbab64b18111d73
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2155611636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a31624b9d5d0bb60f71b6060d5ecff210cff22184804a51f07aa5c2f403b22`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 19:36:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 May 2024 18:18:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.1/traefik_v3.0.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 22 May 2024 18:18:11 GMT
EXPOSE 80
# Wed, 22 May 2024 18:18:12 GMT
ENTRYPOINT ["/traefik"]
# Wed, 22 May 2024 18:18:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241bde7d4f3acae2008c131651582fc2bb7b130e1f5b90583702d17cad8acd2f`  
		Last Modified: Wed, 15 May 2024 20:42:14 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5348b7ea4552b1e7984764e064717539bf60fd86677df1f0f109dc8bbec2062c`  
		Last Modified: Wed, 22 May 2024 18:21:09 GMT  
		Size: 42.9 MB (42934621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f6882238ebaf24d6f27cc79473b75887f15f214e6d8d3b3a17d7f09f93e668`  
		Last Modified: Wed, 22 May 2024 18:21:00 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a66d877486ee5a3d9168782436fd7cab1580ab8d60a893b61621b031d0ee0a`  
		Last Modified: Wed, 22 May 2024 18:21:00 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4ce5df8fa80543558e73d20869ad32b8ef63cba1c94b073fbcb1accb612f0e`  
		Last Modified: Wed, 22 May 2024 18:21:00 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
