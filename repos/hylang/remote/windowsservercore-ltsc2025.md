## `hylang:windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:00edb9b87820cc62e9c3ae50caa912c0aeccddffbcb6bf7f8b6245084e8f6613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `hylang:windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull hylang@sha256:9f4ab736e26051463c6f3d14c9f42db08c9d2fa1ac6d85722b55e38756307755
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3498679794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c1f0dcc2d9c12e91f593ec3e2fdee9e29db8b6c921d58bcddb8c46c3588140`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Wed, 14 May 2025 21:06:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:06:20 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 14 May 2025 21:06:21 GMT
ENV PYTHON_VERSION=3.13.3
# Wed, 14 May 2025 21:06:23 GMT
ENV PYTHON_SHA256=698f2df46e1a3dd92f393458eea77bd94ef5ff21f0d5bf5cf676f3d28a9b4b6c
# Wed, 14 May 2025 21:07:04 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 14 May 2025 21:07:05 GMT
CMD ["python"]
# Mon, 02 Jun 2025 17:51:59 GMT
ENV HY_VERSION=1.1.0
# Mon, 02 Jun 2025 17:52:00 GMT
ENV HYRULE_VERSION=1.0.0
# Mon, 02 Jun 2025 17:52:35 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Mon, 02 Jun 2025 17:52:36 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a4ef4e4d73b05caaab2082fc7018c027c9310244e7b4a9b225e8d68bdc39e1`  
		Last Modified: Thu, 15 May 2025 19:51:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c665c60b3d4322eb53659c3425143cfcc5327efd398f000aa97577a98f81fe`  
		Last Modified: Thu, 15 May 2025 19:51:53 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3cc0e87e6f3775ae384ac3922c46e38555659a1bf81206a41379346f68fb51`  
		Last Modified: Thu, 15 May 2025 19:51:53 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e6010113211087603b63b1266b003f6001cc3da065eda28db19b925df8405a`  
		Last Modified: Thu, 15 May 2025 19:23:47 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc06783e62966c39df2f8e290d1bb8bae99aa0dccc256d9e3b5ceae2aee2f21`  
		Last Modified: Thu, 15 May 2025 20:08:08 GMT  
		Size: 59.3 MB (59310029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fa4a1bf2a41a3a14f8c960d2c97a264067f61613ef37d42954cd46e21e44f6`  
		Last Modified: Thu, 15 May 2025 19:23:47 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97622119da67a047bcce4cffd738e1de70066c508c93009717b2a29d7230584f`  
		Last Modified: Mon, 02 Jun 2025 17:52:41 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdd15ef5f41f36a237f7240159c76da10bd564040b84780f45f8445ca5935d8`  
		Last Modified: Mon, 02 Jun 2025 17:52:41 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd754958e377027735e075e5c9fd4122542c438ccaabb1d00141ae548b340df`  
		Last Modified: Mon, 02 Jun 2025 17:52:43 GMT  
		Size: 8.6 MB (8593480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fc29664eb979c944c07a778ef5882a1e5f77a9a34a2a186defb7bc0ff6aea6`  
		Last Modified: Mon, 02 Jun 2025 17:52:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
