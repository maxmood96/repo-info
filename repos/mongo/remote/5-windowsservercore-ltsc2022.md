## `mongo:5-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:52f48def99269850043967c51bb22b32ffb1255c413aacf1ef78f38481d85eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `mongo:5-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull mongo@sha256:ad87f6ac4ad39f519f5216b54daf4e52f34a5f389b6ec34efa0d4ec579f81491
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311711296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f89056da94109fa22193b8566521feaeefeca7c5cb7d1868874da9688a19ccb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:59:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Apr 2024 23:59:29 GMT
ENV MONGO_VERSION=5.0.26
# Tue, 09 Apr 2024 23:59:29 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.26-signed.msi
# Tue, 09 Apr 2024 23:59:30 GMT
ENV MONGO_DOWNLOAD_SHA256=dbe45ab5b3b04170fab6861629932354408d4033f773c54248dcd0680ea39ef8
# Wed, 10 Apr 2024 00:00:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 00:00:21 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Apr 2024 00:00:21 GMT
EXPOSE 27017
# Wed, 10 Apr 2024 00:00:22 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738bade152e42932cbb3a3a2a9d3f6dfb6af3e9d6141d41f0eb5b177d3a2afc7`  
		Last Modified: Wed, 10 Apr 2024 00:00:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ab88abad150906eb038885ebef22d465de591c1d205c13509fb00bbdc0aa08`  
		Last Modified: Wed, 10 Apr 2024 00:00:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459da51d53aab5d7b77bbc405a2476e67af368169fd0e9555c2fff25c81bf5c0`  
		Last Modified: Wed, 10 Apr 2024 00:00:28 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4cd4d9c9069264bbb5b1778ec4102d7cb448f2b38e794e85ed00cab176889ab`  
		Last Modified: Wed, 10 Apr 2024 00:00:26 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d234125134c7ff76f77fd9942f3f83fbc8006e33684f268111cb8f826662ed42`  
		Last Modified: Wed, 10 Apr 2024 00:00:59 GMT  
		Size: 312.3 MB (312328624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288a801315b59b5ddaa0adc0264b4ccd8c183ea2ae02782bdc67bbaaa0007537`  
		Last Modified: Wed, 10 Apr 2024 00:00:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87055630872a38e0160b9d6b07217a819f9f25cb1be9ab8efc80fb4552ccc7c`  
		Last Modified: Wed, 10 Apr 2024 00:00:26 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8008e14de4c4ddf973cc8c84af9cec0c12a56d7bb22dc683a029da4c0f6833`  
		Last Modified: Wed, 10 Apr 2024 00:00:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
