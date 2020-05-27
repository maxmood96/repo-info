## `mongo:4-windowsservercore-1809`

```console
$ docker pull mongo@sha256:0768e7755712a5a86421a0aad9801e3b4a46f639e89c231011e92a67bb1e59cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `mongo:4-windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull mongo@sha256:4ed9e722e7208713cd0db6a994342a5483148f86bc300bafd9f9f4e43bf42e86
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1809830349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d954257223b8067b2f76ab42ca080fecccd675349304fb3dd346c6c2940500`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 13:04:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 26 May 2020 22:44:00 GMT
ENV MONGO_VERSION=4.2.7
# Tue, 26 May 2020 22:44:01 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.7-signed.msi
# Tue, 26 May 2020 22:44:02 GMT
ENV MONGO_DOWNLOAD_SHA256=d085db55ea34452617e73a5d7ad80fbc4b9eaf75990e49080a7c3ced13fbb42c
# Tue, 26 May 2020 22:59:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 26 May 2020 22:59:51 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 26 May 2020 22:59:53 GMT
EXPOSE 27017
# Tue, 26 May 2020 22:59:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6e220442d94ba050201e82fee90c58b5e714748e7906735032367404c473c91c`  
		Last Modified: Wed, 13 May 2020 14:27:38 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148092c4435cf78eff436f984249c16455c3fd73ccd14fbd73a652c7d12c02ac`  
		Last Modified: Tue, 26 May 2020 23:02:25 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a6670dd73092a916e2bb60d9cfd18576c62161e4d7378234d72762cc8390ea`  
		Last Modified: Tue, 26 May 2020 23:02:25 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ecbc9c56cf05c70234679ca9c4388698435cbc9048adc26a47462551f272e9`  
		Last Modified: Tue, 26 May 2020 23:02:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f012da451af8403018701ff858d9d57da34dfebf622dfdac58dd6e802852cbe6`  
		Last Modified: Tue, 26 May 2020 23:03:31 GMT  
		Size: 91.5 MB (91489428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32b9807e649220503e2dd7f1cbee829c2dc204b226c8da31b7689673bcb5b6`  
		Last Modified: Tue, 26 May 2020 23:02:23 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0994eba96cdc955f61635a7d34b69c2e2af2c075b0a80f08bc0844d57340b1`  
		Last Modified: Tue, 26 May 2020 23:02:23 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0923e406427821d369de21bd06c7f171d01ec8c2d884cc08064b12c2c261dfe9`  
		Last Modified: Tue, 26 May 2020 23:02:23 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
