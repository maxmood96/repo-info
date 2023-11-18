## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:54d5597f5252c7667f57e449d1ab34bed3d06f116660ef7fd9c074cd836ecb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.5122; amd64

```console
$ docker pull nats-streaming@sha256:e70e08f4da3feaebc5b3ed23fc0b453063e4959f1a29364054e290bbbfae1718
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2066136738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c52ee67415fd766abb836f51194fb89dea9acc4f5e29c89de79506403ed2e60`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 03:20:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Nov 2023 05:04:35 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Nov 2023 02:15:44 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 18 Nov 2023 02:15:45 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Sat, 18 Nov 2023 02:15:46 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Sat, 18 Nov 2023 02:16:56 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Nov 2023 02:19:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Sat, 18 Nov 2023 02:19:02 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:19:03 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 18 Nov 2023 02:19:04 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e4111e1324ff2110def2382c3796071edd92a76a262efa6c0657d549b64496`  
		Last Modified: Thu, 16 Nov 2023 04:21:07 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18b0af12f04914a99bd0e5616b75c205f8a22c3c23bb3e13ea8fb557b765ec1`  
		Last Modified: Thu, 16 Nov 2023 05:11:46 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2c88afdf8aa9af5173b3c8c128d4bcab7bbbfc61260c1a8a06caabf129202f`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b9c35daf71d710280381df335a3a73f13f7a49f2b050d0fd2e5a7e0ad70c43`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38aa9d9ac84d59b315d189635288cd861d2270b2e7084325252a6ce902127ab`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696922a5b3c732f5492bb89d8732890d4d9e9326827a11ed3c12078d6aaae41e`  
		Last Modified: Sat, 18 Nov 2023 02:19:41 GMT  
		Size: 457.2 KB (457228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ca1c650d4640e728726b56f2a343d6b4ed6fd7a5e8cf5f7d9be2f8e21c5364`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 8.2 MB (8236590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9221495cf1fb3fe6d3d8a32fe845adb595d262f4755ad2d7bcb475a4bba2d430`  
		Last Modified: Sat, 18 Nov 2023 02:19:41 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83b2bee4daa90dd6450149ac6839f54aaa3297bf58b3e87d204e0154e93c2d`  
		Last Modified: Sat, 18 Nov 2023 02:19:40 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2520e3f1aa07523fb9e5b0f97f51acf5c7915f0d0f3433d63b89ed58b7e61dc`  
		Last Modified: Sat, 18 Nov 2023 02:19:40 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
