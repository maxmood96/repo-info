## `hylang:windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:f1dc69c313d3e9619f9e624339c2eebbea670a7b6ea2c12f24986accf860d252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `hylang:windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull hylang@sha256:1b7281f672ecae8bdea25c975f5587395ff487d07beb42dcad7f28cefa9c4d44
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349285599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed69080c66409e070f15d178744e2a9493c072f0c89688be335160a10802016`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Tue, 07 Oct 2025 20:43:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Oct 2025 20:43:49 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 07 Oct 2025 20:50:40 GMT
ENV PYTHON_VERSION=3.13.8
# Tue, 07 Oct 2025 20:50:41 GMT
ENV PYTHON_SHA256=f17f216f057ed805b653f80a607c0d97d52884b4ed00380acabf199f0c025b14
# Tue, 07 Oct 2025 20:51:19 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 07 Oct 2025 20:51:20 GMT
CMD ["python"]
# Tue, 07 Oct 2025 21:09:12 GMT
ENV HY_VERSION=1.1.0
# Tue, 07 Oct 2025 21:09:13 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 07 Oct 2025 21:09:48 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 07 Oct 2025 21:09:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55aae93905df42ad1616e54b1014ca296f220a9ca9884cb79c33417dd5d013d`  
		Last Modified: Tue, 07 Oct 2025 20:50:30 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee29297541ec950c18c3ec0d86af1d7d690d8b9261863f53d0f2650d3342013a`  
		Last Modified: Tue, 07 Oct 2025 20:50:31 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a82c6dcaec75538d698e2611a49227023c4430d76cd2e937e901b7eb27b06e`  
		Last Modified: Tue, 07 Oct 2025 21:41:56 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c6cfd73f11e02743103f90146e16ac5371e898148e3b09be404e80097fcf64`  
		Last Modified: Tue, 07 Oct 2025 21:41:56 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4150b11d8fd6ad019418a052171a1321f8347ac79c1edd2c604b5b7d64a91af4`  
		Last Modified: Tue, 07 Oct 2025 22:09:33 GMT  
		Size: 58.6 MB (58642084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f2d402b5fe0dc3bfbdfd72801b785811ec34367061d651e478523dbaeafa65`  
		Last Modified: Tue, 07 Oct 2025 21:41:56 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108cd3f4568424a9ed6411c9ef065d03fddea2f764938b6bda1ed656031ecec1`  
		Last Modified: Tue, 07 Oct 2025 21:10:08 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4333ee54e4c4f16ef6a6680c259264c1adef4f9a1055bf3427ac3da13eb18f35`  
		Last Modified: Tue, 07 Oct 2025 21:10:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0619f1541d1b84511cdfd5ea84ca8a4e35417cbcedb7cacae86b75d1f5ca105`  
		Last Modified: Tue, 07 Oct 2025 21:10:09 GMT  
		Size: 8.5 MB (8488077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e109f8f73cf145a79072b6124b5f836e99f8a87084aaa1c4171326c451d51aa7`  
		Last Modified: Tue, 07 Oct 2025 21:10:07 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
