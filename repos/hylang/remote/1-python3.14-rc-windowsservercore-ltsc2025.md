## `hylang:1-python3.14-rc-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:99fc85e86bdc2d2b0d0fa59d8c7f7886d5ce5bd789236a81634852f0df767baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `hylang:1-python3.14-rc-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull hylang@sha256:009bb7132a413814a06c370551e371087ab5f5dc3d48711a37374d886b207ea6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3640903825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a8db5d077b503b8a37b63b295d5404e3f0385ee15721a6a43c655429740cba`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Thu, 18 Sep 2025 20:18:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 18 Sep 2025 20:18:08 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 18 Sep 2025 20:18:09 GMT
ENV PYTHON_VERSION=3.14.0rc3
# Thu, 18 Sep 2025 20:18:10 GMT
ENV PYTHON_SHA256=638ac495e0e43ccbb76f6116f78cb7b27f55ee8461ffcb4d9e7ee0f7b996a144
# Thu, 18 Sep 2025 20:20:27 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 18 Sep 2025 20:20:28 GMT
CMD ["python"]
# Thu, 18 Sep 2025 21:12:36 GMT
ENV HY_VERSION=1.1.0
# Thu, 18 Sep 2025 21:12:38 GMT
ENV HYRULE_VERSION=1.0.0
# Thu, 18 Sep 2025 21:14:00 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 18 Sep 2025 21:14:00 GMT
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
	-	`sha256:b84de76bd2afd730cc609e321ebccacb0ab04350ccf75990a849af441aefd9c5`  
		Last Modified: Thu, 18 Sep 2025 20:40:04 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3ee2a38db3ffb1b9c0e95f21c09ae01cc454cab35519986eeb4772b1e8532a`  
		Last Modified: Thu, 18 Sep 2025 20:40:04 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e50a2aecf9875a8906625ecc47648e2747a4f92eb563cf1bba7591c4ce2ece3`  
		Last Modified: Thu, 18 Sep 2025 20:40:04 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb88d0699704d098efebf0faef98d73ad0da44d321655dd78e4c5a6fa744d8a0`  
		Last Modified: Thu, 18 Sep 2025 20:40:04 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106634174b1ebdae8b2a9dcd992d15d41e2e63f4ae06b0564f214011656ac9a6`  
		Last Modified: Thu, 18 Sep 2025 20:40:24 GMT  
		Size: 60.9 MB (60853295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2826fed298ac28dab05e2e83f52c14fa9d65e9719127ee653cfc72db877aa182`  
		Last Modified: Thu, 18 Sep 2025 20:40:04 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15215e7e58809b7c669f29f397957c8acb9f916f19f85cadb51a56359131eecf`  
		Last Modified: Thu, 18 Sep 2025 21:14:13 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6029c192846b86e8ba932070b1f2b52b7c8cafd07e3f1924304780127d6b352`  
		Last Modified: Thu, 18 Sep 2025 21:14:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01df1cb22671b2afaae6d91c4fa493640054d9d1c8712cd9043947dc8659cb0`  
		Last Modified: Thu, 18 Sep 2025 21:14:15 GMT  
		Size: 8.6 MB (8600373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21b072ac1b6a562b78e307c83a3ebfb78127de68a08cf60f6ae55394e889179`  
		Last Modified: Thu, 18 Sep 2025 21:14:13 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
