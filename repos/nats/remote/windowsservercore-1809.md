## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:697ec56703339f66b45f1f84d1d28c50fea6d1913340dc3417f07cb03466d039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:143e9e296c13d7a71bfa00b08230709e757e96150a25e8bce3ad72f9538c4d93
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908432251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b77a82bb41c8594376ef53c13cf0fb93896749662022faf0b92f3ff75dc3b18`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 10 Oct 2024 00:38:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 10 Oct 2024 00:38:10 GMT
ENV NATS_DOCKERIZED=1
# Thu, 17 Oct 2024 22:15:24 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 22:15:26 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Thu, 17 Oct 2024 22:15:28 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Thu, 17 Oct 2024 22:16:23 GMT
RUN Set-PSDebug -Trace 2
# Thu, 17 Oct 2024 22:17:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 17 Oct 2024 22:17:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 17 Oct 2024 22:17:38 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 17 Oct 2024 22:17:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1196a5b13ab4e3918e43ddd7bbb877dbf52e832257c9ec3eb8019cd414af2e3a`  
		Last Modified: Thu, 10 Oct 2024 00:40:53 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484871eca2e8c738eb04d659975dd4a80e9dae8daf6e59d2297e6c3e81f03bd6`  
		Last Modified: Thu, 10 Oct 2024 00:40:52 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368fa5ecea627e9b785fb5887c6fc61ba24222a0164cff921e705fe2608d154`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9475e61a46a9199c2067156908c860a41c2e9745af42c903fb4ef6422082a246`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948095eebb084fb778711564072ea58aea5733478d3b2f451850a8f19705193f`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd37e14f1bd78d70c68d454292424b48c3ee9cd02835c28d253c0acaef2e1947`  
		Last Modified: Thu, 17 Oct 2024 22:18:25 GMT  
		Size: 444.4 KB (444352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f75af290818f7d902ec97658a83cd371aed1a0648369ba143d70e628c2c480`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 6.1 MB (6149451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e19f4bee2c3ad99b0a342f55ddab3fad4c6537df793f3d0f2e0c0afbba481b`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1d61f19a1bcb3733a1bdefa6317397344bd1380cbc31ed46f8449ac9ca0710`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97cbc0f6dd89bcef1b602c11babb7e58e8383097a287ac1c8e8d079b0c735af9`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22bd1ed76deddbcee8c0032b3760f182c88d86e44473ce346a6796644395b35`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
