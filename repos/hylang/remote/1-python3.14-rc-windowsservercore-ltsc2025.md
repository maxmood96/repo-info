## `hylang:1-python3.14-rc-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:f97238f0355f895fc8e1fac6094ec515eadfb80aa009c0c655b9b1d84484b0f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `hylang:1-python3.14-rc-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull hylang@sha256:c53f02cbbb9e5721aff8f2777c3851068b1b47a15757fcda30f1c7bd86df4f43
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3503268865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bbcf259c08c9fa6f34e5c2444b74c5960c7153a4ef8a52def66c8853d31ebe`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Wed, 14 May 2025 21:06:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:06:31 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 14 May 2025 21:06:33 GMT
ENV PYTHON_VERSION=3.14.0b1
# Wed, 14 May 2025 21:06:35 GMT
ENV PYTHON_SHA256=a878026c12b1a606d02f5bbf3ed65aa780ee8272964b8f95d8348ffa2d6ca096
# Wed, 14 May 2025 21:07:21 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Reinstalling pip to workaround a bug ...'; 	Remove-Item -Recurse C:\Python\Lib\site-packages\pip*; 	python -m ensurepip --default-pip -vvv; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 14 May 2025 21:07:24 GMT
CMD ["python"]
# Wed, 14 May 2025 22:13:03 GMT
ENV HY_VERSION=1.1.0
# Wed, 14 May 2025 22:13:04 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 14 May 2025 22:13:36 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 14 May 2025 22:13:36 GMT
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
	-	`sha256:4326fbfdaedf2ee482b8bd16fcfb5ee9ad4457108f68165a4a38b5942ab39639`  
		Last Modified: Wed, 14 May 2025 21:07:28 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3485313d0c62aaf09d3f0536e468e75096199f8de4958b59f699528016b598`  
		Last Modified: Wed, 14 May 2025 21:07:27 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c31c2a9d94028719a7b2a0d4db2d5ee38f2a6057541e80efd560a977eafe786`  
		Last Modified: Wed, 14 May 2025 21:07:27 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6861250362a010c9bcba849490ade14b2f966842fb6cd4eda81d673fd2ad1d2`  
		Last Modified: Wed, 14 May 2025 21:07:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb7508c86e97bd836dd030ab63993a79552c94f3bbfc72bf0724b1c0d5d49ab`  
		Last Modified: Wed, 14 May 2025 21:07:34 GMT  
		Size: 63.9 MB (63891967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26358008559c88011d35d23e1d9029eb3a5900e8501f79bbfeedf37847a0e881`  
		Last Modified: Wed, 14 May 2025 21:07:27 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba9355c60cf421ba27c478def5b6428a0ab4ea1a0438179add4e57959bc8f68`  
		Last Modified: Wed, 14 May 2025 22:13:41 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbafd659f3710bb7bd3fc1eb43457b4cc8264dae1dda590a17a71b630025e381`  
		Last Modified: Wed, 14 May 2025 22:13:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b64fcadf725ecabd2920e2ff404421d47421579a57773299093798ba4a98bb1`  
		Last Modified: Wed, 14 May 2025 22:13:42 GMT  
		Size: 8.6 MB (8600686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0ad2626977968832e70fd78c96e0980762415e1d04861cb8580f02cbeccacc`  
		Last Modified: Wed, 14 May 2025 22:13:41 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
