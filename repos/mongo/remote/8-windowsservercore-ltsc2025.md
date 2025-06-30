## `mongo:8-windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:80a07317fe99e66a622246418978f2282fb229039ef3fc503101cdc3b827b2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `mongo:8-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull mongo@sha256:2703cf0993abc144663c20313e88b33cf4e9e860c1e6fa4a4809f9a0d22c5ba6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 GB (4251851313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a52abbc57440e30a1b35f20b12b3830930ba0a3273e2fb0b0099c7fd66e3b8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Mon, 30 Jun 2025 17:33:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 30 Jun 2025 17:33:13 GMT
ENV MONGO_VERSION=8.0.11
# Mon, 30 Jun 2025 17:33:14 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.11-signed.msi
# Mon, 30 Jun 2025 17:33:15 GMT
ENV MONGO_DOWNLOAD_SHA256=887b2869804fec5f7412f4d848ab6bc587819fb2ee1ab49e2fac1538ccc53a91
# Mon, 30 Jun 2025 17:34:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 30 Jun 2025 17:34:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 30 Jun 2025 17:34:53 GMT
EXPOSE 27017
# Mon, 30 Jun 2025 17:34:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f289ccf36d787faff6667c77f87af5179c559808ee0632a728adf03d3454e4`  
		Last Modified: Mon, 30 Jun 2025 17:38:31 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd1fe1d6af42cb0a7c67b8cf90ad69dd4d0ec9ff9ce5c26552108eb9bb34e7a`  
		Last Modified: Mon, 30 Jun 2025 17:38:31 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9100df697eaac84a7d5d28c969859ca63dc83d83d4c7f902cf1fd01696e9f927`  
		Last Modified: Mon, 30 Jun 2025 17:38:30 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400bffd8dffbe95e8e2bb4f0cdfd27ed4da443c56ee97cf9033ebaefaa1089c6`  
		Last Modified: Mon, 30 Jun 2025 17:38:31 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facf0f50a22d2f6ff761476fd2a884addc86e009f5986150bbec985aac93755c`  
		Last Modified: Mon, 30 Jun 2025 19:08:27 GMT  
		Size: 775.7 MB (775668039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6796d33b1d1578fd8e3b2279fd46f60b6f5a6f9b8704eee6f1e9e3155df8f0`  
		Last Modified: Mon, 30 Jun 2025 17:38:30 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046a4054c3279ed4cc552e15e60bb13fd8a26ea236cdacaee9ef2de8bd2ff950`  
		Last Modified: Mon, 30 Jun 2025 17:38:31 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa5798a3979f776055a136b6218d149825bd5cd50ccc2416f2f601a2d1f277f`  
		Last Modified: Mon, 30 Jun 2025 17:38:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
