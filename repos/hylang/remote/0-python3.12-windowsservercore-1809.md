## `hylang:0-python3.12-windowsservercore-1809`

```console
$ docker pull hylang@sha256:ae0eb7742a9e9c476d0176fcb7a0fe7aa4e054fc56bd0a03c8664f94c9ad039f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `hylang:0-python3.12-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull hylang@sha256:d2c0e82ad5789d9dc598fffa399b99f1259e30ee4d10f0f1942f4b36cf27401a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1785690309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c872e0cb4da807c4437087c09bb52a99bb260b0529f3aa2ff66d5a6d679f63`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 12 Sep 2024 21:08:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Sep 2024 21:08:10 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 12 Sep 2024 21:08:10 GMT
ENV PYTHON_VERSION=3.12.6
# Thu, 12 Sep 2024 21:09:21 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 12 Sep 2024 21:09:22 GMT
CMD ["python"]
# Thu, 12 Sep 2024 22:07:36 GMT
ENV HY_VERSION=0.29.0
# Thu, 12 Sep 2024 22:07:38 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 12 Sep 2024 22:08:13 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 12 Sep 2024 22:08:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a8a3fa39ca74aa60ecd3111a61827b15d11f6220ed097e223019d119e21abc`  
		Last Modified: Thu, 12 Sep 2024 21:09:26 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360d1a51576275a94cd0dfe8a124e3cd0fa110822e7eb01a0afad14a7e7795e4`  
		Last Modified: Thu, 12 Sep 2024 21:09:26 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0679e2bae2b8b434fde6871c386c1140ab11c61007ddbfbdd60e868ce24186`  
		Last Modified: Thu, 12 Sep 2024 21:09:26 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b079c6f85c40bb3e514712ee4ac201db9d1df0ad78beabf1ec21f7f4a9cd6ef`  
		Last Modified: Thu, 12 Sep 2024 21:09:31 GMT  
		Size: 58.2 MB (58248193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d93350a2bf1b16dd17176bf472125c26f00d23e340a37c9d0897e27f5ae196e`  
		Last Modified: Thu, 12 Sep 2024 21:09:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1095c6966cf7c4c9ee135b24cea0836b1dc2c7195be30200380ff96b4cf4b738`  
		Last Modified: Thu, 12 Sep 2024 22:08:18 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8c499df3d9039ab3bdb9d8566bd9a8d85f376a0b43e78ef5f55c80e4dea150`  
		Last Modified: Thu, 12 Sep 2024 22:08:18 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62252e813b2e9f0dc3697b86e9ad5cdedb6e1be6c7823619fe3fce332fa9a8c2`  
		Last Modified: Thu, 12 Sep 2024 22:08:19 GMT  
		Size: 7.2 MB (7164576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1009f03af3cff8a576628a9712fa4849896f0eda4fe6c34220aaa6515ef99179`  
		Last Modified: Thu, 12 Sep 2024 22:08:18 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
