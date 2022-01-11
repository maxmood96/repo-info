## `python:3-windowsservercore-ltsc2016`

```console
$ docker pull python@sha256:f8b2d2e329832b098366d08fcf2b7d6c3087207868c355a3ec07ed06cc87bad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4886; amd64

### `python:3-windowsservercore-ltsc2016` - windows version 10.0.14393.4886; amd64

```console
$ docker pull python@sha256:095bb57e571bd6ea126e95ee17f9a417b2f45504192822a0f051303b1551719a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6331014897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edead9fb5bf39da86333c5e298f1b3a6a0bb28ac60e2e31cb17e92c26496ffa`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 06 Jan 2022 14:33:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Jan 2022 19:14:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jan 2022 19:14:56 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 11 Jan 2022 19:14:57 GMT
ENV PYTHON_VERSION=3.10.1
# Tue, 11 Jan 2022 19:14:58 GMT
ENV PYTHON_RELEASE=3.10.1
# Tue, 11 Jan 2022 19:17:14 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Tue, 11 Jan 2022 19:17:16 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Tue, 11 Jan 2022 19:17:18 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 11 Jan 2022 19:17:19 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Tue, 11 Jan 2022 19:17:20 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Tue, 11 Jan 2022 19:19:10 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 11 Jan 2022 19:19:12 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8428508ffd63b4af1ba690ec41e82a116f10ec6c3fb70962348f5448d42e5835`  
		Size: 2.2 GB (2208216859 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9b5116c05ddf6ecb5a348f7628e3f3264afbb9909d86798316dbaff4a0e991a2`  
		Last Modified: Tue, 11 Jan 2022 19:35:13 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8b3bc3878f949fbf5438b0feb9174e5a8cc254aae43ef0d67c3edd9d0487e8`  
		Last Modified: Tue, 11 Jan 2022 19:35:12 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ae534465c536bcb4bb4d3b9dbb500346418101a39eeeac0cca9407160bd000`  
		Last Modified: Tue, 11 Jan 2022 19:35:11 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bfdbc5d5e7fec35ad32102015c33a90f5a0a43ff0b5ac23c675ea21ca3ad12`  
		Last Modified: Tue, 11 Jan 2022 19:35:10 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329ef0631d65fd66970ba1f25db27576fab75302a241b2d75f12a41765399664`  
		Last Modified: Tue, 11 Jan 2022 19:36:02 GMT  
		Size: 46.3 MB (46346646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7433eb796a7d476eb97b807e9727428a0793c83979e6d1fed191f3c6db4cc3fe`  
		Last Modified: Tue, 11 Jan 2022 19:35:10 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76b39e5936509924656b4c4c8650c2d2ee4487915c49bae88b009b824a21606`  
		Last Modified: Tue, 11 Jan 2022 19:35:09 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4659d7bd62f68c25133374a913d2ce65f64fe862457ef188768f3b22425e7ac`  
		Last Modified: Tue, 11 Jan 2022 19:35:08 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e618596ce74853539b57b3aed4f5e7f18a09c852c53a3a175430db7e151971b`  
		Last Modified: Tue, 11 Jan 2022 19:35:08 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb8710c1e584c50b576db99c8cf968b2e55942096a6f25ad229ad2292f484ea`  
		Last Modified: Tue, 11 Jan 2022 19:35:10 GMT  
		Size: 6.5 MB (6452786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f846565038c6f34d4306f60f8feaf7e97bc40152a5eafc662aa0ac29ad89d07`  
		Last Modified: Tue, 11 Jan 2022 19:35:08 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
