## `mongo:5-windowsservercore`

```console
$ docker pull mongo@sha256:4628295b03631dfdc0769938669469759e71dd4b6801840f382c6a8d0f8bf2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `mongo:5-windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull mongo@sha256:8cf1267170dc361aa1a1725f1a61225463118fda3ae6ace702779dd2188ca622
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2424871647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b3dd3113e30809d7764d532630c8e4aedd18b82c017b049075765757bcca55b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 21:59:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 22:00:01 GMT
ENV MONGO_VERSION=5.0.26
# Wed, 15 May 2024 22:00:01 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.26-signed.msi
# Wed, 15 May 2024 22:00:02 GMT
ENV MONGO_DOWNLOAD_SHA256=dbe45ab5b3b04170fab6861629932354408d4033f773c54248dcd0680ea39ef8
# Wed, 15 May 2024 22:00:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:00:46 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 May 2024 22:00:48 GMT
EXPOSE 27017
# Wed, 15 May 2024 22:00:49 GMT
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
	-	`sha256:cd8f5127f25fc517f332b0e8449b86eb0e25f1d18a47743512cbfe0bfe0706ba`  
		Last Modified: Wed, 15 May 2024 22:00:53 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67931fe3d1bf17f7522517cfa4286ad51911e1422af1bcc5145665439000366c`  
		Last Modified: Wed, 15 May 2024 22:00:53 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532ed3ee5aaa8745771cbbebdb3c24cd2889cc42b33b46ee076e132d8314cb13`  
		Last Modified: Wed, 15 May 2024 22:00:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076d99ea990692965ffed187887fb48a51a94bc560c2f0024a6889dee114687f`  
		Last Modified: Wed, 15 May 2024 22:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4bbc8175bf4b89c0e90a6c392d48b1d57bf645c065cc4bb9e7ee4a912874114`  
		Last Modified: Wed, 15 May 2024 22:01:24 GMT  
		Size: 312.2 MB (312191220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da663381cdb24ae0a212ac4104fafd7426dda2cf94a6bcf0cbafe2ab04211218`  
		Last Modified: Wed, 15 May 2024 22:00:52 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84444fffff98984edd288cb009ab93480d32893f6db0cbd3acb73c9ce95a0c26`  
		Last Modified: Wed, 15 May 2024 22:00:52 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a984ed537e547fa8a257f06b135964f03d95719c53376345f4ed74e1fd83eac`  
		Last Modified: Wed, 15 May 2024 22:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull mongo@sha256:11fa4a65c7a969ff0bf94d42af40c16faf484f0ba31f288a034b3589c210ee7a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2492063357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0270e83e5fd7699c7c3ccc91184ac9a82a12f435087862dc01184b442ab7c3`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:51:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:51:19 GMT
ENV MONGO_VERSION=5.0.26
# Wed, 15 May 2024 21:51:20 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.26-signed.msi
# Wed, 15 May 2024 21:51:20 GMT
ENV MONGO_DOWNLOAD_SHA256=dbe45ab5b3b04170fab6861629932354408d4033f773c54248dcd0680ea39ef8
# Wed, 15 May 2024 21:53:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:53:59 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 May 2024 21:54:00 GMT
EXPOSE 27017
# Wed, 15 May 2024 21:54:01 GMT
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
	-	`sha256:360d6afaa6337bbff94721bcbda3861bcd407c30bcded4a1fab62e5c187be89f`  
		Last Modified: Wed, 15 May 2024 21:54:05 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39aae747a5e642657cda0d1c5d4e2f2bcb9cb040560366cef8af7628fcb75a3`  
		Last Modified: Wed, 15 May 2024 21:54:05 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f2adf317dcff4050bab83f1da70836401420fba5b03473777a54358ca3db57`  
		Last Modified: Wed, 15 May 2024 21:54:05 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b9b8c650ab392f7a18f1c7ca5ce0d818f09779a727b98a12391d74d3410cb2`  
		Last Modified: Wed, 15 May 2024 21:54:04 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30770d10ab4eda621226ff0211e85f88d7cd6aa1e3076c1dd7b05e12128a8da`  
		Last Modified: Wed, 15 May 2024 21:54:34 GMT  
		Size: 312.3 MB (312342900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daad568e3afa675599463db0914d6602e83c8e7963814d190a349cd20faddddc`  
		Last Modified: Wed, 15 May 2024 21:54:03 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a9fed6dc49a9d9c695438504f717d270b9ec1a04ec554d84d5688a1ca1d157`  
		Last Modified: Wed, 15 May 2024 21:54:03 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f6219aece45b185d4043206dfeee24ee0e4ea5e7679c904f93fba428369578`  
		Last Modified: Wed, 15 May 2024 21:54:03 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
