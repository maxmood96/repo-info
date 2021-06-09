## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:e86cdc0cb1ce27e7d790872f30cdcbcefbe40bb9cc7a818e4dac93051c9f3e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:b02d0fddc42e8f50f6dccf56bc6da2c299fa6ca12dac2a91142f5ea6f3c3b4d2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2646572446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec0469d99bdcdeb93ecb4cd714c002dc5344cdd980081af67522abd90cb61f56`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 13:15:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 15:52:54 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Jun 2021 15:52:57 GMT
ENV NATS_SERVER=2.2.6
# Wed, 09 Jun 2021 15:52:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.6/nats-server-v2.2.6-windows-amd64.zip
# Wed, 09 Jun 2021 15:53:01 GMT
ENV GIT_DOWNLOAD_SHA256=c1712f41e4e811027701a036b6ff67b1f09fb298b0674098b26f875d37e709b2
# Wed, 09 Jun 2021 15:53:32 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Jun 2021 15:54:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Jun 2021 15:54:44 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Jun 2021 15:54:47 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Jun 2021 15:54:49 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Jun 2021 15:54:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:639bb6bb2beb4cfdcacb9f0844344448fe26494665d5fe78a494419f86fbb18f`  
		Size: 923.3 MB (923252167 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ae7d2dc4b590128efeafd375d02122e65a2525623ac2be100c1a390caf8a4b49`  
		Last Modified: Wed, 09 Jun 2021 15:28:02 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507a90d55d261855b42c7b5905599cdc274ca135ad962fffffe1fa6246c9bba7`  
		Last Modified: Wed, 09 Jun 2021 15:59:38 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a0385e3ae1d1d8c00cf0ca66edc248c97d96c91e476559b29c6c52c46d3fe8`  
		Last Modified: Wed, 09 Jun 2021 15:59:37 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e1c1a9e404ff727f004e12aef5245aa88eb270ce9e3f73be3e85f2df635f3f`  
		Last Modified: Wed, 09 Jun 2021 15:59:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a88b6cac0f81b699f58105a6102b27018ddf36099cc8cf069fa44ad96e2fa0b`  
		Last Modified: Wed, 09 Jun 2021 15:59:37 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda44751dc046b037f6feced0dd9d70b6acfe04fc9099997ee322d8207cbe35c`  
		Last Modified: Wed, 09 Jun 2021 15:59:37 GMT  
		Size: 343.2 KB (343169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7df0a3f2eb0c7743406c39664c54d6dce8e83061bfa9d6fdc98ddb08231f479`  
		Last Modified: Wed, 09 Jun 2021 15:59:36 GMT  
		Size: 4.6 MB (4630934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebd05a6c49ff1da6167088c0efd1b8272094cd2930c4d10b9c4423900006425`  
		Last Modified: Wed, 09 Jun 2021 15:59:34 GMT  
		Size: 2.0 KB (1976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017fad8ec54342ed6819d801e462a0d9586120616b12bdac050efd3b2b3f10ed`  
		Last Modified: Wed, 09 Jun 2021 15:59:34 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4498408c64a82cbf1b4299f721bce414f88e9db0c6fdd6ec622145e162095d7a`  
		Last Modified: Wed, 09 Jun 2021 15:59:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11779cb16754ca0392b14675af366dbb6f10875912082da0e4faaad270fedc8b`  
		Last Modified: Wed, 09 Jun 2021 15:59:34 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
