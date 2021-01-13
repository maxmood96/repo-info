## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:ea0be7c6f01582d60f391e779978dd496c114087cac9dff08c979b91ca2777c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull nats@sha256:aada5edd446c33d7f0cdec0fefcb38a8b5590e44d4dc3c96a251e4dc70dc3331
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2454148019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c031dbf4ba2968a5141c84684c424493436b1c5c06ceada8f998aad51a31a186`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 15:20:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jan 2021 19:04:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:04:05 GMT
ENV NATS_SERVER=2.1.9
# Wed, 13 Jan 2021 19:04:06 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 13 Jan 2021 19:04:06 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 13 Jan 2021 19:04:37 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jan 2021 19:05:47 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jan 2021 19:05:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:05:49 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:05:50 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:05:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f84df50d9e20cf852bfd3555d4e56feabf7b9c735e48c613fc461146876bc03`  
		Last Modified: Wed, 13 Jan 2021 18:31:55 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff779c93810f460e9728c49a995f9cdd81c09b10ffc6e842f2272d19bf4389c`  
		Last Modified: Wed, 13 Jan 2021 19:10:22 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faaba717596a54bf51953c222df419b525a196529e9d4d0c98e44bf6c7bc4ee`  
		Last Modified: Wed, 13 Jan 2021 19:10:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cb7951519de47a30ef002cff4cb9c60650027cae289b36b71148ac51859b63`  
		Last Modified: Wed, 13 Jan 2021 19:10:21 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e01bfa5d9722f31f0db2b1d9a8b4c590620491626f2bd622eebef651c8aa8`  
		Last Modified: Wed, 13 Jan 2021 19:10:19 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62774ffa1eced43b67a7b2e3ad24b3bade3513280a5135aa994e68fd6744ab46`  
		Last Modified: Wed, 13 Jan 2021 19:10:19 GMT  
		Size: 5.0 MB (4995396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07cd3dac74e385b2c29cc30fee72c5dba6fe50c4e8693107469d14a3ac38e40`  
		Last Modified: Wed, 13 Jan 2021 19:10:17 GMT  
		Size: 13.4 MB (13369683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac73259d45c25f57b84af56ae813f5c1071b64fd365abc139468c74741017c90`  
		Last Modified: Wed, 13 Jan 2021 19:10:14 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e972d90c5bf2368649731e44c25e0b6d0d7615adbeeb4830fdd61d05c703710`  
		Last Modified: Wed, 13 Jan 2021 19:10:17 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fe9f87a1c2bb4a7311943263ac9446984971e7804672e6c71473ec4619d723`  
		Last Modified: Wed, 13 Jan 2021 19:10:15 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c96eb244980fd8b710cd559fc78aba2933f3cd5bb8b7d0d8cdd2a7bc287227`  
		Last Modified: Wed, 13 Jan 2021 19:10:16 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
