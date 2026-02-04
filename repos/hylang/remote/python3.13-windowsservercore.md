## `hylang:python3.13-windowsservercore`

```console
$ docker pull hylang@sha256:140fc920932a035f031ce279ff75eb37d4f72ecbac9b8b7283e1d55bb5d50bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `hylang:python3.13-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull hylang@sha256:dbe09dad1984191c6e644818d427e8a2ff5cde9abf0af9f29423cd097db248fa
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1563107789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f099de729d96a694c22383d81aa2c455768ddb98101f84cb39f66805207d4f45`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Wed, 04 Feb 2026 20:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Feb 2026 20:07:49 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 04 Feb 2026 20:07:50 GMT
ENV PYTHON_VERSION=3.13.12
# Wed, 04 Feb 2026 20:07:51 GMT
ENV PYTHON_SHA256=96159fcb523ae404b707186a75b4104ee23851e476a5e838e14584cf1e03f981
# Wed, 04 Feb 2026 20:09:14 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 04 Feb 2026 20:09:15 GMT
CMD ["python"]
# Wed, 04 Feb 2026 21:05:51 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:05:51 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:06:19 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 04 Feb 2026 21:06:20 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8da9a1d07ad7ea62c87094fba16781bc925d1737240296d82d769222878135`  
		Last Modified: Wed, 04 Feb 2026 20:09:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937f0c13f93c6d2ec9646369ae6d346959d33769edea08d12348814dfdcd118d`  
		Last Modified: Wed, 04 Feb 2026 20:09:20 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a879e81cbd5e0df52caf1053cd7e95842260ce3e93c6a3e4405ccf93e12b166c`  
		Last Modified: Wed, 04 Feb 2026 20:09:20 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856fd829094d14f7cfb7e1acf472e1d14763dde1d665c2b6aa22d3b14ebb24e4`  
		Last Modified: Wed, 04 Feb 2026 20:09:20 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680213b75387920254ead7e301d0cd556c68f0c0b07448f7aa9027e5590c1c55`  
		Last Modified: Wed, 04 Feb 2026 20:09:26 GMT  
		Size: 58.9 MB (58909149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d8fff5552af118699f6db9e9988f1531b844e4d460ba824910628bb1f00984`  
		Last Modified: Wed, 04 Feb 2026 20:09:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c1276dbb5a02f07f6fefff7752e77fe39dca4f8bf14b3b793ae60b4dfdce28`  
		Last Modified: Wed, 04 Feb 2026 21:06:24 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c17653cb9fadf3a37122102bb28e11e71cdb9f24d427084962a1b71229dc5e`  
		Last Modified: Wed, 04 Feb 2026 21:06:24 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47805d54877da8145559911b1f3d2289f10c48ac35232982f496ea05e9d2690`  
		Last Modified: Wed, 04 Feb 2026 21:06:25 GMT  
		Size: 8.4 MB (8427876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce1d0685e172e3e00141eeac97f2cad04dee0a44a4fc625a6a78636a5277c2c`  
		Last Modified: Wed, 04 Feb 2026 21:06:24 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.13-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull hylang@sha256:bb238b546fc7ed86c4cedacb1d490feca2ebdead4019b64c38fc660bc2b6b5a7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1902918412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad86cad8ac70f006fec489aeae0d318899d5a142a9c5e336a39737ff7bfe670b`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 04 Feb 2026 20:05:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Feb 2026 20:05:10 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 04 Feb 2026 20:12:04 GMT
ENV PYTHON_VERSION=3.13.12
# Wed, 04 Feb 2026 20:12:04 GMT
ENV PYTHON_SHA256=96159fcb523ae404b707186a75b4104ee23851e476a5e838e14584cf1e03f981
# Wed, 04 Feb 2026 20:12:46 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 04 Feb 2026 20:12:46 GMT
CMD ["python"]
# Wed, 04 Feb 2026 21:06:13 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:06:13 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:06:48 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 04 Feb 2026 21:06:49 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09f561cc9817aa5a71306c1f7a3185d4427e4552b15b4a465e8b8457f965985`  
		Last Modified: Wed, 04 Feb 2026 20:06:33 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b8630af6c7b0ce1ea7c3a422843d98abcf56718529bc1a38039030b1094970`  
		Last Modified: Wed, 04 Feb 2026 20:06:31 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de7fbbec08e8e332e2c2627cc97da93601c528b8a9ddf633dec73fc391354c9`  
		Last Modified: Wed, 04 Feb 2026 20:12:52 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744636fe0d1c7237850076a73196a3912aa5f15d64979aa50e76d7773d77d47f`  
		Last Modified: Wed, 04 Feb 2026 20:12:52 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9873e3ef7dbdc2fb4e14ce872907ab809d1abcd8a5e06fea87cf349e23c3d9f`  
		Last Modified: Wed, 04 Feb 2026 20:13:03 GMT  
		Size: 58.9 MB (58917376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739df5b51b0f44dcdbcdc88092b9ccfbc06e1b2b5eda0dea3753eccb621d52d2`  
		Last Modified: Wed, 04 Feb 2026 20:12:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bae0a28fecfb751d330ed45951f50adfee0cde6efaeb28e701ab863ed7e12cc`  
		Last Modified: Wed, 04 Feb 2026 21:06:53 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f16026fd2542d9de06ec645c8c3a9f43c74969f8e6e2c55a2b6112f4e124e2a`  
		Last Modified: Wed, 04 Feb 2026 21:06:53 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e46a0078d5ac75b59ecae3ff1231a74679cda4d0dc1fe5ba79ad1f84a52c256`  
		Last Modified: Wed, 04 Feb 2026 21:06:54 GMT  
		Size: 8.3 MB (8331288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b4417aac1ff9f32a6f7054504c9a89a822c25314caf3252c4927a2b9a064bb`  
		Last Modified: Wed, 04 Feb 2026 21:06:53 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
