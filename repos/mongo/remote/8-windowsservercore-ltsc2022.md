## `mongo:8-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:82896eb80c445d9f4529975813a3c7e9a5a9ba5eb080d134af225dccfbaebe61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `mongo:8-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull mongo@sha256:104bef9082ca209689a1d468b5bdf7531ece4c00e818bcc1123f8f097b18e059
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3021036863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be99c0d705f7f6bd64fc9f17fe77f2148a31274dac120acc07a83c91599d64a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 20:12:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Nov 2024 20:12:32 GMT
ENV MONGO_VERSION=8.0.3
# Thu, 14 Nov 2024 20:12:33 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.3-signed.msi
# Thu, 14 Nov 2024 20:12:33 GMT
ENV MONGO_DOWNLOAD_SHA256=f064b0d5096136a70edd9a4a1c17d23c78f62600ba860512523eee2206a018b9
# Thu, 14 Nov 2024 20:14:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 14 Nov 2024 20:14:10 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 14 Nov 2024 20:14:10 GMT
EXPOSE 27017
# Thu, 14 Nov 2024 20:14:11 GMT
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
	-	`sha256:68965c48940231b5fb626c18bdcfa23bcdb6201b17b9cf8c79eb16e5011f7e70`  
		Last Modified: Thu, 14 Nov 2024 20:14:15 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceabd9f0091214a0700edd3df213158a29848e9b55147182420d1dfd11701db2`  
		Last Modified: Thu, 14 Nov 2024 20:14:15 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad13e9dd64be6b7347bd9706951c1adf27948e0308f1693de3cd7ec75a33c3da`  
		Last Modified: Thu, 14 Nov 2024 20:14:15 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877e0fd228bf732c0fd742ee177791132fb4b0d480178a6094cbfa5a191621ee`  
		Last Modified: Thu, 14 Nov 2024 20:14:14 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61ad68908d8e5a905dcb3749b11b5a83be1b4b823b37f91b2e6c1732071998f`  
		Last Modified: Thu, 14 Nov 2024 20:15:16 GMT  
		Size: 768.5 MB (768543629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0fb8b87d0f7b44e606fbedc4350de4d668e238c9f2f3455072dc767961f1c3`  
		Last Modified: Thu, 14 Nov 2024 20:14:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e66cda621851460f482cd961a8af19d43c214c15ecd10fd6eab020e9f27825c`  
		Last Modified: Thu, 14 Nov 2024 20:14:14 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d48e718d980129dc3e71d1aa7e599f20df110740ea665461fbb22ae8439ef1`  
		Last Modified: Thu, 14 Nov 2024 20:14:14 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
