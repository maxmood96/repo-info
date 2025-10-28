## `hylang:1-python3.13-windowsservercore`

```console
$ docker pull hylang@sha256:c2feb45439f0a652017ee62908685760a004baf1eb06ad2a25519d26a2648172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `hylang:1-python3.13-windowsservercore` - windows version 10.0.26100.6905; amd64

```console
$ docker pull hylang@sha256:f432d6fb9e30691655e3d9d0557763c79ea6b1c34f7f2d8f0ce93db790ef22f2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3287858071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8915bf32ff243bcc1680df3fa674e6c220c2ea34a45874bed571aa8d93842268`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:26:16 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 24 Oct 2025 18:26:17 GMT
ENV PYTHON_VERSION=3.13.9
# Fri, 24 Oct 2025 18:26:17 GMT
ENV PYTHON_SHA256=200ddff856bbff949d2cc1be42e8807c07538abd6b6966d5113a094cf628c5c5
# Fri, 24 Oct 2025 18:26:59 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:27:00 GMT
CMD ["python"]
# Tue, 28 Oct 2025 19:15:55 GMT
ENV HY_VERSION=1.1.0
# Tue, 28 Oct 2025 19:15:56 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 28 Oct 2025 19:18:08 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 28 Oct 2025 19:18:08 GMT
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
	-	`sha256:ab9235cc3c3cb68485c33877f779011c5a8c97c24f91de0e5999d9885837e759`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e2c2cc80b77d4bf2e0bc39add23822707559916244c48e15f3fb9954e6a4c8`  
		Last Modified: Fri, 24 Oct 2025 18:27:17 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43761e16d5afb8e84fd3a6e344ba295a0dc12eb28eeb76c7e88d6641d693e7b`  
		Last Modified: Fri, 24 Oct 2025 18:27:17 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948104ac00c5296cd21aca25452c7b81cc51db87acbbe9dec1a92654b84dc1b5`  
		Last Modified: Fri, 24 Oct 2025 18:27:17 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fd638c936fd79a33e4da12dd3f4fba83dd9bac26cdbf0ffbff14c5bc06d95f`  
		Last Modified: Fri, 24 Oct 2025 18:27:24 GMT  
		Size: 58.7 MB (58713601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e42090ac5a542e796c2cc2eea3b1257287fea47b873ccedc4f27e018bed6bb6`  
		Last Modified: Fri, 24 Oct 2025 18:27:17 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ced983f29c82db0dfa5b56ef2a55ab36948f8eb0158bd03b6cacfef933f8a5`  
		Last Modified: Tue, 28 Oct 2025 19:18:22 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9054825cdf1cb2813421958db3e0bb1225da74e63c24e1c93b4380e58bc58a6`  
		Last Modified: Tue, 28 Oct 2025 19:18:22 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed616ee53e60fd90893bb85a6490b3146755eedf1fb43022170448cbf18edfa6`  
		Last Modified: Tue, 28 Oct 2025 19:18:24 GMT  
		Size: 8.8 MB (8786951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e300922b7f2ed2f7c86708568c06d5350946cca7a00ede0dfbd1472b9d374602`  
		Last Modified: Tue, 28 Oct 2025 19:18:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-python3.13-windowsservercore` - windows version 10.0.20348.4297; amd64

```console
$ docker pull hylang@sha256:75b426d1bc551408ab8cc04d0c63f736089916526f8ca67b82a9e85004e9876e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1644354896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e074aade587d518201887c8467a4805daed7ade6ac898a8772227d76d2b84863`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:21:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:26:35 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 24 Oct 2025 18:26:36 GMT
ENV PYTHON_VERSION=3.13.9
# Fri, 24 Oct 2025 18:26:37 GMT
ENV PYTHON_SHA256=200ddff856bbff949d2cc1be42e8807c07538abd6b6966d5113a094cf628c5c5
# Fri, 24 Oct 2025 18:27:33 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:27:34 GMT
CMD ["python"]
# Tue, 28 Oct 2025 19:11:55 GMT
ENV HY_VERSION=1.1.0
# Tue, 28 Oct 2025 19:11:55 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 28 Oct 2025 19:12:34 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 28 Oct 2025 19:12:35 GMT
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
	-	`sha256:17e969c09e3393939c9e6a500d472036f493ca065945e74c4ac359749c0216ff`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ed0f48851cb8ebadc08edbcd723a0aba0ec67a74f4dc5b6e76c9747521698e`  
		Last Modified: Fri, 24 Oct 2025 18:27:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0a60efd9965753055cb68503227c09ba5abdbe221c0e6b74dcde2c7c38aa6f`  
		Last Modified: Fri, 24 Oct 2025 18:27:53 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a7e38a9d1b07703a27631c0e189bb73bbcdee7707c0688abdd4f330388e0c5`  
		Last Modified: Fri, 24 Oct 2025 18:27:52 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35fdc421d8fac456c0606595efe50cb1d9a089449f9b853444366d38e07928c`  
		Last Modified: Fri, 24 Oct 2025 18:27:59 GMT  
		Size: 58.7 MB (58746548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4a2d36a0251972ef9bd5c0187f259175a174b510af6a882234b3ed1e08ac9e`  
		Last Modified: Fri, 24 Oct 2025 18:27:52 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a7ae994bfb555cf6a2e46b8e62423af14fd760e2b838e0eabc51c23676c5fd`  
		Last Modified: Tue, 28 Oct 2025 19:12:46 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69948a861cd38e598f37df366613a7e8973afc729984266667244b3152589afa`  
		Last Modified: Tue, 28 Oct 2025 19:12:46 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91ed1efabafc2c71c3c692929cbef0b95b36e837f2d47986d6e48020ae91ed7`  
		Last Modified: Tue, 28 Oct 2025 19:12:47 GMT  
		Size: 8.4 MB (8404870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa50f25e86552d23315f8010e34dcd6778a14fcfd882e1075cb6c74e8d779439`  
		Last Modified: Tue, 28 Oct 2025 19:12:46 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
