## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:263dc1906c5b5a2332d0b6a46ffc6603ffe9285a2c17792b4656f000c0d11b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:f117a76806e0323d616ab3f876137fb624b8547621e54f964fd34cb25486c9c0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076135685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929ad88f44da625ee4ed8ae7cab19a27a773275a97a49eb6dd7ed8907a90cd74`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Fri, 02 Feb 2024 22:15:06 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 22:15:07 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.10/nats-server-v2.10.10-windows-amd64.zip
# Fri, 02 Feb 2024 22:15:08 GMT
ENV NATS_SERVER_SHASUM=d135040811bbf093dc9eb84df2db3c895d497133278e4db70f6f5b26b421838c
# Fri, 02 Feb 2024 22:16:21 GMT
RUN Set-PSDebug -Trace 2
# Fri, 02 Feb 2024 22:18:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 02 Feb 2024 22:18:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 02 Feb 2024 22:18:07 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:18:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 02 Feb 2024 22:18:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e53ca3719e6e9112088f66f71aaef8bbb197e6092f22f1ba72c850be7530914`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413040ec09514434dca5d5aad02ae31a8c640cf903dac2fa7e664b3d38467ff4`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60133191d49be76203feabf2af44a7cbb53ba8b87d63060935a27d55a156e7c5`  
		Last Modified: Fri, 02 Feb 2024 22:19:15 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811e367ec399c652035faf850e6b86983b298764b8235f63243d25543c43a40`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 454.2 KB (454247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8116acb67fede86d4954fdd4e3f74a2fbe6dbc59a63cebf20f2d2432fa871bf9`  
		Last Modified: Fri, 02 Feb 2024 22:19:15 GMT  
		Size: 5.9 MB (5945679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f74635b53e0ec71d3a86fa2893343f620736a1d8c5479a971d6d59c7a89a8ab`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa627392b90e6e082a6e9f016fc01148762aa2e29a87024d2c0bd7e1b196942`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f4c34896adf534815a28f43f4ed0521bc607062da66b18cec2f9593be17011`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbf8f98271f2fc5cf9645300a39dc8d565dd717915e89e8d7d9fa01a753cef2`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
