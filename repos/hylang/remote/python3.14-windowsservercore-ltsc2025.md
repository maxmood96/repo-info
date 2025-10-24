## `hylang:python3.14-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:22e6d0aaf7dd7ae9fe4be23f9b4f0dd669ad592afe2e9ce922dd40502e137bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `hylang:python3.14-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull hylang@sha256:7413f68cc03d4265b6e37cd90c9a331980e6893bdf3757a47a651ea310fd59cb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3289737458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e22da29e06a995eece571dbe8991856a69c40f5d4c71d00ee1a9006b7717614`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:26:01 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 24 Oct 2025 18:26:02 GMT
ENV PYTHON_VERSION=3.14.0
# Fri, 24 Oct 2025 18:26:02 GMT
ENV PYTHON_SHA256=52ceb249f65009d936e6504f97cce42870c11358cb6e48825e893f54e11620aa
# Fri, 24 Oct 2025 18:26:49 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:26:50 GMT
CMD ["python"]
# Fri, 24 Oct 2025 19:22:41 GMT
ENV HY_VERSION=1.1.0
# Fri, 24 Oct 2025 19:22:41 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 24 Oct 2025 19:23:22 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 24 Oct 2025 19:23:23 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2306afc06fe394817b697769f818a638f384b35e7a7bdcfd10e74c6c7ee210f8`  
		Last Modified: Fri, 24 Oct 2025 18:23:16 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555e21fbe78df3503ea38a395ba413b5f558c015e0dfc07f0103a646eeec3f78`  
		Last Modified: Fri, 24 Oct 2025 18:27:16 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0bf2e24210488dfa0a68f5cf0859a7a3223925b885084b48224d8a44aa6060`  
		Last Modified: Fri, 24 Oct 2025 18:27:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a551edbd83e434e74b91dc02db01c8a5b6fb4f1d679d9bb434de70e9f78cf6`  
		Last Modified: Fri, 24 Oct 2025 18:27:16 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f6eb59176e72aebdf64a7b691c8b363a10f6f49f76cf66567a3fd45414efde`  
		Last Modified: Fri, 24 Oct 2025 18:27:23 GMT  
		Size: 60.8 MB (60788485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42596bb77eccdcbb1040b5350decf6f5b00fb6b12d3839bc54cd0f73259cdd50`  
		Last Modified: Fri, 24 Oct 2025 18:27:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c451cfa054d7b75c32d84f861dfbabd28ae8a0bc724323f130cfb57b7c3122`  
		Last Modified: Fri, 24 Oct 2025 19:23:35 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7945ad44adf41dfb5eafdb9737fc68aa027966b84e7d5548af16f7c0e07cd1ab`  
		Last Modified: Fri, 24 Oct 2025 19:23:35 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f54b583fc8bc78ad024e06b89a4f51bf2eeede1cb60b9490ada82da3c139c0`  
		Last Modified: Fri, 24 Oct 2025 19:23:36 GMT  
		Size: 8.6 MB (8591481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890a41f41b85e978a8146dfe8a11f1456ba1c873236fb623d3cb4b700fb95a85`  
		Last Modified: Fri, 24 Oct 2025 19:23:35 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
