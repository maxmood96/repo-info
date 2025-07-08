## `hylang:pypy3.11-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:e45138438c5fa2206015b1a1985bf7e0fa570bd5b6fc609df2cd4f380dee24a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `hylang:pypy3.11-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull hylang@sha256:e6ddc34cd29b406dd8bb4dc9648e6f79a3e577c212774daa477e969916847059
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2334184507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:480854ea9ad92164243f4339db754c7a4f349bc6b96d7462536af32afd810a34`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Mon, 07 Jul 2025 20:57:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 07 Jul 2025 20:57:48 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Mon, 07 Jul 2025 20:58:05 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Mon, 07 Jul 2025 20:58:06 GMT
ENV PYPY_VERSION=7.3.20
# Mon, 07 Jul 2025 20:58:55 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.20-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a8d36f6ceb1d9be6cf24a73b0ba103e7567e396b2f7a33426b05e4a06330755b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.20-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Mon, 07 Jul 2025 20:58:56 GMT
CMD ["pypy"]
# Tue, 08 Jul 2025 16:58:34 GMT
ENV HY_VERSION=1.1.0
# Tue, 08 Jul 2025 16:58:35 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 08 Jul 2025 16:59:35 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 08 Jul 2025 16:59:36 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8deccc19a6afef9e871d04b43c80fe996fed19378bb5a4c1e364bce445c8be3d`  
		Last Modified: Mon, 07 Jul 2025 20:59:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a3db8b3c4fadae7525ce14430f0a0d0c12fcf0c566cef7ee7e2dc7a2bf1ff2`  
		Last Modified: Mon, 07 Jul 2025 20:59:22 GMT  
		Size: 358.2 KB (358153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a789111a1136d5491bd6960900f8ba7267eb5f240a100a0d2a4e76a4530ce4ab`  
		Last Modified: Mon, 07 Jul 2025 20:59:27 GMT  
		Size: 15.5 MB (15545311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5601f4bd231414e9d297700165ef2c1f389af07630bbafa3c1cfb606a7d2018`  
		Last Modified: Mon, 07 Jul 2025 20:59:22 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abf6db8c7fdf11db7a3f56b927d3652aff6cad30a307c847d5df827ffd69da5`  
		Last Modified: Mon, 07 Jul 2025 20:59:24 GMT  
		Size: 30.6 MB (30642464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5856fb1634186546cbbfd8e3ba6b13c3a69bc7aa4ba2b92bbd5b7825fbd38e21`  
		Last Modified: Mon, 07 Jul 2025 20:59:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2bbb1d2e42bbba7bc4f1b13753497f956eba8fb3b86dc5a1b7493c8bd0854d`  
		Last Modified: Tue, 08 Jul 2025 17:19:07 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3f19cfab8a523ccf56a0380c04df9ed1b50464638e933ce0ab6bf2f6ff698a`  
		Last Modified: Tue, 08 Jul 2025 17:19:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d80980a494119a63f056d5dcc28ab1f4179f5cc5f1437355630f72ca12f961d`  
		Last Modified: Tue, 08 Jul 2025 17:19:08 GMT  
		Size: 7.4 MB (7379251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670793c1d3d0875765e51e752a1b5ba23288a0727751f9dc82c32232667a4885`  
		Last Modified: Tue, 08 Jul 2025 17:19:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
