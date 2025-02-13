## `python:3-windowsservercore-1809`

```console
$ docker pull python@sha256:096a5ff2f5e1396565b6557a81365ea3d78b006a7654cca85c4626f07c0aa9f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `python:3-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull python@sha256:cd95961d37c9327201d8a1a808ee4c8d463e9b8445253112c64db9229e0a84a8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2180050699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7738301cf82c9e1d51cd70b5e616487a41ca6545702d739d9ec9a2296ae849`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 06 Feb 2025 22:26:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 Feb 2025 22:26:34 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 06 Feb 2025 22:26:35 GMT
ENV PYTHON_VERSION=3.13.2
# Thu, 06 Feb 2025 22:26:35 GMT
ENV PYTHON_SHA256=9aaa1075d0bd3e8abd0623d2d05de692ff00780579e1b232f259028bac19bb51
# Thu, 06 Feb 2025 22:27:55 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 06 Feb 2025 22:27:55 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 20:54:32 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c72deea1069d3ffcc9217d5a73da83c09a908c8da44ae6672a6089dbedee443`  
		Last Modified: Fri, 07 Feb 2025 02:02:34 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75ea8f3a755224c42ec66b4149bd3aa3325bfaaf0e08a1e9f3d493a8157ad67`  
		Last Modified: Fri, 07 Feb 2025 01:16:43 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a373011d1ca8388477009beab507ad8e843053fb0f93a5c32c34a1c0dc32c7`  
		Last Modified: Thu, 06 Feb 2025 22:28:31 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d0eb078a40fd5353762c83bb62a85a6edac53db0127e20f3a51daad339ac50`  
		Last Modified: Thu, 06 Feb 2025 22:28:31 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1c66aa5982fd91e7613caee541810d2c78ab91d63482c8441e035f369b9a85`  
		Last Modified: Thu, 06 Feb 2025 22:28:34 GMT  
		Size: 57.8 MB (57831739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de4fa75f188989e85d10264585faf60e16da370654650327403e3c4e013ee4`  
		Last Modified: Thu, 06 Feb 2025 22:28:32 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
