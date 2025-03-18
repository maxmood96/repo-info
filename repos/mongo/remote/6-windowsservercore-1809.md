## `mongo:6-windowsservercore-1809`

```console
$ docker pull mongo@sha256:5574d839f244352d108f81c6eb0d17c7f6c32ec0ddf3b097dc022ae593c9422e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `mongo:6-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull mongo@sha256:7a4b2109e427d364335475da093c6022274bb6a65f1cfcf17877fcc62f77242e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2678803838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4c0918261b5e253a7d081bb6b6016d13d7ba4c784cd95c4b484f56f217a93b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 18 Mar 2025 17:21:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 18 Mar 2025 17:21:16 GMT
ENV MONGO_VERSION=6.0.21
# Tue, 18 Mar 2025 17:21:17 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.21-signed.msi
# Tue, 18 Mar 2025 17:21:18 GMT
ENV MONGO_DOWNLOAD_SHA256=5bf510cf298083b313149ba7ee98fae10c4300513967b090ec14048b6515c0d8
# Tue, 18 Mar 2025 17:22:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:22:33 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 18 Mar 2025 17:22:34 GMT
EXPOSE 27017
# Tue, 18 Mar 2025 17:22:34 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4c8c72bc9f7038a4da130fab85e09924f89e4d9fe56e7f28ce909821bfafbe`  
		Last Modified: Tue, 18 Mar 2025 17:22:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974090de8ddc4c2dd0e4245d08d53d5298ba46f7e3e706f845bdb8daea0990bb`  
		Last Modified: Tue, 18 Mar 2025 17:22:41 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac787c2770273d13630dae74d94654d52f43a878fbd94a55899c33e458670c96`  
		Last Modified: Tue, 18 Mar 2025 17:22:41 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df83b9a57b058a26ccbb6ff740c894d878ca06b8bfa647b955340b3595971e66`  
		Last Modified: Tue, 18 Mar 2025 17:22:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88cc30e88fb47c32a01af3071ff859cc8cd4c7030c21c540a9466d6d61c9fc3`  
		Last Modified: Tue, 18 Mar 2025 17:23:28 GMT  
		Size: 527.2 MB (527160100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c378cedcec8016649c3cbafcd887ee711626e13b5584097c297167d28ac8fc`  
		Last Modified: Tue, 18 Mar 2025 17:22:39 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d11aeb7992a6adbd8af61bb06888d5b09cdabf0b12a858aa02af08453a16e9`  
		Last Modified: Tue, 18 Mar 2025 17:22:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9414e840c1999744173c2e33b7f361f1baefc158e96e57d4416540407e6c07b8`  
		Last Modified: Tue, 18 Mar 2025 17:22:39 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
