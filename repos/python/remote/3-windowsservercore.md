## `python:3-windowsservercore`

```console
$ docker pull python@sha256:df6904858a28676424aa2c2c54babbe518a42144bafa091b1d39c3768de34ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64

### `python:3-windowsservercore` - windows version 10.0.26100.4061; amd64

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

### `python:3-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull python@sha256:eea954120be856d845f9650b214430b942d71f9f63dbd6b59bfb473f2b117495
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2332728648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f46e9d24b97cb4a842c05e825fcc145ddfd3656976e207160f8902bd1876ff`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 04 Jun 2025 17:06:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Jun 2025 17:06:01 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 04 Jun 2025 17:06:01 GMT
ENV PYTHON_VERSION=3.13.4
# Wed, 04 Jun 2025 17:06:02 GMT
ENV PYTHON_SHA256=94f53bb832539ea02d6ce581d7c1fcc36228e04a611b8dcfe797ad4bbc0a45c1
# Wed, 04 Jun 2025 17:07:00 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 04 Jun 2025 17:07:02 GMT
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
	-	`sha256:5186485bd037d64b6fab9b42606ed40550235a210c8329dd303a98dd137007bb`  
		Last Modified: Wed, 04 Jun 2025 17:12:15 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8275514e3b5d959b97ad977a906a7a0e256ebe9a555bee9a01970eea179d6adb`  
		Last Modified: Wed, 04 Jun 2025 17:12:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b92f6b742d0f62e97b8757e8c8097a387f7aec5b9470d9089cee6cc433af1a9`  
		Last Modified: Wed, 04 Jun 2025 17:12:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd2094fa14194a6d8bd67fb3f93b6a2c30001ce7978346b2426c322255b0c61`  
		Last Modified: Wed, 04 Jun 2025 17:12:21 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb932e8982bfa70999cd1e2b21d29c5a2aa48e43aed1799fb2cdd0dedee21e84`  
		Last Modified: Wed, 04 Jun 2025 18:03:27 GMT  
		Size: 59.1 MB (59094011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee054360590b5f07a651a2265b40edd7821bf325b32d563e4d28abceecf2e44`  
		Last Modified: Wed, 04 Jun 2025 17:12:24 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
