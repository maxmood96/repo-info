## `hylang:1-python3.12-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:8742d853689ccc7bfcd1c0255a281aba40393881b212c3def423d2d2dd9e3b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `hylang:1-python3.12-windowsservercore-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull hylang@sha256:8f20243b5e91c88141edb0031bb6b60f0d9477ad798c6e33c6717025bd4357f0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3464111975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53e9e01949c67e11443882cfbc889304fe53ba8521ad5f4e4778c1dadd56ea6`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 03:25:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:25:57 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 18 Apr 2025 03:25:59 GMT
ENV PYTHON_VERSION=3.12.10
# Fri, 18 Apr 2025 03:26:01 GMT
ENV PYTHON_SHA256=67b5635e80ea51072b87941312d00ec8927c4db9ba18938f7ad2d27b328b95fb
# Fri, 18 Apr 2025 03:26:46 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:26:47 GMT
CMD ["python"]
# Fri, 09 May 2025 17:35:52 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 17:35:53 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 17:36:29 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 09 May 2025 17:36:30 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bfebb56527ad4aef8432daaeff9617209a68719ee3b14c1df22e71769f7930`  
		Last Modified: Fri, 18 Apr 2025 03:26:52 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758a8f7a55279782208ac16d3e6ffcdb5635843bd91501c0ead16c1631fcb8f1`  
		Last Modified: Fri, 18 Apr 2025 03:26:50 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bdb2e4c2d70694a42c4b2a52bf8682b1564f1d242588b30beef04febd6f28c`  
		Last Modified: Fri, 18 Apr 2025 03:26:51 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53462f7e0697459c262c3405ff3b9243f44be9d21e2653ff37fb601094ea362e`  
		Last Modified: Fri, 18 Apr 2025 03:26:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc17563038ddffa9902157bbdb1eec06015ed76b6a1f1806d009ba14f3ff94a`  
		Last Modified: Fri, 18 Apr 2025 03:26:56 GMT  
		Size: 60.3 MB (60265448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55123ad269da486599e9108ca32d3015309d97d4b4a9c7d6f5ca05c8ebb7085d`  
		Last Modified: Fri, 18 Apr 2025 03:26:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa8593db6556c380a6607878db74273e4642f63afc11e5f6dcc6405e92959dd`  
		Last Modified: Fri, 09 May 2025 17:36:35 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fddb7c6388058bd1f66ce783e054164b7f78f3ac57cf7b57b8472596ae70513`  
		Last Modified: Fri, 09 May 2025 17:36:35 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28355e67379fed5acd6563572d2b8a27f832c7ba3667ea2bc8a6cdb140bdf563`  
		Last Modified: Fri, 09 May 2025 17:36:37 GMT  
		Size: 8.7 MB (8674611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae23b1bffd35404e99be6151569db2bc045b97448d909275ba651665a9d5c3e9`  
		Last Modified: Fri, 09 May 2025 17:36:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
