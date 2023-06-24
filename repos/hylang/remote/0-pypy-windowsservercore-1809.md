## `hylang:0-pypy-windowsservercore-1809`

```console
$ docker pull hylang@sha256:34b3aa4c316945b3c4b6894a1e83dec5116d3555ae82053b4bfe9ed25ddff5d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `hylang:0-pypy-windowsservercore-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull hylang@sha256:c8c11af2618111c3f14a53f606d134e988467e35d8fbef507d317f5bb2b0851c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1700997940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ce4a147a0559849dba4ce37af818f56554fc47a188041a51f0efad5427d16f`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:40:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 05:34:57 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Sat, 24 Jun 2023 05:35:33 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Sat, 24 Jun 2023 05:35:34 GMT
ENV PYPY_VERSION=7.3.12
# Sat, 24 Jun 2023 05:41:26 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.9-v7.3.12-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '0996054207b401aeacace1aa11bad82cfcb463838a1603c5f263626c47bbe0e6'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.9-v7.3.12-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Sat, 24 Jun 2023 05:41:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Sat, 24 Jun 2023 05:41:28 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Sat, 24 Jun 2023 05:42:41 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Sat, 24 Jun 2023 05:42:42 GMT
CMD ["pypy"]
# Sat, 24 Jun 2023 06:16:13 GMT
ENV HY_VERSION=0.26.0
# Sat, 24 Jun 2023 06:16:14 GMT
ENV HYRULE_VERSION=0.3.0
# Sat, 24 Jun 2023 06:18:32 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Sat, 24 Jun 2023 06:18:33 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58717a727cd3a756d7c1180dfb74e95d49735ed12628bd25d2058bc90fa96991`  
		Last Modified: Sat, 24 Jun 2023 01:20:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4364ada14698d2eda7d3752a78e31d6af867a89b0eac2760a772ae57a6cbf`  
		Last Modified: Sat, 24 Jun 2023 05:50:54 GMT  
		Size: 305.6 KB (305595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832619dc643d543e1c4630feee3e3e8e0eac347c4cd2629305c922c835861e2a`  
		Last Modified: Sat, 24 Jun 2023 05:50:56 GMT  
		Size: 15.4 MB (15436921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd88d6c9cdc098f48777121793f33fddf37f06656d763ef542b5e92210659305`  
		Last Modified: Sat, 24 Jun 2023 05:50:54 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b205e4cfc0b5d518e8aeda31dc208ec839385d47028b05b078cc6351379841d3`  
		Last Modified: Sat, 24 Jun 2023 05:51:48 GMT  
		Size: 26.5 MB (26495543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44c8179911460b9f2fda6385d07dadd4025d996ed37c0b6657319df10412d50`  
		Last Modified: Sat, 24 Jun 2023 05:51:41 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3908394bf2427c6d166c9ab5aa2aa67458d24da13ce07e308a39e24be97ef1a4`  
		Last Modified: Sat, 24 Jun 2023 05:51:41 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2f9feefb24e284b820a7164a59a354219b7ea106d66c453d9ab1464a7ce038`  
		Last Modified: Sat, 24 Jun 2023 05:51:43 GMT  
		Size: 3.4 MB (3437606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275d204fd8ff95e251c859826dfe48c7a659571ee8c4c17b1d76d1952a11a466`  
		Last Modified: Sat, 24 Jun 2023 05:51:41 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41af3dfb757c5a2519fa9f05bda36550cd5f377dd9c13771a65d5535def5033e`  
		Last Modified: Sat, 24 Jun 2023 06:19:48 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e13dfb38340bea3e0409f01be8aa9d04863d1d6fa5d69b08a54deeada73553`  
		Last Modified: Sat, 24 Jun 2023 06:19:48 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f824b593a924896741235da0e934a0544c2934108bb7672ffaf7525c4f2d1774`  
		Last Modified: Sat, 24 Jun 2023 06:19:51 GMT  
		Size: 4.6 MB (4574231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43d8c4e4cefa80f0d8b141dbfa10cf82eb20db0a4cf0ccaf87eef15ef2c8b8c`  
		Last Modified: Sat, 24 Jun 2023 06:19:48 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
