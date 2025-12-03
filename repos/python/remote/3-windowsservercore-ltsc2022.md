## `python:3-windowsservercore-ltsc2022`

```console
$ docker pull python@sha256:cb988b7eb0fac7e4a48b3e27efc419f97527c1c8553fc358676a35fcbf5be3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `python:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

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
