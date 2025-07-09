## `hylang:1-python3.14-rc-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:825cbba4fc7def0ac2d1624275ae2a71e823911185e813ccc16d7bf22e8f1721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `hylang:1-python3.14-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull hylang@sha256:a7b181f59cd8ed8f49f953bafdacbec7eed46f72329ba444f98feec266f510bb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349889042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1887b982cb81de041efbb63a1c2dc1cd7800539dc54abc72b387066765f7fc`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Tue, 08 Jul 2025 20:31:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Jul 2025 20:31:51 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 08 Jul 2025 20:31:53 GMT
ENV PYTHON_VERSION=3.14.0b4
# Tue, 08 Jul 2025 20:31:54 GMT
ENV PYTHON_SHA256=0f8bbdfd7d1f99a0b8df86278a99e4c0248582b93e9d7d4d6e63e787098dad00
# Tue, 08 Jul 2025 20:33:18 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 08 Jul 2025 20:33:19 GMT
CMD ["python"]
# Tue, 08 Jul 2025 21:08:36 GMT
ENV HY_VERSION=1.1.0
# Tue, 08 Jul 2025 21:08:37 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 08 Jul 2025 21:09:20 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 08 Jul 2025 21:09:22 GMT
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
	-	`sha256:88e6e2bb48062d975aed98679f32f5c586fe5447e488187b458636c2a7f5d61f`  
		Last Modified: Tue, 08 Jul 2025 21:07:54 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28db1989669fe1ce8b2e99189395ef3294d0139c4ee230fa798fa643f9b0998f`  
		Last Modified: Tue, 08 Jul 2025 21:07:54 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf130763c173d9b795649ed11a8205e61586f6bc47a38f178ab26ef568806396`  
		Last Modified: Tue, 08 Jul 2025 21:07:54 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd35d1fb9a2b9b8ff0879e3fedaca04f80f362d95aa9227c3d645b680c81671`  
		Last Modified: Tue, 08 Jul 2025 21:07:55 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c72dfd2e097270d5e6c97c24e2cb953b267a0aea5c86e4a1c1dfa634e69919`  
		Last Modified: Tue, 08 Jul 2025 21:08:01 GMT  
		Size: 61.1 MB (61145425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b10149fc3f88d74b44c33da07d6d3e26e9986865ba9e7d25b00a74c3962009`  
		Last Modified: Tue, 08 Jul 2025 21:07:55 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b643754785b5098a5c9276ee6c3f96ce7bbd95d2830a0828d23744875e1138`  
		Last Modified: Tue, 08 Jul 2025 23:19:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83b484afc8f506e265a801665182c3a09b9d2e7592f2b839af640cd50454fd1`  
		Last Modified: Tue, 08 Jul 2025 23:19:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b44ae17dcbd19fe304c7bb1a377fceceba1c113f7aaa535e1ad5bdef60be80`  
		Last Modified: Tue, 08 Jul 2025 23:19:25 GMT  
		Size: 8.5 MB (8481773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078b6f225d3677812a1b6bce5d6d10ca184cba609884cde3c6dbb664bcf90f86`  
		Last Modified: Tue, 08 Jul 2025 23:19:25 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
