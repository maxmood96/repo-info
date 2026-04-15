## `hylang:python3.13-windowsservercore`

```console
$ docker pull hylang@sha256:e874470301fe499c39de68efd115d66b7f9479b5127e7132bfc3a6ba5d771d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `hylang:python3.13-windowsservercore` - windows version 10.0.26100.32690; amd64

```console
$ docker pull hylang@sha256:4c8f1fcb7ebf49fd307a9e1eff90b5cd1d96deae2e334912c860db793789dab2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2197576070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aba466b369074fecf405a552718dcfdf47a54b37a3e0707fd5a60ef45b7fc77`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:02:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:16:15 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 14 Apr 2026 21:16:16 GMT
ENV PYTHON_VERSION=3.13.13
# Tue, 14 Apr 2026 21:16:17 GMT
ENV PYTHON_SHA256=3c9c81d80f91c002ced86d645422d81432c68c7d9b6b0e974768ca2e449a4d00
# Tue, 14 Apr 2026 21:17:00 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:17:00 GMT
CMD ["python"]
# Tue, 14 Apr 2026 22:15:07 GMT
ENV HY_VERSION=1.2.0
# Tue, 14 Apr 2026 22:15:07 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 14 Apr 2026 22:15:46 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 14 Apr 2026 22:15:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8132c872e75f25bfa323300a3940e534262afa9775f557483dcc1c0951ee5277`  
		Last Modified: Tue, 14 Apr 2026 21:03:51 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd96d123a94c2e96da10a3bd0747ea0e160e9b2cdee1d607f8ba49e13b2ecbb`  
		Last Modified: Tue, 14 Apr 2026 21:17:05 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513fed98c0242987a59790f45dda4da448e18cb5d3c98d5823a13cbf2655dc41`  
		Last Modified: Tue, 14 Apr 2026 21:17:05 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c9427b7e7928132139b82ace25661d40c8c9afddfaf727cf775643ea1dfb18`  
		Last Modified: Tue, 14 Apr 2026 21:17:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5908d8849ea04d9ba6848b83d07f812c6ab937025c5dfb0c7bf0d3e95762866`  
		Last Modified: Tue, 14 Apr 2026 21:17:10 GMT  
		Size: 59.2 MB (59156829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9b333ef449d79783bcad63d085d9dd3945ecd7a10e47e83fe44d51519b9ade`  
		Last Modified: Tue, 14 Apr 2026 21:17:05 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fecf7321eb98482440a5648fcd287b9fc3bf69e6c41d53722f081a9cac04ee`  
		Last Modified: Tue, 14 Apr 2026 22:15:51 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bb81ba25c846028fc1d2292b9715efc6f059c8e14f349086feba3a49e116be`  
		Last Modified: Tue, 14 Apr 2026 22:15:51 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2462bf0fa7b8b1bce4e8b4405459693fcced2aa6717d4e554a80acedb034e3`  
		Last Modified: Tue, 14 Apr 2026 22:15:52 GMT  
		Size: 8.4 MB (8422724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99695e0f3f5255cf838a6e06bb5dc9442e16f225e9ce5b91b54ad11e35a1109`  
		Last Modified: Tue, 14 Apr 2026 22:15:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.13-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull hylang@sha256:efbd43ce3f47f7bf3f60fb84786b589f667691c712d7307aafd70e177bd490ca
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2137466311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f9a4e6c25c3d6f9c38485c6c801c40ad28d3edb45b0c1203bb5455b7e45d3f`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:03:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:26:56 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 14 Apr 2026 21:26:56 GMT
ENV PYTHON_VERSION=3.13.13
# Tue, 14 Apr 2026 21:26:57 GMT
ENV PYTHON_SHA256=3c9c81d80f91c002ced86d645422d81432c68c7d9b6b0e974768ca2e449a4d00
# Tue, 14 Apr 2026 21:27:58 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:27:59 GMT
CMD ["python"]
# Tue, 14 Apr 2026 22:17:42 GMT
ENV HY_VERSION=1.2.0
# Tue, 14 Apr 2026 22:17:43 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 14 Apr 2026 22:18:11 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 14 Apr 2026 22:18:12 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7859559f7e482ab69f3dddf83b05a23fb97e6c47cc09bb11f9f91ea0b96dbf26`  
		Last Modified: Tue, 14 Apr 2026 21:05:58 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89437b07bc34e480f349a26343836e3ed5139e1b10f8972f2d3ddec312d2d611`  
		Last Modified: Tue, 14 Apr 2026 21:28:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1bd2253f26c1508194e0bf77f67b13da7b081cd79cdb41daaddbfc46ed5de4`  
		Last Modified: Tue, 14 Apr 2026 21:28:06 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4485c9fd3753ce85b6f7c329af21719b49ba3ad7b1bb3e2ccd5ac879f55daca5`  
		Last Modified: Tue, 14 Apr 2026 21:28:06 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d5ac3e78b81afb6d0b156609c966bde6fc28256ea05418a9e541891b4b5067`  
		Last Modified: Tue, 14 Apr 2026 21:28:14 GMT  
		Size: 59.0 MB (58997850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29c621a69ff97f7f9f0fe2c1151b86524f70582f734ef006f13879ca2f6cdd2`  
		Last Modified: Tue, 14 Apr 2026 21:28:06 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb51a32a879ec4b89428b3fbd071746eb200ddcdb9132b96f4bed496f6b87924`  
		Last Modified: Tue, 14 Apr 2026 22:18:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484215f9090e90733b649596cb5ad44b482360eb62d76e6a90ce4c5c8e17e994`  
		Last Modified: Tue, 14 Apr 2026 22:18:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03272de8b736b3305f8bca26a23a99b3bb53a9b99ab2cbe3219fe243b4efb3c1`  
		Last Modified: Tue, 14 Apr 2026 22:18:17 GMT  
		Size: 8.2 MB (8246708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df353006c2305f69b550866c37ddb4e3e7dab0151b65269d295dbde638f6246a`  
		Last Modified: Tue, 14 Apr 2026 22:18:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
