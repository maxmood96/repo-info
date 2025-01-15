## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:128b1c74ab0996145fc91466d5f7fb291db149635c8cb5def733d8aba701c222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull traefik@sha256:398eda76bb0c46ba4e7b8b86baadb0251b077f657f32f5b40fc2805a6a620777
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2309285828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5242d3bede868724c3d8ebf32390a8068bb26c9b9154979c60362755bc75e2`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:33:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:33:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.18/traefik_v2.11.18_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 14 Jan 2025 23:33:21 GMT
EXPOSE 80
# Tue, 14 Jan 2025 23:33:21 GMT
ENTRYPOINT ["/traefik"]
# Tue, 14 Jan 2025 23:33:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.18 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96fc3bc9066aa1dd5fe98f4848c3dc118688fe355b7da136143f89bb3ab88642`  
		Last Modified: Tue, 14 Jan 2025 23:33:26 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d533d4c261bca3cf8526c6029c8bcdac155e86f361cbb31ec90eb8622ea54f7b`  
		Last Modified: Tue, 14 Jan 2025 23:33:33 GMT  
		Size: 46.9 MB (46895454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca04b8b104b1193c5dbfde5df6dddd9b2afae1d75d6595beeceb8e11fda967a6`  
		Last Modified: Tue, 14 Jan 2025 23:33:26 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df5e810a11df8ec9bc09e208750b8746859ad665061c8010b16a9d343a14545`  
		Last Modified: Tue, 14 Jan 2025 23:33:26 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc265793b9d9baebf875647c4a7be787e343d6d358a501321bb84d7554c453d7`  
		Last Modified: Tue, 14 Jan 2025 23:33:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
