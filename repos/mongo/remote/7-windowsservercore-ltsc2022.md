## `mongo:7-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:4502000ec59ba30253944108968f8639ce70331c754c3f718a2c1eccb9d82c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `mongo:7-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

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
