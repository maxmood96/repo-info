## `mongo:3-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:9e2f204b7bcbbf47771fc967acbc876059a2f629325f3ca14ca7ecc3932d3a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3930; amd64

### `mongo:3-windowsservercore-ltsc2016` - windows version 10.0.14393.3930; amd64

```console
$ docker pull mongo@sha256:912c28626ca278864ed31cada2e9697bc01e7d665b404afdac85b07531b646a2
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5831709507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5027008de96ac2601d20dd0db3b06efda7fac0af30487ef771ea1e1b53b0b1f3`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 01 Sep 2020 19:14:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Sep 2020 13:23:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Sep 2020 20:38:23 GMT
ENV MONGO_VERSION=3.6.19
# Wed, 09 Sep 2020 20:38:23 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.19-signed.msi
# Wed, 09 Sep 2020 20:38:24 GMT
ENV MONGO_DOWNLOAD_SHA256=4375a8fa0d87dd0b16ab40a20487ddb5870d6f056d42ef654debf3e7fab6ae40
# Wed, 09 Sep 2020 20:41:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Sep 2020 20:41:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Sep 2020 20:41:25 GMT
EXPOSE 27017
# Wed, 09 Sep 2020 20:41:26 GMT
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
	-	`sha256:a978721fa010ac9a32ed265f4f4741f0ed2f4b33705c4b7f6b04a252e855f1ab`  
		Last Modified: Wed, 09 Sep 2020 21:05:11 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee72aced194911cf459b6c847db2752917a452301285360bf24b07c92ce5370`  
		Last Modified: Wed, 09 Sep 2020 21:05:11 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91d6b3ad4b814837d7b6badb22247dcf546aa2bb34b45ca5e6774d696bae540`  
		Last Modified: Wed, 09 Sep 2020 21:05:08 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306da4882447b21efa56c66e49c00f44017e5053a352b91f25a31e97dbfedc26`  
		Last Modified: Wed, 09 Sep 2020 21:05:27 GMT  
		Size: 92.4 MB (92447106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1846b69ee2c5b4e604aced82fc1ad22e73b4f666c172f75163578308c44e89f2`  
		Last Modified: Wed, 09 Sep 2020 21:05:09 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2daa82c02b6f1a9c9b7e6dd9b7bc9668e5bf38e24767f9d77445a86d76af595`  
		Last Modified: Wed, 09 Sep 2020 21:05:09 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842f76cd30b4fb83cdb60b7d65823791341813064a2602c0561bd8aed25848ac`  
		Last Modified: Wed, 09 Sep 2020 21:05:08 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
