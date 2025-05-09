## `hylang:1-python3.14-rc-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:6e9f0f22edc6324a201f610c72e94d41fec3d01a2f66ade8e3548f5590441f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `hylang:1-python3.14-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull hylang@sha256:b216552a5c6520426e3a883b372e7e3f5c8bb68d8373adb9abc2c5d8145366be
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345942996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943a41a1b0399afd6f63c9868a98b1c5b0dfc95004c2abaf3bb566d528b9ef65`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Thu, 08 May 2025 21:01:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 08 May 2025 21:01:49 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 08 May 2025 21:01:50 GMT
ENV PYTHON_VERSION=3.14.0b1
# Thu, 08 May 2025 21:01:50 GMT
ENV PYTHON_SHA256=a878026c12b1a606d02f5bbf3ed65aa780ee8272964b8f95d8348ffa2d6ca096
# Thu, 08 May 2025 21:04:24 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Reinstalling pip to workaround a bug ...'; 	Remove-Item -Recurse C:\Python\Lib\site-packages\pip*; 	python -m ensurepip --default-pip -vvv; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 08 May 2025 21:04:25 GMT
CMD ["python"]
# Fri, 09 May 2025 17:30:52 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 17:30:52 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 17:31:55 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 09 May 2025 17:31:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77ac229fd430772d28ff8bd422201baf2162fa3bd6d5a753b0bf14b3819ff75`  
		Last Modified: Thu, 08 May 2025 21:04:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f62bd2f04e256071c04669da32543921691cc128bd5396fb6bfa31eb0a15759`  
		Last Modified: Thu, 08 May 2025 21:04:27 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33c3a5c7a3bfb6a62ae1c787525d99969ddb03e01b8e384c4ff236b7605e5dc`  
		Last Modified: Thu, 08 May 2025 21:04:27 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f187d6387794e3a368eac5c5531b616310b56495a8c378a929bd56816c50deb`  
		Last Modified: Thu, 08 May 2025 21:04:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65ad62684f17a178594e1d092fb46615753253ae4cc7be0d644ed1123cd0a41`  
		Last Modified: Thu, 08 May 2025 21:04:32 GMT  
		Size: 63.8 MB (63832221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a6652b296e686e517dd0b32bd29ac0eb1a1d030095f7cfca4c9c0d8eceb881`  
		Last Modified: Thu, 08 May 2025 21:04:27 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83927c534a25d76f93f73cd13a5ae221ac5d22864de564cda6671a169fb9ea74`  
		Last Modified: Fri, 09 May 2025 17:31:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a65882d9924950cc5bd5e93e22d812e0dd544fbf6216eae9bf93ffa5567993`  
		Last Modified: Fri, 09 May 2025 17:31:59 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade6d07000471c491dad045a779d63a6c34394f9fa49bb5ebd2bff940f135884`  
		Last Modified: Fri, 09 May 2025 17:32:01 GMT  
		Size: 8.5 MB (8517962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9321c8d7b4cfcf564bd81f2fbf76bd8f4d87b6c1428aafaf7accdc77c35741c9`  
		Last Modified: Fri, 09 May 2025 17:31:59 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
