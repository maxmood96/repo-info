## `mongo:4-windowsservercore`

```console
$ docker pull mongo@sha256:2ddee4a6bfd66479aabec6e2901b3e6c72106719124981bc0c21632fb8f5276b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `mongo:4-windowsservercore` - windows version 10.0.20348.1006; amd64

```console
$ docker pull mongo@sha256:b0522026946d88278209d43973e92466873adfd34dc2d7d6cace3d445bbc69fc
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2592457091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f96efedcbafa212064eda6631c7171fedc241fe91b340105a4d3e0367a92494`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 13:31:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 29 Sep 2022 20:31:15 GMT
ENV MONGO_VERSION=4.4.17
# Thu, 29 Sep 2022 20:31:16 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.17-signed.msi
# Thu, 29 Sep 2022 20:31:17 GMT
ENV MONGO_DOWNLOAD_SHA256=29aa0584c70c5c473f2a0a5d5bd90e38897c10de1d3e4bc0cefa28ae9a532a8b
# Thu, 29 Sep 2022 20:32:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 29 Sep 2022 20:32:45 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 29 Sep 2022 20:32:47 GMT
EXPOSE 27017
# Thu, 29 Sep 2022 20:32:48 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a16438b2cffe7980c606769d49003f7f1c4d27549445f824511a81834513616a`  
		Last Modified: Wed, 14 Sep 2022 18:58:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf727ecd221336f82a407cf4ba5e6cba04e9ebfd6ed0802f44a98201598a421`  
		Last Modified: Thu, 29 Sep 2022 20:51:41 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb4ebb92fbf4faab7b19875b63fca82cf7524d8e356557790cf8397a8136583`  
		Last Modified: Thu, 29 Sep 2022 20:51:41 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b54003d427f8f1ba5878e1c3e28ab50119fee8497b271d0551c473c2a65636a`  
		Last Modified: Thu, 29 Sep 2022 20:51:39 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b69f2c31772583bdd26e2404b27e5037fc0f011ecf3d41601ead13061ac385`  
		Last Modified: Thu, 29 Sep 2022 20:52:23 GMT  
		Size: 245.5 MB (245497589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f114d01b49c4e832cda8cc041ddb9ee6f40e34e1f136fca815696d55f9b944`  
		Last Modified: Thu, 29 Sep 2022 20:51:39 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27fde3bd1331bdc01c542ba413a87316c0b5327371a99a12709931308f7a3bb9`  
		Last Modified: Thu, 29 Sep 2022 20:51:39 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7c450a6cf48033f9299dc5556d7f2c2851bd1e52450716f008f194720116f4`  
		Last Modified: Thu, 29 Sep 2022 20:51:39 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-windowsservercore` - windows version 10.0.17763.3406; amd64

```console
$ docker pull mongo@sha256:804b32078cb84762f4c399afcfa8037ce23e648397a7df4868f9bc0da7481fd0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2948874698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41084db79a02dc5b232da3d3315c2c211a1b69107015c8033fbdb3f7895f70d5`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Wed, 14 Sep 2022 13:39:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 29 Sep 2022 20:32:57 GMT
ENV MONGO_VERSION=4.4.17
# Thu, 29 Sep 2022 20:32:58 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.17-signed.msi
# Thu, 29 Sep 2022 20:32:59 GMT
ENV MONGO_DOWNLOAD_SHA256=29aa0584c70c5c473f2a0a5d5bd90e38897c10de1d3e4bc0cefa28ae9a532a8b
# Thu, 29 Sep 2022 20:35:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 29 Sep 2022 20:35:15 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 29 Sep 2022 20:35:16 GMT
EXPOSE 27017
# Thu, 29 Sep 2022 20:35:17 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3c428406510f0a47ed60f28060a7d625d42344a95fdcb7c4f5746fb8857c3328`  
		Last Modified: Wed, 14 Sep 2022 15:42:13 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad280df959a17ad3f4890f21f84d22139a6a998618ce8f4536948227270148b`  
		Last Modified: Thu, 29 Sep 2022 20:52:39 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6336063c57211f06efbb801d27653f67f9a1ead7cf8a088226097089c1f4a2b`  
		Last Modified: Thu, 29 Sep 2022 20:52:39 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29499fcd1d90cfad7715eb42305ae6020c14ad0767904f9416715e44399500f6`  
		Last Modified: Thu, 29 Sep 2022 20:52:36 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e94233c4f1dc6a88ff975051aa38f1a67c3ffa5b50797f158699ab24f084387`  
		Last Modified: Thu, 29 Sep 2022 20:53:20 GMT  
		Size: 245.3 MB (245300046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bff789c0b10176e0f51cf37f4a709ead36613465215f7bdcc1c0ac1e8b7633`  
		Last Modified: Thu, 29 Sep 2022 20:52:36 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0ff227138c6df0b8008bae6eac03796731aeee2b524d3980392a9e35f6eb4b`  
		Last Modified: Thu, 29 Sep 2022 20:52:36 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa933956c55e9d82b796f54a2c1e3f1380eca0b4d1e9023de2dc23545d27e926`  
		Last Modified: Thu, 29 Sep 2022 20:52:36 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
