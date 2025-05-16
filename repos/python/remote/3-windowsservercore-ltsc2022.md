## `python:3-windowsservercore-ltsc2022`

```console
$ docker pull python@sha256:673d5f03e81550c964341cb7ebe83f89239cadf5270b6f3e677321b5b0158f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `python:3-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull python@sha256:a656895d12a8720ae66e221c597bb572c6cbcf1000efcc8c473534ee425d8b4d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2332810450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eae9a08e609b5a5e63fc0ae2f99dc106b8dc89617b5b9279d6e48ccd3bc73ed`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 21:07:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:07:36 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 14 May 2025 21:07:37 GMT
ENV PYTHON_VERSION=3.13.3
# Wed, 14 May 2025 21:07:37 GMT
ENV PYTHON_SHA256=698f2df46e1a3dd92f393458eea77bd94ef5ff21f0d5bf5cf676f3d28a9b4b6c
# Wed, 14 May 2025 21:08:17 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 14 May 2025 21:08:18 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff0e4dd7efa5989e8bc4bafdbae8281cfe3b6c6e1fb0ace7c967f6875197e87`  
		Last Modified: Thu, 15 May 2025 20:01:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8439e54412a351baecd7ee30786516c6f5036f5b96608f42509eac909a0f390`  
		Last Modified: Thu, 15 May 2025 20:01:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b713148db48039f3c25322ba75c80b23161d10cd5c7e302ebfc4e702adadda`  
		Last Modified: Thu, 15 May 2025 20:01:24 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f054dc4466e7987629a9722e60275374536c2c3b29703e2b2d07192cd059fe13`  
		Last Modified: Thu, 15 May 2025 19:23:48 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74235f4593ddfb2baac17bcb20948f042e338a4f0f37d56bf9925093b3b088e0`  
		Last Modified: Thu, 15 May 2025 20:01:32 GMT  
		Size: 59.2 MB (59175874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6268e252e5779b0bc804c98ddc3a45ab90d41933b87b6b7dfc90e071f972fd6`  
		Last Modified: Thu, 15 May 2025 19:23:48 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
