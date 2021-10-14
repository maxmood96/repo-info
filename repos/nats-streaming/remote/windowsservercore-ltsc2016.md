## `nats-streaming:windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:8d096afab2c01c6c4189b4061d7988c4ba7bcdc910cac57638a57a3cf984af30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4704; amd64

### `nats-streaming:windowsservercore-ltsc2016` - windows version 10.0.14393.4704; amd64

```console
$ docker pull nats-streaming@sha256:5c0d5082815925265b3c67b9d5ed588e001509eb17effcadd7806d7a7b864347
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6285311144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e885a9c11ace0b8c8881b5829dcef25968971a93a07868cab39c3829de8ccdb1`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 06 Oct 2021 21:16:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Oct 2021 00:39:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Oct 2021 00:39:25 GMT
ENV NATS_DOCKERIZED=1
# Thu, 14 Oct 2021 01:30:04 GMT
ENV NATS_STREAMING_SERVER=0.22.1
# Thu, 14 Oct 2021 01:30:05 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.22.1/nats-streaming-server-v0.22.1-windows-amd64.zip
# Thu, 14 Oct 2021 01:30:06 GMT
ENV NATS_STREAMING_SERVER_SHASUM=4516852b493111b73ec06477be4a27e66f5abc9ca1ff4dd2b970232271611264
# Thu, 14 Oct 2021 01:31:01 GMT
RUN Set-PSDebug -Trace 2
# Thu, 14 Oct 2021 01:32:52 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 14 Oct 2021 01:32:53 GMT
EXPOSE 4222 8222
# Thu, 14 Oct 2021 01:32:54 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 14 Oct 2021 01:32:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0c776a8e8e3c02d360995b7fa26a3fd7c0928965795fac57b69ff07418ab07bf`  
		Size: 2.2 GB (2202780626 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4d3c52a3fe41298469bd9ca8471cd22a349f75bf82b049e968c97dd7cbf538b9`  
		Last Modified: Wed, 13 Oct 2021 00:44:16 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5e5e67c70d509eb320faa6c55dd5fdc5c5440334d85dd07ea0e919299624b2`  
		Last Modified: Wed, 13 Oct 2021 00:44:15 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46690a656a07854c0c11f7feb03f03cc89e757939b5e2e1b3acaf7009df6582d`  
		Last Modified: Thu, 14 Oct 2021 01:33:52 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e632bd8184f1a16d50e13ae4489bf215fc1b21ed8012f38bf6f9459ec1cd08`  
		Last Modified: Thu, 14 Oct 2021 01:33:52 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a57fcc852206a34bd2a0d73b7e25fab6f59b83cc5cc0ac3f89bb583a4d34079`  
		Last Modified: Thu, 14 Oct 2021 01:33:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44472af09915d6db7ad37492fa748f31e8dbb25d0e73a43c9c54dd2bc2004e50`  
		Last Modified: Thu, 14 Oct 2021 01:33:50 GMT  
		Size: 348.4 KB (348375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f7e74c499272d322f27b18ae64bb610922dd18b559ed0b39f5f89e8dbe7366`  
		Last Modified: Thu, 14 Oct 2021 01:33:53 GMT  
		Size: 12.2 MB (12185014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b959cfc7526dcc4834f5515e1fc73239f4709c09a3cec6846b93654333a90e2`  
		Last Modified: Thu, 14 Oct 2021 01:33:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e057e49465df3a405770ced34ba8dca7a4e8b31d09b14ff1c15743af43f13ff`  
		Last Modified: Thu, 14 Oct 2021 01:33:50 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c44dd27158348b601e232ca49c5efc784ee598bcd1b7b67a91b4566e9c8ced`  
		Last Modified: Thu, 14 Oct 2021 01:33:50 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
