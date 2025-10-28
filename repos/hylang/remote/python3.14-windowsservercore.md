## `hylang:python3.14-windowsservercore`

```console
$ docker pull hylang@sha256:1b4b8fee15c58b116702659f02bd89179fe0a4fecebcbbe73d72fd22e7a5d260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `hylang:python3.14-windowsservercore` - windows version 10.0.26100.6905; amd64

```console
$ docker pull hylang@sha256:096c8d8c5c05b4c27b49090dcb6b5ceb218f6eda5485c0262344228d79ba1cfd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3289736644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb895c784efa8c8520f997397e6841745e9e6925d9e8ff999558ad44adf2f700`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:26:01 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 24 Oct 2025 18:26:02 GMT
ENV PYTHON_VERSION=3.14.0
# Fri, 24 Oct 2025 18:26:02 GMT
ENV PYTHON_SHA256=52ceb249f65009d936e6504f97cce42870c11358cb6e48825e893f54e11620aa
# Fri, 24 Oct 2025 18:26:49 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:26:50 GMT
CMD ["python"]
# Tue, 28 Oct 2025 19:12:23 GMT
ENV HY_VERSION=1.1.0
# Tue, 28 Oct 2025 19:12:24 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 28 Oct 2025 19:13:00 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 28 Oct 2025 19:13:00 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2306afc06fe394817b697769f818a638f384b35e7a7bdcfd10e74c6c7ee210f8`  
		Last Modified: Fri, 24 Oct 2025 18:23:16 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555e21fbe78df3503ea38a395ba413b5f558c015e0dfc07f0103a646eeec3f78`  
		Last Modified: Fri, 24 Oct 2025 18:27:16 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0bf2e24210488dfa0a68f5cf0859a7a3223925b885084b48224d8a44aa6060`  
		Last Modified: Fri, 24 Oct 2025 18:27:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a551edbd83e434e74b91dc02db01c8a5b6fb4f1d679d9bb434de70e9f78cf6`  
		Last Modified: Fri, 24 Oct 2025 18:27:16 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f6eb59176e72aebdf64a7b691c8b363a10f6f49f76cf66567a3fd45414efde`  
		Last Modified: Fri, 24 Oct 2025 18:27:23 GMT  
		Size: 60.8 MB (60788485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42596bb77eccdcbb1040b5350decf6f5b00fb6b12d3839bc54cd0f73259cdd50`  
		Last Modified: Fri, 24 Oct 2025 18:27:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820c33d894e8e881cec56b78fcde635c1c45aac3c45cf8e8cbbfa99f80c6b573`  
		Last Modified: Tue, 28 Oct 2025 19:13:17 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649be611220f2633abd333beee7909f532ec1de20b0188f0b837799229a841be`  
		Last Modified: Tue, 28 Oct 2025 19:13:17 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c608f1fcdcc2587293e61a1cd2741930e006e0df04627ab11be203ffc548a0d`  
		Last Modified: Tue, 28 Oct 2025 19:13:18 GMT  
		Size: 8.6 MB (8590679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2d0f7527d309b568027644ddf9b15685e16e3dd40ee835050ef0792ba6ffdc`  
		Last Modified: Tue, 28 Oct 2025 19:13:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.14-windowsservercore` - windows version 10.0.20348.4297; amd64

```console
$ docker pull hylang@sha256:4df3516057e948195712f9be1cd858d4ec5b5e0c5c070bc8dbb57ccf02025d92
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1646506104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d071078b92d72bc499f354c6124d8db770a2504f429a618c70b6570f0c74059f`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:26:05 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 24 Oct 2025 18:26:06 GMT
ENV PYTHON_VERSION=3.14.0
# Fri, 24 Oct 2025 18:26:07 GMT
ENV PYTHON_SHA256=52ceb249f65009d936e6504f97cce42870c11358cb6e48825e893f54e11620aa
# Fri, 24 Oct 2025 18:26:47 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:26:47 GMT
CMD ["python"]
# Tue, 28 Oct 2025 19:13:19 GMT
ENV HY_VERSION=1.1.0
# Tue, 28 Oct 2025 19:13:21 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 28 Oct 2025 19:14:16 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 28 Oct 2025 19:14:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98378885855372677fffe8ed8a7b41c35f9d46d0075c0e37dc6cc153fdc4a1d`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1924b9997ef2221f01e1003f5aa30dfca54d7fad188168e997a297759b55c646`  
		Last Modified: Fri, 24 Oct 2025 18:27:02 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03565572ba0c1bf21285de38b7bfab35787a4660cd6599206c0fc1bab5aaa163`  
		Last Modified: Fri, 24 Oct 2025 18:27:02 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783520f892120026f51a2322783c3151a1a7b17ccb638160da6b0e27f6109a31`  
		Last Modified: Fri, 24 Oct 2025 18:27:02 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1463a77dd8fd7c3d004a4b16ee84730c772456afcd20d5616a06bf79abcde982`  
		Last Modified: Fri, 24 Oct 2025 18:27:10 GMT  
		Size: 60.8 MB (60824125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9454631f7fba1576db2877953703f0e3acf3300b9bca16d09de43a43306179bf`  
		Last Modified: Fri, 24 Oct 2025 18:27:02 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1371d3bc88b22624f50c3b08ec4005ec922a4cc05f9ce14ea230c833a83da9fc`  
		Last Modified: Tue, 28 Oct 2025 19:14:29 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8301a69cdcbea122dde20f5836e2f93b98bedbcb192b22b83880e73bf4bd41`  
		Last Modified: Tue, 28 Oct 2025 19:14:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d4f893c6d0d15ccc0731991b5b89c3aa18d0b849bed65873cd8fb193256630`  
		Last Modified: Tue, 28 Oct 2025 19:14:30 GMT  
		Size: 8.5 MB (8478543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0dc7aec67bb590bf458d2bdcb42ffa0285a7e8b169d3f82d69fa74aefd9727`  
		Last Modified: Tue, 28 Oct 2025 19:14:29 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
