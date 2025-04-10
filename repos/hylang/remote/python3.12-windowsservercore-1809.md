## `hylang:python3.12-windowsservercore-1809`

```console
$ docker pull hylang@sha256:88e0e567cff5788b66500753ad1ccb768e6f679eb6afdea76fd1967ef469ac47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `hylang:python3.12-windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull hylang@sha256:2ecae3329c3fee51491cfe6590519db84553bfa7a4fe8ae861c1144a65496905
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2228671371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce3f0c141119b28dbc3210eae828985371f6d8d1f7fdb7cb7963d8acf3bb460`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 01:02:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 01:02:28 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 09 Apr 2025 01:02:29 GMT
ENV PYTHON_VERSION=3.12.10
# Wed, 09 Apr 2025 01:02:30 GMT
ENV PYTHON_SHA256=67b5635e80ea51072b87941312d00ec8927c4db9ba18938f7ad2d27b328b95fb
# Wed, 09 Apr 2025 01:03:52 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 01:03:53 GMT
CMD ["python"]
# Wed, 09 Apr 2025 02:46:17 GMT
ENV HY_VERSION=1.0.0
# Wed, 09 Apr 2025 02:46:18 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 09 Apr 2025 02:47:02 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 09 Apr 2025 02:47:03 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110e26040701cb49ac340641b349bdeaa54367ec3c93f96d3325280dea48a913`  
		Last Modified: Wed, 09 Apr 2025 01:03:56 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f09cab5642bf91df7fc5ca50e2c5cf725e2a33015ff110b5f54be11201ee47`  
		Last Modified: Wed, 09 Apr 2025 01:03:55 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7ae6073c8cb051c2bee7cbfdbd33ca75664d52a664b38c69ef0b1e4de25a7f`  
		Last Modified: Wed, 09 Apr 2025 01:03:55 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfee6bf26290a4b084c58b15888db08eb86c7df95fb7b456699250ad1bdc5015`  
		Last Modified: Wed, 09 Apr 2025 01:03:55 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c539e642cf0a6941dd38953427e6a0ce6fc770846d2f0e1481a31f567bb4378e`  
		Last Modified: Wed, 09 Apr 2025 01:04:00 GMT  
		Size: 58.7 MB (58747570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0610279dde6d5c6b95d508661ce12994c6cb3af98e3c3b2b6cb07a50af0f04d`  
		Last Modified: Wed, 09 Apr 2025 01:03:55 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a312d3d3ed50edd8e66a4c8b8cc7893897f62ba415bcf367753efad72ba6bec9`  
		Last Modified: Wed, 09 Apr 2025 02:47:07 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0dd6382274faaf7581660d56860313a93e8f812a42112ffe9d943fccc455fd`  
		Last Modified: Wed, 09 Apr 2025 02:47:07 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf48de3e11ac6fae4f303c5b68e6d4e8a593b472e114832da1d0c5808dd15a3c`  
		Last Modified: Wed, 09 Apr 2025 02:47:09 GMT  
		Size: 7.2 MB (7187556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3c97d977072620e80127e59b86438276fd4fb8b448262c6ef0767ec3fb7ce0`  
		Last Modified: Wed, 09 Apr 2025 02:47:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
