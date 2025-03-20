## `hylang:1-python3.13-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:4c204eaae45798bf2e98fc95f6bbe0943ddab7f9bd27834a439d181bb0e72bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `hylang:1-python3.13-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull hylang@sha256:cdc24631e1cf34a9c272b8415255e832d967c1b013e9f882982965ff52313071
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2337547811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4fbd21f1e7fbe6a9738947312b00136380c0b526ffd261eb611d74bb1e4e76`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 19:05:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 19:05:36 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 12 Mar 2025 19:05:37 GMT
ENV PYTHON_VERSION=3.13.2
# Wed, 12 Mar 2025 19:05:38 GMT
ENV PYTHON_SHA256=9aaa1075d0bd3e8abd0623d2d05de692ff00780579e1b232f259028bac19bb51
# Wed, 12 Mar 2025 19:06:29 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:06:30 GMT
CMD ["python"]
# Wed, 19 Mar 2025 23:12:08 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 23:12:09 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 23:12:48 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 19 Mar 2025 23:12:49 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d117d2b306c4a9efdb192b47ef35e094ff26524560ebe6f1c4667dc24b6b278`  
		Last Modified: Wed, 12 Mar 2025 19:06:33 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408c0dbfe38dcc275928577ba52d0522b23c588a52f2ae02bfe2914f3737f39d`  
		Last Modified: Wed, 12 Mar 2025 19:06:32 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c105133d2d861d6b62ea70a342d2eca0334a3ce26112ba2429da2c4eb9444e9`  
		Last Modified: Wed, 12 Mar 2025 19:06:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9b6bdc718a5d7c67dc2bb33d7f33f0362571e96b00e5cd2ca7f193e55a3662`  
		Last Modified: Wed, 12 Mar 2025 19:06:32 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc95cf06368369047c38e863ce6592935e4414f77332c3afdb3eb5b804dd2b7`  
		Last Modified: Wed, 12 Mar 2025 19:06:37 GMT  
		Size: 59.1 MB (59082607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eda5f8cbc2aaa97fada4d17ebba41695d121212cc7ab220cceabc5fcb9cc9a8`  
		Last Modified: Wed, 12 Mar 2025 19:06:32 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a60379f2ea62870363b56a3ff176311ed71e96748dbc2b4ed6e208add8e960`  
		Last Modified: Wed, 19 Mar 2025 23:12:52 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673a8f6fd664cff3c18c11d3c1fda08dbdee1ad66e3574d39cc8184ee0f95e74`  
		Last Modified: Wed, 19 Mar 2025 23:12:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c0dd5fe81f1dfacefd59bdf659a1a857dec0e08a96a4e1814e68b0706d7fec`  
		Last Modified: Wed, 19 Mar 2025 23:12:53 GMT  
		Size: 8.5 MB (8513670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f72c3884d603a8a01c9a3483d0acc8788d4a771f36b086838d45c407016e05`  
		Last Modified: Wed, 19 Mar 2025 23:12:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
