## `mongo:6-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:1991970735ff8c36bcc41245333c29c534cc73052e88caaf7c24c362389dd9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `mongo:6-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull mongo@sha256:e1ffcacee228db24c9d8f9536ba54698338a2c5993cc29fe41e2a80d07c159e1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2809111760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a0c4c0b8af2ff728097a78834c01bdc0096827dfac449cab18ce8a7672e9add`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:32:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Aug 2025 20:32:19 GMT
ENV MONGO_VERSION=6.0.25
# Tue, 12 Aug 2025 20:32:20 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.25-signed.msi
# Tue, 12 Aug 2025 20:32:21 GMT
ENV MONGO_DOWNLOAD_SHA256=1303e7480877cbd373bf1dbe1233631985d61898d7d5c85d3e8ef1ecca7d5f63
# Tue, 12 Aug 2025 20:33:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:33:05 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 12 Aug 2025 20:33:06 GMT
EXPOSE 27017
# Tue, 12 Aug 2025 20:33:07 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c264997c9bc449474e8a0e5ebe865a81af57261c342f00be89360bfc2d416ec`  
		Last Modified: Tue, 12 Aug 2025 20:34:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deff1e07244ddd7cb746033ea1b37bdd890f32905b13bdf497689bdd6e217ce3`  
		Last Modified: Tue, 12 Aug 2025 20:34:48 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c214b9fab1a23148791578fcb3e613d73af459ce40d76cd8c1967841974d26e2`  
		Last Modified: Tue, 12 Aug 2025 20:34:49 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332c9db24a797be16bfa9f97bcbfcf059873dc79073d030f521d0b13ff7e96af`  
		Last Modified: Tue, 12 Aug 2025 20:34:49 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e600e40e2412365952462d3df837e7458b7f003cc56cf483740864cb1328c7a`  
		Last Modified: Tue, 12 Aug 2025 20:45:51 GMT  
		Size: 527.4 MB (527410811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9105ea31a68080306f829308aa389065bdd147017be4e9ac7ae5621cff14c520`  
		Last Modified: Tue, 12 Aug 2025 20:34:48 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d94322b43f550c509c3691791a6d6b33566448da1fbbe7a9845edb2ca96f25`  
		Last Modified: Tue, 12 Aug 2025 20:34:48 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d8a1364b3af94769bab63060025bf2c28592d9f16136ec5eff33596a067c75`  
		Last Modified: Tue, 12 Aug 2025 20:34:48 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
