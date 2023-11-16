## `mongo:4-windowsservercore-1809`

```console
$ docker pull mongo@sha256:7782b22ac438f3067c836f01a695029aef9633825e4ca5e1ef7cd73993a99581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `mongo:4-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull mongo@sha256:4670efd9d61ae758037f3cf60ad5c9093439f8dc161ab9fc5235b8c21db84586
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2302991767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ccf2299d766b03764361c5e702066cecf8099a393e07871586bf76ee42645b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 03:20:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Nov 2023 04:12:49 GMT
ENV MONGO_VERSION=4.4.25
# Thu, 16 Nov 2023 04:12:50 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.25-signed.msi
# Thu, 16 Nov 2023 04:12:51 GMT
ENV MONGO_DOWNLOAD_SHA256=e9158fe81fd49b1e0bb121c5505e674864587e78b72683d8b477b4326da8472a
# Thu, 16 Nov 2023 04:14:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 04:15:01 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Nov 2023 04:15:02 GMT
EXPOSE 27017
# Thu, 16 Nov 2023 04:15:03 GMT
CMD ["mongod" "--bind_ip_all"]
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
	-	`sha256:e6b188dc001be88eee85de9ff2a267e1250c9253605ef96a0dec940d70a0faa1`  
		Last Modified: Thu, 16 Nov 2023 04:59:07 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f960343093692149cf59cd851b0bdcb8e528ee5ca03128cdc45a40d08bdb0fc`  
		Last Modified: Thu, 16 Nov 2023 04:59:07 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8310353bd03833ef3643fbd2c8b156ab99ce989a7a40509d0f3997e1826cbf`  
		Last Modified: Thu, 16 Nov 2023 04:59:05 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4e20547895c6ff44b701209a5ab5aca95820099649d7849b9351489eb930e2`  
		Last Modified: Thu, 16 Nov 2023 04:59:49 GMT  
		Size: 245.6 MB (245550664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3475d61487f7ddc2e861eae2fa6f14db834cfbd2c95671c50bb397b6d9077aaf`  
		Last Modified: Thu, 16 Nov 2023 04:59:05 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54886a0b8bde85c79a8cae0d164d235130159e9dfd7a00276ebdf7e573dc07e0`  
		Last Modified: Thu, 16 Nov 2023 04:59:05 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e0e546c3bc50186a7793173107e3dacc10f143d3264ca7a57ede04e70a7ca5`  
		Last Modified: Thu, 16 Nov 2023 04:59:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
