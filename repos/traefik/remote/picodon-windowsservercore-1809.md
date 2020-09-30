## `traefik:picodon-windowsservercore-1809`

```console
$ docker pull traefik@sha256:5cb304280cbe507eafd7920f4b80306f3151837b8a60c0c2e0f799a0ba1239e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `traefik:picodon-windowsservercore-1809` - windows version 10.0.17763.1457; amd64

```console
$ docker pull traefik@sha256:97a0e71e68783984b2d1cb3eef61272320e5c433b57727ca0ddb8f0ae1cca2e7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2385663898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4d73fbf8524ab8cb6df34938b8b0a7dd767d660d4302d99f761288ed97161e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 30 Sep 2020 01:17:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 30 Sep 2020 01:17:37 GMT
EXPOSE 80
# Wed, 30 Sep 2020 01:17:37 GMT
ENTRYPOINT ["/traefik"]
# Wed, 30 Sep 2020 01:17:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1fd4e6a50b0ffc66121e6c4458ac569afa32220d376b8dee78a54afdea3f04`  
		Last Modified: Wed, 30 Sep 2020 01:18:21 GMT  
		Size: 34.4 MB (34387102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0147705163f048eb7010f9b1f3d9d2935ffb29b8ed03495d41ca1d8743b287`  
		Last Modified: Wed, 30 Sep 2020 01:18:02 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e310db912dce00d88f8404bf2c994f89213ec10cf37a39a40943834c4b2d0575`  
		Last Modified: Wed, 30 Sep 2020 01:18:02 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae00372149856d2b440437fb779f341f7b0c9a73b7264edc18f7066b758c1584`  
		Last Modified: Wed, 30 Sep 2020 01:18:02 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
