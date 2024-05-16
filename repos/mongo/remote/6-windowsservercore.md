## `mongo:6-windowsservercore`

```console
$ docker pull mongo@sha256:9e7c0bbd4f7c222518e999cab2c3fc50919dacb835a842a634eb0ffc4b03fa62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `mongo:6-windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull mongo@sha256:282c34816f1a4b875d54fea3dc482efb90d89f9e567ceae2f6cf9abd6a0329d5
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2630067224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae439e9baa684dc56453edfb856a69b1c3a0c7feb345d8d310696febfea1e01`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 21:58:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:58:27 GMT
ENV MONGO_VERSION=6.0.15
# Wed, 15 May 2024 21:58:27 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.15-signed.msi
# Wed, 15 May 2024 21:58:28 GMT
ENV MONGO_DOWNLOAD_SHA256=a59408edea70438c1c9793ecdbc8b2111e44f10dd90f1ed0d2cc8071ae1cc95f
# Wed, 15 May 2024 21:59:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:59:47 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 May 2024 21:59:48 GMT
EXPOSE 27017
# Wed, 15 May 2024 21:59:50 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406610d468c382954868f174165421e798c719ed8c17957b964e45418a71995b`  
		Last Modified: Wed, 15 May 2024 21:59:56 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f63d871c941daa209aa42bb8a87a228d50d55b5082654caebf390f005d73c73`  
		Last Modified: Wed, 15 May 2024 21:59:56 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2002b2b191cec4aa2e89ffc2ef1a34212325a9b6001371909574fe58a20f744c`  
		Last Modified: Wed, 15 May 2024 21:59:56 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840724dd5f8e56e2ebd84d0dd68d5d8313f213554f40665010eb0190b8e22123`  
		Last Modified: Wed, 15 May 2024 21:59:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6532a705ccefd9db7183989df239b666f4b2870997a7a1d231b99746e72912d6`  
		Last Modified: Wed, 15 May 2024 22:00:39 GMT  
		Size: 517.4 MB (517386836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf6ffeb9161d2e7e692357d5e3bd24ab7f6456b352ac7a3424175a6e54ef43c`  
		Last Modified: Wed, 15 May 2024 21:59:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9690f94cb44098c1083d7fe1f95a917537d0025ccd239a9b6f3c978a085e6120`  
		Last Modified: Wed, 15 May 2024 21:59:54 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2680ef5f2626ebcaf7cc9a083e0e3982c590383835c1f3703bc314c73ddbfdf`  
		Last Modified: Wed, 15 May 2024 21:59:54 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull mongo@sha256:e1aedc4b4b66a8f5486caf2986f93c46a61909ddb17997b856c5f85eb0d6adbe
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2697258923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2afee8d064c4dc5403f1bb663aad5d5d5c0891e3b0855cbbda78850fd0cd0040`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:51:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:51:23 GMT
ENV MONGO_VERSION=6.0.15
# Wed, 15 May 2024 21:51:24 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.15-signed.msi
# Wed, 15 May 2024 21:51:25 GMT
ENV MONGO_DOWNLOAD_SHA256=a59408edea70438c1c9793ecdbc8b2111e44f10dd90f1ed0d2cc8071ae1cc95f
# Wed, 15 May 2024 21:55:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:55:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 May 2024 21:55:15 GMT
EXPOSE 27017
# Wed, 15 May 2024 21:55:16 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a43f289e45cae9c2a639863a925bb3e72e1f7c48bf3b7f082279a9299920704`  
		Last Modified: Wed, 15 May 2024 21:55:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9ccf7dfeead859f80254554a9e2a28671949a4a4a0c928251ffdb89580796f`  
		Last Modified: Wed, 15 May 2024 21:55:19 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fadddf4c090cbc62fd9e73c66d11381b691500acab30c332ff735458312c555d`  
		Last Modified: Wed, 15 May 2024 21:55:19 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a77607d27ae7f60996783a65200413eb3bf0a5db0e4b8943506fdc0d925a5a`  
		Last Modified: Wed, 15 May 2024 21:55:18 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7522f95b73005bde8b1ccea1d2062b3f7bf4106e35cfee50c97df48c242b72d5`  
		Last Modified: Wed, 15 May 2024 21:56:00 GMT  
		Size: 517.5 MB (517538428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4197358dce1e0a82c9785ae5a5db6236a39a1646f673413502052ec10237a4`  
		Last Modified: Wed, 15 May 2024 21:55:18 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2f11d3fc4df19c07bf7937c470c29f16ca7da2a52299b00e4c6b3b2bb0ffb2`  
		Last Modified: Wed, 15 May 2024 21:55:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bef4eac271bdf6203e5f79af1c33f1edde0c0eb8eb6840432449cec7d09585b`  
		Last Modified: Wed, 15 May 2024 21:55:18 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
