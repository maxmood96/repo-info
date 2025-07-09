## `mongo:7-windowsservercore`

```console
$ docker pull mongo@sha256:cc272534dda52d65c2d76fcca9be10a212b897e1a85847839d0ae0d65b35eed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4652; amd64
	-	windows version 10.0.20348.3932; amd64

### `mongo:7-windowsservercore` - windows version 10.0.26100.4652; amd64

```console
$ docker pull mongo@sha256:904c35e1372bf6198aadcf0ce04744ac8af2f85caeef78588872ffc45663b5d1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 GB (4107146426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7e5a05a177fa9de12949193977d1d92aa808e331b9c3206bef526f2e0d41a4`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Wed, 09 Jul 2025 19:00:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jul 2025 19:00:32 GMT
ENV MONGO_VERSION=7.0.21
# Wed, 09 Jul 2025 19:00:33 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.21-signed.msi
# Wed, 09 Jul 2025 19:00:34 GMT
ENV MONGO_DOWNLOAD_SHA256=35baeddf28f20f63a50d6a65bdb19492afdea42005bfb8621a8ec433ec9c748b
# Wed, 09 Jul 2025 19:02:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Jul 2025 19:02:02 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Jul 2025 19:02:04 GMT
EXPOSE 27017
# Wed, 09 Jul 2025 19:02:05 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275b3c7a57efffb771da2e3ed7b31700c4cdc75f927f7e010e1d69eefb5c35b4`  
		Last Modified: Wed, 09 Jul 2025 19:05:48 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f108477306775bfd4d9fe5359a00ceddcbeb1d281427bdb2a4b90acdf82f594f`  
		Last Modified: Wed, 09 Jul 2025 19:05:49 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5c1ff82bd40793bbfe02fff4f04a8c09a1c629353675271c11d03d84ba36f7`  
		Last Modified: Wed, 09 Jul 2025 19:05:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f737ac448158e40a9b31a72803512fa8c386bbd2b38ac36d81750091ba80d3e`  
		Last Modified: Wed, 09 Jul 2025 19:05:49 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b9abc5fd73cea4ff36292ca80d818aa8160ec68024ee017eca4066fa2aa7c9`  
		Last Modified: Wed, 09 Jul 2025 22:09:06 GMT  
		Size: 616.0 MB (615964015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523affde96ae6b86511abec9eb41b909a4bbfacf3824a4b1e73cb782ac7da282`  
		Last Modified: Wed, 09 Jul 2025 19:05:49 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0a8465b265a7d8a2c79ce54eebc49a43f50e6ee68fe2fd48d8e086a81ad394`  
		Last Modified: Wed, 09 Jul 2025 19:05:49 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a686036c304ce81127ee79cdb1fbdc758617c5f52ee733c9c43b28b14b5e52d`  
		Last Modified: Wed, 09 Jul 2025 19:05:49 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.20348.3932; amd64

```console
$ docker pull mongo@sha256:08ae0e9d6c292b76bbfdfbc90e7b531a239619fee0ea7189bc3d58252977a683
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2896535008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5486a0fb3e689e578c4a7e6f4ff5bfdb9b648872ac2ceaf6ff5c2ccfdbdccd71`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Wed, 09 Jul 2025 18:06:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jul 2025 18:06:58 GMT
ENV MONGO_VERSION=7.0.21
# Wed, 09 Jul 2025 18:06:59 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.21-signed.msi
# Wed, 09 Jul 2025 18:07:00 GMT
ENV MONGO_DOWNLOAD_SHA256=35baeddf28f20f63a50d6a65bdb19492afdea42005bfb8621a8ec433ec9c748b
# Wed, 09 Jul 2025 18:08:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Jul 2025 18:08:08 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Jul 2025 18:08:09 GMT
EXPOSE 27017
# Wed, 09 Jul 2025 18:08:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9189012eab36e49b6c9694af1c840a7323675c9d0e7d0b16636fb131fc78b8d`  
		Last Modified: Wed, 09 Jul 2025 19:08:33 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6896c3a8c13beee7d939c8ea35e7d00d85048589c051fad24f8cf7745b02ba`  
		Last Modified: Wed, 09 Jul 2025 19:08:33 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3437609dfef1183a1134dac710fffe97649a6693d0031160de2738a9311434`  
		Last Modified: Wed, 09 Jul 2025 19:08:34 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458ac62a829c04c824ad9dceb825c478b634f489317caf10dfa4ddb106cd2f0c`  
		Last Modified: Wed, 09 Jul 2025 19:08:34 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0481088208a26da054a2a0078222c6d082351a37ad5d83e9a194e4300a68aefd`  
		Last Modified: Wed, 09 Jul 2025 19:09:06 GMT  
		Size: 615.9 MB (615922469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8b9bb8b0d7322d266fb5abcc73c5bebbd62604dbcb31fd4439cac2db45b1e3`  
		Last Modified: Wed, 09 Jul 2025 19:08:35 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04440b4494a46043c56e6986185a42e4dea7438cf32c7059b1cd89f94f049857`  
		Last Modified: Wed, 09 Jul 2025 19:08:36 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b449852e1d01d1c1777862c638ee26135b132edecccdbdabaebac0b90358ad`  
		Last Modified: Wed, 09 Jul 2025 19:08:37 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
