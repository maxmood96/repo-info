## `python:windowsservercore-ltsc2025`

```console
$ docker pull python@sha256:0c741c349797663a99f33f1d90ecf585f554aeeb4f63ee5fb4e7db09d72d7442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `python:windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull python@sha256:a0df136bc3a00c792bc23fadcdf12af5730efdfac7ca00ac166c838f0754b9cb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3557514484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11399487e44ec21bc8308a71fd52b957aaf131e99f41162b6e7a8f0aa7586c39`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:35:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:35:34 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 12 Aug 2025 20:35:34 GMT
ENV PYTHON_VERSION=3.13.6
# Tue, 12 Aug 2025 20:35:35 GMT
ENV PYTHON_SHA256=5edce6f0597a9b250c72790dc076649b06c1dc4754f3c68d7c284a1f10c33f36
# Tue, 12 Aug 2025 20:36:10 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:36:10 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aeae9aaa83aa6cc7e393b13e816987c2c7b2efc65c6629b646a627dbdfa1137`  
		Last Modified: Tue, 12 Aug 2025 20:39:52 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843256200b1f196033e8d09775c3e7bd95b65cee3e5731b568b9ef6d0f37fa3b`  
		Last Modified: Tue, 12 Aug 2025 20:39:52 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef166841d522ca9f763ca4af1ae8a3c0d65ee04ba1a7bce793dbc181f139196`  
		Last Modified: Tue, 12 Aug 2025 20:39:52 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f33cc5ed7fc7a479a0356b1a8b1046864978568e3cff563e28c768b5f7155c`  
		Last Modified: Tue, 12 Aug 2025 20:39:53 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b040e8587aa9c80e010bcd97158bd1ffcae70d1c3584e664e4e00785362b2764`  
		Last Modified: Tue, 12 Aug 2025 20:40:04 GMT  
		Size: 58.7 MB (58677443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd96ad62b3a1607f5a73da89623ac8f33ae1958bce8767ceb0783c960410c804`  
		Last Modified: Tue, 12 Aug 2025 20:39:53 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
