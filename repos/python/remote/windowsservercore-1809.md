## `python:windowsservercore-1809`

```console
$ docker pull python@sha256:c690ba4b6c5970ada3efc6b16ca4fcc1d26012464e3479a1086bd80745d608ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `python:windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull python@sha256:fab03495a9967e27bf87a4d27bc33048cf73f64aa19e0a1aa75e27b583fb8027
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2759066696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43a48db1eb9f6aac4c64aca35a894c0fd991f9ddaa985c7504bb562513ba530`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 01:42:04 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 08 Dec 2021 03:18:58 GMT
ENV PYTHON_VERSION=3.10.1
# Wed, 08 Dec 2021 03:18:59 GMT
ENV PYTHON_RELEASE=3.10.1
# Wed, 08 Dec 2021 03:21:30 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 08 Dec 2021 03:21:31 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Wed, 08 Dec 2021 03:21:32 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 08 Dec 2021 03:21:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Wed, 08 Dec 2021 03:21:35 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Wed, 08 Dec 2021 03:23:49 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 08 Dec 2021 03:23:51 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee2ce0a831648c226fdfd8a770d37d8e9c0650713bff4b3ffcea537a7e6a678`  
		Last Modified: Wed, 10 Nov 2021 02:08:43 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e269839ee626915677236659aa4ed6ab0cfa66f483b7c22fa796b80a67aa8eda`  
		Last Modified: Wed, 08 Dec 2021 03:31:18 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed77e38a44a9b7e006c764b4864babf4b5ed32b5aa9652971f678cada8e212b`  
		Last Modified: Wed, 08 Dec 2021 03:31:18 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29f045051ba4d45459deb3f3fac4a1e7e6a676bcfc16f4e38054bd937e6719f`  
		Last Modified: Wed, 08 Dec 2021 03:32:07 GMT  
		Size: 46.4 MB (46443848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbeef802395bf0f3e4499495e26bd3528f32e9cbcb0c96dfdc065d29bfe2ae3`  
		Last Modified: Wed, 08 Dec 2021 03:31:18 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3137c08ca1466393634c5dd01fd8308b8e697ef812cc7e005f4662ec5a924770`  
		Last Modified: Wed, 08 Dec 2021 03:31:15 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7efa0375313f6df30186a7eab7ee42ad22fabc08a7fc3973cc26668cbf11697`  
		Last Modified: Wed, 08 Dec 2021 03:31:15 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c204cd6629ad1eba9d225c403d71c003f147e128c97c2d33957a6dabb80c21`  
		Last Modified: Wed, 08 Dec 2021 03:31:16 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa4e3c8d5b87899752474be5815fa44ecb4fc4e86aaae9b93e0794fae917b22`  
		Last Modified: Wed, 08 Dec 2021 03:31:18 GMT  
		Size: 6.5 MB (6488933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f6d3f2fbb5ec29b7c22aabcab7ebc1548fc8c1599ea7e44cdea03f9c0b58fc`  
		Last Modified: Wed, 08 Dec 2021 03:31:15 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
