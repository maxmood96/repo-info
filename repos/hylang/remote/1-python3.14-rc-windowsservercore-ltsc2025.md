## `hylang:1-python3.14-rc-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:071fcdb946560c360be9cd1b53907e56230ef81ce07a5d6c61400359c19b215a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `hylang:1-python3.14-rc-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull hylang@sha256:280075ef5bb2890244591d1cb3534f5710cdc975e8c4629a1fa31203d9e823a0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3545981755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0bc2ed2bf92945368dc973349c7de5da30a824dbb95882450a0f88003dcede`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Wed, 18 Jun 2025 16:41:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 18 Jun 2025 16:41:22 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 18 Jun 2025 16:41:23 GMT
ENV PYTHON_VERSION=3.14.0b3
# Wed, 18 Jun 2025 16:41:24 GMT
ENV PYTHON_SHA256=c2f136916e45d3bf9c110ddfe0d3787a2e3c73e313aec983c06e03fa2caa8b3f
# Wed, 18 Jun 2025 16:42:04 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 18 Jun 2025 16:42:05 GMT
CMD ["python"]
# Tue, 08 Jul 2025 17:04:06 GMT
ENV HY_VERSION=1.1.0
# Tue, 08 Jul 2025 17:04:07 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 08 Jul 2025 17:04:42 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 08 Jul 2025 17:04:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b1e0066c85e6579dbcac4f2233ba4e47e6669de26f88c16ebfc1b7b4a766f3`  
		Last Modified: Wed, 18 Jun 2025 16:45:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3f0df1148d8ae4aa003b959b804692ac85f4d19bf1a5dd500ed05281245eea`  
		Last Modified: Wed, 18 Jun 2025 16:45:47 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bed7371579bbb258bf0f01268ce589d70804b38bff8e97145b4652dd906bea9`  
		Last Modified: Wed, 18 Jun 2025 16:45:47 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad308db14d292c1fd185dd2aac5ef4ff06d595fccad9470f4e128b4af70bcd4`  
		Last Modified: Wed, 18 Jun 2025 16:45:47 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25cf32437c34df6c2f320bf8bd4325967ef436a9361167c3ad024983a9bca19`  
		Last Modified: Wed, 18 Jun 2025 16:45:45 GMT  
		Size: 61.2 MB (61203808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c491ea11184dd204aada8c58b068c58d5a9c32b5410daccb821be00883377be`  
		Last Modified: Wed, 18 Jun 2025 16:45:41 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4341bee4720ce23d2c9a752bb9a5adca22d141c94ccbe4d079d6754e5bd030`  
		Last Modified: Tue, 08 Jul 2025 17:23:24 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2310fda72e099d6efb6b9aeda060c5eda01d2d58314ab2c0a7fde4d249d9ea53`  
		Last Modified: Tue, 08 Jul 2025 17:23:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9e0430289a97aa085ad67efd909a14a974486bf67d97d13e4f0e1b3cedf233`  
		Last Modified: Tue, 08 Jul 2025 17:23:27 GMT  
		Size: 8.6 MB (8593412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb0e12fdbdfc6605d9282d3d61bbbcaf3ede0c2c8525676ba5adf9b08a608a9`  
		Last Modified: Tue, 08 Jul 2025 17:23:26 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
