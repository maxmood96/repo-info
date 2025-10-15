## `hylang:python3.13-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:795fe5c4d41c48c5091ff4b7f8baf53709abb3fc87a5b84c1dd807ff0d695d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `hylang:python3.13-windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull hylang@sha256:645b84f1dfa0925bfc45df27bff6f622603ca9ca958db130b6cad1b5adc50949
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556123599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353d8c023277b0c8a501332066c60f49ef24156eb6425a56a33d278f0a7d2bf3`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:41:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:51:12 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 14 Oct 2025 20:52:23 GMT
ENV PYTHON_VERSION=3.13.8
# Tue, 14 Oct 2025 20:52:24 GMT
ENV PYTHON_SHA256=f17f216f057ed805b653f80a607c0d97d52884b4ed00380acabf199f0c025b14
# Tue, 14 Oct 2025 20:53:05 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:53:06 GMT
CMD ["python"]
# Tue, 14 Oct 2025 21:15:19 GMT
ENV HY_VERSION=1.1.0
# Tue, 14 Oct 2025 21:15:19 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 14 Oct 2025 21:15:52 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 14 Oct 2025 21:15:53 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d69910297fad50ffc461b607623e7deea128c2f2ed652341ab8682223c1249b`  
		Last Modified: Tue, 14 Oct 2025 20:45:19 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3446127170afdeb57742ca016297854803b344289f853d2569ae7f8ad174ec26`  
		Last Modified: Tue, 14 Oct 2025 20:52:15 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d885c5709c87eb38ed5ca551ae478c2acaea0d963e4a04d984584ceea201221f`  
		Last Modified: Tue, 14 Oct 2025 20:53:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240925fe8ea52bbcb89e5be181c9962edf989d50c89b5caa3aa6313792ed85f3`  
		Last Modified: Tue, 14 Oct 2025 20:53:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3090ab8ff77be92d486f4c6349f4734d05c5fb35db552fddf6174cd395903d0d`  
		Last Modified: Tue, 14 Oct 2025 20:53:29 GMT  
		Size: 58.6 MB (58625335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab163e11bec47fdabe60798f58168275e93f8fac8c86ff39a1f9bac32446c266`  
		Last Modified: Tue, 14 Oct 2025 20:53:24 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1376c66b42fa965298026a7da68b08513dc3ee3bb8efeff4993461349ef8f16b`  
		Last Modified: Tue, 14 Oct 2025 21:16:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cbfecb83aa771acaea44711f4294c4140edd575c9e9abd9a0bd606d32082c1a`  
		Last Modified: Tue, 14 Oct 2025 21:16:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8438ac4eb00a3f57fe41c31b942e671990b128b9d07f7b9a4b8c5e8dba36a2f8`  
		Last Modified: Tue, 14 Oct 2025 21:16:11 GMT  
		Size: 8.5 MB (8468721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53da52b7d35e4a03087d2bae85ce240bd2b5317b32f8ea380b00d124ec9c97cd`  
		Last Modified: Tue, 14 Oct 2025 21:16:10 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
