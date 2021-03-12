## `python:windowsservercore-ltsc2016`

```console
$ docker pull python@sha256:6aecb7fc8da3c79da007bab9c381c29237cc3a528f90485cf9654b5793e712e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4283; amd64

### `python:windowsservercore-ltsc2016` - windows version 10.0.14393.4283; amd64

```console
$ docker pull python@sha256:238f32f98492b75484d1f00f8cfb91deafd0d5b692ead87e2dadce9b718c1984
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5872315635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708a275597fcefecfdf27835b7be053d6fc16575aeaa026e40344613e6eb8a8f`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Mar 2021 18:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Mar 2021 13:42:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Mar 2021 17:06:22 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 10 Mar 2021 17:14:04 GMT
ENV PYTHON_VERSION=3.9.2
# Wed, 10 Mar 2021 17:14:05 GMT
ENV PYTHON_RELEASE=3.9.2
# Wed, 10 Mar 2021 17:16:33 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Wed, 10 Mar 2021 17:16:34 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Wed, 10 Mar 2021 17:16:35 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Wed, 10 Mar 2021 17:16:36 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Wed, 10 Mar 2021 17:18:33 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 10 Mar 2021 17:18:34 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30bda99601c5cbd3b2118409f401852ea648e2319bd81518723e476b28d764c5`  
		Size: 1.7 GB (1726924885 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:76680da9dc6db108ddf2e353c494b45e8486a6751619a13ed8fb3ad64b9a16e9`  
		Last Modified: Wed, 10 Mar 2021 14:06:08 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125fe0eea998b84d015b04287600700e6c6b273702461066209a3d1b9df51d0`  
		Last Modified: Wed, 10 Mar 2021 17:27:40 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed2e9a44384a6d453a04b3313aaa12467471d177d8c0ed4980d82be57c4ea15`  
		Last Modified: Wed, 10 Mar 2021 17:28:47 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdbad875fe96756c8299fe929c78e5423c7a400ef49b1dee295f5df8c019e439`  
		Last Modified: Wed, 10 Mar 2021 17:28:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b403c9d04546f8c300967f024060d3996779400e3a50bf9e74b22e3ee575e80`  
		Last Modified: Wed, 10 Mar 2021 17:28:56 GMT  
		Size: 59.7 MB (59696576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b295d07e874de0e134b80bb9067428afad98fac5f8a3882694e66b4b0dce4d1b`  
		Last Modified: Wed, 10 Mar 2021 17:28:43 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bfe82913f6294c6f655377f2dc26edc587734a94fb83783ad92a0d7ea3d325`  
		Last Modified: Wed, 10 Mar 2021 17:28:44 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e45e00b9ab192f80d299a33a043e4a4e933540f39f05bdace8e89878dd48bd`  
		Last Modified: Wed, 10 Mar 2021 17:28:43 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82f656531e8942eb7a4967bf407d1b5a97212554388f0ef8549caf41f1181df`  
		Last Modified: Wed, 10 Mar 2021 17:28:47 GMT  
		Size: 15.7 MB (15696959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e1ed09d483a2ef163c76967626b23ae6432b2c12f9ed8ffe74b0eba7525fef`  
		Last Modified: Wed, 10 Mar 2021 17:28:46 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
