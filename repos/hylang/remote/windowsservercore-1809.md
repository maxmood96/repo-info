## `hylang:windowsservercore-1809`

```console
$ docker pull hylang@sha256:f8e2dcc6279af838ed0161e9660e5d4a160c0fb50f5785e2554cc90ccf505a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `hylang:windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull hylang@sha256:15064744d6977dbe1798ad45b9d00befa78194e40d7a6e9643c5ae0172cf6ee4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1966510517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35b6f0d01ee142ae03c93455081a673e295151416809fb408c18f25a36b1908`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Sat, 19 Oct 2024 00:56:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 19 Oct 2024 00:56:57 GMT
ENV PYTHONIOENCODING=UTF-8
# Sat, 19 Oct 2024 00:56:58 GMT
ENV PYTHON_VERSION=3.13.0
# Sat, 19 Oct 2024 00:56:58 GMT
ENV PYTHON_SHA256=78156ad0cf0ec4123bfb5333b40f078596ebf15f2d062a10144863680afbdefc
# Sat, 19 Oct 2024 01:00:31 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Sat, 19 Oct 2024 01:00:32 GMT
CMD ["python"]
# Sat, 19 Oct 2024 02:10:26 GMT
ENV HY_VERSION=1.0.0
# Sat, 19 Oct 2024 02:10:28 GMT
ENV HYRULE_VERSION=0.7.0
# Sat, 19 Oct 2024 02:12:16 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Sat, 19 Oct 2024 02:12:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c385df1fb404367c1a3213a6e895d386632f8e1a1c19943cb063d39d91d633`  
		Last Modified: Sat, 19 Oct 2024 01:00:38 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5069924187efac790623def20497bc254a411ef7c6c7a6a654aeea2904f45119`  
		Last Modified: Sat, 19 Oct 2024 01:00:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22a1b9c1ac79f6981b86132bc02df388abdc75f841937267126af8520510106`  
		Last Modified: Sat, 19 Oct 2024 01:00:36 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa1633593a19dec46edbba9ee3159daf2e3aae822c4536248a13d13d473f977`  
		Last Modified: Sat, 19 Oct 2024 01:00:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc65a6af266e755e874adb1f063d3c59baff656c0cdd3abf8aeee2300ea9c46`  
		Last Modified: Sat, 19 Oct 2024 01:00:41 GMT  
		Size: 57.6 MB (57555561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0d6ea00fdd0e498cfc7af9cc1a6a728a3c02a15a2576e2a43cb33df0be824b`  
		Last Modified: Sat, 19 Oct 2024 01:00:36 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca97d25f0104d1aeabc3da5e1107e10a2572e35a4b05c30a996a323b61fa318f`  
		Last Modified: Sat, 19 Oct 2024 02:12:21 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f9665a7eb08e5da71b27f1299e201229cb14b45ebad4fe21a59953ebcd63fd2`  
		Last Modified: Sat, 19 Oct 2024 02:12:21 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd82b8accb926096ca945aa14480ebea1c067d90754b7fbabb81d2488c50a8c`  
		Last Modified: Sat, 19 Oct 2024 02:12:22 GMT  
		Size: 7.1 MB (7119167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5170a9677dc90359c5de743258980746a50f8a7e435c254462345d72f858e2`  
		Last Modified: Sat, 19 Oct 2024 02:12:21 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
