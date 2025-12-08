## `python:windowsservercore`

```console
$ docker pull python@sha256:0a1f3d0fa7ed34357bd300c8420761485eed5159d6e23eec3727d1c6ead5eeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `python:windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull python@sha256:7432fc9b49baea15414db383aeb0f4f3757f9bb0179801daec42f89017dfae93
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3296301485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e70b6656774d0f4f3de0c6f3729181c63801d8756305ca8e0cb954455998c5`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Wed, 03 Dec 2025 01:06:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 01:06:07 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 03 Dec 2025 01:06:08 GMT
ENV PYTHON_VERSION=3.14.1
# Wed, 03 Dec 2025 01:06:08 GMT
ENV PYTHON_SHA256=74e1516408744190fcc12307c150de30902898444f77f85f4c2ac18f36788a80
# Wed, 03 Dec 2025 01:07:26 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 03 Dec 2025 01:07:26 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d45a5687ec46714f68b9dec2efacd73bde08924cc55d3e2f375120fc0027acd`  
		Last Modified: Wed, 03 Dec 2025 01:16:24 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5ffa566e17e33db847bdf8d07e4d3515cec353c992df60d6052307ad7f3e45`  
		Last Modified: Wed, 03 Dec 2025 01:16:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712641b7f5bedec62fe5a7723f2e6c455f0f715fa4e5dc4ae98ecd798abf7899`  
		Last Modified: Wed, 03 Dec 2025 01:16:25 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124c3953d95b1f7cce6d5fce7401954249d931109eaf1a6dcae8c135b4d60d66`  
		Last Modified: Wed, 03 Dec 2025 01:16:26 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c791592b2747f84a77351d35acf579b64eb56e3a12d6317302128d10f121f253`  
		Last Modified: Wed, 03 Dec 2025 01:16:30 GMT  
		Size: 60.8 MB (60839158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074a5b8ba2a103f45a4cae30459f014a1e2a668a3c89b8eed01539a42888b4f0`  
		Last Modified: Wed, 03 Dec 2025 01:16:26 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull python@sha256:567eca4cca215ed0392f6ff4934561a225d4352791fc5bd44db06de2eed3f86c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1830913398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9d3da321f855ef9a4f337a2a7c90a12e17182b21907c8580b2da92df67178f`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Wed, 03 Dec 2025 01:05:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 01:05:27 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 03 Dec 2025 01:05:28 GMT
ENV PYTHON_VERSION=3.14.1
# Wed, 03 Dec 2025 01:05:30 GMT
ENV PYTHON_SHA256=74e1516408744190fcc12307c150de30902898444f77f85f4c2ac18f36788a80
# Wed, 03 Dec 2025 01:06:39 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 03 Dec 2025 01:06:40 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27be210d6833cdc827bfc15972f5d728f0d871b50e3aa17e152f86594cb31ba`  
		Last Modified: Wed, 03 Dec 2025 01:12:24 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14fddf0b287656bd22c11db1941d0dac9b8298027d4deeb2f20f0c2fc07c4bd`  
		Last Modified: Wed, 03 Dec 2025 01:12:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735d45cf80e1838869461b613b84034ebde2378b5dde4341d8c26e4e2e327500`  
		Last Modified: Wed, 03 Dec 2025 01:12:37 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f5801afbbb07dc121162a03ec40e37be0764f8fcd90a307293e563c5982cb7`  
		Last Modified: Wed, 03 Dec 2025 01:12:24 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638d982268f0601a8853f4a723db335bdade0cf5f3b69e75f7b3b848c63eedec`  
		Last Modified: Wed, 03 Dec 2025 01:12:29 GMT  
		Size: 60.9 MB (60945374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcdb429ddbeeaadd3b01bc240bdafbd232bbc3b52821c1e897c9b07dfd6af5f`  
		Last Modified: Wed, 03 Dec 2025 01:12:24 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
