## `python:windowsservercore-1809`

```console
$ docker pull python@sha256:1401ec5eb5edb97271a461ecdb46534c1809669d5ea26e112609e12efc587af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `python:windowsservercore-1809` - windows version 10.0.17763.7136; amd64

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
