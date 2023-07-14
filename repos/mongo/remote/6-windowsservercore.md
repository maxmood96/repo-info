## `mongo:6-windowsservercore`

```console
$ docker pull mongo@sha256:f086ebc85e185dad1902a3d1287fbcdacfa4d7730a22b50cd08fc24db08ea026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1850; amd64
	-	windows version 10.0.17763.4645; amd64

### `mongo:6-windowsservercore` - windows version 10.0.20348.1850; amd64

```console
$ docker pull mongo@sha256:00aa82d5cead3c1afbf4ca14cd779fe1a8dd1e1040d1f19ab7ac80a8982bc2a4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2254974362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43b7999e03177d93a85ffffb55f4a4f62b83ba3591b9c4c98031620db30e382`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jul 2023 21:29:32 GMT
RUN Install update 10.0.20348.1850
# Thu, 13 Jul 2023 22:35:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 14 Jul 2023 04:11:34 GMT
ENV MONGO_VERSION=6.0.8
# Fri, 14 Jul 2023 04:11:35 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.8-signed.msi
# Fri, 14 Jul 2023 04:11:36 GMT
ENV MONGO_DOWNLOAD_SHA256=06ee15df933f9f76757084c4b226eb06f79ad1471b293d9343484a6bc84e11eb
# Fri, 14 Jul 2023 04:13:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 14 Jul 2023 04:13:38 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 14 Jul 2023 04:13:39 GMT
EXPOSE 27017
# Fri, 14 Jul 2023 04:13:40 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84a7416e1317a892f4786a89c62493b21df55e0e06b82a4bb007cc79df0f949`  
		Last Modified: Tue, 11 Jul 2023 18:03:32 GMT  
		Size: 348.8 MB (348766456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2bae42a1ce047820c1f128e4587a430377ba56a110db0d98ec3ccfbd3de58a`  
		Last Modified: Thu, 13 Jul 2023 23:23:36 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879990fd18ab28a0fb7b3513d12fadd750a8f33c06be6650cf00a3d1e7fed531`  
		Last Modified: Fri, 14 Jul 2023 04:38:04 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e551c4da27e6650feb08703803c0c997d8a5b0cb5819f6ad45fa254f1df3ec`  
		Last Modified: Fri, 14 Jul 2023 04:38:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48becdb4c51dd7d95d50a8e0cef030f3bd020dd4537b7a77d0a5bd7fb37a8915`  
		Last Modified: Fri, 14 Jul 2023 04:38:02 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d649ae17701bdd0891addc1dddd56aa2c0739ef5cb967037948bdcf386995389`  
		Last Modified: Fri, 14 Jul 2023 04:39:28 GMT  
		Size: 517.6 MB (517599229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1587a8530a7f31e77b9182b4b0a849702bd84ddc9769b76f91b4243ecd50a830`  
		Last Modified: Fri, 14 Jul 2023 04:38:02 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567e5a7e524f0c3fb6a7a47afe67b04d3cfb41b48b03905d76f603d722bb2438`  
		Last Modified: Fri, 14 Jul 2023 04:38:02 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5848a88fe13042cdde3d702c75ef98c5136834931dd02e82459dc30450381a5`  
		Last Modified: Fri, 14 Jul 2023 04:38:02 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-windowsservercore` - windows version 10.0.17763.4645; amd64

```console
$ docker pull mongo@sha256:d8d6182e46ad944da9371a60d885baeb45642d57119d7baff4f54897e2832297
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2457320026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84edf72c1dbda50524265190e6f8e71a961a1b2cdf758c39ea77d5ec1fc018a3`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 22:38:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 14 Jul 2023 04:13:47 GMT
ENV MONGO_VERSION=6.0.8
# Fri, 14 Jul 2023 04:13:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.8-signed.msi
# Fri, 14 Jul 2023 04:13:49 GMT
ENV MONGO_DOWNLOAD_SHA256=06ee15df933f9f76757084c4b226eb06f79ad1471b293d9343484a6bc84e11eb
# Fri, 14 Jul 2023 04:16:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 14 Jul 2023 04:16:31 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 14 Jul 2023 04:16:32 GMT
EXPOSE 27017
# Fri, 14 Jul 2023 04:16:33 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b452db6d50a62b6e0e8dadb19715cfcf62cf73e54b5d3bac96621c1093673c`  
		Last Modified: Thu, 13 Jul 2023 23:25:18 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baab52a9e6872b81b76171a05c0fa0445fbeee6c7bc3cb4bb3774d6a85dd2016`  
		Last Modified: Fri, 14 Jul 2023 04:39:44 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730d01837135d0f64f6112c2d0f6cdf9ce093288b534d9ca387d1877cf29a62f`  
		Last Modified: Fri, 14 Jul 2023 04:39:44 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a48d4b1649d86c1df5b2ba598aba5fb4744976afb78c4b2e2f23b4ab6b79b3f`  
		Last Modified: Fri, 14 Jul 2023 04:39:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4030fcaeff7e7eed840517ee378b5d6371190141b2d7522fbb701788dd1fffc1`  
		Last Modified: Fri, 14 Jul 2023 04:40:58 GMT  
		Size: 517.6 MB (517621343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1f03bb1f0915b0dc56527da03d3018dc558e8a09c6905142106771d70bcdeb`  
		Last Modified: Fri, 14 Jul 2023 04:39:42 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebf850e48d8c3fceba12f5aa8e929db7a50a14314a464e71c231bf37bcaecc8`  
		Last Modified: Fri, 14 Jul 2023 04:39:42 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec4699cdda0ebc02279c22ba418deec6dabdc3a7f3251147cd1db6364388052`  
		Last Modified: Fri, 14 Jul 2023 04:39:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
