## `mongo:7-windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:2ebe0dd943e30b8aad318dfc0516ce4a4c6d3aed3f31286394a91ac227189e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `mongo:7-windowsservercore-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull mongo@sha256:f611632da9f3ee751232f5892565858ccae7730d233725d872e3a693455d5a9a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 GB (4007244634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6ee4408647066b83b6d24e8d3c89f375239a44d6f2daca33b63517146729b0`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:49:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Apr 2025 00:49:19 GMT
ENV MONGO_VERSION=7.0.18
# Wed, 09 Apr 2025 00:49:21 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.18-signed.msi
# Wed, 09 Apr 2025 00:49:22 GMT
ENV MONGO_DOWNLOAD_SHA256=ab23d0e0488dd0b9ab07bae73e481271c7574e212b4bb61b1331400a3cffb02b
# Wed, 09 Apr 2025 00:50:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:50:44 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Apr 2025 00:50:46 GMT
EXPOSE 27017
# Wed, 09 Apr 2025 00:50:47 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab4f58be0c99ff30f3be7eded1f891da65e7325c900cb3c7f774c44b34883ddd`  
		Last Modified: Wed, 09 Apr 2025 00:50:59 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb2bd3a78e0949323984f77857b0cc0708b8e2ad6c2e4f118f2857fa38a4da2`  
		Last Modified: Wed, 09 Apr 2025 00:50:58 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d499fc64185957b8303ce96fc0b45d638739fd581f658436a259ab19bf6849`  
		Last Modified: Wed, 09 Apr 2025 00:50:58 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13bd50fd9b464f170b4d08c8e98405e96b66d54122419a5b367031f7b8a15f91`  
		Last Modified: Wed, 09 Apr 2025 00:50:57 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2924e4d4bb9b53d3059a16870234820d56221e589373a37f0d9c8f572e38c1`  
		Last Modified: Wed, 09 Apr 2025 00:52:02 GMT  
		Size: 612.6 MB (612556044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8367fc87415a698589bcfb728ac6e7d9eca365eeab9c44ac37187631e150eb3`  
		Last Modified: Wed, 09 Apr 2025 00:50:57 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930fba3a318611444d5b4ee591275d38639309af29994aa836a2b7ac756d072e`  
		Last Modified: Wed, 09 Apr 2025 00:50:57 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20719550a8674a88161b89a9a549d5be2cd3858bac04d739210e42449ac8c7e`  
		Last Modified: Wed, 09 Apr 2025 00:50:57 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
