## `hylang:python3.12-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:49b8f233340c9b16aaf52706a2a22761768c1b89de667a11f41606362c635d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `hylang:python3.12-windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull hylang@sha256:7d0cc958730a555df705f0b2a852235ba4236cedc7924abd0689bdd21e9ae596
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2342196710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421c73488fee9be30da723caa9bf7274977a5ccecaf21f59309e89a39ea06bad`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:33:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:33:42 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 18 Apr 2025 03:33:42 GMT
ENV PYTHON_VERSION=3.12.10
# Fri, 18 Apr 2025 03:33:43 GMT
ENV PYTHON_SHA256=67b5635e80ea51072b87941312d00ec8927c4db9ba18938f7ad2d27b328b95fb
# Fri, 18 Apr 2025 03:34:29 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:34:30 GMT
CMD ["python"]
# Fri, 09 May 2025 17:31:20 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 17:31:21 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 17:32:48 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 09 May 2025 17:32:49 GMT
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
	-	`sha256:bb1670ace436f01df2ae26c88b67ea25ce3851de115472002ac2aa6c1fff21c1`  
		Last Modified: Fri, 18 Apr 2025 03:34:33 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5020059e17eb9ab367aa1574b3fcd6ffd3d7243e2632a98a3925c15cbd6a81`  
		Last Modified: Fri, 18 Apr 2025 03:34:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e254f6822776b4c909b71939f7ceca0835142f61b55002331196cc2f32ef71d0`  
		Last Modified: Fri, 18 Apr 2025 03:34:32 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130640ecc92c0e24af03108bf709d397f090f693d7a7fee4b34943a56b1ef100`  
		Last Modified: Fri, 18 Apr 2025 03:34:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6255d4cc5dfe3e8d1279dfa11961bb40fdbcb546d5c3b3fa4609e7ab8e0eacaa`  
		Last Modified: Fri, 18 Apr 2025 03:34:37 GMT  
		Size: 60.1 MB (60081222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e232a140184d1458fd3896bd1dba607341529d30d22f0de7c7bd1a7b0e906a`  
		Last Modified: Fri, 18 Apr 2025 03:34:32 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5363632e2baf56c1fd18cf620c8936b0fc73c49977e4cfb13d1800cdd25a544`  
		Last Modified: Fri, 09 May 2025 17:32:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd3d147d53cdc6847f7b91be20bc9a305ab1b8b7b9722df2009c1a6505bb7e7`  
		Last Modified: Fri, 09 May 2025 17:32:51 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f368b7ee80199d638ed8ef30bdafe37ccd6eab4089c23e80c878eee87cc1db5d`  
		Last Modified: Fri, 09 May 2025 17:32:52 GMT  
		Size: 8.5 MB (8522633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687ebab7f36ae68c386cb4eeea4ce0e70bcd81a034974a22aaa476a9a6144a2e`  
		Last Modified: Fri, 09 May 2025 17:32:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
