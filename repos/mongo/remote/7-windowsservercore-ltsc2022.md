## `mongo:7-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:e447984209d1d1eb38463ea4fe7e6171fab50be73be111a0b02fa37b3ac1e0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `mongo:7-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull mongo@sha256:fdc6a0fcd9a88fbba815f88e0215dc76a4261dc9db2eeac728927d54766d29dc
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2575271386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45bd006bceeb7043bbcc9af8c3ed2ab8c6a4ee991871f46a9720bfdcbf759a0`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 03 Apr 2024 20:50:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 03 Apr 2024 20:50:59 GMT
ENV MONGO_VERSION=7.0.8
# Wed, 03 Apr 2024 20:51:00 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.8-signed.msi
# Wed, 03 Apr 2024 20:51:00 GMT
ENV MONGO_DOWNLOAD_SHA256=30b8b6a96c5887a49e671ba72a7995279be7f232a666acd6717a59f7c68295f3
# Wed, 03 Apr 2024 20:53:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 20:53:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 03 Apr 2024 20:53:58 GMT
EXPOSE 27017
# Wed, 03 Apr 2024 20:53:59 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fe8c3ef5dccf9800806f8d1d87830423bc307fff4e627cb559d0484193df53`  
		Last Modified: Wed, 03 Apr 2024 20:54:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e092c7571913f13aec1194969aee04dadff963062f701d6116ad8d4e0e483f`  
		Last Modified: Wed, 03 Apr 2024 20:54:03 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c9c15d7e0ab1082478292cf30e74f6571da8a69162c4cc6bc0602b09011673`  
		Last Modified: Wed, 03 Apr 2024 20:54:03 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c98984540c816dea737902e6aeed9239f35110f142be39804f76ca9b99ddb2`  
		Last Modified: Wed, 03 Apr 2024 20:54:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54358aa94e42a912d0c3b869eec605b696a279c761d1dcfdce0e2a836afe8e73`  
		Last Modified: Wed, 03 Apr 2024 20:54:50 GMT  
		Size: 617.8 MB (617803326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6fab670b98dd35c8b1d342ddc7d805ac7419afcd4931abac175ea563caa8d5`  
		Last Modified: Wed, 03 Apr 2024 20:54:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ce08824d37fa9b3e26429c6c5895515068449816b46d9ab35627fac8914f4e`  
		Last Modified: Wed, 03 Apr 2024 20:54:02 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb84c6b69455ef0a02b98f17a73859922fe85893e032dfcc02bd5fc826a888ce`  
		Last Modified: Wed, 03 Apr 2024 20:54:01 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
