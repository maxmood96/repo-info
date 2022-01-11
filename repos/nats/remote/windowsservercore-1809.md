## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:aaac8717c9c75e91d70deb34b19c63f52da570a1829cd3d554b272c27f0b67a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull nats@sha256:9ec8ecb3264f72f02ee69c7ffa975d56e48203369afb34418dea94dba2b4ae0c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2716929335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e7aaeb57ee35abc8e939452d2e15bd08ba606e342209e2667809e0983874c5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 19:57:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Jan 2022 19:57:20 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 21:12:44 GMT
ENV NATS_SERVER=2.6.6
# Tue, 11 Jan 2022 21:12:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Tue, 11 Jan 2022 21:12:46 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Tue, 11 Jan 2022 21:13:46 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Jan 2022 21:15:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 11 Jan 2022 21:15:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 11 Jan 2022 21:15:20 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Jan 2022 21:15:21 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Jan 2022 21:15:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6b0d3bf43971fbd8415d8d92eb7059b4aed9092fc3c7878b893d688b3b6b478c`  
		Last Modified: Tue, 11 Jan 2022 21:19:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1547439af6c2636b60dd7d8627268efd629795e6a4f8bcd3c3f7ebba364c6b79`  
		Last Modified: Tue, 11 Jan 2022 21:19:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3ff1c837c1400cecad7ec1d811046fe0722b68715bcf14f5af1910f3485d95`  
		Last Modified: Tue, 11 Jan 2022 21:19:05 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a1cc9fed9c4abe6482a7b323773c3c3b00e60b512bce0320d363810a5c6739`  
		Last Modified: Tue, 11 Jan 2022 21:19:05 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b587187b8e7626c09b3fb4301012dbe9334ecaade04dd66d4fa372c7b39432`  
		Last Modified: Tue, 11 Jan 2022 21:19:05 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ce345f905ae339c28db8299c640fa0d816de800bcb1923ba32734cd7095e71`  
		Last Modified: Tue, 11 Jan 2022 21:19:05 GMT  
		Size: 357.9 KB (357866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34fe804846d4cd3fdffe22f6741fb065c85c7185812ccd5470c53e6c23a0fd1`  
		Last Modified: Tue, 11 Jan 2022 21:19:04 GMT  
		Size: 5.0 MB (4973955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1b304d7ae255fcb3f210d82c5ad1f247de9909e3ad5f1d7972731886cc7df8`  
		Last Modified: Tue, 11 Jan 2022 21:19:02 GMT  
		Size: 2.0 KB (1960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b48b4cfd461e66eb15052c70bd5b25b014f531faff5fd01e402a0877ab230a`  
		Last Modified: Tue, 11 Jan 2022 21:19:02 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4a7a58abee158d079c7b5e4d53c206270f552ef48dcc1d93b59cd7346873b7`  
		Last Modified: Tue, 11 Jan 2022 21:19:02 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e905ef8fd5ad6ed59146ccf1e68bc412b441e4a242d3de9411a85f3f4c82373a`  
		Last Modified: Tue, 11 Jan 2022 21:19:02 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
