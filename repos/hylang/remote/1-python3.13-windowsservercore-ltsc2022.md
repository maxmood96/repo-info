## `hylang:1-python3.13-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:7a364e77dc14c09f1afd52304883570950ba29c90053c9ab0531938557a8f45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `hylang:1-python3.13-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull hylang@sha256:0eb252f8ba6d841de4ba2d92ee245b95e383b5fac7d2a99bc6d03705ea8321ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2321493812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7467e8f4893964bd3c148fe35933f9683e4f476f492c49e51419b45fd23327eb`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:37:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:37:20 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 11 Dec 2024 20:37:21 GMT
ENV PYTHON_VERSION=3.13.1
# Wed, 11 Dec 2024 20:37:22 GMT
ENV PYTHON_SHA256=6b33fa9a439a86f553f9f60e538ccabc857d2f308bc77c477c04a46552ade81f
# Wed, 11 Dec 2024 20:38:02 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:38:03 GMT
CMD ["python"]
# Thu, 09 Jan 2025 22:30:03 GMT
ENV HY_VERSION=1.0.0
# Thu, 09 Jan 2025 22:30:04 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 09 Jan 2025 22:31:28 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 09 Jan 2025 22:31:28 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Fri, 13 Dec 2024 16:30:53 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e95c0093c21afbeda79e4867f4eccad5ff26e13343017442c1a3b850e1a75f`  
		Last Modified: Wed, 11 Dec 2024 20:38:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a4330b2fb7ad670d2513d07dbffc98e84fdc4a7fca889f95c2f1b91e9dff5c`  
		Last Modified: Wed, 11 Dec 2024 20:38:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0db332b21aa3aeb835884622885ad2b90366a9ce509d73e8e951910a669879`  
		Last Modified: Fri, 13 Dec 2024 19:09:43 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f457976f3d563af85195be2d77c112bcd169173f13efeb82e92e3c3b7fb977f`  
		Last Modified: Wed, 11 Dec 2024 20:38:07 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325b7fb11b299a9979156036c7f4c2aa96fb849f1e4e1800c38583f6d89d3e62`  
		Last Modified: Fri, 13 Dec 2024 19:18:43 GMT  
		Size: 59.1 MB (59076500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c08314161d2f2857d274c11b5dba888175e1c7277d562b4905ddfec3bf04db9`  
		Last Modified: Wed, 11 Dec 2024 20:38:07 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7787011676c51af6dc04084f613f9c76671955a69696e70fad6ad6a96f7c5ed6`  
		Last Modified: Thu, 09 Jan 2025 22:31:31 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4836d34eb8b9a783c947d8ad36e0b71827e880eb647b0e3ce72714de9975ed59`  
		Last Modified: Thu, 09 Jan 2025 22:31:31 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96295c5f87e283fa2d526a0a95fc9fc457073a8a17c4f958a70cdd74dc27389c`  
		Last Modified: Thu, 09 Jan 2025 22:31:32 GMT  
		Size: 8.5 MB (8533227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac36ac87091679a8116e693b37aca6037d2dc4eef672e37799831ea3922317c`  
		Last Modified: Thu, 09 Jan 2025 22:31:31 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
