## `hylang:python3.12-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:ca75b2dd1a8c11640b0aaf743aba5cfbddb7c3b3082f5e891be7f2d55fd42c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `hylang:python3.12-windowsservercore-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull hylang@sha256:3e78f017d2ccab66c861a66d061a8606307d7a71f415a2b156a786e3318cd3aa
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3463462247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590b247ec56658c8642a927d606b18eeb68478b45696975cb9d0d4beeb0deeab`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 01:48:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 01:48:44 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 09 Apr 2025 01:48:45 GMT
ENV PYTHON_VERSION=3.12.10
# Wed, 09 Apr 2025 01:48:47 GMT
ENV PYTHON_SHA256=67b5635e80ea51072b87941312d00ec8927c4db9ba18938f7ad2d27b328b95fb
# Wed, 09 Apr 2025 01:49:26 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 01:49:27 GMT
CMD ["python"]
# Wed, 09 Apr 2025 02:17:10 GMT
ENV HY_VERSION=1.0.0
# Wed, 09 Apr 2025 02:17:11 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 09 Apr 2025 02:17:45 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 09 Apr 2025 02:17:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b0297bed10ae5cb01ea0afba6f2b16ac88f2b6396a4bf35fcd74994a037c84`  
		Last Modified: Wed, 09 Apr 2025 01:49:30 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6083a1fabbec39a140af9490d38af76e620b6020f8cf065e0a8d4d8518ef4d24`  
		Last Modified: Wed, 09 Apr 2025 01:49:29 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c62cf9387265f246634b476f0c09ef490751f7aa5ee7d0e7ff70207a1500af2`  
		Last Modified: Wed, 09 Apr 2025 01:49:29 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7379c01643eab133d132841154c6569777530e267adc56263ce73ab42498cd56`  
		Last Modified: Wed, 09 Apr 2025 01:49:29 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82a24e38f4ae66e1aac3290cb8ed77cdeb56617f65c85d296c661e32ce88102`  
		Last Modified: Wed, 09 Apr 2025 01:49:34 GMT  
		Size: 60.2 MB (60151379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d98a6fca48b9230ae2895b0ed0ac3dc194cfeb3ac7519ace8fdd2d40248ee5`  
		Last Modified: Wed, 09 Apr 2025 01:49:29 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbb37b7753b1d946437b52946330969c96e498c956f0d3f09de25a0fad114b1`  
		Last Modified: Wed, 09 Apr 2025 02:17:49 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f0610a356941caa93b480a3690a3c2249db8f08e974f4f9ba18d36adf9ec5d`  
		Last Modified: Wed, 09 Apr 2025 02:17:49 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cadf58c71576f6bc52eafb389dc7c8bc48a2c2baad9a76e70f73b7ff9e84667`  
		Last Modified: Wed, 09 Apr 2025 02:17:51 GMT  
		Size: 8.6 MB (8621044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dc6986203014fc15e0b85430b5e72a9a1ff0e0720e7d299025d522723675d9`  
		Last Modified: Wed, 09 Apr 2025 02:17:49 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
