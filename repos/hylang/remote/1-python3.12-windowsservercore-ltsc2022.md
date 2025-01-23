## `hylang:1-python3.12-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:c16c6e6d55a2688ba8ad446996af915d97669bae33032c7858f460f7a8cafa00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `hylang:1-python3.12-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull hylang@sha256:0c7eadf73fd4010ef3f6909eeec5a1e0b5da40bc72b1801505416197025286d4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330855861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5ef61e8d874b363d4fe26fecedc9dcd9f88ec8558ff576b65cc6dedb9098e6`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:41:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:41:31 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 14 Jan 2025 23:41:32 GMT
ENV PYTHON_VERSION=3.12.8
# Tue, 14 Jan 2025 23:41:33 GMT
ENV PYTHON_SHA256=71bd44e6b0e91c17558963557e4cdb80b483de9b0a0a9717f06cf896f95ab598
# Tue, 14 Jan 2025 23:42:15 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:42:15 GMT
CMD ["python"]
# Thu, 23 Jan 2025 01:36:29 GMT
ENV HY_VERSION=1.0.0
# Thu, 23 Jan 2025 01:36:30 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 23 Jan 2025 01:37:08 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 23 Jan 2025 01:37:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e345f709a03b37a92d1b07b36775fb23ae15006296f9fda8198f0c3f489fc21`  
		Last Modified: Tue, 14 Jan 2025 23:42:20 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0657588927af7a1b5180f95fbf58d2488627f28ea757b9e463f976fcffe22b9d`  
		Last Modified: Tue, 14 Jan 2025 23:42:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958d3073855dc7802aad8c3771f4d1466b226750f8105e23228827967768a97e`  
		Last Modified: Tue, 14 Jan 2025 23:42:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d10042c9b8e27b3c7b3038d0637587c2d6a8f50e8ed1cf5861f9c47958ccdf`  
		Last Modified: Tue, 14 Jan 2025 23:42:19 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878ad5275689bca6663b648c0ad67dc0094d59a6d39c7e9cc73121e652c629a6`  
		Last Modified: Tue, 14 Jan 2025 23:42:24 GMT  
		Size: 59.9 MB (59930353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c889a99c4562cd4934f0cb625b48d7d254c3f48ab5bc15fcc2d2e8c503eaa71`  
		Last Modified: Tue, 14 Jan 2025 23:42:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c4ad19d96830efd3a327e452319bca423c5fda0ec665ad80150fa2ef318029`  
		Last Modified: Thu, 23 Jan 2025 01:37:11 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72962784a5a8e33eb7e19e7f502c145b71633eaecb3b6de1cbabb2dd64ec5f34`  
		Last Modified: Thu, 23 Jan 2025 01:37:11 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d820dbfa2a4a7184ec5a6870e4b02f579d4afac30f3c25eeb47d1f3204ebe93`  
		Last Modified: Thu, 23 Jan 2025 01:37:13 GMT  
		Size: 8.5 MB (8529970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6df2eb35fc5b1f3865ad4182ca736df22bafefa4f11fd9834f76b41d60e9211`  
		Last Modified: Thu, 23 Jan 2025 01:37:11 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
