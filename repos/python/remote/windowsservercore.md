## `python:windowsservercore`

```console
$ docker pull python@sha256:06408ee726be8e53558d0569895b33e2902f2aaa60796c0f978b841edc6d4b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `python:windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull python@sha256:d3889755591dc4ccbd310fdd7b2ae72aa545093896a87744539db2cf786672e6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556758073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176e10bbde95e78fa14423d08e161cabf8fc3847abef45ae0d5e4c5c357dab11`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Wed, 04 Feb 2026 20:04:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Feb 2026 20:04:58 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 04 Feb 2026 20:04:58 GMT
ENV PYTHON_VERSION=3.14.3
# Wed, 04 Feb 2026 20:04:59 GMT
ENV PYTHON_SHA256=b68ad91421afbbd1a628105199c8c5f6179b21ba799067a8d8c0bbac3b7defb0
# Wed, 04 Feb 2026 20:06:15 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 04 Feb 2026 20:06:15 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a7823555ed5c20d755d21033745828bc03e2ccca2d35c5b18064212ac49eba`  
		Last Modified: Wed, 04 Feb 2026 20:06:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af17caa91f12bdf234ff3a1cea719f6f0217fcff6c2028c2c2b840c41db92b75`  
		Last Modified: Wed, 04 Feb 2026 20:06:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8e04c1edecef8540b07b300fc2efcc799f17a2f1ad1d601e87b0f0889a48a8`  
		Last Modified: Wed, 04 Feb 2026 20:06:19 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2162d87dc79b7a3f65a7ab29b8564a4ef02f4ef1e987f56b953829b7f9bfc7a`  
		Last Modified: Wed, 04 Feb 2026 20:06:19 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f1db5519ae519c883f5e4d550cbc2adb83c21357d8adf12f67f5f5604b148b`  
		Last Modified: Wed, 04 Feb 2026 20:06:26 GMT  
		Size: 61.0 MB (60991232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e601fa44e3ce5bd55f385d1460fd43a70035f47e1845ae858f6b5f0d30a88d3`  
		Last Modified: Wed, 04 Feb 2026 20:06:19 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull python@sha256:e998c3558cc26fcbed7cd23910b2097b0bda0bcb913ba5c486a79ae2392c6b1c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896652649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f949cc337c8fc73d120a22130297027fd10a7eacbb8589a717cce48988dab0`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 04 Feb 2026 20:05:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Feb 2026 20:05:10 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 04 Feb 2026 20:05:11 GMT
ENV PYTHON_VERSION=3.14.3
# Wed, 04 Feb 2026 20:05:11 GMT
ENV PYTHON_SHA256=b68ad91421afbbd1a628105199c8c5f6179b21ba799067a8d8c0bbac3b7defb0
# Wed, 04 Feb 2026 20:06:26 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 04 Feb 2026 20:06:27 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09f561cc9817aa5a71306c1f7a3185d4427e4552b15b4a465e8b8457f965985`  
		Last Modified: Wed, 04 Feb 2026 20:06:33 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b8630af6c7b0ce1ea7c3a422843d98abcf56718529bc1a38039030b1094970`  
		Last Modified: Wed, 04 Feb 2026 20:06:31 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61254da76d58722ea606dcd714f15cdda3970369a24ebcca39717a9b5271070f`  
		Last Modified: Wed, 04 Feb 2026 20:06:31 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488858954fff995194657bb21432bb2e74ff0df05281e0d0c4b5d216e58476a6`  
		Last Modified: Wed, 04 Feb 2026 20:06:31 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e61b1ffea45b48b500468ef3f2eb69c7916092e68e23c4b8da9b1b861987639`  
		Last Modified: Wed, 04 Feb 2026 20:06:38 GMT  
		Size: 61.0 MB (60986898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429d69ee6c51152cf5cbe1f70b18db0873456e6e061b94185d48b11822a2a828`  
		Last Modified: Wed, 04 Feb 2026 20:06:31 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
