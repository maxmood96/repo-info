## `python:3-windowsservercore-ltsc2025`

```console
$ docker pull python@sha256:14a945dc6ceec4123a2bf7ac3fdf9c44e286bdcf0a61e73d237048856498567c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `python:3-windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull python@sha256:faa635c8f4910e20d159dc1fb87f4f4f9bedaca89355d7b3bc5a7decb2854c0b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2026126882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d2fabce14f1a9c5b149c93a11b8aae67a152fb488c77c906b8ebbbd31c8aad`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:52:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 23:00:37 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 10 Feb 2026 23:00:38 GMT
ENV PYTHON_VERSION=3.14.3
# Tue, 10 Feb 2026 23:00:39 GMT
ENV PYTHON_SHA256=b68ad91421afbbd1a628105199c8c5f6179b21ba799067a8d8c0bbac3b7defb0
# Tue, 10 Feb 2026 23:01:21 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 10 Feb 2026 23:01:22 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942885af5f1040d875248ce1d2400453748814d65b787a4ea2740b1e0e828013`  
		Last Modified: Tue, 10 Feb 2026 22:53:32 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10323dffe4dd9165f2ce7e6f14f8f39479bc1235a2f59d273cf1146e7ae5d743`  
		Last Modified: Tue, 10 Feb 2026 23:01:26 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ed9298278394f921df61925e2d0f90405fb5c226f9e75c9a12cd5ed426369e`  
		Last Modified: Tue, 10 Feb 2026 23:01:26 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79965ef6a47eb54e50d3c9226009307fb8e1391f2f73bb88999bf020a738ded3`  
		Last Modified: Tue, 10 Feb 2026 23:01:27 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440d46707defeca4fa751c87007660ff192759267a2b2f2410bc9e7beffcf7df`  
		Last Modified: Tue, 10 Feb 2026 23:01:32 GMT  
		Size: 61.4 MB (61360367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164504a398db339cce2efb3c2b4076edbce3aeefe9604d8ef50b51bd91fbc5d3`  
		Last Modified: Tue, 10 Feb 2026 23:01:26 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
