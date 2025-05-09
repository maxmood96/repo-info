## `hylang:python3.13-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:52425a3b5bb60051cea6f65266386a3135a98adff0499ab7526bccbdc90c0121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `hylang:python3.13-windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull hylang@sha256:14bde5de5e19be48400181e693491431e1241cff7344f05e1322e9b75b78e4b0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2341304428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5db4165809ec7146fd0d7e691e8d73a2f59475dac1dd05d148778ea96894c34`
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
# Fri, 09 May 2025 17:30:35 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 17:30:36 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 17:31:15 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 09 May 2025 17:31:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704650a8a28ca17ca00d876625fdc0f84dbcefad10ac48197742f584dbb72c8a`  
		Last Modified: Fri, 18 Apr 2025 03:32:22 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e791e7ad1db1b287e759b5c5affb1ff58410f18d284bf535a37aca0a9f57bd`  
		Last Modified: Fri, 18 Apr 2025 03:32:21 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8753e93d7b7fe6bd41a177a320c9e1a7f29950a758f5cc8810f02ba4bf06573`  
		Last Modified: Fri, 18 Apr 2025 03:32:21 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22dc93b6b2ffe80d6091fb548574c227d03d7debb1bed35b6002ff6e23f6a1aa`  
		Last Modified: Fri, 18 Apr 2025 03:32:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590a16674286b05d15af077c948073ebe416991eab4c3485573250cf16e5df0a`  
		Last Modified: Fri, 18 Apr 2025 03:32:25 GMT  
		Size: 59.2 MB (59215920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693c223e2d8b0e7064074ef7e60c2a77e14491cfdddb41902d092ff32cdf8abf`  
		Last Modified: Fri, 18 Apr 2025 03:32:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec0f57348827d7a6d58ed3f7ed52d706240aa2702f36d59e9d26061259eea33`  
		Last Modified: Fri, 09 May 2025 17:31:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3249a654cdd9b58487d73221127f3af4d748286718abc35611e7428ebfdaae`  
		Last Modified: Fri, 09 May 2025 17:31:20 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a5cb927c77d775c912f838d54bb82f8aad5985ba779b431684e97901c57bb2`  
		Last Modified: Fri, 09 May 2025 17:31:22 GMT  
		Size: 8.5 MB (8495693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2edb46d8b7633e7ab948da43990f544b5b70da1c9db8fbbfd4e5687a13e7d8`  
		Last Modified: Fri, 09 May 2025 17:31:20 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
