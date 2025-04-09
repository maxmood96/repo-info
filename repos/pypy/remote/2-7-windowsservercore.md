## `pypy:2-7-windowsservercore`

```console
$ docker pull pypy@sha256:097cac31db82f8c8a326671ec19263bfc4dbd3c6af018465d35cb60c5f6a285e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7009; amd64

### `pypy:2-7-windowsservercore` - windows version 10.0.26100.3775; amd64

```console
$ docker pull pypy@sha256:9ec852734b616642b85b83abd9276d1e4b799648c78d5cf6ec68218b884baf48
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3436172659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7c728e574179e5bd5ddc3998d842ec0612a9a6a257ea79b06fa2a92585f84d`
-	Default Command: `["pypy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:45:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:45:21 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 09 Apr 2025 00:45:28 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:45:38 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:45:39 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 09 Apr 2025 00:45:59 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy2.7-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'fbdcd4fe681981c020a25c1a35225209dc3d651f6117ebe9e4d212b66a2b46ec'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy2.7-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:46:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 09 Apr 2025 00:46:00 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 09 Apr 2025 00:46:17 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:46:18 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a23ba817f78f0b4b18767e192e7183c419edeefd63cef8d2b4a7d1b4aab6e2`  
		Last Modified: Wed, 09 Apr 2025 00:46:26 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce41276d89dad4b9a0eb02cb24e4be41c56f5b1f65245af9dbf979f04caaf78`  
		Last Modified: Wed, 09 Apr 2025 00:46:25 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45c9b94cf1655da3b2f0b6cfd757e87aeb4e0345c39e273dc0d251e4cf4daf0`  
		Last Modified: Wed, 09 Apr 2025 00:46:24 GMT  
		Size: 365.4 KB (365350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79c09f7873bed37923c6c5cc53816bb3da912ac5a8195c7c2e9ea57a1f0de3`  
		Last Modified: Wed, 09 Apr 2025 00:46:26 GMT  
		Size: 15.5 MB (15548443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4b0907f8e36dd4536b93d934cfdcaf319d39f4290517727ce67c7e442015fd`  
		Last Modified: Wed, 09 Apr 2025 00:46:24 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6ee59eafbdb6f4c92d1cde45866ce561ba0ef79e37ae816b86db6f3e5af8db`  
		Last Modified: Wed, 09 Apr 2025 00:46:25 GMT  
		Size: 22.9 MB (22903625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5853cd625eccdef77c6f35d786e72613b39a226a3fe228de140dc2ad2f427166`  
		Last Modified: Wed, 09 Apr 2025 00:46:22 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3ad47e15bd4e5e096ffb1b2f590bf01b629ade025d637b8dae2139fad41241`  
		Last Modified: Wed, 09 Apr 2025 00:46:22 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205eee0aef7763ffd564a58982349293eadbb2f147523b57f1e1c9cab7275cab`  
		Last Modified: Wed, 09 Apr 2025 00:46:23 GMT  
		Size: 2.7 MB (2667922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd9565e2422b1a1d1d22ed724139873c8b0a0ba7802cbb8bb3405744e6af979`  
		Last Modified: Wed, 09 Apr 2025 00:46:22 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-7-windowsservercore` - windows version 10.0.20348.3453; amd64

```console
$ docker pull pypy@sha256:7e37e075bf1014448a02c9b1a41f94941e0661a9144b1c33efb5e08a1b6a916c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312408577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172f868e3fe1029a818c109015bb6a555ff969839d3f9f980efb81a91fb2b86d`
-	Default Command: `["pypy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 00:56:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:56:38 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 09 Apr 2025 00:56:50 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:57:00 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:57:01 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 09 Apr 2025 00:57:21 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy2.7-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'fbdcd4fe681981c020a25c1a35225209dc3d651f6117ebe9e4d212b66a2b46ec'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy2.7-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:57:23 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 09 Apr 2025 00:57:24 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 09 Apr 2025 00:57:40 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:57:41 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a763d15f73fce526fb69342ecb34f8946206562d0f6c60024a1078920049fe4b`  
		Last Modified: Wed, 09 Apr 2025 00:57:49 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e698242e4fe8a1655956f78c32b1134f57579a753b618aead867ab682976fd8`  
		Last Modified: Wed, 09 Apr 2025 00:57:48 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e0783948c672f78be221d997b062757753e40e878c40b4a156dd08ea5845ff`  
		Last Modified: Wed, 09 Apr 2025 00:57:48 GMT  
		Size: 343.9 KB (343941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e680d70e812f577657c1667844be439ecd48942a86ccf9253a3d4b387dafc15`  
		Last Modified: Wed, 09 Apr 2025 00:57:49 GMT  
		Size: 15.5 MB (15530666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43eaa752287e7e582d752dbc24429b2967743eebc35013e6438a740796aba928`  
		Last Modified: Wed, 09 Apr 2025 00:57:47 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bac664d1b652bbc573a728828b68ce9da6ac7d316fa84e0de6829ae93de895`  
		Last Modified: Wed, 09 Apr 2025 00:57:49 GMT  
		Size: 22.9 MB (22884474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f9f51a7374ece479044e408f98980adb2b74a0b44523db2a90448358af40a6`  
		Last Modified: Wed, 09 Apr 2025 00:57:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e4c826e63c5fe3239e7f534c4e259fb29219af948bdd48b21d25d6e111d541`  
		Last Modified: Wed, 09 Apr 2025 00:57:45 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19bdf473ee4b0f3ab26fe300c552bbc54a4906581889cc4501e71eae5017fda`  
		Last Modified: Wed, 09 Apr 2025 00:57:46 GMT  
		Size: 2.6 MB (2645997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62331588987f2d8213c526521c5850bb7a9c9aa953e89d93decf3adeb4469b19`  
		Last Modified: Wed, 09 Apr 2025 00:57:45 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-7-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull pypy@sha256:354eb4d538b2a89c9ba07a54a97c832e25ffa8bd6d842e69c4a6c936ba2b2699
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2192931440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be2d0d76177b7ae37c3c4585a2aa5f730257775761af3c00881aff7e3875341b`
-	Default Command: `["pypy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 19:03:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 19:03:06 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 12 Mar 2025 19:03:39 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:03:55 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:03:56 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 12 Mar 2025 19:04:17 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy2.7-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'fbdcd4fe681981c020a25c1a35225209dc3d651f6117ebe9e4d212b66a2b46ec'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy2.7-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:04:18 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 12 Mar 2025 19:04:19 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 12 Mar 2025 19:04:38 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:04:39 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8dc13edae0c49a661c97e7a4b773ae8dbc544539d6f06546c87a3f0ee8d0e1`  
		Last Modified: Wed, 12 Mar 2025 19:04:48 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218c4dafd24459babc08f26de3c7975402871e373026fa375c79612bbf17b002`  
		Last Modified: Wed, 12 Mar 2025 19:04:46 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab5e29023310a119591a8dce667385be5166edb60e75dd65bf4bf4266b57243`  
		Last Modified: Wed, 12 Mar 2025 19:04:46 GMT  
		Size: 323.1 KB (323060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5affb7dd98c52ae053a82f7cec473923da8865bb51004f31972f6b465b2b4554`  
		Last Modified: Wed, 12 Mar 2025 19:04:47 GMT  
		Size: 15.5 MB (15491932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160359f5b290b02d3d32ae5351acb44302f4c63175048f5fd933726d249052a3`  
		Last Modified: Wed, 12 Mar 2025 19:04:46 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0e67781b8e039895cef71d117a7cbd3843512e22d99dc31da01d089a727b49`  
		Last Modified: Wed, 12 Mar 2025 19:04:47 GMT  
		Size: 22.8 MB (22845034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39bc510e3fc0281d175dec50fa3e983ba1fb25cc6b00e654b120a35c0d2059bc`  
		Last Modified: Wed, 12 Mar 2025 19:04:44 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731caeac5b6a1e0b4eca01457ed309c75b8112e6364e145f282f6be2413ea8a1`  
		Last Modified: Wed, 12 Mar 2025 19:04:44 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4469e9234a34dd0d3f819332dec48701919138ab89ad0fbf425f0735f335144f`  
		Last Modified: Wed, 12 Mar 2025 19:04:45 GMT  
		Size: 2.6 MB (2628906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37dd7fe132a85a0e7301a1d27b6ee617829a31f2aa423cdf5346d182733d8edf`  
		Last Modified: Wed, 12 Mar 2025 19:04:44 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
