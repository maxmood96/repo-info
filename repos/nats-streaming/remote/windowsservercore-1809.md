## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:d68ec26ab81994c8142ad8f24f5642b4c4398b61a9da446ccbffe53db6f110ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats-streaming@sha256:0df66a3e69a3bf2e0a227f1fb870bde32badb04d3d11e62a78e7fb520cde69ac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2512156670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db51f87e79820c2b2396793cf1b83e81e68ee0afad5f04f979211715ea2194b3`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 14:39:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 16:30:32 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Wed, 11 May 2022 16:30:33 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.6/nats-streaming-server-v0.24.6-windows-amd64.zip
# Wed, 11 May 2022 16:30:34 GMT
ENV NATS_STREAMING_SERVER_SHASUM=86e1e573706b41a109baf84e93d00cfa7e3f4e47d59068bda18e972a7d3768f4
# Wed, 11 May 2022 16:31:21 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 May 2022 16:32:58 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 May 2022 16:32:59 GMT
EXPOSE 4222 8222
# Wed, 11 May 2022 16:33:00 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 May 2022 16:33:00 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c1e63aec5d8d83ee6bf4eb10d12ff30fe2e0eee737a2ef9291ead11cfb5cc`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0414182f3892da8f7d095665f62200d67f6f8d2e246b130708b2b88a21687c3b`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164dca4c618438c46a2dc1963e12b45c2f8d43eef1d1fe7fae7e1c8c4e05ff0`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e40e75ccc6601c1be113a440f55f08afdecc037cdac48a489fdb828a760e8a8`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c46d136ed5db00b4518191e335ea48c04342ffbc2c41da9beeabc326232cb0d`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 482.5 KB (482509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9183e4d25dff6451cdfedc68317c4dd57922535f5d6aa35c5fb21dac3734fef`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 7.6 MB (7607166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bec91034c767639b4ccbb6a280e45a12dd83565d0f24400b5bb5a291c40cb7`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea7dc716bc45aacd9709e081731dbf3715f48204651675a9177cafd8253f5dd`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6b5bf987b96cb6c0b09277a5ba367b7ce2f6c83dd0412319b03eb875d90030`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
