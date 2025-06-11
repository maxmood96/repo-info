## `hylang:python3.14-rc-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:787ae4f45a29d34c6dd3c36898fbf265f4f181394eed70362bb2a2abd66bff55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `hylang:python3.14-rc-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull hylang@sha256:47c68440263a004ec17600b15a296b9552e22047a83c08fa4751141dc86fbe70
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3545842372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c29af40bcb6a6ccfa14f36dcce52c5adaf4520aa9f7d85541497d4c617c4c13`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Tue, 10 Jun 2025 21:29:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Jun 2025 21:29:32 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 10 Jun 2025 21:29:33 GMT
ENV PYTHON_VERSION=3.14.0b2
# Tue, 10 Jun 2025 21:29:34 GMT
ENV PYTHON_SHA256=279b1d0e2b1b6cece6f03e49218aacccfd10367e07b785edeb1d4135507434c1
# Tue, 10 Jun 2025 21:30:13 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 10 Jun 2025 21:30:13 GMT
CMD ["python"]
# Tue, 10 Jun 2025 22:14:15 GMT
ENV HY_VERSION=1.1.0
# Tue, 10 Jun 2025 22:14:16 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 10 Jun 2025 22:14:48 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 10 Jun 2025 22:14:49 GMT
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
	-	`sha256:944acb53ce5d1399deb759478257f18c2225a74ecc174820f0949bb67bedce15`  
		Last Modified: Tue, 10 Jun 2025 22:09:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c8a23e6d5c8e9de30eb49e902cb2a869f36595b530af7a47184c86a365ade4`  
		Last Modified: Tue, 10 Jun 2025 22:09:08 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b6bc8ac2fb496e462609b9cab9531a9b6e1e6ae720122943d9d768b9ab93a0`  
		Last Modified: Tue, 10 Jun 2025 22:09:08 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c859f864a6f10fffccdb9054582366c97bd9a3dbc054dfc7964d093f351787df`  
		Last Modified: Tue, 10 Jun 2025 22:09:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f605fb05175820d25b217042653c27b0137f518bcb0d19b0759323521b71ad`  
		Last Modified: Tue, 10 Jun 2025 22:09:13 GMT  
		Size: 61.1 MB (61075690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ae0f880178cd1a6e0a1512658ef916a93166cc8279a6465bddf539d380ca3d`  
		Last Modified: Tue, 10 Jun 2025 22:09:14 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f92101d0fd3620b69d373d076888aee6438ccb0e14aae992488ccf4f2ee76d`  
		Last Modified: Tue, 10 Jun 2025 22:15:07 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f921173a21cbbefd4c4b95153ce6f46fd5702f5dc0d5b7a54d45bb0a47fd0880`  
		Last Modified: Tue, 10 Jun 2025 22:15:07 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941a383f2f3a89a83e93ba85722baf554ab0f0bcc393d2546edfc53d805ed656`  
		Last Modified: Tue, 10 Jun 2025 22:15:07 GMT  
		Size: 8.6 MB (8582215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55df3ac7a43ef5d1f042bd0f9e369ecff2b944ad7c6718b062cec1323185cc33`  
		Last Modified: Tue, 10 Jun 2025 22:15:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
