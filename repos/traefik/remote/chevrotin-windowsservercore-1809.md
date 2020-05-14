## `traefik:chevrotin-windowsservercore-1809`

```console
$ docker pull traefik@sha256:ca4312fe85511e21893fe539421ea93da2f6464509c49e5f2497b7d444579f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `traefik:chevrotin-windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull traefik@sha256:7fbd90aab6acf67c19504581f5caded1990e7389fecb12e488c014ebfcd8fc14
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1740038176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c247acbc36a543d818f7c87fbea69d702b6c5672f1880dd65d63033b5bee8f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 21:21:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.1/traefik_v2.2.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 May 2020 21:21:07 GMT
EXPOSE 80
# Wed, 13 May 2020 21:21:08 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 May 2020 21:21:09 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:77613e754ba9d62c0acd4ef271c4ee7d3af091b8c8b310afa404560a9d281f82`  
		Last Modified: Wed, 13 May 2020 13:00:20 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fa29920fc854a77ba720ac8b8e0eed9ef597d92c18b107ffe5801005256dc7`  
		Last Modified: Wed, 13 May 2020 21:22:27 GMT  
		Size: 21.7 MB (21700680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c8483b98ec5f2b158924193bfadc31f25e0ca35c1c9089373af16e373cb48b`  
		Last Modified: Wed, 13 May 2020 21:22:21 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046993ac671fe9dcebee1183352773045ac5df2903d9dbf653c4c76a73c1aa4e`  
		Last Modified: Wed, 13 May 2020 21:22:21 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3eeea401cecc78c68f4f66becc292a22894683116088d010b1620d9d693c680`  
		Last Modified: Wed, 13 May 2020 21:22:20 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
