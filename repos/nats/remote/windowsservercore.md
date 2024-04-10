## `nats:windowsservercore`

```console
$ docker pull nats@sha256:b04dc3c962bbed963b7ed2272999339683a9eb46cdeaa06a77c1dbbdfe93b834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `nats:windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:29380f4863fb3a6f2b04217f477bee6eac525e6b36400d4446ee1680024de74e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2170781570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa73df6040c74fa785c0df500e4c8a7a76a5ce054b396330c2b4631b211c5a06`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Wed, 10 Apr 2024 01:40:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Apr 2024 01:40:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:40:04 GMT
ENV NATS_SERVER=2.10.12
# Wed, 10 Apr 2024 01:40:05 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.12/nats-server-v2.10.12-windows-amd64.zip
# Wed, 10 Apr 2024 01:40:06 GMT
ENV NATS_SERVER_SHASUM=bc944f832fdc3eaa0072c0a5e278efd672cec394159661070e7aea4f5d483cbc
# Wed, 10 Apr 2024 01:41:22 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Apr 2024 01:43:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Apr 2024 01:43:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:43:16 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:43:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:43:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6ae8ddefe4f7d0224959df0cc91d01044dce7f127ee7c23257cf0b63bfd7ac`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266ac5d9d5680f1e3a65f9d272fc3a2ab7f67eda1b00c961365853e0a9c3e27`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b45aa9398ff56a16e042bfdf01b44ff7daebf93e7cba5d601367d2c0e5a55ed`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe31b64ec7d8949724e118281dfca112c508483cc5b28076aaadd223f212b4a4`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f68caae1490441aa87bfa98ed09fc4717d036f13634615fe4eb4a1efe4925a6`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567ed00bc244d7ef610728b1545d39345e73e8e86ee441b586eea2238d1bf1dd`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 241.8 KB (241850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f8817e79dfbc8f56443618f486d64c5ac11608663b3bdf7a25f87f2412c473`  
		Last Modified: Wed, 10 Apr 2024 01:48:02 GMT  
		Size: 6.1 MB (6099353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60589928d42d9fc2f8e9ccd4a26ba13cebed25894380700f63bace8ca5fc27c0`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbe842b574fe798f092ac13841eea2cee6361f8232a3539375c0503e5911af7`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619674a0794dc85dc23997a189c9659f4612bf24f1fd187f2d26e38dbf6a8691`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd24c8b4dbeddc4174617445fd1d056589be9451dfd07af7f714867654c353f`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
