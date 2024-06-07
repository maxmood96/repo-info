## `python:windowsservercore-1809`

```console
$ docker pull python@sha256:b00a21015c4b57f87007acf7dc430a439251900016a153e6d15d8c766760d05b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `python:windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull python@sha256:443c6aa459d837f0474fb394cb42edd20cf701b585565433a22ca4eeb4435b6b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2238117013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531f7ed71b4e3e51e878baee313ba7b357e81caa3c9d3d9ca516523d732e0b30`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 19:38:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:46:30 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 07 Jun 2024 19:26:17 GMT
ENV PYTHON_VERSION=3.12.4
# Fri, 07 Jun 2024 19:28:36 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Fri, 07 Jun 2024 19:28:37 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 07 Jun 2024 19:28:38 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 07 Jun 2024 19:28:39 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 07 Jun 2024 19:30:19 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Fri, 07 Jun 2024 19:30:21 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716a2aa6d68dd7a7e7745c65cd54a1e2713d737d3f4fdd07e5e1c2fce38b5d24`  
		Last Modified: Wed, 15 May 2024 20:44:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473733cedcfb3913e217a092138e80e13efc814222894dc6d8d80771bc989b8f`  
		Last Modified: Wed, 15 May 2024 23:05:39 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b6f723df9557bb9774723ce0bd60ea55e652504a5bf4803ecca884216ecb87`  
		Last Modified: Fri, 07 Jun 2024 20:16:34 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac1d8ea7a5ef7bc1d8cb99954b3fb1ebc6a9515c95d817dedd2823ee35b0c60`  
		Last Modified: Fri, 07 Jun 2024 20:16:40 GMT  
		Size: 48.7 MB (48709697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda6738b4c8df1861c031d5deac7a0634062d22451ea90dbfdcf31fbff847e50`  
		Last Modified: Fri, 07 Jun 2024 20:16:32 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ede6b03728ee3003909f4fa8609ef8b6d0a6c6d53300b865a6bcd88fcb92e5`  
		Last Modified: Fri, 07 Jun 2024 20:16:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55324ce920ec7422837b03d7cccac1bf2a9d15d1412f787465980a00d4788e72`  
		Last Modified: Fri, 07 Jun 2024 20:16:32 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e1fcac9311e199f39f854c62599670cfd838448f58aa8f17287ec5fffd5997`  
		Last Modified: Fri, 07 Jun 2024 20:16:34 GMT  
		Size: 9.7 MB (9685941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940e48ebd5e1b71946489a257817675bda19071570b8e0d7a7aee2dda999ab22`  
		Last Modified: Fri, 07 Jun 2024 20:16:32 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
