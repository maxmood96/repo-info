## `mongo:7-windowsservercore`

```console
$ docker pull mongo@sha256:0ea068841bfec866db6dc0622ee61ac457f5602f1bdf986601ad05424ffc6f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `mongo:7-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull mongo@sha256:d1ef963c403237a0c234d0b48455996fba557410820f652106149a2c0a9ac0a1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408996088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fca3dfcb5ff7d9e144329acee150ad804bcd89964745f1d6c814475ae42d9f6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Wed, 09 Oct 2024 23:00:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Oct 2024 23:00:29 GMT
ENV MONGO_VERSION=7.0.14
# Wed, 09 Oct 2024 23:00:30 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.14-signed.msi
# Wed, 09 Oct 2024 23:00:30 GMT
ENV MONGO_DOWNLOAD_SHA256=2471a7919223aee2f14443a31c7a1cbfb14c5149b8ecaea05710286731908499
# Wed, 09 Oct 2024 23:01:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:01:38 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Oct 2024 23:01:39 GMT
EXPOSE 27017
# Wed, 09 Oct 2024 23:01:40 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8f18311de3f8fc948a3bef60df369410ccb4dde8d43569278d756fff4ccafd`  
		Last Modified: Wed, 09 Oct 2024 23:01:45 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5fae38c9915328c3f53ef15e27b0e8c666e605095b24246e5c89536081d41e`  
		Last Modified: Wed, 09 Oct 2024 23:01:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae13ac7d954eb24abe7c1c69254e0e4bc0e6ca02b52122a66e4d10e15f930b0`  
		Last Modified: Wed, 09 Oct 2024 23:01:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3181a1796d225aa9cc37130144ca3a8b6c2ee1d69f93828aa5e7cb58ab6edf06`  
		Last Modified: Wed, 09 Oct 2024 23:01:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7777c4f5793683abbaec66b3facafac5d0dc8e2545ec2054d67417597fb04ca1`  
		Last Modified: Wed, 09 Oct 2024 23:02:33 GMT  
		Size: 609.6 MB (609645552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72497cc0000f0d1ba6768f313f00bb5fd9286b54f1efd371f3b9712ffe4a570`  
		Last Modified: Wed, 09 Oct 2024 23:01:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d061630cd308f73c9df009832bfa00996217c6c298318d6a2e03b7c9268d9400`  
		Last Modified: Wed, 09 Oct 2024 23:01:44 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76157ed6840230797877284e5d9bcb69f9add8aaec93f253b9daa2d23f4cb394`  
		Last Modified: Wed, 09 Oct 2024 23:01:44 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull mongo@sha256:31f5e58515b8413ee5d5cefdee230e58b9c78afe65e1d6ac22eb51b34ed72ccc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2511492785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98e3c36139131441a7af03535aaefd64079771389967b4babdaf92e12176674`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Wed, 09 Oct 2024 23:08:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Oct 2024 23:08:42 GMT
ENV MONGO_VERSION=7.0.14
# Wed, 09 Oct 2024 23:08:43 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.14-signed.msi
# Wed, 09 Oct 2024 23:08:45 GMT
ENV MONGO_DOWNLOAD_SHA256=2471a7919223aee2f14443a31c7a1cbfb14c5149b8ecaea05710286731908499
# Wed, 09 Oct 2024 23:11:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:11:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Oct 2024 23:11:08 GMT
EXPOSE 27017
# Wed, 09 Oct 2024 23:11:09 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c939059098033d5725d57b7815f715f0fc665d6a5c67d904a518ccbd231554`  
		Last Modified: Wed, 09 Oct 2024 23:11:12 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9be0808cede504fdbb3b0677537023b99b996b8aa8b728dd6ae923bfcc56775`  
		Last Modified: Wed, 09 Oct 2024 23:11:12 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39dae233b9dec8c9aa472100a8436f12435a7835d7017d1a87d53cdedb9f1e2`  
		Last Modified: Wed, 09 Oct 2024 23:11:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1794cb2e9960ba2f42373246684b8663bbb0885f2c2623b225ee0995e1afd88e`  
		Last Modified: Wed, 09 Oct 2024 23:11:11 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e226e5a96b13f7bc0ee340c514a8e0a9e59c4161d10a282868e0ee6c78f81d`  
		Last Modified: Wed, 09 Oct 2024 23:11:59 GMT  
		Size: 609.7 MB (609658454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffe719d398d14b3fbc25dcf5a2a322913b351612322a0181546fb81d6076112`  
		Last Modified: Wed, 09 Oct 2024 23:11:11 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b4ef8d72ef87315573617e01a3f322c115568588c1b0abeee397447cd32dfe`  
		Last Modified: Wed, 09 Oct 2024 23:11:11 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5203781adee9d7948312b018ca6d39ec65571cb5175cf9ab6533bf65a26471b3`  
		Last Modified: Wed, 09 Oct 2024 23:11:11 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
