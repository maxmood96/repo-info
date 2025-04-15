## `mongo:7-windowsservercore-1809`

```console
$ docker pull mongo@sha256:b416ecc8a7037d2638c1b2bdc8d2ed38040e1de25c8cc3e58a3c676f1095ace3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `mongo:7-windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull mongo@sha256:04981486ed984d0f59fc30f1aaa68565b5d3027eeada21a116bffdef217df93c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2775421168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dac959f7f21d06c871a5e7a2618252a2f5d73b5db1b69a9cb586a9bf3dd6b6c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Mon, 14 Apr 2025 23:15:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 14 Apr 2025 23:15:34 GMT
ENV MONGO_VERSION=7.0.19
# Mon, 14 Apr 2025 23:15:35 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.19-signed.msi
# Mon, 14 Apr 2025 23:15:36 GMT
ENV MONGO_DOWNLOAD_SHA256=815ab9b621acea764f1ecc99c0b686162116ded842a384e4b280713343a3bf9b
# Mon, 14 Apr 2025 23:18:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 14 Apr 2025 23:18:10 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 14 Apr 2025 23:18:10 GMT
EXPOSE 27017
# Mon, 14 Apr 2025 23:18:11 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9c553ccfd83187062430363be0daf4e7ad6ae4945bb29666a1de9a38bb813f`  
		Last Modified: Mon, 14 Apr 2025 23:18:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94fbc570c072a847ca1e9ca16844bb5f1ae5147905a132b71f7d2c26e1b9b1c`  
		Last Modified: Mon, 14 Apr 2025 23:18:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10e230a433aa1fa39f76a2714ea6bf05136532e4273c1891e8068c15abf72bd`  
		Last Modified: Mon, 14 Apr 2025 23:18:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a029725b629ad59d8f9357c5bd4e3c7d1582197c905cd0dce8af23a067a994a`  
		Last Modified: Mon, 14 Apr 2025 23:18:14 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95403a9752233f9758b6a1a7c2ee39009554b57c389ad7d1307dc1bfc23d3f27`  
		Last Modified: Mon, 14 Apr 2025 23:19:03 GMT  
		Size: 612.7 MB (612686292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0d3a9f8a95a72d81f4f653330409029db757748a86afdc4ea45c51d58d0670`  
		Last Modified: Mon, 14 Apr 2025 23:18:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77264ac6e914d556ead65b16cb4437379dcc09db2a835088102d85d8ef90811`  
		Last Modified: Mon, 14 Apr 2025 23:18:13 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f05e1923967818d3b077c64569f9cba038609d19f0b5abca41928b67db7ba7`  
		Last Modified: Mon, 14 Apr 2025 23:18:13 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
