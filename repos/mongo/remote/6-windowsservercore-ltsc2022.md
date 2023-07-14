## `mongo:6-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:9363985c2855a765060fc3182cdb593a75f238862560ca892bd2a75ea47985d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1850; amd64

### `mongo:6-windowsservercore-ltsc2022` - windows version 10.0.20348.1850; amd64

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
