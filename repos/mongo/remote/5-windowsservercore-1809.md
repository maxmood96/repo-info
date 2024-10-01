## `mongo:5-windowsservercore-1809`

```console
$ docker pull mongo@sha256:d1a95d6ced61e9d30292aac3e04ffff13c8a4ce1a9f207d2a41cee5f900b94bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `mongo:5-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull mongo@sha256:55b9ce8287b392dff0da8e4dcd1bc1ede062c5ec991872c373b03ca0a42669c7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2032781005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ea42073547620617d2da5dc975c76f25900442e619fd4fdfb0004463067080`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 01 Oct 2024 01:50:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 01 Oct 2024 01:50:37 GMT
ENV MONGO_VERSION=5.0.29
# Tue, 01 Oct 2024 01:50:38 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.29-signed.msi
# Tue, 01 Oct 2024 01:50:38 GMT
ENV MONGO_DOWNLOAD_SHA256=3188d1a49244ce4a6bc4d853a3d79c178a9d0ae5e6613e4f42cf4156e6b25178
# Tue, 01 Oct 2024 01:52:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 01 Oct 2024 01:52:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 01 Oct 2024 01:52:41 GMT
EXPOSE 27017
# Tue, 01 Oct 2024 01:52:42 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de0802909f612c27aa1c2a921ff285c092ff0315298370b5219575467b76234`  
		Last Modified: Tue, 01 Oct 2024 01:52:47 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8905e420cb470bf27abe5ab72fd27d6741bae31d351b690ea492ffb3227619`  
		Last Modified: Tue, 01 Oct 2024 01:52:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27432b530c547fcac7da01d41a6b9737e5000ba0ebe07a5e8d1a308a6e1998ca`  
		Last Modified: Tue, 01 Oct 2024 01:52:47 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406db03bb98bc46c633541cc0af9988484c7ceaa23554be3e1e9b36cae14746`  
		Last Modified: Tue, 01 Oct 2024 01:52:46 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb30f61184a0d013da7893e61cfa3f4dd5d725a78e1a6ff53ebbc9f3fa07ec4`  
		Last Modified: Tue, 01 Oct 2024 01:53:15 GMT  
		Size: 312.5 MB (312503543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e9544e6c7dfd311487804db08aba7bfb2e3a179a050ba37cbc9f6d239b5855`  
		Last Modified: Tue, 01 Oct 2024 01:52:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3200a748a95820826d3ae26d3ca21c3938d96157507dfcf81bf1fd22895c9b8`  
		Last Modified: Tue, 01 Oct 2024 01:52:46 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e69d9e18e35aef18c37f7121a274e23ab701749d55666ec91c7116759b8c1ef`  
		Last Modified: Tue, 01 Oct 2024 01:52:46 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
