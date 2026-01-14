## `hylang:python3.13-windowsservercore`

```console
$ docker pull hylang@sha256:9897db8d4e0ab622eaba2a9d0119a817c91f2a384e123200aa417d3d7c9ad214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `hylang:python3.13-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull hylang@sha256:279dfc353896c9bdb4f5a1fc445c46f49ab4f9845e1f7bd502135e208ad67b44
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1563147155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5b18a03269d8c7fcc8caec9dda8824834154de8b2fa150980b37b22c9b611f`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:53:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:01:24 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 13 Jan 2026 23:01:24 GMT
ENV PYTHON_VERSION=3.13.11
# Tue, 13 Jan 2026 23:01:25 GMT
ENV PYTHON_SHA256=30d4654b3eac7ddfdf2682db4c8dcb490f3055f4f33c6906d6b828f680152101
# Tue, 13 Jan 2026 23:02:03 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:02:04 GMT
CMD ["python"]
# Tue, 13 Jan 2026 23:42:36 GMT
ENV HY_VERSION=1.1.0
# Tue, 13 Jan 2026 23:42:37 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 13 Jan 2026 23:43:08 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 13 Jan 2026 23:43:09 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:56:33 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e80c7a7f1e619446ad0a75155ab3ad1a8da7712a1614331cebc9b4d2f8665b8`  
		Last Modified: Tue, 13 Jan 2026 22:58:32 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a3f9db7bb6367c3f39b3002ca5e40d5262cc734f61dc1be2e0543b728f5a5b`  
		Last Modified: Tue, 13 Jan 2026 23:02:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c964053a13707fe67dc8b53aa5b6c9ac064cdba1a11e572ae98e3cf5f4dd543`  
		Last Modified: Tue, 13 Jan 2026 23:02:21 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca01222e389a3dd818e7ba7cfeb41d6b4974eee525e705f638be6f9f2c2ca08`  
		Last Modified: Tue, 13 Jan 2026 23:02:21 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4e337a8bb209adb29e364cd3209832f16408e79d5382615ac0f398107291af`  
		Last Modified: Tue, 13 Jan 2026 23:02:26 GMT  
		Size: 58.8 MB (58826548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b630af33bded8b9b71370129a5588bfa980fc851f7be2391d2c70d3be8f6dd8a`  
		Last Modified: Tue, 13 Jan 2026 23:02:21 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848760819d29d64e396e97dd70b5b8aeaa28105c99ef98f9949fc11d2843d2f2`  
		Last Modified: Tue, 13 Jan 2026 23:43:25 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0848cb35c466aeb471a6a48f83502ff421964b9746b45787b2c8568f7962cc`  
		Last Modified: Tue, 13 Jan 2026 23:43:19 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cacb1f2cec6319f749d4d045b2d632d37907d96634f306ae9aaf7d84572436d`  
		Last Modified: Tue, 13 Jan 2026 23:43:20 GMT  
		Size: 8.5 MB (8549827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b6377bf4d88d0d22239a33405b682dbd7f362817407984bd1f89fe493a30c5`  
		Last Modified: Tue, 13 Jan 2026 23:43:19 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.13-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull hylang@sha256:4e7c2eef00065a666dadda794ffa73a8300f02d5a8b2260555804ddcb10f103d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1902969350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f3af09e6a2a279adee68ebbb94d3f95ee81583955292cf149ddfc2213b50d3`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 22:53:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:12:37 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 13 Jan 2026 23:12:38 GMT
ENV PYTHON_VERSION=3.13.11
# Tue, 13 Jan 2026 23:12:38 GMT
ENV PYTHON_SHA256=30d4654b3eac7ddfdf2682db4c8dcb490f3055f4f33c6906d6b828f680152101
# Tue, 13 Jan 2026 23:13:21 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:13:22 GMT
CMD ["python"]
# Tue, 13 Jan 2026 23:39:34 GMT
ENV HY_VERSION=1.1.0
# Tue, 13 Jan 2026 23:39:34 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 13 Jan 2026 23:40:01 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 13 Jan 2026 23:40:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:28:58 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f681901ae8b8270ef4ad40879b419cd45d092d5d347a675266218039d5b88a0`  
		Last Modified: Tue, 13 Jan 2026 23:01:20 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592680e3698d8f38797a3d48148155e0f3ed6fd84fe59b55aa983306e8e7430e`  
		Last Modified: Tue, 13 Jan 2026 23:13:40 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98725bbfac9e58f5e9f204d42ddeac79b826f28e2cba15876058fb24804ba2b`  
		Last Modified: Tue, 13 Jan 2026 23:13:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576db8afdbb7e2ca01068a1839bba93677d4059bba9b7e0dc0c2017fbff3927d`  
		Last Modified: Tue, 13 Jan 2026 23:13:40 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2409f31cd7c69f59ef9c0897b436fcbeb4c7c5c7b455fb494ff4c2b804b2f1d7`  
		Last Modified: Tue, 13 Jan 2026 23:13:49 GMT  
		Size: 58.9 MB (58852398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9acb5c3d35d8880f2106ce6ea2d85b131872f1c02b0f89eabd16b383be1e80`  
		Last Modified: Tue, 13 Jan 2026 23:13:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdbdc16f244dbd01e7ea5bb257d7910eb37a99ad6800d72b3c11861c079039a`  
		Last Modified: Tue, 13 Jan 2026 23:40:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09be768fd1ee9bbc67c1c6cb33066e1f4a785bb08517f1f4ad0fb0fb426f569`  
		Last Modified: Tue, 13 Jan 2026 23:40:14 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eeb8881d3819c21cb3148af8d448a27894fda197bcb0cb63e65b84259dacf6d`  
		Last Modified: Tue, 13 Jan 2026 23:40:15 GMT  
		Size: 8.4 MB (8447373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2ad57a91b67543cb43e38465e7be742c213977252c7497c4d6f392451a21a0`  
		Last Modified: Tue, 13 Jan 2026 23:40:14 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
