## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:c310176382896f4a10beb26fbcfdd25844d3ce06c0267a7a470b1f4f7e60576e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64
	-	windows version 10.0.17134.1184; amd64

### `mongo:windowsservercore` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:37ed0ce402c453d82362c8674a95a84ccdc02c9864bfa4fc8170d49d42584a92
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816058219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb916a127f9cd60ef9757a818d2c965590bd5303ed4476b1c5a8445ac0b6e2a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:35:26 GMT
ENV MONGO_VERSION=4.2.1
# Wed, 11 Dec 2019 23:35:27 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.1-signed.msi
# Wed, 11 Dec 2019 23:35:28 GMT
ENV MONGO_DOWNLOAD_SHA256=0bd9f5361d21cf358156e8e18aae3f4bc0298e9949b4b988c4b15b52913f91d6
# Wed, 11 Dec 2019 23:44:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:44:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:44:50 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:44:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c30838129c9ab8ebc7cfc1437e4655ad2fcbf99b7c2a4f618f0dadeb02ee9b1`  
		Last Modified: Thu, 12 Dec 2019 00:08:43 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e12474c86cd0cf6cec9ffc98ee72da8f5c5ef236665b487ed4590f3083cb5d`  
		Last Modified: Thu, 12 Dec 2019 00:08:43 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de05e906a577fa8f95e8df9641ed2d7b042e8ab039218c711f9be88e153f43c4`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0735cfc26b92c99aa40bf6c1feb6c344f5d7113c006c50441f5304fe92fd8285`  
		Last Modified: Thu, 12 Dec 2019 00:09:03 GMT  
		Size: 93.3 MB (93345990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77636ccac26ca06e73af52744671d5c6ae3db8960b110a60b0e95ed0231a9619`  
		Last Modified: Thu, 12 Dec 2019 00:08:41 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e83b06286df83053a894432b81bf6c78acc9a1000308697438915c8072f4210`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262bd20abcdfdee728fa18bff25d7071edeb206e56c11f9b4a4080018ca2db1f`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.17134.1184; amd64

```console
$ docker pull mongo@sha256:672798fb05567fe529909cf3f81422c76d5fe1a2bdbd1974abd9aa238b639f36
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2809636910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def4de6e07cdaff0556a068451bdd6043d77ee91d167288d24f922343dab649d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 15:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:45:17 GMT
ENV MONGO_VERSION=4.2.1
# Wed, 11 Dec 2019 23:45:19 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.1-signed.msi
# Wed, 11 Dec 2019 23:45:20 GMT
ENV MONGO_DOWNLOAD_SHA256=0bd9f5361d21cf358156e8e18aae3f4bc0298e9949b4b988c4b15b52913f91d6
# Thu, 12 Dec 2019 00:03:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 12 Dec 2019 00:03:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 12 Dec 2019 00:03:18 GMT
EXPOSE 27017
# Thu, 12 Dec 2019 00:03:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:70c803815d644f3772896add8df055dfd33f5934921ca0c57efc290d42454abf`  
		Last Modified: Wed, 11 Dec 2019 18:00:43 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cbbbce208b5a8e143d43012de06b33cd12dc212fae3e3f6cf28b1acd900861`  
		Last Modified: Thu, 12 Dec 2019 00:09:45 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f72bd77f828256b25eb7375c46fdec577565bc53d89a05fa8a100796450f599`  
		Last Modified: Thu, 12 Dec 2019 00:09:45 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d00e37fa3cf44154da5932563d6cfcff58333ffd56b34c2933a9b14f273b96`  
		Last Modified: Thu, 12 Dec 2019 00:09:42 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5c13eeee73b3c63164fa7984e8859a050bb173cb69c2b162e7d93845778b5f`  
		Last Modified: Thu, 12 Dec 2019 00:10:40 GMT  
		Size: 453.1 MB (453066744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de21f5bd53ce10a88ff8e77419719b9a2283c1a3f88706ebc56116df5d13e82e`  
		Last Modified: Thu, 12 Dec 2019 00:09:42 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aecef79094cae66ab1003365b8a64bce825e973f8fc6fdaac26462fb31363a15`  
		Last Modified: Thu, 12 Dec 2019 00:09:43 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1b6171741d09ad84e50e1a007624e0807534f6adc039d848e5915d26bcdfa9`  
		Last Modified: Thu, 12 Dec 2019 00:09:43 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
