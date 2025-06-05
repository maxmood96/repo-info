## `hylang:windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:a8fb29900c9ae8fd8bee6d670ac4fd85f6053c1a80e38dd1d509baa184e075d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `hylang:windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull hylang@sha256:181081bb4f06d13f107ac05c36a4138f9ddd8d83c6435cb8f4980562aca698ba
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2341179178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dab6f07cfa31c245a8e2e16aed045394718245a48b8db478b6d2a58a7cc8e9e`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 04 Jun 2025 17:06:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Jun 2025 17:06:01 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 04 Jun 2025 17:06:01 GMT
ENV PYTHON_VERSION=3.13.4
# Wed, 04 Jun 2025 17:06:02 GMT
ENV PYTHON_SHA256=94f53bb832539ea02d6ce581d7c1fcc36228e04a611b8dcfe797ad4bbc0a45c1
# Wed, 04 Jun 2025 17:07:00 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 04 Jun 2025 17:07:02 GMT
CMD ["python"]
# Wed, 04 Jun 2025 21:21:17 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:21:18 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:22:50 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 04 Jun 2025 21:22:50 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5186485bd037d64b6fab9b42606ed40550235a210c8329dd303a98dd137007bb`  
		Last Modified: Wed, 04 Jun 2025 17:12:15 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8275514e3b5d959b97ad977a906a7a0e256ebe9a555bee9a01970eea179d6adb`  
		Last Modified: Wed, 04 Jun 2025 17:12:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b92f6b742d0f62e97b8757e8c8097a387f7aec5b9470d9089cee6cc433af1a9`  
		Last Modified: Wed, 04 Jun 2025 17:12:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd2094fa14194a6d8bd67fb3f93b6a2c30001ce7978346b2426c322255b0c61`  
		Last Modified: Wed, 04 Jun 2025 17:12:21 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb932e8982bfa70999cd1e2b21d29c5a2aa48e43aed1799fb2cdd0dedee21e84`  
		Last Modified: Wed, 04 Jun 2025 18:03:27 GMT  
		Size: 59.1 MB (59094011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee054360590b5f07a651a2265b40edd7821bf325b32d563e4d28abceecf2e44`  
		Last Modified: Wed, 04 Jun 2025 17:12:24 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e996b128a2e7f3768545eb8ccc802419a68837f511bfdc260dbae366da9d357`  
		Last Modified: Wed, 04 Jun 2025 21:23:04 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3198011a4f3de6818947610f4e8a4465e08f22379c2f4eef805a540c87a0db`  
		Last Modified: Wed, 04 Jun 2025 21:23:04 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633d0ba76ba0260c7d705882efa2cb7fc559c1062edc74ce14947f88c3a7bdf3`  
		Last Modified: Wed, 04 Jun 2025 21:23:06 GMT  
		Size: 8.4 MB (8446662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1326f7c0526982381b701e4d50a1ca5b3f0dff6b832ef748c93f255361b53a29`  
		Last Modified: Wed, 04 Jun 2025 21:23:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
