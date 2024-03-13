## `mongo:6-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:0e6bab9b325d3e62b60784649680f7ac277d4dd57d98bf23b4d02a2a66a2a234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `mongo:6-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull mongo@sha256:e44a9e6de513fa3ffa2966475727d79e0a63414f8972c85ff6deb3c6c4f31040
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2479543698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e70c2633f8b138c1bf0e15f517b7fd27f7470ef1441e03cfccfeed9395825039`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:05:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 00:05:32 GMT
ENV MONGO_VERSION=6.0.14
# Wed, 13 Mar 2024 00:05:32 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.14-signed.msi
# Wed, 13 Mar 2024 00:05:33 GMT
ENV MONGO_DOWNLOAD_SHA256=871a352e6eb31f2d4d74816b6511cc350697c2004580f79f652f1a9237ea15c8
# Wed, 13 Mar 2024 00:06:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 00:06:41 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Mar 2024 00:06:41 GMT
EXPOSE 27017
# Wed, 13 Mar 2024 00:06:42 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cfa97908b3f9dd77753c385f5402b2411b6d22f916cb15f23849aed63083eb`  
		Last Modified: Wed, 13 Mar 2024 00:06:46 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a71e3250d03f18197a34f39032c6771df8252cf35f9656310d373fd941198ce`  
		Last Modified: Wed, 13 Mar 2024 00:06:46 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5564a7ba18790fb68b7336accbf3b756d2cdb41d614de41e9df31a2119ebc1f2`  
		Last Modified: Wed, 13 Mar 2024 00:06:45 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254099542996f72fe7ddaed32eb0a599ebbc7b9e154f9469289ff5536f842d18`  
		Last Modified: Wed, 13 Mar 2024 00:06:44 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c382b2262661b86449aab0af2dce3acf988d145338acae5f45eab8c35528f667`  
		Last Modified: Wed, 13 Mar 2024 00:07:32 GMT  
		Size: 522.1 MB (522075652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431dafe0eba7c3edb17108309c347558600a86ce2ddf92459fad15584ae8a234`  
		Last Modified: Wed, 13 Mar 2024 00:06:44 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc68aff943803668e6a09ae2953d37f8b8275eef20f90823103a8aaebe74112`  
		Last Modified: Wed, 13 Mar 2024 00:06:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b703f6d02922678e7464bbe9239b16ad18ade9a9a035ddbba2729287c9baf8`  
		Last Modified: Wed, 13 Mar 2024 00:06:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
