## `mongo:7-windowsservercore`

```console
$ docker pull mongo@sha256:0ba8824c3a1ecbdaa6be817ff7eeeb772b9b382a21d3c06d11c5ecf8af588c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `mongo:7-windowsservercore` - windows version 10.0.20348.2582; amd64

```console
$ docker pull mongo@sha256:38c7a63ec667009a653800c4236c18bf63e823296a1584ef2d5ae2fbe989b090
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2748412507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbacb63a51c95a192fb04bb2bb128a6744fb7579c4fd94afc6ce0e04ccda1f6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Wed, 10 Jul 2024 17:10:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jul 2024 17:10:21 GMT
ENV MONGO_VERSION=7.0.12
# Wed, 10 Jul 2024 17:10:22 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.12-signed.msi
# Wed, 10 Jul 2024 17:10:22 GMT
ENV MONGO_DOWNLOAD_SHA256=314f1b988490d46c9831cbf7ad7669a949507df17cc0674f7bdac47de74281b1
# Wed, 10 Jul 2024 17:11:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jul 2024 17:11:37 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jul 2024 17:11:37 GMT
EXPOSE 27017
# Wed, 10 Jul 2024 17:11:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b66442b3774eda8a4f58abec1b96076891645fb3038ea9d89daca32775055d`  
		Last Modified: Wed, 10 Jul 2024 17:11:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e56a5cedc2fbbb8940908b91f2ac46ced5ebf56daf310693f66c0a118558b3`  
		Last Modified: Wed, 10 Jul 2024 17:11:42 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f64cb73e6f9d624a6c369b9e80f257920f458f5132d67c8b7a4b0123446c5c`  
		Last Modified: Wed, 10 Jul 2024 17:11:42 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68eba4583870fe2acf4d322b8c4f1c0b5981404db0a5e8dcf9ed6cfc3b1c5663`  
		Last Modified: Wed, 10 Jul 2024 17:11:41 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e47b9d2a7afd0e59c8d22d15658342ebed4084b3539b68053166fa4c9a8e0ff`  
		Last Modified: Wed, 10 Jul 2024 17:12:29 GMT  
		Size: 608.8 MB (608803184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7f9490ad4220a722ca210008ab6c42010cdc317c329112c2bf87f2671ab279`  
		Last Modified: Wed, 10 Jul 2024 17:11:41 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4515bf5a753aab326e358986c70a89ac6df24c298ebcef0737b93e1beb9748a`  
		Last Modified: Wed, 10 Jul 2024 17:11:41 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4ec846f9ab8b406697f538845d4707f3aa5f61a2ce7c66483adeebdaf199de`  
		Last Modified: Wed, 10 Jul 2024 17:11:41 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull mongo@sha256:614707668546f6b736afe7377dda1bcc8a8dc4ba524a50db986357f43a1d0c4b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2847393267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01faa765f580a630352484ecf01a287996921c548874e595e826d4ad7bce466b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 17:10:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jul 2024 17:10:53 GMT
ENV MONGO_VERSION=7.0.12
# Wed, 10 Jul 2024 17:10:53 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.12-signed.msi
# Wed, 10 Jul 2024 17:10:54 GMT
ENV MONGO_DOWNLOAD_SHA256=314f1b988490d46c9831cbf7ad7669a949507df17cc0674f7bdac47de74281b1
# Wed, 10 Jul 2024 17:12:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jul 2024 17:12:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jul 2024 17:12:48 GMT
EXPOSE 27017
# Wed, 10 Jul 2024 17:12:49 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679fff9013457a49c59f60ed074913e606f3b8e91cdb632d23509fa19f5820f9`  
		Last Modified: Wed, 10 Jul 2024 17:12:54 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f95717cfc7ffa5ef17a8ef15d298df35aed40df2f6140338c9f8310b163627`  
		Last Modified: Wed, 10 Jul 2024 17:12:54 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4014c6d08f4c34ab5a7f93181033b27dc292d152b49b99569d8391a4020cdacf`  
		Last Modified: Wed, 10 Jul 2024 17:12:54 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b3e1ea7aa52b8a19d60a7f949f6b5f584f9b03bb678eee558495e610ab14e3`  
		Last Modified: Wed, 10 Jul 2024 17:12:52 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd30bc4eda1a335b13a1746230b939de48fc7a8509fa126b5d0d6333e8b9a8b`  
		Last Modified: Wed, 10 Jul 2024 17:13:42 GMT  
		Size: 609.0 MB (608954821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5214033fa0a9bf0f69f1a9214cfe1f6b79df8a3b372bd505db9bcd1539a3defa`  
		Last Modified: Wed, 10 Jul 2024 17:12:53 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ceff4dc281b5159b85bca9b9dcbf5423f621f0950e56940d86d44a11b76f3f`  
		Last Modified: Wed, 10 Jul 2024 17:12:53 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78cc9acbcec203557af3a3a507f45f16549754ad33676198ef0ba7dc4bee494f`  
		Last Modified: Wed, 10 Jul 2024 17:12:53 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
