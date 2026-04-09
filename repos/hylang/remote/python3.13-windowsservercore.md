## `hylang:python3.13-windowsservercore`

```console
$ docker pull hylang@sha256:5fc8ada7c4c67ec60031e37070edecef1fe67e933ed5c8be5d88795bb00de680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `hylang:python3.13-windowsservercore` - windows version 10.0.26100.32522; amd64

```console
$ docker pull hylang@sha256:8a7d6c0618007e7a5496f01225becfd2449893075293c8841c1fe2840f1751fe
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2148749111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9512813fab0b5f50ab48d0e58480a33fccdf00a938d3bcce6ee8453abcb580e2`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Wed, 08 Apr 2026 17:19:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Apr 2026 17:38:55 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 08 Apr 2026 17:40:14 GMT
ENV PYTHON_VERSION=3.13.13
# Wed, 08 Apr 2026 17:40:14 GMT
ENV PYTHON_SHA256=3c9c81d80f91c002ced86d645422d81432c68c7d9b6b0e974768ca2e449a4d00
# Wed, 08 Apr 2026 17:41:04 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 08 Apr 2026 17:41:04 GMT
CMD ["python"]
# Wed, 08 Apr 2026 18:19:05 GMT
ENV HY_VERSION=1.2.0
# Wed, 08 Apr 2026 18:19:07 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 08 Apr 2026 18:20:39 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 08 Apr 2026 18:20:39 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b73ee1becf0ed5f5aa0fcaa41b40ac94cff6cd901ea093aac9ee00f641873f5`  
		Last Modified: Wed, 08 Apr 2026 17:21:55 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b1efb13983909bbb9740c1f271f1f48fac6d1be5efdd0e0a4267ff5072c483`  
		Last Modified: Wed, 08 Apr 2026 17:39:52 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf55d37f19a1104d80d0b68c3c6282cbd45b55a94ac1100d1b98e5e8a9cf97b0`  
		Last Modified: Wed, 08 Apr 2026 17:41:11 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd8c97ff9512a9a9ea919644e4a533f2a94b27a46f196bb5cd1e4781c7b28cb`  
		Last Modified: Wed, 08 Apr 2026 17:41:11 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5098b2bebfed31c8015764bfea62686b0b7aeea96ebaa094c12752fbf525d166`  
		Last Modified: Wed, 08 Apr 2026 17:41:17 GMT  
		Size: 59.2 MB (59150732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6096e950c119534bca162332005743d1f5ee0bcdea36a4905b5e2ab56d98c92a`  
		Last Modified: Wed, 08 Apr 2026 17:41:11 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627af0979c5e0268ae833d5f7a66980d65f4644bbb17d6299e4614bf81b535b3`  
		Last Modified: Wed, 08 Apr 2026 18:20:44 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ea2d5464f0b791f27848183a0a97b5ba2cc1342ded48f9c449ba5a3f463bcc`  
		Last Modified: Wed, 08 Apr 2026 18:20:44 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29510ff6a78583546308e9e19af7c743123d6d60089e13449b0c2c455f4658f2`  
		Last Modified: Wed, 08 Apr 2026 18:20:46 GMT  
		Size: 8.4 MB (8391747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb4cb658b1f9f8b27f509c455c7d2ad9d8edc016f3d34338319855cdc67ecab`  
		Last Modified: Wed, 08 Apr 2026 18:20:44 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.13-windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull hylang@sha256:48fc4fd1b7b2a1610680f6ac21a71a2c8bb7620ccb41449e5f944466548a2205
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2049568556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9efc3168db963e0067bd732b9222587eb105ff77ee1fd6a5e7415bc0cd82b2`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Wed, 08 Apr 2026 17:19:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Apr 2026 17:39:01 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 08 Apr 2026 17:40:18 GMT
ENV PYTHON_VERSION=3.13.13
# Wed, 08 Apr 2026 17:40:18 GMT
ENV PYTHON_SHA256=3c9c81d80f91c002ced86d645422d81432c68c7d9b6b0e974768ca2e449a4d00
# Wed, 08 Apr 2026 17:41:15 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 08 Apr 2026 17:41:15 GMT
CMD ["python"]
# Wed, 08 Apr 2026 18:22:46 GMT
ENV HY_VERSION=1.2.0
# Wed, 08 Apr 2026 18:22:48 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 08 Apr 2026 18:23:30 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 08 Apr 2026 18:23:31 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa9d35e228f44ebc38cf54fabf7460ff93b6a1a6ef494e4aacdd3d1d9ab206f`  
		Last Modified: Wed, 08 Apr 2026 17:22:25 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaf7a96970b496c56c37e5f000f1cbc4e63aae4db30554350384bf08919fb5c`  
		Last Modified: Wed, 08 Apr 2026 17:39:52 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ef064ace3b96dd90d04ffcc5f44601f8641a775ff043e60c5714e82637d0fa`  
		Last Modified: Wed, 08 Apr 2026 17:41:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742556ca9f9e04ac54d5b8eb8c43f8971374e10dea1f387fe6ed1eaafa00cf40`  
		Last Modified: Wed, 08 Apr 2026 17:41:20 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714c7f497eab06c35ca00ceaa078158502903c650ff0163923b22b8054be3be8`  
		Last Modified: Wed, 08 Apr 2026 17:41:26 GMT  
		Size: 59.0 MB (59019921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f3fffb569b5a7e7c1de4a924e7a66d319a66d4681000af39bcbaf12dd1e0d6`  
		Last Modified: Wed, 08 Apr 2026 17:41:20 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a4bbf7ae651edc9d77cacb221b65753e149949113ef1f481fe155998ddbbe1`  
		Last Modified: Wed, 08 Apr 2026 18:23:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429c15a8b11fe8f87323489173e0601f47619f2b23ac9bbc78d65cc010cfeabf`  
		Last Modified: Wed, 08 Apr 2026 18:23:35 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c5f94c4b7a044a1e3ff87e62a0cfabecc90bf1cc195daf6dd5501203f6e9aa`  
		Last Modified: Wed, 08 Apr 2026 18:23:37 GMT  
		Size: 8.3 MB (8256779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51061ee4fffc6d70e6bc5bad75b8c06ac6dbed39149598833cbc652fb6f95036`  
		Last Modified: Wed, 08 Apr 2026 18:23:35 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
