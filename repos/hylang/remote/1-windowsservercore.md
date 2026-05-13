## `hylang:1-windowsservercore`

```console
$ docker pull hylang@sha256:8d382ef0d793fab360e13258e872e3d6fdb205fd55712bc92aa8f962822e4072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `hylang:1-windowsservercore` - windows version 10.0.26100.32860; amd64

```console
$ docker pull hylang@sha256:ec9e2ca9de86b08d0f0989284ff70df1b80b4504bde181683a216c099b6ea923
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2275757848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca86a981b8f859f2f155210a2e2b96892a25f8f1e0f31800590df9692b0cc977`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:50:01 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 12 May 2026 23:50:01 GMT
ENV PYTHON_VERSION=3.14.5
# Tue, 12 May 2026 23:50:02 GMT
ENV PYTHON_SHA256=f9c09f5ed6f796fd1a8bc5ddfa41715a494b453c4781f0e35d5077cf9fa58f6d
# Tue, 12 May 2026 23:50:43 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:50:44 GMT
CMD ["python"]
# Wed, 13 May 2026 00:30:26 GMT
ENV HY_VERSION=1.2.0
# Wed, 13 May 2026 00:30:26 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 13 May 2026 00:31:01 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 13 May 2026 00:31:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d188d7f4a5421b58c277ec337ae635de99e29dcb259e15d0521f9f034b9389`  
		Last Modified: Tue, 12 May 2026 23:40:52 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c855b0a869238548e35027126893ffdaca30a464fd624c1620934f52c0959ecd`  
		Last Modified: Tue, 12 May 2026 23:50:49 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92122d749a5d51e526ebf6aada6f98e9e35c40733efb71ccf2a229b20c34bcb3`  
		Last Modified: Tue, 12 May 2026 23:50:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08824b384a0da70df6c9f9f748a7aefe5bdb0b9cbbc2c1618e24036a8c546b95`  
		Last Modified: Tue, 12 May 2026 23:50:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb50e2e31ecbae4894b157e17cb692176f5a3d79a0bf9346ecfb3362426195b`  
		Last Modified: Tue, 12 May 2026 23:50:55 GMT  
		Size: 61.3 MB (61338866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e53701d2b2b04d99f34efdb0a69c516cf8fcfc08f12203223dab1b275ca746`  
		Last Modified: Tue, 12 May 2026 23:50:49 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf130a1877bb1a3c4147291d45f565554b3190e3bf13faedb5c11ecf9c81e278`  
		Last Modified: Wed, 13 May 2026 00:31:06 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38653f026087416b4a6d3d1d190ee0ce1edb9c7920531b90a14485e092c39626`  
		Last Modified: Wed, 13 May 2026 00:31:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418a44ae99c4e751588e14d71e1e50f5f4febfa6e6dbd1745f433d1602e1b554`  
		Last Modified: Wed, 13 May 2026 00:31:08 GMT  
		Size: 8.5 MB (8466561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e77f7b207e0b9400538b6e3788bb0d306e35e3e3f6b37fb5495b41de2a4b604`  
		Last Modified: Wed, 13 May 2026 00:31:06 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull hylang@sha256:201ad6c628aa9c45d05f3751ecba599dd27c711a7fc374bd82fa071b00e6ffb9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2192773386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71c637b60cb64a6ee1d656d19f2ea6eb4330525a5d73361bd27651cf167b3be`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:38:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:58:09 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 12 May 2026 23:58:10 GMT
ENV PYTHON_VERSION=3.14.5
# Tue, 12 May 2026 23:58:11 GMT
ENV PYTHON_SHA256=f9c09f5ed6f796fd1a8bc5ddfa41715a494b453c4781f0e35d5077cf9fa58f6d
# Tue, 12 May 2026 23:58:51 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:58:52 GMT
CMD ["python"]
# Wed, 13 May 2026 00:32:36 GMT
ENV HY_VERSION=1.2.0
# Wed, 13 May 2026 00:32:37 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 13 May 2026 00:33:19 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 13 May 2026 00:33:20 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cbb80a80947ff97fb5674c26478afa4331c7d4b2fefabd1ea650765bffae78`  
		Last Modified: Tue, 12 May 2026 23:40:06 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7f3cfa06a6dfb39cc22416a3fe6eff4b710bfeeccf05db45d77158ff23cf7b`  
		Last Modified: Tue, 12 May 2026 23:58:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91ad01b1d407414ae266c6d5f8d9c0bb0b2689fe371c38a7571438ad85c0e7f`  
		Last Modified: Tue, 12 May 2026 23:58:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74178a30e0303c0c21ed95e5ff390e5b58a1a755bd7d53d4167832a08c74400e`  
		Last Modified: Tue, 12 May 2026 23:58:56 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c55dd5cfe2037fd17b90af958774b3cbfbd7147faa9264d71df2de5ca55808f`  
		Last Modified: Tue, 12 May 2026 23:59:02 GMT  
		Size: 61.7 MB (61678797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114d0893892b1275f89469f1046c4d8eb67d669829d0ed2b72970a4b73e53803`  
		Last Modified: Tue, 12 May 2026 23:58:56 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbcdeabd4f744e030f044762224448d932632381bf09223bb1940b25ea9f4470`  
		Last Modified: Wed, 13 May 2026 00:33:24 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da8a7ab9885aa10e70a867b36ea938f31bad377ef4b3c74ba22ddb587e4adf7`  
		Last Modified: Wed, 13 May 2026 00:33:24 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c8ba8208ca88101952175c9c517e83a038d1a635b3893697f29b0e43b2d5ab`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 8.7 MB (8663447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03dcefda00dca3ff500774d0c842e6276ffb8c19de3a8cb869c405a18d09eb0`  
		Last Modified: Wed, 13 May 2026 00:33:24 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
