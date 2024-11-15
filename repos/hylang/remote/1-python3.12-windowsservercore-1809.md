## `hylang:1-python3.12-windowsservercore-1809`

```console
$ docker pull hylang@sha256:22ed641b40a628a39edd1082abe7da99966ef87a9ca59f8f727d8714b18c2020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `hylang:1-python3.12-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull hylang@sha256:74649db9618d5969deab26af0e47a39a8188da61afda8667eb0d7d24328bcf66
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076214183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607f4f1edde526c067b31301b0303405a807715b59ec86be4d7d2245820542bc`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:19:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:19:22 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 14 Nov 2024 20:19:23 GMT
ENV PYTHON_VERSION=3.12.7
# Thu, 14 Nov 2024 20:19:23 GMT
ENV PYTHON_SHA256=1206721601a62c925d4e4a0dcfc371e88f2ddbe8c0c07962ebb2be9b5bde4570
# Thu, 14 Nov 2024 20:21:05 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:21:06 GMT
CMD ["python"]
# Thu, 14 Nov 2024 21:21:55 GMT
ENV HY_VERSION=1.0.0
# Thu, 14 Nov 2024 21:21:57 GMT
ENV HYRULE_VERSION=0.7.0
# Thu, 14 Nov 2024 21:23:22 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 14 Nov 2024 21:23:23 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f57c6b8857127fb0a81aa3d37e3349d112d9a6a517734fcb303a2b82b7828e`  
		Last Modified: Thu, 14 Nov 2024 20:21:10 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ade2f63adeafa487862b5dd740a7b0ab78cd68d8597c4b475dd10756f9f890`  
		Last Modified: Thu, 14 Nov 2024 20:21:09 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edea0c4bcc8da59dfa3f1ca5a3dce6538509dd728771a10525caaa6d1e656e0`  
		Last Modified: Thu, 14 Nov 2024 20:21:09 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983073e5013af0f2ee351d083006453d2c93f7774c701a8e4fa7b665571b1573`  
		Last Modified: Thu, 14 Nov 2024 20:21:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da66ea5021b948223efe2a1d076ce7d8b71d47924d8e45d2886c81f0585486ad`  
		Last Modified: Thu, 14 Nov 2024 20:21:13 GMT  
		Size: 58.4 MB (58412604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5becb9724dbbe3dd12e0efbb51b2f7ec74880ad32531395585db6c03cec53622`  
		Last Modified: Thu, 14 Nov 2024 20:21:09 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9482bcab40eb92b4195b243d36f9029f6727a899804c32426e2b8b4b6aa2491f`  
		Last Modified: Thu, 14 Nov 2024 21:23:26 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b85eb396747ca0f0beaa7336e79156c57e51d67785ac31cea155df7fa0edbf0`  
		Last Modified: Thu, 14 Nov 2024 21:23:26 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3e133cde516070f885c5ec7a146c79ba856a6ff330df836bdd40c6b9395764`  
		Last Modified: Thu, 14 Nov 2024 21:23:26 GMT  
		Size: 7.1 MB (7137409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c2edad7cd5a1303447d1bd1e2c9f5a9aefc4f4605f38a89e2187ba4a9a400e`  
		Last Modified: Thu, 14 Nov 2024 21:23:26 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
