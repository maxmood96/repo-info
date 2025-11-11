## `hylang:1-python3.14-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:2608549de382d34cdc0c099c7c00e32c35118647b72b5b1410c9c82c8239e34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `hylang:1-python3.14-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull hylang@sha256:7aa32727e9e7a2da3182dfbcce7c9d2d6fe496dfba76016554f422b143e4149b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1839341522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07c9a9fd52d0452220f50a6349b0fe6b14e8f8a1e9f8a063de046db14658295`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:29:16 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 11 Nov 2025 19:29:17 GMT
ENV PYTHON_VERSION=3.14.0
# Tue, 11 Nov 2025 19:29:17 GMT
ENV PYTHON_SHA256=52ceb249f65009d936e6504f97cce42870c11358cb6e48825e893f54e11620aa
# Tue, 11 Nov 2025 19:29:58 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:29:59 GMT
CMD ["python"]
# Tue, 11 Nov 2025 20:17:34 GMT
ENV HY_VERSION=1.1.0
# Tue, 11 Nov 2025 20:17:34 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 11 Nov 2025 20:18:05 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 11 Nov 2025 20:18:05 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c47b7190b9ffc37d6229c244251af53d022884b4b7dab60e0c54d9354c4adc5`  
		Last Modified: Tue, 11 Nov 2025 19:18:52 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418bbdf766763bf02cd3dee58d3a6fc0159716525580f2c308cb278ee448e10b`  
		Last Modified: Tue, 11 Nov 2025 19:30:17 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1848a7309b90d8a9ccbe5193fd9a77bb3d0fb68a31905530f9c9137c7ecf33a7`  
		Last Modified: Tue, 11 Nov 2025 19:30:17 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3979c420f3c2129c3114593b1af9690d977830f6fda7ba407040103dc96d74`  
		Last Modified: Tue, 11 Nov 2025 19:30:17 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d228f7f5fdfc142ea4d0800ca21b14d89d4712e187bb1d6bdf833abc5eb630`  
		Last Modified: Tue, 11 Nov 2025 19:30:24 GMT  
		Size: 60.9 MB (60853956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706456b291493cedef846bdac9237a021e4ab410c6d8cf47c1036728d6629ce`  
		Last Modified: Tue, 11 Nov 2025 19:30:17 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6dbb5f29208ad33415dcbf5dbacdfeb0e652603ec2d5c74436c744f2c996a4`  
		Last Modified: Tue, 11 Nov 2025 20:18:20 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8faae9c14f7cb917dedf61b5e58caa3318cfe82d9b553f5717c2f3acb46cc5`  
		Last Modified: Tue, 11 Nov 2025 20:18:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6eb9b02aa7b7d00259ecd946bf5abc00fcf647a6fa1cc9b5c8454026da9449c`  
		Last Modified: Tue, 11 Nov 2025 20:18:21 GMT  
		Size: 8.5 MB (8515555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a1ecc94e513a06e2ec78f6af43f26a1c4e95be5940fb43db3b595986d268ab`  
		Last Modified: Tue, 11 Nov 2025 20:18:20 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
