## `pypy:2-windowsservercore-1809`

```console
$ docker pull pypy@sha256:90f3e54f38acbc3f640a679298486c01470d3048aa33b5a5136c8a367de6a0e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `pypy:2-windowsservercore-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull pypy@sha256:84808fde95f14a005aa36134d4d039bc815bb1695abde097f9af94526de7ed00
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2682494786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e7ee08ad1f39d3a568879018d0d741256d0830f74ea159801efe14792c4177`
-	Default Command: `["pypy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 12:10:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jun 2021 12:15:45 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 09 Jun 2021 12:16:14 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 09 Jun 2021 12:16:52 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 09 Jun 2021 12:16:55 GMT
ENV PYPY_VERSION=7.3.5
# Wed, 09 Jun 2021 12:17:57 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy2.7-v7.3.5-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '0b90eded11ba89a526c4288f17fff7e75000914ac071bd6d67912748ae89d761'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy2.7-v7.3.5-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 09 Jun 2021 12:18:00 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Wed, 09 Jun 2021 12:18:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 09 Jun 2021 12:18:07 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 09 Jun 2021 12:19:42 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing "pip == {0}" ...' -f $env:PYTHON_PIP_VERSION); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 09 Jun 2021 12:19:46 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:639bb6bb2beb4cfdcacb9f0844344448fe26494665d5fe78a494419f86fbb18f`  
		Size: 923.3 MB (923252167 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7863ef96846d497ea06fe442ea13dcecaf5c248ce238c69800475281a4fa848e`  
		Last Modified: Wed, 09 Jun 2021 12:20:41 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5789912c867ed5d9d277acf797c2a9373efb14a0496fb5ec7fce90fb3907d5b7`  
		Last Modified: Wed, 09 Jun 2021 12:21:19 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8101813d054a478291fc59f1877bc1daf4e7df6c49e4c525a03b718b41f5014b`  
		Last Modified: Wed, 09 Jun 2021 12:21:18 GMT  
		Size: 349.2 KB (349166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024ede9fa93db63569cb4e89631c5a1b1b1f2bbb11389e0be0b13d237cb024ed`  
		Last Modified: Wed, 09 Jun 2021 12:21:21 GMT  
		Size: 15.5 MB (15486312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a934f0ce8fe8c74daa1a229e7cdce45326e50cf25d57d6fe3aaa480d2fe0a2d4`  
		Last Modified: Wed, 09 Jun 2021 12:21:18 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2ef9e85aa3bab6a24449e07e8583ab18cf6a16607b111f606259a81d2bca06`  
		Last Modified: Wed, 09 Jun 2021 12:21:25 GMT  
		Size: 22.4 MB (22396097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1996c0a3320f73eec0b64a312f13cd07db99b4288f689421c8566d2a2227ee9`  
		Last Modified: Wed, 09 Jun 2021 12:21:15 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c56f6c2169efad2465c85ce84c133256f91b457d89c29e909ec2abe0991a02`  
		Last Modified: Wed, 09 Jun 2021 12:21:15 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350f88081ed8d73214e43c95723f1c0300b788bd0292fc4c7d1704a14850937b`  
		Last Modified: Wed, 09 Jun 2021 12:21:15 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3909fa8743737845542fb63163d4949d958dd36cfb5377ef6ff14e4f838a7176`  
		Last Modified: Wed, 09 Jun 2021 12:21:16 GMT  
		Size: 2.7 MB (2668276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072b04831511c9193752873434a96a3fac6b71c2888815ce09d9707e46185ae7`  
		Last Modified: Wed, 09 Jun 2021 12:21:15 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
