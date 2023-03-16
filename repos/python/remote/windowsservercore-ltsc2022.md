## `python:windowsservercore-ltsc2022`

```console
$ docker pull python@sha256:e5b77b2bd9530db7387c93727fa53658e49e7b9d5f150a2aaa6ae7fb6063b769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1607; amd64

### `python:windowsservercore-ltsc2022` - windows version 10.0.20348.1607; amd64

```console
$ docker pull python@sha256:f84bcd8bdd919791503c7df6834b745596ec1fbf85ce96d7a364b83c2c26fc2d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1770759200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b4d5c27b7af215cbc881f75fc197f64f58a01d7c44d6ddec17da501f8c37f5`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 10 Mar 2023 06:37:36 GMT
RUN Install update 10.0.20348.1607
# Thu, 16 Mar 2023 00:38:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Mar 2023 07:40:54 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 16 Mar 2023 07:49:19 GMT
ENV PYTHON_VERSION=3.11.2
# Thu, 16 Mar 2023 07:50:55 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Thu, 16 Mar 2023 07:50:56 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Thu, 16 Mar 2023 07:50:57 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 16 Mar 2023 07:50:58 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d5cb0afaf23b8520f1bbcfed521017b4a95f5c01/public/get-pip.py
# Thu, 16 Mar 2023 07:50:59 GMT
ENV PYTHON_GET_PIP_SHA256=394be00f13fa1b9aaa47e911bdb59a09c3b2986472130f30aa0bfaf7f3980637
# Thu, 16 Mar 2023 07:52:22 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 16 Mar 2023 07:52:24 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c921d7eac594f5e3ce3ef10adb8fd0f71bdbb713c4854336b995d25f89c44d42`  
		Last Modified: Thu, 16 Mar 2023 01:41:04 GMT  
		Size: 327.9 MB (327911088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bca4593035ae0e8d1b6e6eb1b053fddc6a6824b28f45f99de726d752d2c0f72`  
		Last Modified: Thu, 16 Mar 2023 01:39:50 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd97074c3f9b465d0ad8267ca2ad1662279ea7cc6464b4b890b784732671ae6`  
		Last Modified: Thu, 16 Mar 2023 08:07:56 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f1b2ac2abf4c00e18c5c1938870df98baf17a14c4c4b77901e34f8299e6a37`  
		Last Modified: Thu, 16 Mar 2023 08:08:46 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fded7f7cd38442ead2a2c18b18920655e298ba823168ccafd6e836b789e070`  
		Last Modified: Thu, 16 Mar 2023 08:08:57 GMT  
		Size: 50.9 MB (50889349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123ddbda3f518ee53e49407866c429f5c8b5fc7d5bc45ebad43d299e3658fba5`  
		Last Modified: Thu, 16 Mar 2023 08:08:45 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b0647c54da0622a29d5c82433557e7d3dd6672bec21ef3a19fb5deaba48384`  
		Last Modified: Thu, 16 Mar 2023 08:08:42 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7279787233d5ba2412b6e93c1c30a6fcd082d3c88fbd14a58cb3f198be4cce2e`  
		Last Modified: Thu, 16 Mar 2023 08:08:42 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5b72e84bd5ead4715440ddfac68f66ffe2cb6842e3afbe41e7a9eec129022a`  
		Last Modified: Thu, 16 Mar 2023 08:08:42 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3675868aa3ef1ef0de11f582d9f3e0a79758f0905a237b74d30d2c1a22d5fca1`  
		Last Modified: Thu, 16 Mar 2023 08:08:45 GMT  
		Size: 5.9 MB (5918460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a53f626a06b1c9a1ff6372996c3eae33795ba6ff68cad41b639ca7b8636ae0`  
		Last Modified: Thu, 16 Mar 2023 08:08:42 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
