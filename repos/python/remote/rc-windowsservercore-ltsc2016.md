## `python:rc-windowsservercore-ltsc2016`

```console
$ docker pull python@sha256:45ad4eabbb1e19f5753dd38846d3875e10179401a506cecf3d0245a26737d73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3866; amd64

### `python:rc-windowsservercore-ltsc2016` - windows version 10.0.14393.3866; amd64

```console
$ docker pull python@sha256:1c73405e756a4c81decc9a96e5bc031acb4e6f45d3c643efcaa9d5c3c449293d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5812706953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6cdbf96c0c1990f14d27db116ce7fe06d29d3e8b5c6f75e1da921e5e5bc60f6`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Aug 2020 20:31:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 18:35:37 GMT
ENV PYTHON_VERSION=3.9.0rc1
# Wed, 12 Aug 2020 18:35:38 GMT
ENV PYTHON_RELEASE=3.9.0
# Wed, 12 Aug 2020 18:37:58 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Wed, 12 Aug 2020 18:37:58 GMT
ENV PYTHON_PIP_VERSION=20.2.2
# Wed, 12 Aug 2020 18:37:59 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/5578af97f8b2b466f4cdbebe18a3ba2d48ad1434/get-pip.py
# Wed, 12 Aug 2020 18:38:00 GMT
ENV PYTHON_GET_PIP_SHA256=d4d62a0850fe0c2e6325b2cc20d818c580563de5a2038f917e3cb0e25280b4d1
# Wed, 12 Aug 2020 18:39:41 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 12 Aug 2020 18:39:42 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:32838d9637dc39d4acee78700b0f93d6c8c9d2db755f12c8009c1b51687d3fbd`  
		Last Modified: Tue, 11 Aug 2020 20:54:28 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e999590307437ef69d5668781881240a81466ddd8e049d8b61093b17d8fbf92`  
		Last Modified: Wed, 12 Aug 2020 18:43:30 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e25404c360b965b617518d85873280986cd7734add7cc95620a96b4cfa3680`  
		Last Modified: Wed, 12 Aug 2020 18:43:28 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97821c37be6420b378518d354519ec0f874094481e7cbbd14328bd1d445b5b7f`  
		Last Modified: Wed, 12 Aug 2020 18:43:38 GMT  
		Size: 59.1 MB (59104044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4d6d51d9169e8171b46c3aee52f3e08b3de528f80e9b8f0879d14ed013276f`  
		Last Modified: Wed, 12 Aug 2020 18:43:26 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a156ad0f2ab12974a2938f6d1bafa8ebec1e4ab57833aa35dbb3e6148e6792e`  
		Last Modified: Wed, 12 Aug 2020 18:43:26 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66358c7d5c881f0835520c70d3c6475adb8511b3cf1b6c5aff50fc952ee3b940`  
		Last Modified: Wed, 12 Aug 2020 18:43:25 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9238e270b1fbe909dbde6fef8dc3218caaba429132e3ec83af8dbf53dfbbc4df`  
		Last Modified: Wed, 12 Aug 2020 18:43:30 GMT  
		Size: 15.4 MB (15447526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b349969b5261d561d0c69238d03537cc11390706aa1b66a86e15b08fd187d4e`  
		Last Modified: Wed, 12 Aug 2020 18:43:25 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
