## `python:windowsservercore-1809`

```console
$ docker pull python@sha256:b6dea283dc94ce8426f6a9b52dc2bebe3d2077a1caf91192202d1e1d294418f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `python:windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull python@sha256:8bab2e9e3375f97d6f783fafee0694d39c5b22364c18565ced6547281900f1a2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2764497824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:112660dfa839b233c886644dba4fd4e94b570e27ac7a03a3df4e6aa63d5b1566`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 18:28:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jan 2022 19:03:16 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 11 Jan 2022 19:10:42 GMT
ENV PYTHON_VERSION=3.10.1
# Tue, 11 Jan 2022 19:10:43 GMT
ENV PYTHON_RELEASE=3.10.1
# Tue, 11 Jan 2022 19:12:47 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Tue, 11 Jan 2022 19:12:49 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Tue, 11 Jan 2022 19:12:50 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 11 Jan 2022 19:12:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Tue, 11 Jan 2022 19:12:52 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Tue, 11 Jan 2022 19:14:34 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 11 Jan 2022 19:14:36 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d817badb08ee5a6edbd47efdaa8f9393db0c59d351be8a78deda5364ab70de7f`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1d7d79b7b7fe7eea084017c3aa788ff192ce295331911516ca7ed3fed49efc`  
		Last Modified: Tue, 11 Jan 2022 19:32:28 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e29bfbc3aa7e1de554cf147330b73987be404d8d760b8c5eabf81e10d3edb4`  
		Last Modified: Tue, 11 Jan 2022 19:34:00 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16891742685d258499fbbc1bf64f0b11187f733ae95e4b630cae3fe719198c2`  
		Last Modified: Tue, 11 Jan 2022 19:33:58 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4064a96c7c2eda2439d0313d0d74915752e5502fdd75cfdb24a6c028afa736`  
		Last Modified: Tue, 11 Jan 2022 19:34:50 GMT  
		Size: 46.4 MB (46430547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa6a92a39210fad7c8a678c7fc9ab1e6db883a1bfaf3639624081aeb83b7900`  
		Last Modified: Tue, 11 Jan 2022 19:33:58 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f74cdc51258a675425b0bb2235c9dec914b1888892e521376e38a2dc65622db`  
		Last Modified: Tue, 11 Jan 2022 19:33:56 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5091d31ac893dcbd43b524cde1ccbb1d066a2c340ccb3404cfc66c151492af96`  
		Last Modified: Tue, 11 Jan 2022 19:33:56 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51519f300b387e3b65949b6162cfce81457fc33b3a18fb8fd968be6770f058e`  
		Last Modified: Tue, 11 Jan 2022 19:33:56 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2df9d042c329ae4c3874564cc4c07c343fae3146ab82efe9724e15fba969fdb`  
		Last Modified: Tue, 11 Jan 2022 19:33:59 GMT  
		Size: 6.5 MB (6470093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa3796aba1946bb2d7ad5dbb02a353589b085ee62061f2ec832483a79d999f2`  
		Last Modified: Tue, 11 Jan 2022 19:33:56 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
