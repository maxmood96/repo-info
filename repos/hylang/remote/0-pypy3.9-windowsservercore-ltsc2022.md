## `hylang:0-pypy3.9-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:f2c46f8a4c19f00d9217fdd019c11377afbe922616ec23b28df283d141077301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2159; amd64

### `hylang:0-pypy3.9-windowsservercore-ltsc2022` - windows version 10.0.20348.2159; amd64

```console
$ docker pull hylang@sha256:9bb63fa64e523ce6b0c06d2fca6751da381b0b9274288a4792bc52257b1cc294
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1941955013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0799750d6786405b9e4d0124c1539ba824f56d5e90754ec91fe56ef18565660d`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Fri, 05 Jan 2024 18:53:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 05 Jan 2024 18:54:07 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Fri, 05 Jan 2024 18:54:22 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Fri, 05 Jan 2024 18:54:23 GMT
ENV PYPY_VERSION=7.3.14
# Fri, 05 Jan 2024 18:54:47 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.9-v7.3.14-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '9b3d8496f2a4729fdf20d9f835299902048950baad3a42019b67da75ca5b38b7'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.9-v7.3.14-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 05 Jan 2024 18:54:48 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 05 Jan 2024 18:54:48 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 05 Jan 2024 18:55:11 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 05 Jan 2024 18:55:12 GMT
CMD ["pypy"]
# Fri, 05 Jan 2024 19:48:24 GMT
ENV HY_VERSION=0.27.0
# Fri, 05 Jan 2024 19:48:24 GMT
ENV HYRULE_VERSION=0.4.0
# Fri, 05 Jan 2024 19:49:43 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 05 Jan 2024 19:49:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677ff406857b02e9184915f6cd41ca3eb3d6fde8b982ed9366fb953f0bbf9d9d`  
		Last Modified: Fri, 05 Jan 2024 18:55:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd19e93ef6766dd1cfe57685b423d3edf558037ebb6281a932a9e281e166b42`  
		Last Modified: Fri, 05 Jan 2024 18:55:19 GMT  
		Size: 493.8 KB (493803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181afeb4522a4b61fbb5fd097055b09573275fbe2416fc18323ee1de6f1f28b3`  
		Last Modified: Fri, 05 Jan 2024 18:55:20 GMT  
		Size: 15.5 MB (15545488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:294e70b5747d76aa5012616405b566c717f33af54c6729ca4e53edf555ef4708`  
		Last Modified: Fri, 05 Jan 2024 18:55:18 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091f4b590f6bd1796e2db45e6053b58c936c4f3212d4ed208906719c4504a664`  
		Last Modified: Fri, 05 Jan 2024 18:55:20 GMT  
		Size: 27.6 MB (27577374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d070fcda86646d7877c9bfa1ed1e232a0d676e80a0591979a68c436efcfe1a4c`  
		Last Modified: Fri, 05 Jan 2024 18:55:16 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43fbf881973ff38093b5ddbe2b30e5aa73b4f31c95ee1c699ddd96596461a71`  
		Last Modified: Fri, 05 Jan 2024 18:55:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa299227d0e6b8eaf3c397e82546e6b29c85c1aa3d0a83449706c629dac9304`  
		Last Modified: Fri, 05 Jan 2024 18:55:17 GMT  
		Size: 3.9 MB (3928233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf729e6d0451420e924d19e3947a38c7297afeb9070a33ffa5d2a53814a6da2`  
		Last Modified: Fri, 05 Jan 2024 18:55:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81d59ac7078b20f1d6f6a26bb21d946a3cedbaa93da10cc4e14477d2e5ecf6e`  
		Last Modified: Fri, 05 Jan 2024 19:49:48 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c848f966b6a48aa28eac1252a19e0cc1f2b0fe75acfc79b41d3d60f0ed38e9f3`  
		Last Modified: Fri, 05 Jan 2024 19:49:48 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e1d7ca704a2d5d218fdcbef04c0c982c60892ead61e96a0acb57f51d222b7a`  
		Last Modified: Fri, 05 Jan 2024 19:49:49 GMT  
		Size: 5.1 MB (5126092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e366c3e9370404a416229b821f3effc37e5aa10ff98e15aaa81877e76afd911a`  
		Last Modified: Fri, 05 Jan 2024 19:49:48 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
