## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:a563fe566f581e3f41e1cac69fe6013582d568d4b4596567e2bb636f2a5a59b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3930; amd64
	-	windows version 10.0.17763.1457; amd64

### `mongo:windowsservercore` - windows version 10.0.14393.3930; amd64

```console
$ docker pull mongo@sha256:c742ed27a3b073d16fb5e2b2a3eb9f1331aeac2ec92a56ab4e3b5b3941f07f26
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5789039610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4599475e820a6c68fdd59a35f95117b1d70b86d07f2a5252b2b9a5733e5b94`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 01 Sep 2020 19:14:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Sep 2020 13:23:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Sep 2020 20:58:02 GMT
ENV MONGO_VERSION=4.4.0
# Wed, 09 Sep 2020 20:58:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-signed.msi
# Wed, 09 Sep 2020 20:58:03 GMT
ENV MONGO_DOWNLOAD_SHA256=ab326721c480dfafe0d0c3c1489c25e3a411b86e830dd91151b5ae24b8c9d508
# Wed, 09 Sep 2020 21:01:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Sep 2020 21:01:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Sep 2020 21:01:18 GMT
EXPOSE 27017
# Wed, 09 Sep 2020 21:01:18 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bc202b498d589027cc702b23cf959b8842907508b3465b9d6ff739c9668e5134`  
		Size: 1.7 GB (1669268544 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1d56eeebea105bba2dd1879a89adb012f98cf42708c0f36ca4af683db7162a2`  
		Last Modified: Wed, 09 Sep 2020 16:49:22 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f06a645024bbeaed7cf528bc04536c9d8a51902c503a5659b4e0dbba1aead7`  
		Last Modified: Wed, 09 Sep 2020 21:08:10 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22cc93b81b3ca6aa6b6a16e2f921f6413812bc72daa6d03c047da681ce48924`  
		Last Modified: Wed, 09 Sep 2020 21:08:10 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75a57ce8523040245fe75d748b18541af866414b2d5ee0e0d3909a58560aeda`  
		Last Modified: Wed, 09 Sep 2020 21:08:08 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96fb4a24465524a5f09969f9abc746d31c56c169a26136f95d49bf93136b9cc5`  
		Last Modified: Wed, 09 Sep 2020 21:08:16 GMT  
		Size: 49.8 MB (49777191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3d0fc9c1431aa06edd850ad06e87dfb68ecb153976dfee10bdb12678151f28`  
		Last Modified: Wed, 09 Sep 2020 21:08:07 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a134c677cecd2a2072dc6339c3ffdef30bea306fe825ef8a94e2f4804b9b08ba`  
		Last Modified: Wed, 09 Sep 2020 21:08:07 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1c2cb50cb177c8af6be57d72a66dd847a954c25dc951600ab53cb8837d1dfd`  
		Last Modified: Wed, 09 Sep 2020 21:08:07 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.17763.1457; amd64

```console
$ docker pull mongo@sha256:1540fa9478816905e891fb0b45d4cb7833da1e3cd35139c0cf30284b0b267455
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2400122912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72816220d9258d2c54504017ce5362ca07acc00d89a9996c959a109f307d6db8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Sep 2020 13:15:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Sep 2020 21:01:29 GMT
ENV MONGO_VERSION=4.4.0
# Wed, 09 Sep 2020 21:01:30 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-signed.msi
# Wed, 09 Sep 2020 21:01:30 GMT
ENV MONGO_DOWNLOAD_SHA256=ab326721c480dfafe0d0c3c1489c25e3a411b86e830dd91151b5ae24b8c9d508
# Wed, 09 Sep 2020 21:03:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Sep 2020 21:03:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Sep 2020 21:03:55 GMT
EXPOSE 27017
# Wed, 09 Sep 2020 21:03:56 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1df31adcc7026c3bf0cb32832a3f307dd6e1e54b8b3e050f8a73b5caee674d88`  
		Last Modified: Wed, 09 Sep 2020 16:48:51 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f75e375cc3906c6c2fcd4e09b37db7da09c0b7fc8011986378add21a7489750`  
		Last Modified: Wed, 09 Sep 2020 21:08:34 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43f9a55e93987b1f6b9f5cf0d87acf4a7d7f8a2f1c3d9c70bdbfb43399f13d1`  
		Last Modified: Wed, 09 Sep 2020 21:08:34 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848c3143cf33c0d1d2240bdd7312d7ae41e0481e52515e4aa58e36972fcc14a6`  
		Last Modified: Wed, 09 Sep 2020 21:08:31 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8672d7ab0664cbfb6b7cea5b291c9addfa7c70b2553900ad662892339e9ba7`  
		Last Modified: Wed, 09 Sep 2020 21:08:40 GMT  
		Size: 48.8 MB (48842756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c917a6e86e1f8d11999c60733c64e9c06c617075af5fb02684688b6f12c18a7`  
		Last Modified: Wed, 09 Sep 2020 21:08:31 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4baa8fe6d87ab0d3b911c59d2acfb3fa6a2cbd31f7ad022c5489dea6b44ad70e`  
		Last Modified: Wed, 09 Sep 2020 21:08:31 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accf01560933a0cbe604f3bdb69ae411e99e9655ef0cca6ec0ad6c938953f93f`  
		Last Modified: Wed, 09 Sep 2020 21:08:31 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
