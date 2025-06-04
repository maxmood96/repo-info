## `python:windowsservercore-ltsc2025`

```console
$ docker pull python@sha256:15cdfbef2fbb28bf29d3836ca5e351f9b20211f48f91ee9b5750835bc9f92f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `python:windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull python@sha256:d028fd20a3b7f6d44cbbf3f1fcd80f9ebd447a78d61fd4643743b5d4f56b2a40
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3490042121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ae8517e59ced561ddef794ef32d413f171ae5c671b9a1accc3a78b4530bf50`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Wed, 04 Jun 2025 17:11:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Jun 2025 17:11:56 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 04 Jun 2025 17:11:58 GMT
ENV PYTHON_VERSION=3.13.4
# Wed, 04 Jun 2025 17:11:59 GMT
ENV PYTHON_SHA256=94f53bb832539ea02d6ce581d7c1fcc36228e04a611b8dcfe797ad4bbc0a45c1
# Wed, 04 Jun 2025 17:12:39 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 04 Jun 2025 17:12:39 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d844406468f54b2d256ef459751156eaffe1f99067b32f5e1fa0e0d2c5f1a0`  
		Last Modified: Wed, 04 Jun 2025 17:16:11 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64faa7383e1a26922df38d2dda041a11534a65688365cf86a5b373e203213e84`  
		Last Modified: Wed, 04 Jun 2025 17:16:11 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c01816d5003bc3f106156ba48219f8d16d58e5047f3bb07b35bfe4a6b21d994`  
		Last Modified: Wed, 04 Jun 2025 17:16:12 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60fe2f17b148b0744b4daa1beca63ac05ae04f3ac03482f8181dfe6bf26b27c`  
		Last Modified: Wed, 04 Jun 2025 17:16:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07273f72c6468638cec183aebf6e5b6a39e384f873adc08f068c6b49bc9d203a`  
		Last Modified: Wed, 04 Jun 2025 17:16:19 GMT  
		Size: 59.3 MB (59269778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd8a7c7fa1d7d8da9564c3ae7fd17c176f7328e6164a882deef9098b97227eb`  
		Last Modified: Wed, 04 Jun 2025 17:16:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
