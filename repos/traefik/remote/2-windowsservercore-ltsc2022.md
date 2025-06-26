## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:ec88e4c967953c6b01c4e247f9362b2fa603d74544ea2eab5bb7e8adae8999a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull traefik@sha256:bcd3da206fcd623199d033e3ddd6e8b48f75e040eedd3158f5df5afc01a35b38
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2334965886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e9614327fb6d10bc31f783e189a93aab7c69c1881fb894aa468ed1b9beb8b1`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 26 Jun 2025 18:53:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 26 Jun 2025 18:54:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.26/traefik_v2.11.26_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 26 Jun 2025 18:54:02 GMT
EXPOSE 80
# Thu, 26 Jun 2025 18:54:03 GMT
ENTRYPOINT ["/traefik"]
# Thu, 26 Jun 2025 18:54:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e920c709525b590c864afa8e7d563a750953716da29ef2ee9d2a933aa477aff`  
		Last Modified: Thu, 26 Jun 2025 19:01:11 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b25b5b6fc290ee7813c2c5372b10db034421d9d7e2b1010120cf73f1a5a231`  
		Last Modified: Thu, 26 Jun 2025 19:01:34 GMT  
		Size: 54.7 MB (54709002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bdd656c45f58148d13b44e8aa25eadfd99a13393b44af194d787de321ba233`  
		Last Modified: Thu, 26 Jun 2025 19:01:12 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0173d486bae244932a269aea923d2e280dc57c1889de4221ee008ee61f177a`  
		Last Modified: Thu, 26 Jun 2025 19:01:13 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e74a27dbe5b2343c7ee103ec62914b4dfbbf04f5a61c011396783251446d41e`  
		Last Modified: Thu, 26 Jun 2025 19:01:15 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
