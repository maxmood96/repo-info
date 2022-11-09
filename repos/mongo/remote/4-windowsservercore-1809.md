## `mongo:4-windowsservercore-1809`

```console
$ docker pull mongo@sha256:92f44186cc88036e395a62c23aee84ffa99e7ada8c1257fb934b04ab97d54a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `mongo:4-windowsservercore-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull mongo@sha256:8a80e8c674a9b36f5cd22dc11ba78a768efe885191d0b6f57037546293e630aa
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3023888473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a56aad28bab0eed88d88abfe7aabfdb13308d18b79eb4033e3bd7dac261c17`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Wed, 09 Nov 2022 14:50:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Nov 2022 18:40:51 GMT
ENV MONGO_VERSION=4.4.17
# Wed, 09 Nov 2022 18:40:52 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.17-signed.msi
# Wed, 09 Nov 2022 18:40:53 GMT
ENV MONGO_DOWNLOAD_SHA256=29aa0584c70c5c473f2a0a5d5bd90e38897c10de1d3e4bc0cefa28ae9a532a8b
# Wed, 09 Nov 2022 18:43:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Nov 2022 18:43:12 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Nov 2022 18:43:13 GMT
EXPOSE 27017
# Wed, 09 Nov 2022 18:43:13 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99941fb33972e616b231a8aadd93463fdfd5de6aece4aa6c470d2feec31839be`  
		Last Modified: Wed, 09 Nov 2022 16:48:23 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388300cd2721fad44bbdaf82768d9e7975e98bfce8df465b2d27a667034d2fdb`  
		Last Modified: Wed, 09 Nov 2022 19:15:42 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb9d31541fcec9cbe7d8b7be631d96123d835a18b5390fb248757f29ffc0e0b`  
		Last Modified: Wed, 09 Nov 2022 19:15:42 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe73e691cb3f9c467691634678504f384b5202fcbd13857f98c47ba4eba017a8`  
		Last Modified: Wed, 09 Nov 2022 19:15:39 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd367789747e4268b3d245c3550ee6de0d4466f7c6a7da6b46146ae30d40f71`  
		Last Modified: Wed, 09 Nov 2022 19:16:31 GMT  
		Size: 245.3 MB (245291804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816f56121cc6d5b93c3265124f1f8663d5e23bba91de4fe34d65ac3a9fe960de`  
		Last Modified: Wed, 09 Nov 2022 19:15:39 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421d55bca2de3c14c9c073a62895437b5a1e356975ce0a8891cfe6fe08d35107`  
		Last Modified: Wed, 09 Nov 2022 19:15:39 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b012b8b4e0290d7fdce461c167492a2529bc8761738a5904aeb04b1311dd2a1`  
		Last Modified: Wed, 09 Nov 2022 19:15:39 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
