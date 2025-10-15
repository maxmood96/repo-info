## `hylang:python3.13-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:368b5d92d12571dc3e0f47945311abe354455be70aeaf47370665b330ea0b72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `hylang:python3.13-windowsservercore-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull hylang@sha256:926eb1f9034f6b007693576e20b69d3af817a7de2d96caabcc45eba5db9d78d1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3287800893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e92e23a519ca30915e88ce76189c12970d2a795a1e2e4d39cfb8024360fbac`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:55:20 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 14 Oct 2025 20:55:20 GMT
ENV PYTHON_VERSION=3.13.8
# Tue, 14 Oct 2025 20:55:21 GMT
ENV PYTHON_SHA256=f17f216f057ed805b653f80a607c0d97d52884b4ed00380acabf199f0c025b14
# Tue, 14 Oct 2025 20:55:58 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:55:59 GMT
CMD ["python"]
# Tue, 14 Oct 2025 21:14:59 GMT
ENV HY_VERSION=1.1.0
# Tue, 14 Oct 2025 21:14:59 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 14 Oct 2025 21:17:05 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 14 Oct 2025 21:17:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b31ef2acd9573fa311450133976eaea07e0ccfd74f3de24d672c7bf465eba24`  
		Last Modified: Tue, 14 Oct 2025 20:51:54 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a501a3b214cea57b153540001e56e8f7fe77064199381518da7d30509d86054`  
		Last Modified: Tue, 14 Oct 2025 20:56:16 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbc87b51a61d7a2ed3ab427f91eed401bed1d4b252fc26b167e1f00f1467b65`  
		Last Modified: Tue, 14 Oct 2025 20:56:16 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc726552ac29e4b450cf5b274d56d65e6a27a89211e5d0932d6f337c18392310`  
		Last Modified: Tue, 14 Oct 2025 20:56:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2372e539ae66eed8bcff6c272270633b7c72968515eb3458ec15ab94b3870cfd`  
		Last Modified: Tue, 14 Oct 2025 20:56:22 GMT  
		Size: 58.7 MB (58721895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef79130f817a6156acf2f337b6ebf8a7dc77ece94732988e956f2a6d85f9bf5f`  
		Last Modified: Tue, 14 Oct 2025 20:56:17 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6c4e953a954edcfd2714fc3ff002a80ab00853fd84646bdbf66cb28577233b`  
		Last Modified: Tue, 14 Oct 2025 21:17:18 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88588a9cfea3c5df81c990a156b1eb66546e66cf3126f15395dcd6a1e6e5b369`  
		Last Modified: Tue, 14 Oct 2025 21:17:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eed4ca36c57c3151803e8db32189739d296d998d74fbfcc07e714a602b2c9e4`  
		Last Modified: Tue, 14 Oct 2025 21:17:18 GMT  
		Size: 8.6 MB (8588045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee54cd92f3702fffa30b834961bcd054453c532340dd015972537a768ce2a0d3`  
		Last Modified: Tue, 14 Oct 2025 21:17:17 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
