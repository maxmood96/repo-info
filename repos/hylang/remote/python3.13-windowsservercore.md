## `hylang:python3.13-windowsservercore`

```console
$ docker pull hylang@sha256:e38e5c719b664191fb1cf9411864692b22b23fab57862c172b9194470dd7e833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `hylang:python3.13-windowsservercore` - windows version 10.0.26100.32860; amd64

```console
$ docker pull hylang@sha256:124ab94fd3ef1574099d89c14f2d24d6e290b2630a979e0d65f891bc6f25a32b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2273448344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac0c16dceefde44dbd538190701aff21c242314dee2bf941a6d111554fa0e3c`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:50:03 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 12 May 2026 23:50:04 GMT
ENV PYTHON_VERSION=3.13.13
# Tue, 12 May 2026 23:50:05 GMT
ENV PYTHON_SHA256=3c9c81d80f91c002ced86d645422d81432c68c7d9b6b0e974768ca2e449a4d00
# Tue, 12 May 2026 23:50:48 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:50:49 GMT
CMD ["python"]
# Mon, 08 Jun 2026 22:49:51 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:49:53 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:51:21 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Mon, 08 Jun 2026 22:51:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c87bd87005852a4147304998d45aaefe6ed6f1c31bd619c918ede8f333f7ec8`  
		Last Modified: Tue, 12 May 2026 23:40:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf388088977d826aed40a8d3c834130136d91c5b9f98c8fe354a761d972d48a7`  
		Last Modified: Tue, 12 May 2026 23:50:53 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84325d74b374aa3c1edaeac6391129f9432548c5e35a733e72cda84f3770a79d`  
		Last Modified: Tue, 12 May 2026 23:50:53 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7236569f44ce0bb0e04470f68976205749614a3f9bcd593bd32778a73e402e28`  
		Last Modified: Tue, 12 May 2026 23:50:53 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc140666cc707ddc346c87a4a3c9cbb2923bda3a1097a28be779f34830fe7a55`  
		Last Modified: Tue, 12 May 2026 23:50:59 GMT  
		Size: 59.0 MB (59023073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01510e8cfb4c54c71b466b74c5ca68c03647d3dbd452accf50d2186e54ee9aec`  
		Last Modified: Tue, 12 May 2026 23:50:53 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e758550d57deef4b30ca05da3322dfb1862f870525ef316e068e2c22c472e24`  
		Last Modified: Mon, 08 Jun 2026 22:51:27 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0f23c3631021bee93a0b11ec0d936997198c0416532026034ac3bb8401f730`  
		Last Modified: Mon, 08 Jun 2026 22:51:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7dec574b28ba503a0720aab0c242d7aaa6b6610148a7f5ada7edbbb50191ee`  
		Last Modified: Mon, 08 Jun 2026 22:51:28 GMT  
		Size: 8.5 MB (8472782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37fb469a9896ec54f25f5acba35da6d3906df2492a1dbc03f24838cef7b9770`  
		Last Modified: Mon, 08 Jun 2026 22:51:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.13-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull hylang@sha256:60a1aa08d7cdb79084df9cdf4b340fd9de2412951bcd78b14a4b125b0c93a188
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190474640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d55b21e2ec2665d4840eff2c0f2aad41b0f0c7f425d134316ba27c7455d1ce`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:39:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:58:13 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 12 May 2026 23:58:13 GMT
ENV PYTHON_VERSION=3.13.13
# Tue, 12 May 2026 23:58:14 GMT
ENV PYTHON_SHA256=3c9c81d80f91c002ced86d645422d81432c68c7d9b6b0e974768ca2e449a4d00
# Tue, 12 May 2026 23:58:52 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:58:53 GMT
CMD ["python"]
# Mon, 08 Jun 2026 22:51:14 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:51:17 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:53:00 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Mon, 08 Jun 2026 22:53:00 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917dd62015b1447671d0b141b1522081735e979c185e6644bec43931db85c017`  
		Last Modified: Tue, 12 May 2026 23:40:45 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726b980ec9302ef258f2bff1dd925cc5bac52c355ccf348d87071044629a355f`  
		Last Modified: Tue, 12 May 2026 23:58:58 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e554f4811458d424db6081e5c92f561e4fbc7075aeeda27b9298e1a7d98a17db`  
		Last Modified: Tue, 12 May 2026 23:58:58 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a0d0292de41f0b03b01c8fb698a17dad90956abf141aa578363fc74fc213ec`  
		Last Modified: Tue, 12 May 2026 23:58:58 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c16d906ff545c24ea4a1a77e1f4a6914db7225a1944076e7a6b1983179cfc1`  
		Last Modified: Tue, 12 May 2026 23:59:04 GMT  
		Size: 59.4 MB (59373641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec1b0b9ede17985d6c43a1ef1908673f5de3eb80e2ddb6fe304a6f3a9a7c099`  
		Last Modified: Tue, 12 May 2026 23:58:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ff803f608eba961b275d1aa961e2c58f5c690827547af08d4516db4009e6bb`  
		Last Modified: Mon, 08 Jun 2026 22:53:05 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a46810a04a4124eb45b61c318fe48152e2039023c17d6c26277189d821630f`  
		Last Modified: Mon, 08 Jun 2026 22:53:05 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f16405dcf2e4545d1116a9afbff3f66471a4210850f120bb02279fb8741d8c`  
		Last Modified: Mon, 08 Jun 2026 22:53:07 GMT  
		Size: 8.7 MB (8669883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d015710525a40d6be035c5696d502d0d9804470bf136905198104c50d600db`  
		Last Modified: Mon, 08 Jun 2026 22:53:05 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
