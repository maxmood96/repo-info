## `hylang:python3.13-windowsservercore`

```console
$ docker pull hylang@sha256:feb468b9a4c50aafde718bc578bad5326ae68743b34167e38eb97fe74a0f8bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `hylang:python3.13-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull hylang@sha256:58f1a03b43f340774b96b55cd48539181a3a8156b0b3caa2ea05292765bceef0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3302679258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb93253e12237b25fc9066fd843829fdab8c6d50ba09df74f5197d1ae45cec91`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Mon, 08 Dec 2025 20:11:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 08 Dec 2025 20:11:42 GMT
ENV PYTHONIOENCODING=UTF-8
# Mon, 08 Dec 2025 20:11:42 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:11:43 GMT
ENV PYTHON_SHA256=30d4654b3eac7ddfdf2682db4c8dcb490f3055f4f33c6906d6b828f680152101
# Mon, 08 Dec 2025 20:13:26 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Mon, 08 Dec 2025 20:13:26 GMT
CMD ["python"]
# Mon, 08 Dec 2025 21:14:11 GMT
ENV HY_VERSION=1.1.0
# Mon, 08 Dec 2025 21:14:11 GMT
ENV HYRULE_VERSION=1.0.1
# Mon, 08 Dec 2025 21:14:45 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Mon, 08 Dec 2025 21:14:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dbbab376dece2eddad77486533e245b05df2926724534eaa20435003080518`  
		Last Modified: Mon, 08 Dec 2025 20:29:16 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc7dc41d8dccba107ca825872336bc9d08299dc4cc711fac0d8eebe800fd310`  
		Last Modified: Mon, 08 Dec 2025 20:29:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d483f86e993764804dd16f3cd4e1144f331d3ddd6b1ce9cb3a768589443e22c4`  
		Last Modified: Mon, 08 Dec 2025 20:29:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca00f0d8ce8cf3c27bba139a5c706bcab07aeac03a2041e13549b16000c3459`  
		Last Modified: Mon, 08 Dec 2025 20:29:16 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f23c168974e3e7d49c1c975524e1b9a7c8d957c32f860662938df2715e21e44`  
		Last Modified: Mon, 08 Dec 2025 20:29:20 GMT  
		Size: 58.8 MB (58766816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9302058624e7a30652c344c3034897a5ebcf927a72b9732b760ebc08c038c9`  
		Last Modified: Mon, 08 Dec 2025 20:29:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65a76018d38d8ea738af06ea78c4fd189b1dcd469d1f10ce3e1e9f1d59ae513`  
		Last Modified: Mon, 08 Dec 2025 21:14:58 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8da4208be5559475d54db74bb06bf5a3c391df339332fdc976485d9fdca715f`  
		Last Modified: Mon, 08 Dec 2025 21:14:58 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ade113c517bb2618d7ed5362db34f573d9b2e7491a1466c8d8c45a1d87855f`  
		Last Modified: Mon, 08 Dec 2025 21:14:59 GMT  
		Size: 8.4 MB (8446129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc471df5a70fc868f98ce73c6e7fdb7c80ca7541ebe599b6a5ee2a87c1c822f9`  
		Last Modified: Mon, 08 Dec 2025 21:14:58 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.13-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull hylang@sha256:e9e9c72104693444a95dc5ecc1ec720f6c867f621fd31bc89723ca1ee8c80558
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1837281104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76610fca27a38a9a03d482f8b6a2d9ec08e2b375c9ec9deab5276db213dcdd8`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Mon, 08 Dec 2025 20:08:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 08 Dec 2025 20:08:26 GMT
ENV PYTHONIOENCODING=UTF-8
# Mon, 08 Dec 2025 20:16:29 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:16:30 GMT
ENV PYTHON_SHA256=30d4654b3eac7ddfdf2682db4c8dcb490f3055f4f33c6906d6b828f680152101
# Mon, 08 Dec 2025 20:17:21 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Mon, 08 Dec 2025 20:17:22 GMT
CMD ["python"]
# Mon, 08 Dec 2025 21:14:56 GMT
ENV HY_VERSION=1.1.0
# Mon, 08 Dec 2025 21:14:57 GMT
ENV HYRULE_VERSION=1.0.1
# Mon, 08 Dec 2025 21:15:44 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Mon, 08 Dec 2025 21:15:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ffc7eb5bf3a3b46cbd160669be7fb8a5459d729b66dc7c646f51082af65d43b`  
		Last Modified: Mon, 08 Dec 2025 20:16:17 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc03fcbb83c064c39d3fc1b18f9c32e0998413f042cc0a70597093dc0727d100`  
		Last Modified: Mon, 08 Dec 2025 20:16:17 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6a7f33e30aaec35b3c3a85dda1ef94d74719128c1b86b6bb9ce5faca01e339`  
		Last Modified: Mon, 08 Dec 2025 20:17:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5c63941bdfa83c6395ad62a7fe01e00aaf32ee96709521144c2b8253c2b0d0`  
		Last Modified: Mon, 08 Dec 2025 20:17:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b48890676bb6cd0e21bfb8a06419e580f51b95c43082f39254443e0c06f808`  
		Last Modified: Mon, 08 Dec 2025 20:17:45 GMT  
		Size: 58.9 MB (58858725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982b73b00fe4093db95cffc035a9611af060ede73d1e9d9fc622df93adeb43b2`  
		Last Modified: Mon, 08 Dec 2025 20:17:41 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bcbfc77e28721e0aeb19aafec63f3971b7370732f33e30efa574ef8bff4559`  
		Last Modified: Mon, 08 Dec 2025 21:16:04 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ec167139fa876e3e437974935be5ca64a9574f4086099f4a16cdd9d6bec80a`  
		Last Modified: Mon, 08 Dec 2025 21:16:04 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67901ac0bbb1ca5fedd4e928808a504d9e5315b16f403356ecd783d128f6f8a`  
		Last Modified: Mon, 08 Dec 2025 21:16:05 GMT  
		Size: 8.5 MB (8450388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb68f3f4907fd4dca34f614bc49f0380ecf23f6da3246e666d9d175c96308af5`  
		Last Modified: Mon, 08 Dec 2025 21:16:05 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
