## `mongo:7-windowsservercore`

```console
$ docker pull mongo@sha256:f202c105f9b6e1731c7fad2f1a54f65d68f3d8345879dac8923ed6fffde2f85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `mongo:7-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull mongo@sha256:4054be1e07320915a9d1e55e6ad3e2e1457daf65d8d0b9f674bfb89f5fd686fe
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3521225129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3474599f0612e334e14ab78e4808a3b4ab00f9f973f5e7aacf0b00a6b47d6f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Mon, 24 Mar 2025 21:24:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 24 Mar 2025 21:24:49 GMT
ENV MONGO_VERSION=7.0.18
# Mon, 24 Mar 2025 21:24:51 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.18-signed.msi
# Mon, 24 Mar 2025 21:24:53 GMT
ENV MONGO_DOWNLOAD_SHA256=ab23d0e0488dd0b9ab07bae73e481271c7574e212b4bb61b1331400a3cffb02b
# Mon, 24 Mar 2025 21:26:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 24 Mar 2025 21:26:15 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Mar 2025 21:26:16 GMT
EXPOSE 27017
# Mon, 24 Mar 2025 21:26:18 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1264a2afaaee0aecfe16410df279122e842deea44a98b0bba467b6ed8f3d04`  
		Last Modified: Mon, 24 Mar 2025 21:26:24 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad1207ab1efa6ad34b5e05d3992f131f37091e5ae9e652e39bd5369e6ead9f1`  
		Last Modified: Mon, 24 Mar 2025 21:26:24 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9d584c67ceb35a75eb5fbca3b2ae3485972e9dd2e076fb4e106f3e26db96b4`  
		Last Modified: Mon, 24 Mar 2025 21:26:24 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a473a9acdeab6ff643132f35f41ac2e0fc6f6dea441e07686e556e92d2a34b3e`  
		Last Modified: Mon, 24 Mar 2025 21:26:22 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecbd17f558b999002871012f5374fb902d581dd2513d9cbb803b14677f2f2be`  
		Last Modified: Mon, 24 Mar 2025 21:27:21 GMT  
		Size: 612.6 MB (612568274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c991540a41ba4471ac148f5da1d88a79f56219c87d9f23ef00abf9b8290ea006`  
		Last Modified: Mon, 24 Mar 2025 21:26:22 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5795aec4ed3c0afcb91e3f306d6c587828053739b1bc7442c3b405500477453`  
		Last Modified: Mon, 24 Mar 2025 21:26:22 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ebfba7673af9fbcf8efe636804df3dcec1ad076352102446ba62e6bcf22ede`  
		Last Modified: Mon, 24 Mar 2025 21:26:22 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull mongo@sha256:fa39059e5f017c6c10a853a6fda64e0d778e0b408940afa0d50a06b9db5fe852
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2882474844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad419674ed9bbb09772811dac8de8280e10002c3a0abd10b1bf91ef85c144f0`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Mon, 24 Mar 2025 21:22:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 24 Mar 2025 21:22:15 GMT
ENV MONGO_VERSION=7.0.18
# Mon, 24 Mar 2025 21:22:15 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.18-signed.msi
# Mon, 24 Mar 2025 21:22:16 GMT
ENV MONGO_DOWNLOAD_SHA256=ab23d0e0488dd0b9ab07bae73e481271c7574e212b4bb61b1331400a3cffb02b
# Mon, 24 Mar 2025 21:23:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 24 Mar 2025 21:23:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Mar 2025 21:23:26 GMT
EXPOSE 27017
# Mon, 24 Mar 2025 21:23:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ed38093e05f979f562bae99f8f5fd888cd7f140de1e0137a6f904d4ecf707b`  
		Last Modified: Mon, 24 Mar 2025 21:23:33 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c5645aeb8ae9d4e142942cb0d02b2a9b134ffcb24bc959c6eecc553c663012`  
		Last Modified: Mon, 24 Mar 2025 21:23:33 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b157681df2d34907aa515c04095eddd667deeeb58a5f31f599634e8d81ae8e67`  
		Last Modified: Mon, 24 Mar 2025 21:23:33 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07f621f45673f27424df8db9b86fc52d3d76bc7e98b0366fe647a2b86dee1d0`  
		Last Modified: Mon, 24 Mar 2025 21:23:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ff6448284b2012c009dfc958847177cd69558dac577ad743fbf6bc07619e9d`  
		Last Modified: Mon, 24 Mar 2025 21:24:21 GMT  
		Size: 612.5 MB (612524695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff51bd16c74c7da607ab0c40b01569a657c999a5ae6c9480e18ef997135b3cb1`  
		Last Modified: Mon, 24 Mar 2025 21:23:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858b7ced5bda43382167d2744c85fd8a5686f6187f2da67276ebcb23d5140214`  
		Last Modified: Mon, 24 Mar 2025 21:23:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024207ef982c7c0df1fe5ece519c2f7730de92a5fe1160f74c5c26343481cd15`  
		Last Modified: Mon, 24 Mar 2025 21:23:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull mongo@sha256:9e095463e374403aba50b0b1f63b5ed0fb2541f1dde9bbcf7c8dcffd89fd5922
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2764175067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e171ea197d05bea409244dcf1937d22767e894b6e69e51d50998be61c0ac5a5`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Mon, 24 Mar 2025 21:31:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 24 Mar 2025 21:31:03 GMT
ENV MONGO_VERSION=7.0.18
# Mon, 24 Mar 2025 21:31:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.18-signed.msi
# Mon, 24 Mar 2025 21:31:04 GMT
ENV MONGO_DOWNLOAD_SHA256=ab23d0e0488dd0b9ab07bae73e481271c7574e212b4bb61b1331400a3cffb02b
# Mon, 24 Mar 2025 21:33:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 24 Mar 2025 21:33:20 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Mar 2025 21:33:21 GMT
EXPOSE 27017
# Mon, 24 Mar 2025 21:33:21 GMT
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
	-	`sha256:240e9dcb3006ed260466158db8e510515c9ba4e95180a02d68aa4e6b7505388f`  
		Last Modified: Mon, 24 Mar 2025 21:33:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047d684a0bed35dccee61f4d38dca84de10113a2f314368770fb01d710cbe8a5`  
		Last Modified: Mon, 24 Mar 2025 21:33:25 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fa3a0fe1ced80f45ffbbbe587fa5d559899d1dfa86c02f57a60789cd949ab7`  
		Last Modified: Mon, 24 Mar 2025 21:33:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7eb85399b837c52d1341eeef3c1d29f5be9b41c8918906972362d5d3bff1345`  
		Last Modified: Mon, 24 Mar 2025 21:33:24 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4aed65f3211a9d41e48ef673947826780a907250167be0ffeabaaf7a7f74068`  
		Last Modified: Mon, 24 Mar 2025 21:34:14 GMT  
		Size: 612.5 MB (612531310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a75c28327ffee8f81ee2bb5af3034542f5d22dda728562bab14c8b0b61dde17`  
		Last Modified: Mon, 24 Mar 2025 21:33:24 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42840b53dc4c948248e44690a1c2eae0cae81fb3c468ce970d88d9843d4cac5b`  
		Last Modified: Mon, 24 Mar 2025 21:33:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23991716f7a656a7db3e48c916e387d96b839d97538741317d74559edc8f6ad`  
		Last Modified: Mon, 24 Mar 2025 21:33:24 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
