## `hylang:windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:8cf34c45ecddff6a79a49337df7b5df9f3e4489b0c640da4ea380ce9798a3fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `hylang:windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull hylang@sha256:1a7898bd1e9477487a787f4b74d85b61c517153930dd9e451871e00f15208fc2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330029162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa41493c62042cab6e057fb63884037d28800b315f6d3b0e3a2a0530271aad90`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Thu, 06 Feb 2025 22:26:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 Feb 2025 22:26:44 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 06 Feb 2025 22:26:45 GMT
ENV PYTHON_VERSION=3.13.2
# Thu, 06 Feb 2025 22:26:45 GMT
ENV PYTHON_SHA256=9aaa1075d0bd3e8abd0623d2d05de692ff00780579e1b232f259028bac19bb51
# Thu, 06 Feb 2025 22:28:48 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 06 Feb 2025 22:28:48 GMT
CMD ["python"]
# Fri, 07 Feb 2025 00:28:04 GMT
ENV HY_VERSION=1.0.0
# Fri, 07 Feb 2025 00:28:05 GMT
ENV HYRULE_VERSION=0.8.0
# Fri, 07 Feb 2025 00:29:20 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 07 Feb 2025 00:29:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 21:54:27 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e308366d496b7e2cacc05448889ba40e8c586de35e4af2ad8029175e74d197e`  
		Last Modified: Fri, 07 Feb 2025 01:16:21 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bbb156d25c3cdc66afb6a31a8f6a34b1f5eaa2d83ccd398a1e0dbfe3e08819`  
		Last Modified: Fri, 07 Feb 2025 01:16:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65a37936d77b9424a520f378978dc4cc8d699112c562174870348288b63a74c`  
		Last Modified: Fri, 07 Feb 2025 01:16:25 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022276ee27b531c369510f4411b40118edf505c29be3c5295b97b62bee121068`  
		Last Modified: Fri, 07 Feb 2025 01:16:28 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af29b763e03a3e97f4f3235c2442919b51e8c5307dbbe54c4aaca83f6ebf7191`  
		Last Modified: Fri, 07 Feb 2025 02:00:11 GMT  
		Size: 59.1 MB (59129092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66e87ad10ef8f39b137e1b10c3d3763e08236b1797a7fcefc6b0eebd9bfe380`  
		Last Modified: Fri, 07 Feb 2025 01:16:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a572b49635529f178e110ab37e2ec02eb8d83aed7f35c45513e44d50a24dd858`  
		Last Modified: Mon, 10 Feb 2025 19:04:35 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b30291006ed566d7d686911cca21a5db7896a79ca1218fd0259533767bc6ef5`  
		Last Modified: Mon, 10 Feb 2025 19:04:35 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf089289c5f66fbf5f86b3f7722c35bab2d3181c1fe17d5a21f271e6589eab40`  
		Last Modified: Mon, 10 Feb 2025 19:04:37 GMT  
		Size: 8.5 MB (8504458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214254715e072c471beab4574f69f4e74271c9b752fe24f675ed68aeed783845`  
		Last Modified: Fri, 07 Feb 2025 00:29:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
