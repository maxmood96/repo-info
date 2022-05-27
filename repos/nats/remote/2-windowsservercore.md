## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:21e6b0cbe3d42465b9005d70c7795eeaf812457704fed30ce2ff785c6378a14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:611c3122e7feffc2768797eac1184a3ffc57c69ed7f023bf7066607f0b006177
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2509547985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16ab36597c6cc5b853a849d91bff282fe7575d89c8d72bacf35977f112ddff2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
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
# Fri, 27 May 2022 00:23:15 GMT
ENV NATS_SERVER=2.8.4
# Fri, 27 May 2022 00:23:16 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.4/nats-server-v2.8.4-windows-amd64.zip
# Fri, 27 May 2022 00:23:17 GMT
ENV NATS_SERVER_SHASUM=911e8b77cf288c6e0997891d1400e5cc59dedd928e8f1685650c468674b52dc8
# Fri, 27 May 2022 00:24:14 GMT
RUN Set-PSDebug -Trace 2
# Fri, 27 May 2022 00:25:37 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 27 May 2022 00:25:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 May 2022 00:25:40 GMT
EXPOSE 4222 6222 8222
# Fri, 27 May 2022 00:25:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 May 2022 00:25:42 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:3e46883112793fbc3f4ba503e0c3adda871fe219fa4792e791c1b0131ec4b76a`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270932ccc85285da4c78794de461bdbf36ec177518c5c609edf7332a3c0e9903`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a573a05b073e99843fb03188f4140e47a95892936eee597e6612b68dea7a276a`  
		Last Modified: Fri, 27 May 2022 01:14:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceeeeb1511ea57b0f10413c14390340603ed50966f7f91aad559fcc32284a027`  
		Last Modified: Fri, 27 May 2022 01:14:56 GMT  
		Size: 497.4 KB (497353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee183f3745d31b3ab9904f03c5506b37bda08b06abc88817563f753d699c4aba`  
		Last Modified: Fri, 27 May 2022 01:14:55 GMT  
		Size: 5.0 MB (4981575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e67025d9a010ea39c79da6be0497e87fda67f62551adc4d81a0e83f06ee4527`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea59effc695238f40330bf321e135d548663a258eb2de36e3cbd0ecc2eb4f0e`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e27ce3724613991b447f6c75de82694a6e3df3a5e6b2f6cb4044f7aa89f3ca`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08833d90efc546bc030a1d2c6f4b15d21da31004d9c19858e051a00407eecc56`  
		Last Modified: Fri, 27 May 2022 01:14:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
