## `hylang:python3.14-rc-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:cfbade2ea2fb810e713c066f40a4b778578bc656082654473ab6919e8bc60ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `hylang:python3.14-rc-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull hylang@sha256:42a22757b53e3046999bf636c763894a2ec0306f5f7a7be2a1efad11a34b263e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3546045772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843ec3fd3c7cacc9e0a5b55052dd5ca63ac19fc3ff2a3f983b6f395e1cdf5838`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Tue, 08 Jul 2025 20:38:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Jul 2025 20:38:11 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 08 Jul 2025 20:38:12 GMT
ENV PYTHON_VERSION=3.14.0b4
# Tue, 08 Jul 2025 20:38:13 GMT
ENV PYTHON_SHA256=0f8bbdfd7d1f99a0b8df86278a99e4c0248582b93e9d7d4d6e63e787098dad00
# Tue, 08 Jul 2025 20:38:57 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 08 Jul 2025 20:38:59 GMT
CMD ["python"]
# Tue, 08 Jul 2025 21:13:50 GMT
ENV HY_VERSION=1.1.0
# Tue, 08 Jul 2025 21:13:52 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 08 Jul 2025 21:14:26 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 08 Jul 2025 21:14:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2e98dd91b5b6ef9e43226413091865e24ff5dc970e69fb1aa0e8008df38978`  
		Last Modified: Tue, 08 Jul 2025 21:08:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860cd99f5575d1bd0653b9d51040544733121b135c41b3ec5a3ed2b5958d3f34`  
		Last Modified: Tue, 08 Jul 2025 21:08:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66cf291a7f8e3178a7b061ebd66dc213c24157678c45234d718ef14e4a9b2798`  
		Last Modified: Tue, 08 Jul 2025 21:08:06 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de44c09b42e8c5d075a59364173a6c2e340d5ea409fb70d905e9d971587453b`  
		Last Modified: Tue, 08 Jul 2025 21:08:06 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311c0e34fd5e783fcd70ee5483a27c0a0f53f866454f716401716ce995c0b88e`  
		Last Modified: Tue, 08 Jul 2025 21:08:15 GMT  
		Size: 61.3 MB (61263842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a834f6f4b873be09cc95f49c335ffe0b39bd40ab0a8c4d1efd16fb2388509d`  
		Last Modified: Tue, 08 Jul 2025 21:08:16 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563809e7c25f9ac9de3dce7452a248d2ca06db83f9e50f5f8569eaaa43204094`  
		Last Modified: Tue, 08 Jul 2025 23:19:32 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546c3d2087a9f423d255e4c00e4c30c2f1fb461fd5eb59eb1558c3c2705fdadb`  
		Last Modified: Tue, 08 Jul 2025 23:19:32 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0362d3d81005d30a2d971887da27c4d6238e906dd58cc4e5d142d4537408e0`  
		Last Modified: Tue, 08 Jul 2025 23:19:34 GMT  
		Size: 8.6 MB (8597438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733cb337b15e60a8876d9bae0c2473bbb205289c6372a2bd827f0251b0e095cb`  
		Last Modified: Tue, 08 Jul 2025 23:19:34 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
