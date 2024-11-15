## `mongo:5-windowsservercore-1809`

```console
$ docker pull mongo@sha256:5a6fbed552f2793e5f890defcfbf82260f1f47713bbf5ae2edad4f03b414964c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `mongo:5-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull mongo@sha256:f618951b7e1a8dc998c8aa29625055384ffdce3b5f5775acfc55a13e546a8444
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2324196574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f91ffd421b59b0e978d128ce5d3eb889a9f3caeb59ebb71f0bdbf89e48baac`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:19:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Nov 2024 20:19:12 GMT
ENV MONGO_VERSION=5.0.30
# Thu, 14 Nov 2024 20:19:13 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.30-signed.msi
# Thu, 14 Nov 2024 20:19:13 GMT
ENV MONGO_DOWNLOAD_SHA256=acabc07cba2e1b4a8bc2a852715a21ca29cae0f08a0dc157d54c1049f586fe45
# Thu, 14 Nov 2024 20:21:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 14 Nov 2024 20:21:03 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 14 Nov 2024 20:21:04 GMT
EXPOSE 27017
# Thu, 14 Nov 2024 20:21:05 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd272c3d30e96511c8a43801771c675d7496a101d9a4bbfe5fd434603edc1a98`  
		Last Modified: Thu, 14 Nov 2024 20:21:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a3a899a1a53035d9891a0d157c1fbc98443d3191148c636b797cc687770f0c`  
		Last Modified: Thu, 14 Nov 2024 20:21:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef564cba9658dff7b86247ce23d482c762c9091904f4673a6d0510cfde8a20c`  
		Last Modified: Thu, 14 Nov 2024 20:21:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b2f0f64b8c6e1fca26ef72cdaaf725983edfcddc59c141919315c8b4a59e80`  
		Last Modified: Thu, 14 Nov 2024 20:21:08 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be689ef182e807ee18a77467dba13e620c2f6c1958a23b774c71f027f34eb3d9`  
		Last Modified: Thu, 14 Nov 2024 20:21:39 GMT  
		Size: 313.5 MB (313533713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3fd85b9c756fb6cc057445f389b02b2fcdee5661efb44171013aad63586318`  
		Last Modified: Thu, 14 Nov 2024 20:21:08 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1c83ed7bb3fb355cec5e2efec991b1a1f65943911f2b1aa304969103fc0fd6`  
		Last Modified: Thu, 14 Nov 2024 20:21:08 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833860faf0f971954611a5a460cd49058de08333f84016d740a03d7f81cf4f7f`  
		Last Modified: Thu, 14 Nov 2024 20:21:08 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
