## `hylang:1-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:20b88c8bb4831caa59e167076345474cd52f2b7152a5642bb64e682db442d3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `hylang:1-windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull hylang@sha256:ed14e65888d4513b287ca42387418c51c1ab27a6da14e670620e0a171cec4313
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2341338251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc95210c949ab9e5ac231565630ddc7c56760ba2893528ed53d9b2f6ea53dda`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:31:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:31:25 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 18 Apr 2025 03:31:26 GMT
ENV PYTHON_VERSION=3.13.3
# Fri, 18 Apr 2025 03:31:27 GMT
ENV PYTHON_SHA256=698f2df46e1a3dd92f393458eea77bd94ef5ff21f0d5bf5cf676f3d28a9b4b6c
# Fri, 18 Apr 2025 03:32:17 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:32:18 GMT
CMD ["python"]
# Fri, 18 Apr 2025 04:16:20 GMT
ENV HY_VERSION=1.0.0
# Fri, 18 Apr 2025 04:16:20 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 18 Apr 2025 04:16:54 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 18 Apr 2025 04:16:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704650a8a28ca17ca00d876625fdc0f84dbcefad10ac48197742f584dbb72c8a`  
		Last Modified: Thu, 08 May 2025 23:22:54 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e791e7ad1db1b287e759b5c5affb1ff58410f18d284bf535a37aca0a9f57bd`  
		Last Modified: Thu, 08 May 2025 23:22:54 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8753e93d7b7fe6bd41a177a320c9e1a7f29950a758f5cc8810f02ba4bf06573`  
		Last Modified: Thu, 08 May 2025 23:22:52 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22dc93b6b2ffe80d6091fb548574c227d03d7debb1bed35b6002ff6e23f6a1aa`  
		Last Modified: Thu, 08 May 2025 23:22:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590a16674286b05d15af077c948073ebe416991eab4c3485573250cf16e5df0a`  
		Last Modified: Thu, 08 May 2025 23:22:58 GMT  
		Size: 59.2 MB (59215920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693c223e2d8b0e7064074ef7e60c2a77e14491cfdddb41902d092ff32cdf8abf`  
		Last Modified: Thu, 08 May 2025 23:22:54 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf65f1b39f2dea80a221400790a95dd46996876a895e6acba95714aaed28f41`  
		Last Modified: Fri, 09 May 2025 07:53:50 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfbe754919a494d2377898a0cd5a8ffdf23bd4331ae238a2432cad9d16d33946`  
		Last Modified: Fri, 09 May 2025 07:53:50 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1346bfc5d6ff28b08596941786c4a2abc54e4d1e9ef04e7a9c731896644d2e2`  
		Last Modified: Fri, 18 Apr 2025 04:16:59 GMT  
		Size: 8.5 MB (8529467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2d344651a50ae6a0dfd13273e2be8dd82180bc1c1d2be438c090b1d67ae17b`  
		Last Modified: Fri, 09 May 2025 07:53:50 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
