## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:e2ba03a0ded072e64dec1f73bda2afdd54124a1f7b2d984b72a59983504e2658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4046; amd64
	-	windows version 10.0.17763.1577; amd64

### `mongo:windowsservercore` - windows version 10.0.14393.4046; amd64

```console
$ docker pull mongo@sha256:bede630f222631f13ec728e62131df9dd00f5249abcef5b6eac088750387b178
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (6012776661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf2d748e44c86afa82cec0b65e5f5a608c9d06221aab479dc1ce10bf058a4f8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 14:26:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 21 Nov 2020 03:01:51 GMT
ENV MONGO_VERSION=4.4.2
# Sat, 21 Nov 2020 03:01:52 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.2-signed.msi
# Sat, 21 Nov 2020 03:01:52 GMT
ENV MONGO_DOWNLOAD_SHA256=84a1f6899e25f90a7d7c2b5996e9e15584a9af54c08832682c962c5794fcab0f
# Sat, 21 Nov 2020 03:21:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Sat, 21 Nov 2020 03:21:56 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 21 Nov 2020 03:21:57 GMT
EXPOSE 27017
# Sat, 21 Nov 2020 03:21:58 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9affba5fa493b09d48e6bd56c0d7b0eb03d1dbaa80493dd08cb18a3c9ddfbb67`  
		Last Modified: Wed, 11 Nov 2020 16:54:10 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8899801562529bd7d1e99f303b69c808ec312960d537270d7bb85354bda028`  
		Last Modified: Sat, 21 Nov 2020 03:47:03 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66351985b011184c0d76b4841b8aaa8c8bf549c5966c8d741ca0c09500cdd64f`  
		Last Modified: Sat, 21 Nov 2020 03:47:03 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76ba79a84c29405fbb8a0589a57c1d083b1f4ee022901c5864ea5c12585f583`  
		Last Modified: Sat, 21 Nov 2020 03:47:00 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf24eb2afd97deff3ee453c30badbbd849ade1c7c0086bd9e8806184ae1ce12`  
		Last Modified: Sat, 21 Nov 2020 03:47:47 GMT  
		Size: 242.2 MB (242209931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f28ded29624d1edbf9a1ff8f448b45d60d675742554650c1240ea15edbb840e`  
		Last Modified: Sat, 21 Nov 2020 03:47:00 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8dbdd136bb6499d7ef60a130937a1cb46f90f0eb5a139ed6bc7b26f9f9ce51`  
		Last Modified: Sat, 21 Nov 2020 03:47:00 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9482967e566fff56f5acfc8c03f685fd06a0a5c5add8f7325e5f149ba1a03f`  
		Last Modified: Sat, 21 Nov 2020 03:47:00 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.17763.1577; amd64

```console
$ docker pull mongo@sha256:4e5cbd3b99278c48b87832a3fead62a308ce24dd4d2c06303f0a00490431abb7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2629330010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0dc696cbf082f856a3388c8361ec630b64eb73206d3a9dccf95470546cf5d7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 14:18:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 21 Nov 2020 03:22:10 GMT
ENV MONGO_VERSION=4.4.2
# Sat, 21 Nov 2020 03:22:11 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.2-signed.msi
# Sat, 21 Nov 2020 03:22:11 GMT
ENV MONGO_DOWNLOAD_SHA256=84a1f6899e25f90a7d7c2b5996e9e15584a9af54c08832682c962c5794fcab0f
# Sat, 21 Nov 2020 03:42:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Sat, 21 Nov 2020 03:42:23 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 21 Nov 2020 03:42:24 GMT
EXPOSE 27017
# Sat, 21 Nov 2020 03:42:25 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e03cd29396986910a2aaaf968e93bebcaf4b0101821290e0560b401893615ccf`  
		Last Modified: Wed, 11 Nov 2020 16:53:20 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3efd0b7437f777e1ad1061483921407eae0e20b57bb0d81a5377a803869052c`  
		Last Modified: Sat, 21 Nov 2020 03:48:08 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d1f55e6b3c91a212d571380392df1d66cf9232f534021ecf9007dcadce15cf`  
		Last Modified: Sat, 21 Nov 2020 03:48:08 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b00f992f497c63e4f5ada847ebf6439034a06c4cda82735b3baf7acfed84eea`  
		Last Modified: Sat, 21 Nov 2020 03:48:04 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1802e4b7ae6421ee510c45fc7927b8f78c752a198ec643a8da6ffb222a8aca6`  
		Last Modified: Sat, 21 Nov 2020 03:48:51 GMT  
		Size: 241.3 MB (241292780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2adedec6a7e9f6a86d8068a2f4ba1ec2720e3429fecbd41b24abd4693f4b70b6`  
		Last Modified: Sat, 21 Nov 2020 03:48:04 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30732b5b719f6d77f2d2d1522c5b968206622d21397238db0ccd7c268c445ea`  
		Last Modified: Sat, 21 Nov 2020 03:48:04 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c005019f01ac1fb34b3fef05d8ee2e306b8528e9119f61417bf5cac5c34e3d13`  
		Last Modified: Sat, 21 Nov 2020 03:48:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
