## `python:windowsservercore`

```console
$ docker pull python@sha256:26562407c6828c2eb44505989c53c5cf22242e1542cc2bd822d94df34db35dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `python:windowsservercore` - windows version 10.0.26100.3775; amd64

```console
$ docker pull python@sha256:222f50c2a1cddbbca791e094d16e53fc7ddb494280a9ac35b3d505f4513e2750
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3453975307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d151d6e0ebc9503dcdb5a8a4094c65c6ed3c4f0f4d7411b5130f750e1eb67380`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:47:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:47:12 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 09 Apr 2025 00:47:13 GMT
ENV PYTHON_VERSION=3.13.3
# Wed, 09 Apr 2025 00:47:15 GMT
ENV PYTHON_SHA256=698f2df46e1a3dd92f393458eea77bd94ef5ff21f0d5bf5cf676f3d28a9b4b6c
# Wed, 09 Apr 2025 00:47:55 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:47:56 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ef29dded149056db476fbc5e297cf3b8e79bad2167d8bbc3e5e19eb82c0ed2`  
		Last Modified: Wed, 09 Apr 2025 00:48:00 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc49a0e09f6e7fb522a0faccc20610b4ccb99a2f3a4343fd39dd1ee977bb7c4`  
		Last Modified: Wed, 09 Apr 2025 00:47:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c3c039a15e6f60a3c0a2d3aae4e77fc5df9748a185fbca4096ac5c6e7d4d55`  
		Last Modified: Wed, 09 Apr 2025 00:47:59 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c079e5924a62fe452d6a33b9a291182ff6c98994cc8ad73a3dbb41d2aa38f86`  
		Last Modified: Wed, 09 Apr 2025 00:47:59 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a92a231439c52fa4b4b639414d020f4ab5ac8991fac452e7856948b53febdc9`  
		Last Modified: Wed, 09 Apr 2025 00:48:04 GMT  
		Size: 59.3 MB (59289282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9233e3370c07ffe93b3ed3730d10e8742502deb6ea2c00b6cdf88af427f84d`  
		Last Modified: Wed, 09 Apr 2025 00:47:59 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:windowsservercore` - windows version 10.0.20348.3453; amd64

```console
$ docker pull python@sha256:bc675fef715461abd04622daa302d0e9b25313afb1c6802061985fd178505d9b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330208279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da05653f00584255107247faea5a61b1433f229b7563643a1ab00296829cd934`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 00:50:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:50:23 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 09 Apr 2025 00:50:24 GMT
ENV PYTHON_VERSION=3.13.3
# Wed, 09 Apr 2025 00:50:25 GMT
ENV PYTHON_SHA256=698f2df46e1a3dd92f393458eea77bd94ef5ff21f0d5bf5cf676f3d28a9b4b6c
# Wed, 09 Apr 2025 00:51:12 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:51:13 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9764f1349e349b8152f998574af9d283e83eb46b083f0455ffdbf4b5e8a96fd`  
		Last Modified: Wed, 09 Apr 2025 00:51:19 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7686f259dc851e055b14390ac15af9c86f61936d2fda926730a71957f53c59e9`  
		Last Modified: Wed, 09 Apr 2025 00:51:17 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a0f63cd93e7c85ec6661d37a3bced43b8096ff8c3286c3de5f8778bc4c8e54`  
		Last Modified: Wed, 09 Apr 2025 00:51:17 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0b88a098dadd0d490bedf600853e714d0ffdff0712cd7087516fbdbc6d4a4b`  
		Last Modified: Wed, 09 Apr 2025 00:51:17 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077a0925a3502417c6ec402be7ac3dbc727cb560aef09f9325181c94778a48de`  
		Last Modified: Wed, 09 Apr 2025 00:51:22 GMT  
		Size: 59.2 MB (59206167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0e7b1a8921c1acebc3e85ba64e8715ba744ce45487d4bfc3b9727b29b5b505`  
		Last Modified: Wed, 09 Apr 2025 00:51:17 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:windowsservercore` - windows version 10.0.17763.7136; amd64

```console
$ docker pull python@sha256:79ec83fbfc43adeb6ecd5340d738681d9c2d72a94aee60b31ab9497d24eb92b7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2220605982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61781b15e1a4b66e963251f3469af839758cf5dace29a1cce3694aa1c93d119a`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 00:56:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:56:36 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 09 Apr 2025 00:56:37 GMT
ENV PYTHON_VERSION=3.13.3
# Wed, 09 Apr 2025 00:56:38 GMT
ENV PYTHON_SHA256=698f2df46e1a3dd92f393458eea77bd94ef5ff21f0d5bf5cf676f3d28a9b4b6c
# Wed, 09 Apr 2025 00:57:35 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:57:37 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf932b60be1f475a4d4c57a797f478fbbf6d65a95a6e803b3fc8fc4971dab42`  
		Last Modified: Wed, 09 Apr 2025 00:57:43 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b10d4bf94dd9459776ce1f41d235200c7b3dbead37ef289add4a1a83f2f77d`  
		Last Modified: Wed, 09 Apr 2025 00:57:41 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce794835a2791a3bf7beb087aedcba938fca7ce76e588e729fc97ddf221e88c1`  
		Last Modified: Wed, 09 Apr 2025 00:57:41 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7f4105dbba2870806af6960d484e535d3f669abcc503ece7b9c91db370f266`  
		Last Modified: Wed, 09 Apr 2025 00:57:41 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c522ea045c9678abe3a845b8dec3ea42bc184e1a51fdc53c3717294caaa749`  
		Last Modified: Wed, 09 Apr 2025 00:57:46 GMT  
		Size: 57.9 MB (57873650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9200f2376d0b8df716d2878a38ae35ade428624cd112624a404dd2dda7b080d`  
		Last Modified: Wed, 09 Apr 2025 00:57:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
