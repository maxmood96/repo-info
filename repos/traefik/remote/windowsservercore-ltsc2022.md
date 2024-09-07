## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:08b9a318fa7a820c7d7336d2434e7c7a20ce2d484f2a7a2e7608b26e8e8b958c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull traefik@sha256:e998ab519cd9b91a9a1e9c2d2c7bcd37fe335ef47256e72728b41301c979ac74
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2187684028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2995be6c092528cb67a48a4da45a7d1510de5af4b95c46c997e9bf017d80c32`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Fri, 06 Sep 2024 20:59:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Sep 2024 21:00:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.1.2/traefik_v3.1.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 06 Sep 2024 21:00:07 GMT
EXPOSE 80
# Fri, 06 Sep 2024 21:00:07 GMT
ENTRYPOINT ["/traefik"]
# Fri, 06 Sep 2024 21:00:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba2996bb5f3611242200fc3b6ee1a1b932c350e40ad2e9bf3b232843e7d2a1d`  
		Last Modified: Fri, 06 Sep 2024 21:00:15 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa13f1b496f507bfb8abed2628608acf8857b202c9976e6347d124018108250d`  
		Last Modified: Fri, 06 Sep 2024 21:00:21 GMT  
		Size: 45.9 MB (45913938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406e979017b6bed24edcbb828a084fb71ff114b7981793ff312a0c4e3002e12f`  
		Last Modified: Fri, 06 Sep 2024 21:00:15 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c68d63d3f7316100d43d3875d9500cc11b1df2b87fa0863302d281a923ff92`  
		Last Modified: Fri, 06 Sep 2024 21:00:15 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a942116e30b18fe8058567159bf29151768612d19ef59a306e982f105fac638d`  
		Last Modified: Fri, 06 Sep 2024 21:00:15 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
