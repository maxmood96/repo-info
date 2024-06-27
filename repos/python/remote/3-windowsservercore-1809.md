## `python:3-windowsservercore-1809`

```console
$ docker pull python@sha256:39210434db6b912450e36e09793597f2d6f3aea84884f2268caf11b9c1129b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `python:3-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull python@sha256:423898430ce7bf86784ddbc25a4d03647aa99acb0c6155d2bbdf9ab8c7b5bf1a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279244704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e98311f75f9d7bbf49b7a43292b0a304cffb5180e85ffb397ee5e34618124d`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Thu, 27 Jun 2024 00:15:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Jun 2024 00:15:19 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 27 Jun 2024 00:15:20 GMT
ENV PYTHON_VERSION=3.12.4
# Thu, 27 Jun 2024 00:16:39 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Thu, 27 Jun 2024 00:16:40 GMT
ENV PYTHON_PIP_VERSION=24.0
# Thu, 27 Jun 2024 00:16:40 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 27 Jun 2024 00:16:41 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 27 Jun 2024 00:17:11 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 27 Jun 2024 00:17:12 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f09dbfbfa48ab8858dfb005f1c950e47542c182b18ad0f48162e89174bf349`  
		Last Modified: Thu, 27 Jun 2024 00:17:16 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12f45c45d966dd198bf129f110e1965a9a500a0d5754cf9a9f47ad86a2a0e9`  
		Last Modified: Thu, 27 Jun 2024 00:17:16 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b85732f503830ed08960bbac305c9895f7a7d4b0c0c42e445761bfee74ab3e3`  
		Last Modified: Thu, 27 Jun 2024 00:17:15 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f1d14ebd9a61e18f1dbb7228b7d70f4008a63a99622b7b39b105d19b206fc2`  
		Last Modified: Thu, 27 Jun 2024 00:17:19 GMT  
		Size: 48.8 MB (48756905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50511c590320bad059a5165443b8d6a435a5bfec87cd74560b6718de9bead147`  
		Last Modified: Thu, 27 Jun 2024 00:17:14 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf454cf975a7d3ea012a344d14a25ed866739a843b6502eacc57c1955364dfa`  
		Last Modified: Thu, 27 Jun 2024 00:17:14 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e8ea0d97e4e4bbbf614abb78994bfa7db6b9318aa5577f7d1730a809c9c167`  
		Last Modified: Thu, 27 Jun 2024 00:17:14 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a52ab9f50465303fc94e4276d9e5cd77002964b30fc71928ca07c87c2859351`  
		Last Modified: Thu, 27 Jun 2024 00:17:15 GMT  
		Size: 9.8 MB (9797562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3727e244b839ad849feffed4cdf1e6148e8d297ccb3a03bb08f2d80595b3a895`  
		Last Modified: Thu, 27 Jun 2024 00:17:14 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
