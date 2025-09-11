## `hylang:1-python3.13-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:eef73362af6ae75333d68cc3f04dde5389afbb1533fee61fcdea99f044d76223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `hylang:1-python3.13-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull hylang@sha256:e1e4a9136f6021c6248ea7e5dd6cfee7b69c2d2870a04b4a290085ae04847c09
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638743659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e586a5be6f382b7601c72eb42ba6ac93268c30002602233fda5b4d281c40cc`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 10 Sep 2025 21:48:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 22:01:47 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 10 Sep 2025 22:01:47 GMT
ENV PYTHON_VERSION=3.13.7
# Wed, 10 Sep 2025 22:01:47 GMT
ENV PYTHON_SHA256=b12e2e82461ac8e51fc43289050bc8eb937a32d84ce4d242e2c88258c37cf2bb
# Wed, 10 Sep 2025 22:02:22 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 22:02:23 GMT
CMD ["python"]
# Wed, 10 Sep 2025 22:21:04 GMT
ENV HY_VERSION=1.1.0
# Wed, 10 Sep 2025 22:21:04 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 10 Sep 2025 22:23:09 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 10 Sep 2025 22:23:10 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae601f0777b06a06d8faad18910ce906d57fb27de067d609e4022dde683f85b1`  
		Last Modified: Wed, 10 Sep 2025 21:57:05 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27a63b304f122634b138bd05ea32c94231bf67feccbc47896d9e45bd676c584`  
		Last Modified: Wed, 10 Sep 2025 22:02:47 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577c2ced753530bd27432e9732926c80702002791a6f808039f6d98f8140e929`  
		Last Modified: Wed, 10 Sep 2025 22:02:47 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a4192c173e760421e3067f73adc3ea8de1fd3ee425b3a6c15f6c0c2392d23b`  
		Last Modified: Wed, 10 Sep 2025 22:02:47 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1d1de0838768c5b871bc9b21a0c2ed9aed316d4ffe67c275e0deab0571fded`  
		Last Modified: Wed, 10 Sep 2025 22:02:52 GMT  
		Size: 58.7 MB (58722415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbee9de201183cccbc6218387f05083a69cf83dbd44ef62c41127c641370f0d`  
		Last Modified: Wed, 10 Sep 2025 22:02:48 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5990b7de0392f7a73ef5d19466d984c5c315ad66fd6a2e5e7faa8774355484`  
		Last Modified: Wed, 10 Sep 2025 22:23:34 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b471f49b8fd5795f565fa9231c8b8c3b8905cb0b40eff781b5614e82167d9be`  
		Last Modified: Wed, 10 Sep 2025 22:23:34 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae658fc0e09424bf8e64ca0b29e89f384d92a8fa7d9b483f4cadeb4bb6ebd9f`  
		Last Modified: Wed, 10 Sep 2025 22:23:34 GMT  
		Size: 8.6 MB (8570980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc366fe9eff782a1fdcb3cd132eec015a03ed082734b317557c8d5aae3018ed7`  
		Last Modified: Wed, 10 Sep 2025 22:23:34 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
