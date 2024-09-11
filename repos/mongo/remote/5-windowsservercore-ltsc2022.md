## `mongo:5-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:b19fda7fe59b66789846805df84b22d1ae9015942159642850cb1488a8978ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `mongo:5-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull mongo@sha256:48e72b731db06478c01e9151dbcb5c3ad5112fcaa98c1c2f871f82611e0b76b6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1775334861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61405c91e449ed548b2ecf9ad094838366b50ee9b64da9ddfc1371cbe6cf81c1`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:00:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Sep 2024 00:00:55 GMT
ENV MONGO_VERSION=5.0.28
# Wed, 11 Sep 2024 00:00:56 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.28-signed.msi
# Wed, 11 Sep 2024 00:00:57 GMT
ENV MONGO_DOWNLOAD_SHA256=db9caacfb85f9f37f7621759d0fad008b9d575c9974bf3e25fa0d4b243000e89
# Wed, 11 Sep 2024 00:01:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 00:01:38 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Sep 2024 00:01:40 GMT
EXPOSE 27017
# Wed, 11 Sep 2024 00:01:41 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3013849534deef500e1c93f7518201a6351d77c994980c38a0861b899c7b020`  
		Last Modified: Wed, 11 Sep 2024 00:01:47 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cd0379a77828b76b6fbfeddb38018e93628e67a21623634270739cdbc9adab`  
		Last Modified: Wed, 11 Sep 2024 00:01:47 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e874fabe7f479230a000e1b3fe40e55a90c88317454223623522991958e05a02`  
		Last Modified: Wed, 11 Sep 2024 00:01:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740ef34d8847410c7effe2f10e8548b6afc62596da4688acc4399eae8ff7995d`  
		Last Modified: Wed, 11 Sep 2024 00:01:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9821891e04de04b9fa4d3ac0714935ef69986b79fb2df08dea51aeafaa300ec2`  
		Last Modified: Wed, 11 Sep 2024 00:02:16 GMT  
		Size: 313.1 MB (313133416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150fc6cdd0203a04bf4eba9342eb51355438599910a77aec8cd84f2e4b51020f`  
		Last Modified: Wed, 11 Sep 2024 00:01:45 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a19a429bfb4a736e4a208c3a727870d2a8fc03621b15ca0a15fb0b6f8c9bf81`  
		Last Modified: Wed, 11 Sep 2024 00:01:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ef90877524398af3a783ae78c928ab25df39a6cd3938fc185002fba03fc7db`  
		Last Modified: Wed, 11 Sep 2024 00:01:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
