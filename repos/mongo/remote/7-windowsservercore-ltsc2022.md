## `mongo:7-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:f06b78f5788b62461555252778f9ed123457aa66cafa227dddf477e45bec14b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `mongo:7-windowsservercore-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull mongo@sha256:8c7ba564396711cc66b78e7c88cb758b874c039f40bac59a64177b04b7d92116
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2499127236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684d8b8ee2ca70a5aa054c7e48a5e05ef6a2c93910699520cf71866d700bd379`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 03:18:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Nov 2023 03:28:06 GMT
ENV MONGO_VERSION=7.0.3
# Thu, 16 Nov 2023 03:28:07 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.3-signed.msi
# Thu, 16 Nov 2023 03:28:08 GMT
ENV MONGO_DOWNLOAD_SHA256=7ec97aa108c6af587e77a49479b4e7239da6ccac2903e163ae984797b3afea14
# Thu, 16 Nov 2023 03:30:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 03:30:27 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Nov 2023 03:30:28 GMT
EXPOSE 27017
# Thu, 16 Nov 2023 03:30:29 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a73dc3dec59ae25ff1232f5fdf2ab39df387f3bf86ba48717ff271d76c2feb`  
		Last Modified: Thu, 16 Nov 2023 04:19:26 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c78e661210df7e9eb5ab41db3aca66d8800d6617c3cf4178125ed3a99b433f`  
		Last Modified: Thu, 16 Nov 2023 04:26:20 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f641ede520e750d1c494a6c9b7222fae54bec5b73cc6c8c5b0bc1a38a911d3db`  
		Last Modified: Thu, 16 Nov 2023 04:26:20 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bee5e2ad383fb7ca0e114ad9dbfec41c4d37be5d9dd7e9081347d24581bc89f`  
		Last Modified: Thu, 16 Nov 2023 04:26:19 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54538a1ac7e0062cb8e2c9ddb6d5ab5accdc3b72a93c74f403ba007b60b200b`  
		Last Modified: Thu, 16 Nov 2023 04:27:51 GMT  
		Size: 612.3 MB (612336247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5052447881a901f21960dfe425b55725b550263b1d3c23864b551154ae4d987c`  
		Last Modified: Thu, 16 Nov 2023 04:26:19 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f073aae9d8bdfa66feadd8697a216b14877c0b9ff347217f211a85746da0d5a`  
		Last Modified: Thu, 16 Nov 2023 04:26:19 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68026f2e761421e59e2cfb6162ffcce6a54d03ea9a269ea4fad3e26650fe542`  
		Last Modified: Thu, 16 Nov 2023 04:26:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
