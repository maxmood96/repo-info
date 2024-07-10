## `mongo:7-windowsservercore-1809`

```console
$ docker pull mongo@sha256:c9bb3dc0e222c80d2a3912ee0d913197a258ab18e996c1908a753c1c8387081e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `mongo:7-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

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
