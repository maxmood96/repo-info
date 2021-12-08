## `python:windowsservercore`

```console
$ docker pull python@sha256:9132d6d418b7b6063191ad3e0114ea98404fe47e36e81ce3d334a5991d69ea39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.20348.350; amd64
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `python:windowsservercore` - windows version 10.0.20348.350; amd64

```console
$ docker pull python@sha256:10821cd58a085755db990ebe13cdc5b90705d8608cadab223dd92197986bbde9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2237981608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0716d5b1ce66a2444b171f0309f9618dc4f447b98a1d21bae018ba5c8d1adc8`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 03 Nov 2021 08:36:33 GMT
RUN Install update ltsc2022-amd64
# Wed, 10 Nov 2021 01:38:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 01:38:21 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 08 Dec 2021 03:16:00 GMT
ENV PYTHON_VERSION=3.10.1
# Wed, 08 Dec 2021 03:16:01 GMT
ENV PYTHON_RELEASE=3.10.1
# Wed, 08 Dec 2021 03:17:33 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 08 Dec 2021 03:17:37 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Wed, 08 Dec 2021 03:17:38 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 08 Dec 2021 03:17:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Wed, 08 Dec 2021 03:17:41 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Wed, 08 Dec 2021 03:18:37 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 08 Dec 2021 03:18:38 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0eb404f1860fa8786ad09d1d9fe9fd580115f83cd38623bc4eb0c46abdaa0a3`  
		Size: 932.9 MB (932907933 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:27ded59d7006d9d7bffa7c253cd04a900a5d6b0d47b84d0edd624d12fd64cdc9`  
		Last Modified: Wed, 10 Nov 2021 02:07:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf213104327874c948c49178d2338f922bb9443acdcbffa4029d62be119c81e1`  
		Last Modified: Wed, 10 Nov 2021 02:07:38 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd9c136efc767b15915b94731e130e09d816b6d4d69713990b5d99ecc2dbc73`  
		Last Modified: Wed, 08 Dec 2021 03:30:07 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bd6abd4a6da0ed4f3817ef0aa1a438f03a6578d664b367a7bcc3f36459a9ea`  
		Last Modified: Wed, 08 Dec 2021 03:30:07 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341b56a6e8f855b89e45797d12c0ad24950ab727248d9faae52f2b7710bfcb4e`  
		Last Modified: Wed, 08 Dec 2021 03:31:00 GMT  
		Size: 46.7 MB (46650506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f118097ce19c559ef586fb15c0ee238154db5a4fe30a2331822cb85907773b2`  
		Last Modified: Wed, 08 Dec 2021 03:30:07 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d957e8ba185c93f90eeac01d57c564d1443961362bd94feb24b582adede05caa`  
		Last Modified: Wed, 08 Dec 2021 03:30:05 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ceb8fc2037601fc94de21349efd49b8bfc5259c4f34afe38202174c665c4fe`  
		Last Modified: Wed, 08 Dec 2021 03:30:04 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f7a4c924964e44066235ac864d92cdbf666c1c1ab16e272a760e24d2a79a89`  
		Last Modified: Wed, 08 Dec 2021 03:30:05 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923c75f4cd622821e1eda5284d9050fca8bab4416d30fc83636e381b5f9f0521`  
		Last Modified: Wed, 08 Dec 2021 03:30:07 GMT  
		Size: 6.7 MB (6711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17dff95ceac2b81d17dfa6fbd55748897c909ceb874f81432a3152a6130b844f`  
		Last Modified: Wed, 08 Dec 2021 03:30:04 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:windowsservercore` - windows version 10.0.17763.2300; amd64

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

### `python:windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull python@sha256:005a5c42734f54f5cd21389563e4735764be86c48843b38f09f036e3e40ff197
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6330471864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d589fb473eca587fc6f8f30a61e944ff1d1467973143b823aec905d2978b36`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 01:53:27 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 08 Dec 2021 03:24:03 GMT
ENV PYTHON_VERSION=3.10.1
# Wed, 08 Dec 2021 03:24:04 GMT
ENV PYTHON_RELEASE=3.10.1
# Wed, 08 Dec 2021 03:26:35 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 08 Dec 2021 03:26:36 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Wed, 08 Dec 2021 03:26:37 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 08 Dec 2021 03:26:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Wed, 08 Dec 2021 03:26:40 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Wed, 08 Dec 2021 03:28:41 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 08 Dec 2021 03:28:42 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee32b722eae60843ab69b9a429e222c325d19f4554fc09616632500513b4739`  
		Last Modified: Wed, 10 Nov 2021 02:10:38 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749f38429f88522cfde7fdf655d8cab75b3c5873ea14091e56f7fb797600e035`  
		Last Modified: Wed, 08 Dec 2021 03:32:24 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26128560d4b0889e75a152f0eae7ba1051a24cef628f3c6ae482cb6b29c9f644`  
		Last Modified: Wed, 08 Dec 2021 03:32:24 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d1e0dcd8c5dba04bf143ff7ae1b2691fc18fc78464150e15098238cbc575dd`  
		Last Modified: Wed, 08 Dec 2021 03:32:33 GMT  
		Size: 50.9 MB (50890332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae325f3da27661753d1a1fb3aef34a110350a51c6bd4bb2239e6ed2a7fff1d57`  
		Last Modified: Wed, 08 Dec 2021 03:32:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a742e618b46d5c76cce97770cd864dd995f6dffcbeb2bb8ae01aaad708cf50`  
		Last Modified: Wed, 08 Dec 2021 03:32:22 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5e9babc8c706368be1b6e742948499c691cab8a6f6f71e112f2d875189ab7e`  
		Last Modified: Wed, 08 Dec 2021 03:32:22 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59dc6d2071ade6b8ae8e22696bdb68fec7053b2afa98c7c99bc2b35d063e92dd`  
		Last Modified: Wed, 08 Dec 2021 03:32:22 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d4d63713ca996c42838624075c40d06690405cb68ca5041db7e2120ff5283b`  
		Last Modified: Wed, 08 Dec 2021 03:32:29 GMT  
		Size: 6.5 MB (6477899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc8359f9e63883a30624390c972b39fb5ccaabb1db07ca5ddf5784a9bd5325f`  
		Last Modified: Wed, 08 Dec 2021 03:32:22 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
