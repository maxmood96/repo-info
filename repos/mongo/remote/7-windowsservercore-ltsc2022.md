## `mongo:7-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:654df355fd0ff74c2291dd3725cf474c26df58d02a28f7f257d79e2fa06daf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2159; amd64

### `mongo:7-windowsservercore-ltsc2022` - windows version 10.0.20348.2159; amd64

```console
$ docker pull mongo@sha256:9ced31aef96058db9bc83c870af1feca596271a0e98abb9853e6239fb99dac43
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2502167928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4abf5fa287d29c586ce5843c91927381a971b0eb6935e85ef958eee0a9b28d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 09 Jan 2024 00:54:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Jan 2024 00:54:03 GMT
ENV MONGO_VERSION=7.0.5
# Tue, 09 Jan 2024 00:54:04 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.5-signed.msi
# Tue, 09 Jan 2024 00:54:04 GMT
ENV MONGO_DOWNLOAD_SHA256=96441addde451b9d81dfaa10aca9678ada35d17d02a9a07481c6137d3df55e2b
# Tue, 09 Jan 2024 00:56:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 09 Jan 2024 00:56:31 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 09 Jan 2024 00:56:32 GMT
EXPOSE 27017
# Tue, 09 Jan 2024 00:56:32 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef725cfdd58d10418af51fa5c89b9d29bd3b76005c748acbdd44330bb06247f9`  
		Last Modified: Tue, 09 Jan 2024 00:56:36 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be74832c2b82556423f128660d399e7188489016220dc5499e8c4719b99b6f7c`  
		Last Modified: Tue, 09 Jan 2024 00:56:36 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fae7c3345f8d9da5643f49bab184f9e786b131819c2abec4076e3f440a0065e`  
		Last Modified: Tue, 09 Jan 2024 00:56:36 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5e98f3c84f62f9e930c6c7c2bfdc4281570ba582b485cfe7820af504a8767e`  
		Last Modified: Tue, 09 Jan 2024 00:56:35 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4111606c38058aa006f8d2fd83b6122275673e1d4381a7c7637eeb9137f98019`  
		Last Modified: Tue, 09 Jan 2024 00:57:22 GMT  
		Size: 612.9 MB (612885305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a6375a916b87593c7c8b02b01fbf8b1dde40edcf43b6ab2a9102ad235e5c3c`  
		Last Modified: Tue, 09 Jan 2024 00:56:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee2628f4f43d0ef7868fcf617db8dca4bb331b54d0beb6347891a88dda6cf5e`  
		Last Modified: Tue, 09 Jan 2024 00:56:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf81cbd5c4b01927e43ee20f3abbaebe726f8a141d31e361b07f468c5add838`  
		Last Modified: Tue, 09 Jan 2024 00:56:35 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
