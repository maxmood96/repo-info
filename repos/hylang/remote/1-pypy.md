## `hylang:1-pypy`

```console
$ docker pull hylang@sha256:6d1711309aa28d2ec31707a60cb9ded6cf614f8f07f1cc04f9561b61d3f15a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `hylang:1-pypy` - windows version 10.0.20348.2700; amd64

```console
$ docker pull hylang@sha256:f9d6133befbf4ace12a083e801c35bd624aaaf503b55b3bffc9486a648719930
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1515762977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ac3802e21c1ba18c6fe8f8b8e85b6e9f281b58a4bcc95cec1657a3b7036dc1`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:01:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:01:51 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:02:33 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:02:35 GMT
ENV PYPY_VERSION=7.3.17
# Wed, 11 Sep 2024 00:03:41 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.10-v7.3.17-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'cab794a03ddda26238c72942ea6f225612e0dc17c76cac6652da83a95024e6e8'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.10-v7.3.17-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:03:44 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 11 Sep 2024 00:03:50 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 11 Sep 2024 00:04:14 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:04:14 GMT
CMD ["pypy"]
# Tue, 24 Sep 2024 01:02:51 GMT
ENV HY_VERSION=1.0.0
# Tue, 24 Sep 2024 01:02:52 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 24 Sep 2024 01:04:39 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 24 Sep 2024 01:04:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb25f82b1aa60155539545208c6bf3749c60e56256da2d899a87306427b19f43`  
		Last Modified: Wed, 11 Sep 2024 00:04:21 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1df4875969466c9d7ab67f4f69669dbd2bcf24f66663bbed547da732093c36c`  
		Last Modified: Wed, 11 Sep 2024 00:04:21 GMT  
		Size: 358.8 KB (358759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2410858e508045647c0fbce7e78143e1d73b8f6c2a1d8eef421278aca7a41b5`  
		Last Modified: Wed, 11 Sep 2024 00:04:22 GMT  
		Size: 15.5 MB (15530786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7c65175dd66e6a6c2da2dda1568b73ed75a5daccffffdddf7bb9ea8595531a`  
		Last Modified: Wed, 11 Sep 2024 00:04:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61833721382abb520125871f254f11e66f279215060c47bdcfda9bcf6e68be10`  
		Last Modified: Wed, 11 Sep 2024 00:04:22 GMT  
		Size: 26.4 MB (26442511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3006e397620a955348cd5cffb4214d2c69eeebe9f8ec0c0640a44a7528f5aeda`  
		Last Modified: Wed, 11 Sep 2024 00:04:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad67fe9bf2f2a1f212f79ef717ff66624f2d05b578624d21fdffab57546a3b29`  
		Last Modified: Wed, 11 Sep 2024 00:04:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3caa8d494919928fed7dd18e8c68cdf3d064e1b6d72b26756eb970cb4bf84e`  
		Last Modified: Wed, 11 Sep 2024 00:04:19 GMT  
		Size: 3.9 MB (3911248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecba01d7fbeb7115adff01659a92006a6af3f940fad78bc3c83b21f7efcd2470`  
		Last Modified: Wed, 11 Sep 2024 00:04:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8430d7de90cc0abb2d900e8720df670a7d2f868ac4e240fb81aa30aa6d66d207`  
		Last Modified: Tue, 24 Sep 2024 01:04:42 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4285617c59f5f1d21560f472725d50e3dcb94807688bfab32e07fe159d97fca1`  
		Last Modified: Tue, 24 Sep 2024 01:04:42 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5246b0f3aed774f7afa490e2e8edc223e16a7aaad1e1079db1ef384ca613cb1`  
		Last Modified: Tue, 24 Sep 2024 01:04:43 GMT  
		Size: 7.3 MB (7316929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175627c33be33539ba1dddc202a7a0f090a50111d16618ee73da6e1335600663`  
		Last Modified: Tue, 24 Sep 2024 01:04:43 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-pypy` - windows version 10.0.17763.6293; amd64

```console
$ docker pull hylang@sha256:f2d5b305224a4349ec704e57cea9ab70fd432c97e05842d1a046459703616d31
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1773744820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031b3923e438683a4ac217118c594a49b8224ce8ef81f9102c750f6b8665a63c`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:05:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:05:22 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:05:54 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:05:55 GMT
ENV PYPY_VERSION=7.3.17
# Wed, 11 Sep 2024 00:07:45 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.10-v7.3.17-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'cab794a03ddda26238c72942ea6f225612e0dc17c76cac6652da83a95024e6e8'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.10-v7.3.17-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:07:47 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 11 Sep 2024 00:07:48 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 11 Sep 2024 00:08:24 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:08:24 GMT
CMD ["pypy"]
# Tue, 24 Sep 2024 01:01:49 GMT
ENV HY_VERSION=1.0.0
# Tue, 24 Sep 2024 01:01:51 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 24 Sep 2024 01:03:16 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 24 Sep 2024 01:03:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f50f0a6841306396beedd592c8c805f7bd62c11fb8f64b1d26c65abc72f7a6`  
		Last Modified: Wed, 11 Sep 2024 00:08:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5f6633fe81d423773822716e6ea3d812d325f81038b9324b70939a94c5ea33`  
		Last Modified: Wed, 11 Sep 2024 00:08:28 GMT  
		Size: 333.2 KB (333231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab4079cda8af652a86f6b8d6ebb4077cf61e6b9568af3aeea8567039714e9f5a`  
		Last Modified: Wed, 11 Sep 2024 00:08:30 GMT  
		Size: 15.5 MB (15502992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac8c68b232cfee63cb42b709a1ad052b52eeaba022e1611b842c40f4583a12f`  
		Last Modified: Wed, 11 Sep 2024 00:08:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f425305633bb6742974da66a8810042de75a72562000926437bd87e4fcda8a`  
		Last Modified: Wed, 11 Sep 2024 00:08:31 GMT  
		Size: 26.4 MB (26430019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513661c61e6e23f066ee7653148cae24ed1853a12ab13f8ea282fff1e59539f7`  
		Last Modified: Wed, 11 Sep 2024 00:08:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43efd8ea8e68ca6760bc2ed90a158806cf507171076867979c4279837579a42`  
		Last Modified: Wed, 11 Sep 2024 00:08:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60051a8e84cc9aaa70d6e144bdb56ab3e64655ef6f1a3b63051a9a5efa87cd6c`  
		Last Modified: Wed, 11 Sep 2024 00:08:28 GMT  
		Size: 3.9 MB (3900788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dc20928c89ccc11f0e9bb7c1e1d769fa4c05807222945c3636c8b189927c4d`  
		Last Modified: Wed, 11 Sep 2024 00:08:27 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2e10c315dc222f04a7c90799dcf6c22eb501d7647f9f2471f431bf3e03cd9c`  
		Last Modified: Tue, 24 Sep 2024 01:03:21 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069dbb6e9226504807c0b32c76be42feb3db6d99d587f85c2280465d4397c962`  
		Last Modified: Tue, 24 Sep 2024 01:03:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6d591a999f5acfdbbe79e24e66e6a22fc268e9a3b774bc7dd1f4f26875eeaf`  
		Last Modified: Tue, 24 Sep 2024 01:03:22 GMT  
		Size: 7.3 MB (7299068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9334a4157e7e47b9ba583474ceff7f01b5e181b5121bc6a2576a36767f7532`  
		Last Modified: Tue, 24 Sep 2024 01:03:21 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
