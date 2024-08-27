## `mongo:windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:1a2980f4f83efa6e46c39718f4e7d0981ceed835b800f03d1ad3a567cd1f223d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `mongo:windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull mongo@sha256:5782ad461946662c7108502563a23055b911e0c88fd4cd82a920c264dc8009fb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2751294982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f9693322db0dfe889937c15c9fc4c39ba82d77a7455878135debd66aacac80`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Mon, 26 Aug 2024 23:04:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 26 Aug 2024 23:04:33 GMT
ENV MONGO_VERSION=7.0.14
# Mon, 26 Aug 2024 23:04:34 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.14-signed.msi
# Mon, 26 Aug 2024 23:04:34 GMT
ENV MONGO_DOWNLOAD_SHA256=8916397b35f2b6b42241ef1625e5c75ba7ad10ad75072cf377450f6f0bdf254c
# Mon, 26 Aug 2024 23:05:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 26 Aug 2024 23:05:53 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 26 Aug 2024 23:05:53 GMT
EXPOSE 27017
# Mon, 26 Aug 2024 23:05:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e3fd2ee4d5a6012f4b3000bbb36f1d579d52711b5232000e3dc225ee75736f`  
		Last Modified: Mon, 26 Aug 2024 23:05:59 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d117f6ae18dd48074cf6fed6dcfae15828ae9fb9f418ab6b2655df48abef373e`  
		Last Modified: Mon, 26 Aug 2024 23:05:59 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff9960bb95f21accbc9773bdcf8529928ed64a789e741b9cde91e5ddb2854f9`  
		Last Modified: Mon, 26 Aug 2024 23:05:59 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc6580a2f7e3e77df85b650ab19d49478cf0b42dfa3af86b2a17248a9e8aee1`  
		Last Modified: Mon, 26 Aug 2024 23:05:58 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a7839a2cbb430345696bd7bc46a31d5aac724e2ddbcb0a163dec6797475079`  
		Last Modified: Mon, 26 Aug 2024 23:06:49 GMT  
		Size: 609.5 MB (609520983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b0806deff299d5769073c7a9b98569379b1e6dd22c7ed7aa14a152cb79fd2c`  
		Last Modified: Mon, 26 Aug 2024 23:05:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0880183e6463f8476567c2defe08a5c5d301ad341c7ec0fe1d26240dc57c4f`  
		Last Modified: Mon, 26 Aug 2024 23:05:58 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc8e75acfea6a485f86fb69b30197fcec0413258248f4431ae509c012e668e0`  
		Last Modified: Mon, 26 Aug 2024 23:05:58 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
