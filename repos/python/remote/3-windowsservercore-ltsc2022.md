## `python:3-windowsservercore-ltsc2022`

```console
$ docker pull python@sha256:545d68366e33f3b34388c15a6a130e72d05ab2327f1bbb2a7199042d381375d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.350; amd64

### `python:3-windowsservercore-ltsc2022` - windows version 10.0.20348.350; amd64

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
