## `hylang:1-python3.14-rc-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:505467bca744694409dd6a0aaf5ceda71cbffbc56b6e9ebbed35104137d3793c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `hylang:1-python3.14-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull hylang@sha256:4a5ad06f341a567797906343c77f06191769a3e7bdaa2b3ebc7187ce93c40609
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349872514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c14758b4c2e6d47866d85664a8706ef612e872892101639f1259fe9f44b191`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Wed, 18 Jun 2025 16:45:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 18 Jun 2025 16:45:58 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 18 Jun 2025 16:45:59 GMT
ENV PYTHON_VERSION=3.14.0b3
# Wed, 18 Jun 2025 16:46:00 GMT
ENV PYTHON_SHA256=c2f136916e45d3bf9c110ddfe0d3787a2e3c73e313aec983c06e03fa2caa8b3f
# Wed, 18 Jun 2025 16:46:45 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 18 Jun 2025 16:46:46 GMT
CMD ["python"]
# Tue, 08 Jul 2025 16:58:41 GMT
ENV HY_VERSION=1.1.0
# Tue, 08 Jul 2025 16:58:43 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 08 Jul 2025 16:59:25 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 08 Jul 2025 16:59:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77ce54c80c0cf1d0f50b0e33779882df2b68da85bb4823cf97a84f62ccaeb55`  
		Last Modified: Wed, 18 Jun 2025 16:48:38 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e9bf5afe4bc5086a0e0c4681b99295692ed0f0a9d1e6ddff95b2501b734304`  
		Last Modified: Wed, 18 Jun 2025 16:48:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7407e3b7016764652b905814a3d10c60aeb0cb86cbd9cca6bdba684d7a59ab84`  
		Last Modified: Wed, 18 Jun 2025 16:48:38 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb8e3b277fec88bd05881fd6f36316960a3c191f2d607410ba6b59306e66257`  
		Last Modified: Wed, 18 Jun 2025 16:48:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892e48bb233785c91ecd591cef9209ecc6e74b7169a9e158bb990a462edccaf0`  
		Last Modified: Wed, 18 Jun 2025 16:48:43 GMT  
		Size: 61.1 MB (61109785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2727d0aeabb5be6af2d986d71b84d09dc27534a557273b2669dd4a9c68dc5df`  
		Last Modified: Wed, 18 Jun 2025 16:48:37 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b14ee047cc8204c9017c3d21e5d22534b3d1f296f116d3bbbc70515e96ef313`  
		Last Modified: Tue, 08 Jul 2025 17:23:23 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc6e93d7b118ea1efff6546726d8a2ae8ef4281145ea014c5ebfd20665fc7e4`  
		Last Modified: Tue, 08 Jul 2025 17:23:23 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc5f4f8bc547f655da3500024056a91f4c2fc0d0ea4efd6c6bea8c33c0f76b2`  
		Last Modified: Tue, 08 Jul 2025 17:23:26 GMT  
		Size: 8.5 MB (8500809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad9d630a780b6f01b642bcc0ae04a9a10e5ff61b1385083071969c095a618d3`  
		Last Modified: Tue, 08 Jul 2025 17:23:25 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
