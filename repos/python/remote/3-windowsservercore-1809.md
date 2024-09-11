## `python:3-windowsservercore-1809`

```console
$ docker pull python@sha256:b3c25fa0cd68df034fac0a5880afccbb6fb47596670f46e48797ccd417b09037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `python:3-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull python@sha256:0c33f9d5a6f7794ae32602ad46968d26b96c0c6b3a29859657c3e50b83f338b7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1776374411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764ffbedb47978852779b2a283238f5e1e36ddbe4a6694a21677b6777d2ba2a0`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:02:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:02:37 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 11 Sep 2024 00:02:38 GMT
ENV PYTHON_VERSION=3.12.6
# Wed, 11 Sep 2024 00:03:16 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:03:17 GMT
ENV PYTHON_PIP_VERSION=24.2
# Wed, 11 Sep 2024 00:03:18 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Wed, 11 Sep 2024 00:03:19 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Wed, 11 Sep 2024 00:03:36 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		--no-setuptools 		--no-wheel 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:03:37 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f560c83830627c123ff413e55b6de3ee5fbfee6b0cbfdd207f84a0fa5dbabe`  
		Last Modified: Wed, 11 Sep 2024 00:03:43 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88bf39a9028af5262433453507c59758287c5d851762f11b4241ebc7f73270a`  
		Last Modified: Wed, 11 Sep 2024 00:03:43 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d0bf9724728478c8b391172d613631d2b9d64f19bab4d0ca7c3c72117cae9f`  
		Last Modified: Wed, 11 Sep 2024 00:03:43 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77121c0bf571784cfab197704fbb498e90cd965229a1d0fc2968387271989e65`  
		Last Modified: Wed, 11 Sep 2024 00:03:47 GMT  
		Size: 47.7 MB (47735404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4da23ad3d45bae5016923a27cbf0d6f3c0358b2d286f48bf82fc46d685f8c22`  
		Last Modified: Wed, 11 Sep 2024 00:03:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19e9c54e8d1f299556f53061dc49ee73d21034f4c2352c7f6dd7e588f25021c`  
		Last Modified: Wed, 11 Sep 2024 00:03:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e29125750ee0139846808fa3992b866b5fe50f440deb4e50c19fd15af19b23c`  
		Last Modified: Wed, 11 Sep 2024 00:03:41 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0795a182284e72abe76116249a55711a9fb740c00228b9b8f15366a3a7af5c8f`  
		Last Modified: Wed, 11 Sep 2024 00:03:42 GMT  
		Size: 8.4 MB (8361567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329efd8926be934d5fa306a5cff348e1659f96a81a237a8e5d87990967340afe`  
		Last Modified: Wed, 11 Sep 2024 00:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
