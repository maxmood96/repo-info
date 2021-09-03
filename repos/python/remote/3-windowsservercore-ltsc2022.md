## `python:3-windowsservercore-ltsc2022`

```console
$ docker pull python@sha256:3960e1d72eddaca3212e7cc07788e5c8f2b78cbe0d3f66c040e528cd597261d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.169; amd64

### `python:3-windowsservercore-ltsc2022` - windows version 10.0.20348.169; amd64

```console
$ docker pull python@sha256:cc5d0e08f6915309db744bf2e3c4e4e142b507f54c193d3f3166152a57a34f76
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2309860885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105eb488c43388cc60aa93030b86cc40478484f991581fdfd049c90327abb66c`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Mon, 09 Aug 2021 15:38:40 GMT
RUN Install update ltsc2022-amd64
# Fri, 27 Aug 2021 17:23:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Sep 2021 01:15:07 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 03 Sep 2021 01:17:41 GMT
ENV PYTHON_VERSION=3.9.7
# Fri, 03 Sep 2021 01:17:42 GMT
ENV PYTHON_RELEASE=3.9.7
# Fri, 03 Sep 2021 01:18:52 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Fri, 03 Sep 2021 01:18:53 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Fri, 03 Sep 2021 01:18:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/c20b0cfd643cd4a19246ccf204e2997af70f6b21/public/get-pip.py
# Fri, 03 Sep 2021 01:18:55 GMT
ENV PYTHON_GET_PIP_SHA256=fa6f3fb93cce234cd4e8dd2beb54a51ab9c247653b52855a48dd44e6b21ff28b
# Fri, 03 Sep 2021 01:19:47 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Fri, 03 Sep 2021 01:19:48 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:393f6f5bddce764d78d9d19db836750d03ca4866c2ec9b794853a461e6f2cf63`  
		Size: 1.0 GB (1001389105 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:788c1927703ffa41d5a2f1824a9c9f2d663fdc9e50b2b49387de1cb0c1b33aa4`  
		Last Modified: Fri, 27 Aug 2021 17:40:17 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b9151efee2499c1021ea6e74f4805e04d77cb2f3931220e40b7a1c5012d7bd`  
		Last Modified: Fri, 03 Sep 2021 01:20:56 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e724eb872c9e66c85dd24c6be08931bf32188a7acf65061e6353a271175c9d88`  
		Last Modified: Fri, 03 Sep 2021 01:21:18 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df741e44b999185d1e13b88d0217c76c1e5773efb3d18ed96f8064b15de76e83`  
		Last Modified: Fri, 03 Sep 2021 01:21:17 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5190d67d952a8ecc944123570a4a81c3a6ec408908af3b822710389015458a35`  
		Last Modified: Fri, 03 Sep 2021 01:21:28 GMT  
		Size: 50.2 MB (50230759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4568f1c9eaa663d34a0051efe056a357c84d4f3fe950014e557e359bbe7805b`  
		Last Modified: Fri, 03 Sep 2021 01:21:15 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82f4fc7ec071dcf64c1d740e0b576226853dd895616cbbc8ed205671d871aa6`  
		Last Modified: Fri, 03 Sep 2021 01:21:15 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a0c16313436dfcca5e90fb55331dec5ec93d137521e27bba70f7d36dd5ca18`  
		Last Modified: Fri, 03 Sep 2021 01:21:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88db3dd0d1b318dddfb273c22a4a8078452e2b48aff669a04edd2c4eecdbc324`  
		Last Modified: Fri, 03 Sep 2021 01:21:17 GMT  
		Size: 6.5 MB (6530595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6901c283085bf6bd1303a8ff34308ca6c6fe27b3328776360e68e6ca8aad5c4f`  
		Last Modified: Fri, 03 Sep 2021 01:21:15 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
