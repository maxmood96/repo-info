## `hylang:pypy3.9-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:2820ea6235dcdc96f328dcc1f137aa558dc2548bff5e645c208e031facb94364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `hylang:pypy3.9-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull hylang@sha256:f9f028945747aa97c4a54fe4932c6fd72f702be9dd06aa6f0cc9f42ce12b9a46
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1952908783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd18b11e3efdaaa008deda33f1dc68f455298530e759c98f8cab20fdd44ab3d2`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Tue, 16 Jan 2024 23:58:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Jan 2024 23:58:53 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 16 Jan 2024 23:59:02 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 16 Jan 2024 23:59:03 GMT
ENV PYPY_VERSION=7.3.15
# Tue, 16 Jan 2024 23:59:21 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.9-v7.3.15-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a156dad8b58570597eaaabe05663f00f80c60bc11df4a9c46d0953b6c5eb9209'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.9-v7.3.15-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 16 Jan 2024 23:59:22 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 16 Jan 2024 23:59:23 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 16 Jan 2024 23:59:44 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 16 Jan 2024 23:59:45 GMT
CMD ["pypy"]
# Wed, 17 Jan 2024 00:55:15 GMT
ENV HY_VERSION=0.28.0
# Wed, 17 Jan 2024 00:55:16 GMT
ENV HYRULE_VERSION=0.5.0
# Wed, 17 Jan 2024 00:56:14 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 17 Jan 2024 00:56:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00452a1070e759d3ca4a95365e16bb1867c3cdcf57d82a438d5867ee6a847c5`  
		Last Modified: Tue, 16 Jan 2024 23:59:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce886381b02044e8a1d042bbb847c1c5456f13b1f58f091f417b0a3521639d6a`  
		Last Modified: Tue, 16 Jan 2024 23:59:52 GMT  
		Size: 488.1 KB (488058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a62a464dabb74f7529295c33fd2895d91f3719881b048029c4ca340979cd2e4`  
		Last Modified: Tue, 16 Jan 2024 23:59:53 GMT  
		Size: 15.5 MB (15540472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79be8cdb064c3b9b386c999bb6a75b31033dad9ec54609e9bc42a09821f0cc4`  
		Last Modified: Tue, 16 Jan 2024 23:59:52 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235ad6a5eee9f35e68492928da0a4ac2fdd61ce56a3f3cbbda1acbf7a5089bfa`  
		Last Modified: Tue, 16 Jan 2024 23:59:53 GMT  
		Size: 27.6 MB (27581903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8667f2296339db4bf0d6500528ba7d6794b89bc789544981a27b5f98a717a41c`  
		Last Modified: Tue, 16 Jan 2024 23:59:49 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deda35a3ee78c246c968826f259491972c91005322cf1f1f7b1ab00cbe054790`  
		Last Modified: Tue, 16 Jan 2024 23:59:49 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516ebcdae6507a6b5cc2e9d0d57f17e6c23a2c1d61eeb85e971073eba593405c`  
		Last Modified: Tue, 16 Jan 2024 23:59:50 GMT  
		Size: 3.9 MB (3927342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600601f226b87dc441e6b11a6385c92bfac2645d74bb56e1c67957e91025160f`  
		Last Modified: Tue, 16 Jan 2024 23:59:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14442a82a872a78b2d64bb01c21d9ffefbd022b247393209871138124fefa8c1`  
		Last Modified: Wed, 17 Jan 2024 00:56:19 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aed3a9c9d56bbfc476920e5b8b69b9419c7478166c39a09950f4fbe86d54ab6`  
		Last Modified: Wed, 17 Jan 2024 00:56:18 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f673b0108cad70f1dcedacaa687f8ccb9e119efaea9b83e3a09750f0cf7757`  
		Last Modified: Wed, 17 Jan 2024 00:56:20 GMT  
		Size: 5.1 MB (5147824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f3c35c7dc66d540e9442b2d33515158126f41deba9fd1b02414cec22f0cdb4`  
		Last Modified: Wed, 17 Jan 2024 00:56:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
