## `hylang:1-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:a1edf7cc80fbc74106025f3fbae2d43b930ae08e1dcb33ed3140414043145981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `hylang:1-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull hylang@sha256:ad01479ef2c74abe339f26e53ef1b24d115669afe96d6ba8ab7c8b683d9f6627
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2347867456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae709afdab05e7e8f2626b3c36a238e96c13c7bb74205dfcc91493b8bfd5ee2`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 12 Jun 2025 22:41:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jun 2025 22:41:31 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 12 Jun 2025 22:41:31 GMT
ENV PYTHON_VERSION=3.13.5
# Thu, 12 Jun 2025 22:41:32 GMT
ENV PYTHON_SHA256=c1cb40978b28f696b111c36034a1bdeda17d25e35c74a08ef5e5ff405a63fc20
# Thu, 12 Jun 2025 22:42:08 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 12 Jun 2025 22:42:09 GMT
CMD ["python"]
# Thu, 12 Jun 2025 23:00:12 GMT
ENV HY_VERSION=1.1.0
# Thu, 12 Jun 2025 23:00:13 GMT
ENV HYRULE_VERSION=1.0.0
# Thu, 12 Jun 2025 23:00:47 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 12 Jun 2025 23:00:48 GMT
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
	-	`sha256:edb2bc983e26c4beaaaa6d256736139d58569850cfcf6f2e3262c6400d3c13d6`  
		Last Modified: Thu, 12 Jun 2025 22:43:45 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581318992fa70b0d36e2a47384c7899cfb90e86038bdebfc857ee3a9b1461623`  
		Last Modified: Thu, 12 Jun 2025 22:43:45 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f43e046fbff66f0ae08f54d23a0ec37640cdd812a3b60e08cf2460a6738b2fc`  
		Last Modified: Thu, 12 Jun 2025 22:43:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f53f0f9aa99f8cfc9f8748c828e2fc7338897c6551cb7c0ead806bbc83e24dc`  
		Last Modified: Thu, 12 Jun 2025 22:43:46 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78aa41a8a46ccd14ae673902fd0ec46a14726172baccf1575f43ec3dd34e2a90`  
		Last Modified: Thu, 12 Jun 2025 22:43:52 GMT  
		Size: 59.1 MB (59106366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e17030daf438bf9a0febbb83bcf1741ad5f367a61bcf6cfa5a6b85344ef786f`  
		Last Modified: Thu, 12 Jun 2025 22:43:46 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0744a3ce89f6d26d600a0af367b61f3ce1096a0f3c344895c12bc9aba949ecef`  
		Last Modified: Thu, 12 Jun 2025 23:06:13 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73faddf1f3ccebd81e7210ff7adb3e0c5f9512f82d814702568366643fb71af`  
		Last Modified: Thu, 12 Jun 2025 23:06:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15196ad011d5c4f7a2779722a6095e7cdc0b90eff62da6c3bc87f3e15fd63c45`  
		Last Modified: Thu, 12 Jun 2025 23:07:36 GMT  
		Size: 8.5 MB (8499176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38fc84ae2c9e298d3edd00e5d96f9dfa10b4655e8a568264a774513a9c2c5f4`  
		Last Modified: Thu, 12 Jun 2025 23:06:17 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
