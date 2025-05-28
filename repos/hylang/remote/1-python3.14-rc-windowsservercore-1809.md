## `hylang:1-python3.14-rc-windowsservercore-1809`

```console
$ docker pull hylang@sha256:3415a35994246661cccfa0759750373192f775efedc81834b18c211c26c2cdb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `hylang:1-python3.14-rc-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull hylang@sha256:6d13ea8eeeede5c41dbc617acb75008205cd07552f1550e7b564e1a134f049f4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2250560920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af56ae0dd5830fd047ea44f7f0f0273d47cb133f9df1e4ad9a62947226cae18`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Tue, 27 May 2025 19:09:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 19:09:44 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 27 May 2025 19:09:45 GMT
ENV PYTHON_VERSION=3.14.0b2
# Tue, 27 May 2025 19:09:46 GMT
ENV PYTHON_SHA256=279b1d0e2b1b6cece6f03e49218aacccfd10367e07b785edeb1d4135507434c1
# Tue, 27 May 2025 19:11:17 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 27 May 2025 19:11:18 GMT
CMD ["python"]
# Tue, 27 May 2025 20:12:01 GMT
ENV HY_VERSION=1.1.0
# Tue, 27 May 2025 20:12:02 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 27 May 2025 20:12:43 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 27 May 2025 20:12:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123717025a2861f93b2fdc09a61aadc82f45cec753e437286c98254cd170d3e6`  
		Last Modified: Tue, 27 May 2025 19:11:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ac9608920ce6c7af0025a05dba2264e8557e3a6769d92a6f3e15549915c2b9`  
		Last Modified: Tue, 27 May 2025 19:11:21 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2854583134be0e01193a61e90d869dde85a307ab4a16c165e783bbfe93fea517`  
		Last Modified: Tue, 27 May 2025 19:11:21 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc35f0372b67835b7f2c53c997dd1028770163f0cb152c67965301ee27a1ce4`  
		Last Modified: Tue, 27 May 2025 19:11:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d75229b4aa79bd66d604eae02f42d6da4de2395ee6b3cff7f600b08fb600815`  
		Last Modified: Tue, 27 May 2025 19:11:26 GMT  
		Size: 59.7 MB (59675215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1da02780c4ebaf9ff290be77db7d9a262ea604d2c082b27d7c830a5967e034`  
		Last Modified: Tue, 27 May 2025 19:11:21 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9625c8cee3fcf67e2e5e4f247fb08c00ace5be18d227930fb795990e4c1f76f5`  
		Last Modified: Tue, 27 May 2025 20:12:48 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76898a7eeea8e6df9bc96acc3c53c4016dae4840e3fd2fdf3452b79c1292c3f3`  
		Last Modified: Tue, 27 May 2025 20:12:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b779ce52c2d96cb61dd2089be52552b0d8c5fc06234cad5ebd962a88ac347cd`  
		Last Modified: Tue, 27 May 2025 20:12:49 GMT  
		Size: 7.2 MB (7157866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2cc55fc35ed9ddf7352f87b9a8a37b39a48f8f09d8b5a189d5c0dca1051a3d`  
		Last Modified: Tue, 27 May 2025 20:12:48 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
