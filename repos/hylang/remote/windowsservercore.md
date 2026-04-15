## `hylang:windowsservercore`

```console
$ docker pull hylang@sha256:44decd2661e099db9b945256cb41feaa8556dd12ac81b213e8aba6c80e709787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `hylang:windowsservercore` - windows version 10.0.26100.32690; amd64

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

### `hylang:windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull hylang@sha256:7fd1ddaec914c42ec33bc46b7296a938124c369af74c7e35e0ff3873d680fdc5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2139595501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9edca2e29613512d8f6e7021967611f09da13725f7de0a48d46de149459bf21`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:13:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:26:35 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 14 Apr 2026 21:26:35 GMT
ENV PYTHON_VERSION=3.14.4
# Tue, 14 Apr 2026 21:26:35 GMT
ENV PYTHON_SHA256=b571567bd11ea98fd7a2cf85791d2c8557a63b1e04e9d1dae665a275cac87f1b
# Tue, 14 Apr 2026 21:27:26 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:27:27 GMT
CMD ["python"]
# Tue, 14 Apr 2026 22:17:39 GMT
ENV HY_VERSION=1.2.0
# Tue, 14 Apr 2026 22:17:40 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 14 Apr 2026 22:18:08 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 14 Apr 2026 22:18:09 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123169191bc868b3dd631fce589535bd12a560eb17f3da89a78dcc3b427e5096`  
		Last Modified: Tue, 14 Apr 2026 21:14:54 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8415de4db98e61c75f40c69540f1a4ebc8d2baff9a3a13fced3a7969e830550`  
		Last Modified: Tue, 14 Apr 2026 21:27:32 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08439f2319bef6d50fd921cb2640df87872aad696f4c6d6f970bc3cde976e22e`  
		Last Modified: Tue, 14 Apr 2026 21:27:32 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d40e1ef00a05272774744ca9493b77c8ac42bb719453b16bd15c64794f6b0cf`  
		Last Modified: Tue, 14 Apr 2026 21:27:32 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23129191cd06d6d760f143093dac47b1339a486bcca350ac31eba49d7c53026f`  
		Last Modified: Tue, 14 Apr 2026 21:27:38 GMT  
		Size: 61.1 MB (61094345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d6b8bedb5bcf85b12a590540f16bb3f3c22f6a8dcef554ca4e679541719692`  
		Last Modified: Tue, 14 Apr 2026 21:27:32 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a414e17c1e6e16df5eee76886afae281443ba7385f27e9c45199e58f27224b1`  
		Last Modified: Tue, 14 Apr 2026 22:18:13 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9407b689f18e28732b2a2b9dccf852ffbe094ede5fc219a76be4b9a16fe1ae88`  
		Last Modified: Tue, 14 Apr 2026 22:18:13 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9e7d269eceeb7e7fa3c03cdc2b9a6d39b98b70b813af7314da36d2fb0dd24a`  
		Last Modified: Tue, 14 Apr 2026 22:18:14 GMT  
		Size: 8.3 MB (8279317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af832cc968afd2bfd7118f25495154daea6b21e640c300b62fd911d69dd08e4`  
		Last Modified: Tue, 14 Apr 2026 22:18:13 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
