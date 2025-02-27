## `mongo:7-windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:78177f368151f5d904e7e2ac37be21dd87bc856ec77785acc409e57206554877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `mongo:7-windowsservercore-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull mongo@sha256:0193a7e292361c23d28c56439f854471ba09481403e0aa33fb83642de21695a5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3429168291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec908ea69078b809563e1cdbbc706a092dda30c5f93ad1ea3a6e6e0e2c73d27`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Thu, 27 Feb 2025 18:18:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 27 Feb 2025 18:18:53 GMT
ENV MONGO_VERSION=7.0.17
# Thu, 27 Feb 2025 18:18:53 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.17-signed.msi
# Thu, 27 Feb 2025 18:18:54 GMT
ENV MONGO_DOWNLOAD_SHA256=4e289d657aea36ecac5fa05a5d82cd1cc377efd75f682a2126ac6473d3a22d12
# Thu, 27 Feb 2025 18:20:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 27 Feb 2025 18:20:27 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 27 Feb 2025 18:20:28 GMT
EXPOSE 27017
# Thu, 27 Feb 2025 18:20:28 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9083c7118293567aca93860e0ee35f5c2a6398adb2c5c480715b29e43afb7bb`  
		Last Modified: Thu, 27 Feb 2025 18:20:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d8f00733d9dbfc94040e26454f8e3d00c05cd2cade85d7095515229154a8b8`  
		Last Modified: Thu, 27 Feb 2025 18:20:32 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9445d5ec48f57d6853a9b18db7131872868be3fc93e2d69ebc7a67d2bc2322`  
		Last Modified: Thu, 27 Feb 2025 18:20:32 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b39d3e90291a76a4b741a5313a77f0ff86ac4a73da86853b9a958b6db0ec105`  
		Last Modified: Thu, 27 Feb 2025 18:20:31 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5626cd05444a4720d6195ea26a12b503f45ba69797810ec43479c81b2c5af6f`  
		Last Modified: Thu, 27 Feb 2025 18:21:31 GMT  
		Size: 612.6 MB (612571609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f468a29f33375b8a288026af4b2121338e1eef5824b2331672fde54340cad10c`  
		Last Modified: Thu, 27 Feb 2025 18:20:31 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ca9ac965389bddb8b3bfbf097eaea7e793eb28127af19213c72744dad093a8`  
		Last Modified: Thu, 27 Feb 2025 18:20:31 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf88ac9980606760dccccee6eb366dafbc0adcd82b41d550fdaaf99dcbf1c75`  
		Last Modified: Thu, 27 Feb 2025 18:20:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
