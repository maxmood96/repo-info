## `hylang:python3.13-windowsservercore`

```console
$ docker pull hylang@sha256:ffd4cec7ebfe3ccf5c3c2d4fa595efdcba8d04e7abda4d232fc5895e6006ca31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `hylang:python3.13-windowsservercore` - windows version 10.0.26100.32860; amd64

```console
$ docker pull hylang@sha256:0ce8e85f53ce9fc60e89b1cc3330ddfade4f5d20b67a510470e525271b8c0c38
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2273443413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0212728365dfeb9fe00c29576833c80ce4cc110ed8fa7111e76aa38eebb566b0`
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
# Wed, 27 May 2026 00:14:52 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:14:52 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:15:30 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 27 May 2026 00:15:30 GMT
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
	-	`sha256:9765c11b19b62521756028240f280b37c9c5b60c9c0b8c5c9cd6640fa2b992ce`  
		Last Modified: Wed, 27 May 2026 00:15:34 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f4a09cb48c8ad6372bcfefb517403e0b1e3cf2b33625e7d5fa37ae26148299`  
		Last Modified: Wed, 27 May 2026 00:15:34 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3627a4534a397ee70bd1e79f41ce0a98fc58636a7a1cfe4d3906421c91888a94`  
		Last Modified: Wed, 27 May 2026 00:15:36 GMT  
		Size: 8.5 MB (8467919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db04a8e4cd674dc18472521add76bd73886e260395b8feabae8e56aa7148a54f`  
		Last Modified: Wed, 27 May 2026 00:15:34 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.13-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull hylang@sha256:82e0b72c54a7f9c12fd0585a1d359608435e8fec8e5ac5c7d0e9bd0c1c387c12
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190469448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a3b8490061f25bd5bde19892d8e642db768368b05323f73f98ad1ada8650cf`
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
# Wed, 27 May 2026 00:15:04 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:15:05 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:16:11 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 27 May 2026 00:16:12 GMT
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
	-	`sha256:27d19289659feb06bf4e5521b567f45290e9839d82644b60c3e3d253dc98711c`  
		Last Modified: Wed, 27 May 2026 00:16:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa2966fd97b22f4eee5749ab2c166b6ed5f13b20e07acdc9c26a380c352935a`  
		Last Modified: Wed, 27 May 2026 00:16:16 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3c772b782c507d80a47b61dddc18668b4421c4b53efdf364cea3629d06b8a2`  
		Last Modified: Wed, 27 May 2026 00:16:17 GMT  
		Size: 8.7 MB (8664738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab9c283ca77c3d657824969548e30056cb4b4ff7339820cb44c3de8ed3c3944`  
		Last Modified: Wed, 27 May 2026 00:16:16 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
