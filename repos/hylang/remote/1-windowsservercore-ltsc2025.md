## `hylang:1-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:086ef0765aeafde0bf803bf61e3d26be8cbed6b25712157feccf3de689d2453a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `hylang:1-windowsservercore-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull hylang@sha256:3e050a056e15cbaf59527f272587f688e7bc7abd277d09da492efeeeeee494c5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199728296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dae39329fa555563b5650a09b632273b55aff3bbcc5456b4ed42814eb2021f2`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:02:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:16:04 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 14 Apr 2026 21:16:05 GMT
ENV PYTHON_VERSION=3.14.4
# Tue, 14 Apr 2026 21:16:06 GMT
ENV PYTHON_SHA256=b571567bd11ea98fd7a2cf85791d2c8557a63b1e04e9d1dae665a275cac87f1b
# Tue, 14 Apr 2026 21:16:49 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:16:50 GMT
CMD ["python"]
# Tue, 14 Apr 2026 22:15:04 GMT
ENV HY_VERSION=1.2.0
# Tue, 14 Apr 2026 22:15:04 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 14 Apr 2026 22:15:47 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 14 Apr 2026 22:15:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285db92ff03740292d2e70ef81a1ebcda5d964ee8082b3dfae77c36c2f844e8e`  
		Last Modified: Tue, 14 Apr 2026 21:03:02 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d73b61104fe53636f42fdda064249b89e5aa9a9c8723cf1450c892f066c6f6e`  
		Last Modified: Tue, 14 Apr 2026 21:16:55 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310b698c0137777ec695fb39dedd7fad1425171d94d65657db8c9b473e8e9506`  
		Last Modified: Tue, 14 Apr 2026 21:16:56 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f39335fa67f9d3298c68d3a6737df2874565cf8291d4d7f7029480383e6eb2`  
		Last Modified: Tue, 14 Apr 2026 21:16:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4a08770f1c1762962f2609cbfe35b2d8098c3a1778d9879a0dc26468c5e8ed`  
		Last Modified: Tue, 14 Apr 2026 21:17:01 GMT  
		Size: 61.3 MB (61267975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8d181863f36f7dfe83219f5602e6dd0917ab9f97781f6e66843c1342064f18`  
		Last Modified: Tue, 14 Apr 2026 21:16:55 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8491e25f537890a0366a61bf48b9b6ed444a5d573f46b70fb8007bda26768986`  
		Last Modified: Tue, 14 Apr 2026 22:15:52 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0907eca094f68730461c96e315f8d11a0572f978e15a1ad492dc51281dcafd7`  
		Last Modified: Tue, 14 Apr 2026 22:15:52 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60f7167d0b4e4d7ad1f352f0fb9d8d3b42b5eede383dc1067b27dea95204521`  
		Last Modified: Tue, 14 Apr 2026 22:15:54 GMT  
		Size: 8.5 MB (8463711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3d723ad538b2b2a27189e362bc3a114c008759aa81fb32fab33f59750bf835`  
		Last Modified: Tue, 14 Apr 2026 22:15:52 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
