## `mongo:8-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:374e6ac640616ab6d0417d1b10d4079175aa0c5789a0dce7255dbe597d9255c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `mongo:8-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull mongo@sha256:a19b50b70925fa9ae022b9215c8146c4c30395961d6ce4fdbc89093159d2b02c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3021188365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c6a409a89f80b31370f0af33980c4c2a869be4650550da868097b3f62e9d19`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Mon, 09 Dec 2024 20:30:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 09 Dec 2024 20:30:20 GMT
ENV MONGO_VERSION=8.0.4
# Mon, 09 Dec 2024 20:30:20 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.4-signed.msi
# Mon, 09 Dec 2024 20:30:21 GMT
ENV MONGO_DOWNLOAD_SHA256=52d30392e6767eb48c03fc9886b831da5a282af7aba49cc46f45c6b0f85280cb
# Mon, 09 Dec 2024 20:33:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 09 Dec 2024 20:33:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 09 Dec 2024 20:33:23 GMT
EXPOSE 27017
# Mon, 09 Dec 2024 20:33:23 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af8f0c60951cedf7e6c9f2a8427300519bce5895bb2c576882629c8f275e4e`  
		Last Modified: Mon, 09 Dec 2024 20:33:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d323c0e28e097f2118425890315075dbafe6d8d75db8c9822849d91cd4b72ab6`  
		Last Modified: Mon, 09 Dec 2024 20:33:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912c811f2f32fc965106c16961b3455f8236562ade7f0dbc15fd938cbbaf0807`  
		Last Modified: Mon, 09 Dec 2024 20:33:27 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc2704e2363da3774c70a1defdcb8f3def090c8300e5c4d24b7b97ff2624a9c`  
		Last Modified: Mon, 09 Dec 2024 20:33:26 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5784d019473150b10d3b489ab00339bcbd5c25a35cc71fbfdc58349500e120`  
		Last Modified: Mon, 09 Dec 2024 20:34:24 GMT  
		Size: 768.7 MB (768694945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8641c1b7455d663c5d11d8c18ee5e8901bc0bedfb0d9faf7af70026be3362159`  
		Last Modified: Mon, 09 Dec 2024 20:33:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1fe9de30d8f95574de70470ad00dec60b1ccfa5b4e66e8cb2bf663e1930738`  
		Last Modified: Mon, 09 Dec 2024 20:33:26 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8fb15ff973f3702e385334fd47bcaf9889388fd5c5ebe1a16bb09317e5c374a`  
		Last Modified: Mon, 09 Dec 2024 20:33:26 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
