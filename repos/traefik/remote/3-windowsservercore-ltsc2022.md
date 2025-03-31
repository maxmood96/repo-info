## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e615db0e8a407e0ff64a7682dc22a1e73a9c865639201f1f586ba86214807b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull traefik@sha256:fe78637c803ee1e033f0eb4a2881ab0bbc2f92e3963a5a4f310577b122566cca
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2324989718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb498cae25154722cf91fe83706ba758b2417dcaa8ab9baaa884c8f45bec908`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Mon, 31 Mar 2025 17:39:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 31 Mar 2025 17:40:08 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.3.5/traefik_v3.3.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 31 Mar 2025 17:40:10 GMT
EXPOSE 80
# Mon, 31 Mar 2025 17:40:11 GMT
ENTRYPOINT ["/traefik"]
# Mon, 31 Mar 2025 17:40:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa378f3bff7cc1c837ee01c1cd26199b292a2c0445a187335f1a3a7d68185b6a`  
		Last Modified: Mon, 31 Mar 2025 17:40:14 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9561c37aa521bae02d46f3573768063045f6f3cba256e8bfeb03d7576a82068`  
		Last Modified: Mon, 31 Mar 2025 17:40:21 GMT  
		Size: 55.0 MB (55043364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a52b1cc94b0ae525d730420d2e8cab6d69c0dc1a5a35740f4592d128755a0c`  
		Last Modified: Mon, 31 Mar 2025 17:40:14 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34923e5266b77883ac91a8e86e88945abcd0cbb76b1ddef2588bd679e250542b`  
		Last Modified: Mon, 31 Mar 2025 17:40:14 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf6e141dd04bbfcfc731326d1309feb441de8e6674471d5b95f10b2b3cb4d77`  
		Last Modified: Mon, 31 Mar 2025 17:40:14 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
