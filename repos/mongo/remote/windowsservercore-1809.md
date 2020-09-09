## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:5ec8bf83d9c8cee4174c9bec7a7f535f461eeec04715b89036d9685065a9618d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.1457; amd64

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
