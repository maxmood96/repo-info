## `mongo:4-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:07b65807b8e468841bef374529139f647a9ac412e4ac480b224a7caa0e8037fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.707; amd64

### `mongo:4-windowsservercore-ltsc2022` - windows version 10.0.20348.707; amd64

```console
$ docker pull mongo@sha256:80e42f2e3d94cb7710bfa34c32f41a3a6901f5e87e96d1d00619001d67ee791f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2480465101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99341c2a154210ea4470eeaba1ef1693c989711dab58a3885744987cac77b9b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 05 May 2022 03:02:27 GMT
RUN Install update 10.0.20348.707
# Wed, 11 May 2022 12:34:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 16:47:01 GMT
ENV MONGO_VERSION=4.4.13
# Wed, 11 May 2022 16:47:02 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.13-signed.msi
# Wed, 11 May 2022 16:47:03 GMT
ENV MONGO_DOWNLOAD_SHA256=0eb6e5c43c74a992301529515c52b7e326239cd12649fb6f91e807fcbbf06f39
# Wed, 11 May 2022 16:48:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 May 2022 16:48:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 May 2022 16:48:23 GMT
EXPOSE 27017
# Wed, 11 May 2022 16:48:24 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:12fb50a031bdc8d2b65d86d694a4ed20e937852ed1bd3c433d8f2f60279cecc7`  
		Size: 800.7 MB (800671635 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:52d280e9bf32da92b07a144022b757d7e39ac8039e166551ad32f8ee416bb55f`  
		Last Modified: Wed, 11 May 2022 14:06:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16900b0eef05f3da0e92232ec13c75628020577bc4a32e6268d53af55563547b`  
		Last Modified: Wed, 11 May 2022 17:40:37 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d273f2b0902cd6a85b4709ad5b13023f37dacc63ce29f95d2c6179676397b4`  
		Last Modified: Wed, 11 May 2022 17:40:37 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8104d667205efc25673bed47d2489d6d21257c7bdd2cd6c1ab1197ac7268a400`  
		Last Modified: Wed, 11 May 2022 17:40:34 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0e1b2506a26c591d6f9b208c8df3a7e37b51fa30990a7f1764931907d6d9f6`  
		Last Modified: Wed, 11 May 2022 17:44:49 GMT  
		Size: 242.9 MB (242920015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298a8f2299fac96a9d0ec9ed76ccb0dbc940d0304806731a48ac8f140a74453f`  
		Last Modified: Wed, 11 May 2022 17:40:34 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960759cf02966e2870463bdfd10b57da4f9d33843a71a643bfb5ee5db2361223`  
		Last Modified: Wed, 11 May 2022 17:40:35 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ae65d004dc816bd537aded125c081049f8a23d92448a9bf49e7252e5d3e34b`  
		Last Modified: Wed, 11 May 2022 17:40:34 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
