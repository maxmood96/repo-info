## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:fc9f3a4493f401deed6acdcadaff40c596751f6fc9b5cd6fd3a5597e876c4841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.3650; amd64

```console
$ docker pull nats-streaming@sha256:e432cca2b1fb2af40ca299e80a02579387266d13a256bf7a23dfd7125a0ae4a1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2787076749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13f247cbd55632a872bae42021882364e6678b369692b701f6ebb8e9b0ddc4d`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Wed, 09 Nov 2022 14:50:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Nov 2022 16:44:45 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Nov 2022 18:16:17 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Wed, 09 Nov 2022 18:16:18 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.2/nats-streaming-server-v0.25.2-windows-amd64.zip
# Wed, 09 Nov 2022 18:16:19 GMT
ENV NATS_STREAMING_SERVER_SHASUM=554b083bb17f8f2e9a875b888dbe74454648f86c6e02bc489d88713431025d9d
# Wed, 09 Nov 2022 18:17:30 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Nov 2022 18:19:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Nov 2022 18:19:40 GMT
EXPOSE 4222 8222
# Wed, 09 Nov 2022 18:19:41 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Nov 2022 18:19:42 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99941fb33972e616b231a8aadd93463fdfd5de6aece4aa6c470d2feec31839be`  
		Last Modified: Wed, 09 Nov 2022 16:48:23 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f3d8a87f0a1540850986ff94131286dfa42ca116f04779e02f60b3a724641b`  
		Last Modified: Wed, 09 Nov 2022 16:48:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe863d992e0c58c9cf1632767e37ade6556903b1bb890c2a4dc02dffeaed78ef`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71a5994065b88d8a198293e12ac4530e9342de0f4d53860ee2743bd2d569013`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8e674abd79efbd197e128d166729af96bcf66ffb1646f10fb80dde56503f83`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec5f49fc868f6f3b72e2f76461f16e59f80e92a4186383b3baf71c06d3d2b21`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 359.2 KB (359194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0897e7aebc234f59c04916a3b53b2a9b5ac2bda1415cddcb71ddf1966d20bdfc`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 8.1 MB (8119591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ea295c4d678432a3afecc78785a990244c290159cc0851aa868efc70979b97`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a938d3ad7b90133750f1d10713db202d85b54f492cb2aef146e304f77b66f49`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b500e39240181724cbcb1a40781d36fae94a34eef9f926a5c612644211b67f`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
