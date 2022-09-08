## `mongo:5-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:2341f83e75dff5a14dd98b8740ee7eb329cc50cdfb0888626c208ffa8cce84b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.887; amd64

### `mongo:5-windowsservercore-ltsc2022` - windows version 10.0.20348.887; amd64

```console
$ docker pull mongo@sha256:3798e18156d6212d4ce267e41544fb9f881220e3b61c951229ffb82acd07e400
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2626951313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ab133b1c5a3bc7ef5e78a05d2fe267e35748899c379526bebeb777c767ba95`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 06 Aug 2022 02:59:35 GMT
RUN Install update 10.0.20348.887
# Wed, 10 Aug 2022 13:33:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 07 Sep 2022 20:16:52 GMT
ENV MONGO_VERSION=5.0.12
# Wed, 07 Sep 2022 20:16:53 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.12-signed.msi
# Wed, 07 Sep 2022 20:16:54 GMT
ENV MONGO_DOWNLOAD_SHA256=640610125c5b555a41fd5ad12c6b69f02639b2f39c92b14dc6b0c96a30dc26dd
# Wed, 07 Sep 2022 20:18:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 07 Sep 2022 20:18:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 07 Sep 2022 20:18:25 GMT
EXPOSE 27017
# Wed, 07 Sep 2022 20:18:26 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:97b25a378238b615dc51216c4d87ce17fd3cc3dca9db458e8705d1a4c17e3bb7`  
		Size: 880.0 MB (880025531 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ff9b89cbdb5f88cb926263140643eb2bfad61fb092119830e290c8f8ff711c8f`  
		Last Modified: Wed, 10 Aug 2022 15:05:31 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad77d998a78e184a69d27783ba6e13eb2c9a5ed5dcf2c786c287d77c702bfae`  
		Last Modified: Wed, 07 Sep 2022 23:19:58 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619b7b704348a00f97ac5dc33939690e1a1de9db9d91dcdb71b7886c97f78c09`  
		Last Modified: Wed, 07 Sep 2022 23:19:58 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf67bd280897df5c338e013bf5dfa195dfa602eb3e2eb6b735bb8ee43562de54`  
		Last Modified: Wed, 07 Sep 2022 23:19:56 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e82ec8916acc9bc62d045b8b96cc37c370e2f48ab3dc18d2450e0c22a321f45`  
		Last Modified: Wed, 07 Sep 2022 23:21:12 GMT  
		Size: 310.1 MB (310052315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e15591f692f07f3dd82a7ec1e5b2439f248f6a9a51e962f5e2e800431d7942b`  
		Last Modified: Wed, 07 Sep 2022 23:19:56 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4629f33c3e9631daef9c48c583febf44b370d72cfc5e54257b99c41ab95c34`  
		Last Modified: Wed, 07 Sep 2022 23:19:56 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f00976a42dd73b5617e3bd73ae93d04054909dc796d2439818018debff80d5`  
		Last Modified: Wed, 07 Sep 2022 23:19:56 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
