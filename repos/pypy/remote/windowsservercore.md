## `pypy:windowsservercore`

```console
$ docker pull pypy@sha256:e9acb94a144d4b495d7c67302175244c4d37410220ab54e21f80a8efcbd445af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7009; amd64

### `pypy:windowsservercore` - windows version 10.0.26100.3775; amd64

```console
$ docker pull pypy@sha256:8fe2257d1063dbe8d1fa970a192ddce0d700722ea7a01b9f039bbe5d2ead1359
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3441375079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b33aca4721c7d3a8aac7ea4ad5b338fcbd2df0661d022b10e1df7210da16d92`
-	Default Command: `["pypy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:53:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:53:51 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:54:01 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:54:02 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 09 Apr 2025 00:54:22 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.10-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'c0d07bba6c8fb4e5804f4a8b3f8ef07cc3d89f6ad1db42a45ffb9be60bbb7cc2'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.10-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:54:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 09 Apr 2025 00:54:25 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 09 Apr 2025 00:54:49 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:54:49 GMT
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
	-	`sha256:d8f7f6a4a2d86d11a841752509b3efd36d97af7c87e12196ba13e8e8d56e2e5c`  
		Last Modified: Wed, 09 Apr 2025 00:54:57 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bfc55683dfe227ede108106a6a5c5fa133bc18a620d1910d3cb33053dfd262`  
		Last Modified: Wed, 09 Apr 2025 00:54:56 GMT  
		Size: 380.6 KB (380611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6438b3bbb6658f69782b106e4caaa5045d6fa1bb9c49591152082c55a391bf8`  
		Last Modified: Wed, 09 Apr 2025 00:54:57 GMT  
		Size: 15.6 MB (15560409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090ef6c7d8be38bb4ceba06f9b36b875eba16dee8e897cba96b80f7ce84dde69`  
		Last Modified: Wed, 09 Apr 2025 00:54:56 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efaa6e3174d18979f3fbe857a43b65ca399f138b4bfeb8d1289d547998d6623c`  
		Last Modified: Wed, 09 Apr 2025 00:54:58 GMT  
		Size: 26.8 MB (26772506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d036ac57784692138961d89f52a3115666aa51ebe342e09217479256b0b6c5c1`  
		Last Modified: Wed, 09 Apr 2025 00:54:54 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192bfdf3e65ce976d7f0c3f9225df69ea751645985f1ccdba7daa6b4760777f2`  
		Last Modified: Wed, 09 Apr 2025 00:54:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3dca0215ddc7c21a5f61dc63246f5aaa8dc259195360034e70502be0dd25982`  
		Last Modified: Wed, 09 Apr 2025 00:54:55 GMT  
		Size: 4.0 MB (3975597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3585440f0fc8d81b7faaadc5cefdc1ed05aeaf8da3a7369d29a5c840455dc2`  
		Last Modified: Wed, 09 Apr 2025 00:54:54 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:windowsservercore` - windows version 10.0.20348.3453; amd64

```console
$ docker pull pypy@sha256:811de02597dcb7b3c8db3c320958fa974fa9438bfcbf766e05142be7702c0ade
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2317533988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08649adaa69bdcc22097eb5ec0b3d2429b72551425ac250f0ab1b563fef2774e`
-	Default Command: `["pypy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 00:50:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:51:08 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:51:20 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:51:21 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 09 Apr 2025 00:51:40 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.10-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'c0d07bba6c8fb4e5804f4a8b3f8ef07cc3d89f6ad1db42a45ffb9be60bbb7cc2'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.10-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:51:41 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 09 Apr 2025 00:51:41 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 09 Apr 2025 00:52:03 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:52:04 GMT
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
	-	`sha256:ccfd52d15b779ffa89d8da9080749b4c263ee4b7470bd6e8ae5fb682a1ad1155`  
		Last Modified: Wed, 09 Apr 2025 00:52:09 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cf7e0b50f1714532731b12dd1ccb9d2174d3ddd83d9a92b0f07b5499372984`  
		Last Modified: Wed, 09 Apr 2025 00:52:08 GMT  
		Size: 346.0 KB (345994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208e03cd1ad862a4f832d89664b198feba437ebb7a8240f965d65fc024731625`  
		Last Modified: Wed, 09 Apr 2025 00:52:09 GMT  
		Size: 15.5 MB (15529474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0938bb2c97b790336d0ffb44b4a557f768df87df9e232b0aaf6e203ac107dce5`  
		Last Modified: Wed, 09 Apr 2025 00:52:08 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a74c53d27da62ab9a4a5ba444eb36de6bfa95627925f8f656261aa32e820c1`  
		Last Modified: Wed, 09 Apr 2025 00:52:11 GMT  
		Size: 26.7 MB (26722680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050eb5527476af6762509bc0a73602d9cc064246443109f1d11ba33452a0a7dd`  
		Last Modified: Wed, 09 Apr 2025 00:52:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db004e51906a5e3613a5882b1c41fa8fae0c6cdd7a84b8a5a6e6d1f6067da61a`  
		Last Modified: Wed, 09 Apr 2025 00:52:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015f8a1dffb9af253185642900ceb7fbf2288148d59da9094aefbd4ec7a4bef9`  
		Last Modified: Wed, 09 Apr 2025 00:52:08 GMT  
		Size: 3.9 MB (3933708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c423372199629d9337fccf6362a5d6c8feafdc6ba3e9bd30b63e3796fff212`  
		Last Modified: Wed, 09 Apr 2025 00:52:07 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull pypy@sha256:f6be68e64afc80400ce10fd00059ead01f31b8f148f507ee1b469c0aed218059
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2198075415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e601c59085563b96710e7cfcee57c84d6339a5eaca16f0b53124bf2dabc83e29`
-	Default Command: `["pypy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 19:02:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 19:03:11 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:03:31 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:03:31 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 12 Mar 2025 19:03:53 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.10-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'c0d07bba6c8fb4e5804f4a8b3f8ef07cc3d89f6ad1db42a45ffb9be60bbb7cc2'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.10-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:03:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 12 Mar 2025 19:03:55 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 12 Mar 2025 19:04:18 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:04:19 GMT
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
	-	`sha256:da1ead927c0791df8b877b6816f421e00c3de1918c724f5eff2ca0555f2123ec`  
		Last Modified: Wed, 12 Mar 2025 19:04:23 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2281273879134f7c1b55858abd9c8751d5dbc20bc00dc8a858ac4a270dd687`  
		Last Modified: Wed, 12 Mar 2025 19:04:23 GMT  
		Size: 329.1 KB (329120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759b0fd295acab9d130f00c605964d5380ad68c1d541c66ca6f3469e7cb51090`  
		Last Modified: Wed, 12 Mar 2025 19:04:24 GMT  
		Size: 15.5 MB (15500867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27651f5116d1609f170bff4c0170da2239c901355e0595ec9963c9715a606e1`  
		Last Modified: Wed, 12 Mar 2025 19:04:23 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39b73c0d1fa4586f5b8564015c757883296b5fb8b9306110184eab035e757d9`  
		Last Modified: Wed, 12 Mar 2025 19:04:25 GMT  
		Size: 26.7 MB (26706123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15094d778815a1cd76163b27677701b20e13629b3c419b5ed020777375ce67c8`  
		Last Modified: Wed, 12 Mar 2025 19:04:22 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d255d239cb95830969fa62c574fb6ea748799d1e96b30ae4dcfdad97ec5eb798`  
		Last Modified: Wed, 12 Mar 2025 19:04:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca0d8d05b1caddc44d774783ef709090dfab46cf3a9e21b60e6b6a4baf6a701`  
		Last Modified: Wed, 12 Mar 2025 19:04:22 GMT  
		Size: 3.9 MB (3898176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6929da386a3b6b53b9338fe8526425b83c8e9d00f5daf4775c43e8b3f35429c`  
		Last Modified: Wed, 12 Mar 2025 19:04:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
