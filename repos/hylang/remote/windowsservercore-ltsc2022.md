## `hylang:windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:069f4b51838a46d57cd522ac6908124b4aeccbbd9048ff930e4c49937830a622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `hylang:windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull hylang@sha256:f52b333307bcda3d194fa6702c7d1219aa76437021015e095f62ac1ac895736e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2347812610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436613bfa37d20869c02b18be4895b7acfdbc13d17ef72bce7fe23782e0a0fd2`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Tue, 10 Jun 2025 21:37:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Jun 2025 21:37:51 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 10 Jun 2025 21:37:51 GMT
ENV PYTHON_VERSION=3.13.4
# Tue, 10 Jun 2025 21:37:52 GMT
ENV PYTHON_SHA256=94f53bb832539ea02d6ce581d7c1fcc36228e04a611b8dcfe797ad4bbc0a45c1
# Tue, 10 Jun 2025 21:38:43 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 10 Jun 2025 21:38:45 GMT
CMD ["python"]
# Tue, 10 Jun 2025 22:16:35 GMT
ENV HY_VERSION=1.1.0
# Tue, 10 Jun 2025 22:16:36 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 10 Jun 2025 22:17:04 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 10 Jun 2025 22:17:05 GMT
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
	-	`sha256:d1a8ed891b7923d283e8c681035f557c3fa6004544c0048282d5bac0072b020c`  
		Last Modified: Tue, 10 Jun 2025 21:40:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42f6085a3d616f9ad0b63c836ac4cd3d0bd7b3c92e4b71fdeaaa4d888fdcabb`  
		Last Modified: Tue, 10 Jun 2025 21:40:10 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea36ce47eb0d27020fa86d660c02442de0278b5d410ace884b0f1e91c262cca4`  
		Last Modified: Tue, 10 Jun 2025 21:40:10 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237605e27b7f7285f4b6cac5962bba8a63be49df77b113e6178e2a5c7f1e9987`  
		Last Modified: Tue, 10 Jun 2025 21:40:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee4db0e10fafa7a9cb77e2b25dc07046b9dce5f9f64544af3f32e0e82cf1da9`  
		Last Modified: Tue, 10 Jun 2025 21:40:16 GMT  
		Size: 59.1 MB (59099068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7c39b22f483b1be0df0dcc2367ba6f361e19cdd0fce5450c95eabe50a8cd8e`  
		Last Modified: Tue, 10 Jun 2025 21:40:11 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4aec3d5f7335b632c2670569fb2b7e54a91229074c8cedb75be60955d03be8`  
		Last Modified: Tue, 10 Jun 2025 22:17:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9741b9bca35fd469a1b3eca333f618d7ff0d33d9de579b7e31fc0d4632de1654`  
		Last Modified: Tue, 10 Jun 2025 22:17:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6de2c07f87975ca5d5d09ba56188500a820f45758f880dbeca30a2b40b7d10`  
		Last Modified: Tue, 10 Jun 2025 22:17:40 GMT  
		Size: 8.5 MB (8451516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba0f2ba4577f36093c8f68c62fcf3e08305c764c5a35db932627e54f20b064f`  
		Last Modified: Tue, 10 Jun 2025 22:17:39 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
