## `hylang:1-python3.15-rc-windowsservercore`

```console
$ docker pull hylang@sha256:6c6f674bbccb95fc2ac5fbe0768076079bd15ddf3da99a495b0734ed19ce1ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `hylang:1-python3.15-rc-windowsservercore` - windows version 10.0.26100.32995; amd64

```console
$ docker pull hylang@sha256:4e7e96f9d90924cf56a13b6fa33c8460730ee9bdfa63c95e5a3f4474f1224254
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2361865368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa957da1fa661f8ccb91c03655db9fe8865e26182adc1c16d0f0471373fd916`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:14:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:25:29 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 09 Jun 2026 22:25:30 GMT
ENV PYTHON_VERSION=3.15.0b2
# Tue, 09 Jun 2026 22:25:30 GMT
ENV PYTHON_SHA256=f73038ee13ab1b131e6b2082a0f5c94e2a6d0aa834c452f2e1cefb90eba92c89
# Tue, 09 Jun 2026 22:26:11 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:26:12 GMT
CMD ["python"]
# Tue, 09 Jun 2026 23:22:14 GMT
ENV HY_VERSION=1.3.0
# Tue, 09 Jun 2026 23:22:14 GMT
ENV HYRULE_VERSION=1.1.0
# Tue, 09 Jun 2026 23:22:52 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 09 Jun 2026 23:22:52 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c11a95d907d89d9848b4e0efb1122a71214bbae8a6ab0810c003f9b999d29c42`  
		Last Modified: Tue, 09 Jun 2026 22:15:31 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebb22ac3f5eaa33d99025ed7a36981b44a4564ff7db18f69571170c2f5e52f3`  
		Last Modified: Tue, 09 Jun 2026 22:26:16 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc45e61bf51af1bca60e0bb8c97c3ccd351ac1d2d5d477ffef1d6b23a7d34c1e`  
		Last Modified: Tue, 09 Jun 2026 22:26:16 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60e98cf7bc9bc1b9b199ade5be210d49c4dab9474aaf5033541b727bf81de44`  
		Last Modified: Tue, 09 Jun 2026 22:26:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955bcf0cc73934f19640d12b043eb1913a54d8a310852971531ae22b4e7457b9`  
		Last Modified: Tue, 09 Jun 2026 22:26:22 GMT  
		Size: 74.4 MB (74380953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd431aad73e7fbad0ec9ba2fb9f0a3f25784d4114f16b372b7e7dcc96d6b7fb2`  
		Last Modified: Tue, 09 Jun 2026 22:26:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72a0c6230441e2d43d367570555ce321035ab55b8773a469587dceda35f177d`  
		Last Modified: Tue, 09 Jun 2026 23:22:57 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d060d711b1b6b8d2d41efae7668ce50a94f2d1a9f8f1cb9ff4d0c485dd4819`  
		Last Modified: Tue, 09 Jun 2026 23:22:57 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f1ab53724b9faf33ad241cab95d66877d6ad5133458da3fc26eefb865aed0f`  
		Last Modified: Tue, 09 Jun 2026 23:22:58 GMT  
		Size: 8.3 MB (8331074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c5c6dc6b232882ec4ea53f44a0def7c849e5c2bab5e934ec2c1a32a4004824`  
		Last Modified: Tue, 09 Jun 2026 23:22:56 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-python3.15-rc-windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull hylang@sha256:8b77756ed7339058bd8a01f958602a58aa29f7e406448613f650307ae872865a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2214735987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e49525f9747224745e618f64f3776be3fee3620dd4d70bb21c1eca091bafa77`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:24:45 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 09 Jun 2026 22:24:46 GMT
ENV PYTHON_VERSION=3.15.0b2
# Tue, 09 Jun 2026 22:24:47 GMT
ENV PYTHON_SHA256=f73038ee13ab1b131e6b2082a0f5c94e2a6d0aa834c452f2e1cefb90eba92c89
# Tue, 09 Jun 2026 22:25:26 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:25:27 GMT
CMD ["python"]
# Tue, 09 Jun 2026 23:26:14 GMT
ENV HY_VERSION=1.3.0
# Tue, 09 Jun 2026 23:26:15 GMT
ENV HYRULE_VERSION=1.1.0
# Tue, 09 Jun 2026 23:27:00 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 09 Jun 2026 23:27:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bb4ff167c8070b9788f2d6d9cd77fafe5a57c62ff4b6c47a449148c900d33c`  
		Last Modified: Tue, 09 Jun 2026 22:13:18 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03b2af339564a62af8249fc8ffa74eb884e4307b9332ecb243ea8fbd6c6a255`  
		Last Modified: Tue, 09 Jun 2026 22:25:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9eca345f7ebbd6eb22b2873fba5edd916581a84584eb1bb7a9015fb262e6a47`  
		Last Modified: Tue, 09 Jun 2026 22:25:32 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59cf9a9f8e4f686a55f9e7e385767e2c345733977181e1a2751a64a2eaa49b2`  
		Last Modified: Tue, 09 Jun 2026 22:25:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54c58a6f68e116ed08afb14f08c8b71ea4789fedf6ab92465077716f0680421`  
		Last Modified: Tue, 09 Jun 2026 22:25:38 GMT  
		Size: 74.4 MB (74392414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2688c62676e3eaa13f137d61c14e47cfc8e0809780d757ba269c2d5313d2955`  
		Last Modified: Tue, 09 Jun 2026 22:25:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af582c75c4acf707dd5e6f6525c86f541e729aeffd99e45ee0870ced671b59c`  
		Last Modified: Tue, 09 Jun 2026 23:27:05 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3142cdc981d40e662a6bf241a6e2db442db379602ecc622968c26042369e33e`  
		Last Modified: Tue, 09 Jun 2026 23:27:05 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aca759d9abce1b13e567a28dec0fab91fe523178f345bcdafcccec2fda26f86`  
		Last Modified: Tue, 09 Jun 2026 23:27:06 GMT  
		Size: 8.2 MB (8207538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0fd4aaedeaa8444cc89252bec74bed3eed213a4c539d7d6d616425ced8ebe2`  
		Last Modified: Tue, 09 Jun 2026 23:27:05 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
