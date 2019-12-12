## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:0c9b36619404d1d314ddf865303bf9685ee307afe94729f36df139ae74bbe37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull traefik@sha256:03c1f073dee16d4badbaa3d77b5022ce6325cafbc60ace7ba5e08405b6893f3f
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2240369397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa38c41dd182a4ca7e4659c8891af9564c6368022f06ed5d62b8dc938ea8682b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 29 Nov 2019 04:34:15 GMT
RUN Install update 1809-amd64
# Tue, 10 Dec 2019 21:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Dec 2019 00:13:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.1.0/traefik_v2.1.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 12 Dec 2019 00:13:56 GMT
EXPOSE 80
# Thu, 12 Dec 2019 00:13:57 GMT
ENTRYPOINT ["/traefik"]
# Thu, 12 Dec 2019 00:13:59 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:faf31ee0aa3d3c60a38dd03c7554d632065cef50eab052ef1444590786249d07`  
		Size: 681.6 MB (681618026 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e147f14e0d6a9cbd5261162dea8f3aac7a34db5d9f6a587a9aac6b88722a2da4`  
		Last Modified: Tue, 10 Dec 2019 22:07:34 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8952d668f7803b5e5ba234c84d477d1a76b8b8a38e0294e2fa48b5e761e07d12`  
		Last Modified: Thu, 12 Dec 2019 00:14:38 GMT  
		Size: 24.1 MB (24061234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3700a9eaad623a697c462b8d6ebd0b2929f47975b373ec46f338b4cc25c8eca`  
		Last Modified: Thu, 12 Dec 2019 00:14:32 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8218c9bcf4bd808b7d3ae21aebfbe854209cc7339d621a612110efbf910e69d`  
		Last Modified: Thu, 12 Dec 2019 00:14:32 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcffe60529c77d8bafd1a46dcec466554c45baa363d2ae7594b522d6793d50ea`  
		Last Modified: Thu, 12 Dec 2019 00:14:32 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
