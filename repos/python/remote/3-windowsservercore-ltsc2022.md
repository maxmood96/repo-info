## `python:3-windowsservercore-ltsc2022`

```console
$ docker pull python@sha256:9e16eeff29d4c77c73ab965bffa5e992d67ae5805449a0dbe7cfe6f4733b86f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `python:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull python@sha256:34fd75067b10507edf11204c6d75540cfe98cda56050bbbc6df50cd7d20984d0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2342878877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c19637ff5db81da1fe9b062b5a8b88fed377658ecfc2b5b860a9b29ca530f77`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Tue, 07 Oct 2025 20:43:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Oct 2025 20:43:49 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 07 Oct 2025 20:43:50 GMT
ENV PYTHON_VERSION=3.14.0
# Tue, 07 Oct 2025 20:43:51 GMT
ENV PYTHON_SHA256=52ceb249f65009d936e6504f97cce42870c11358cb6e48825e893f54e11620aa
# Tue, 07 Oct 2025 20:45:02 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 07 Oct 2025 20:45:03 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Thu, 09 Oct 2025 10:32:05 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55aae93905df42ad1616e54b1014ca296f220a9ca9884cb79c33417dd5d013d`  
		Last Modified: Tue, 07 Oct 2025 20:50:30 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee29297541ec950c18c3ec0d86af1d7d690d8b9261863f53d0f2650d3342013a`  
		Last Modified: Tue, 07 Oct 2025 20:50:31 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625889b090d16992f131f130ec41d0ecdc8fbefce374fe00e76de023c433145a`  
		Last Modified: Tue, 07 Oct 2025 20:50:30 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a03b397f6ddecaaf7efe5580b02c4e836e12eb817d31066e3a3ece5daf524d`  
		Last Modified: Tue, 07 Oct 2025 20:50:30 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5073aab0cab6dbb083c9729001591ba68b1f7bae764e614d141e469cdeb854`  
		Last Modified: Tue, 07 Oct 2025 20:50:33 GMT  
		Size: 60.7 MB (60727321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999c294a4134b0e567d52117cca77ab39e454650bdf2671f4a6bcf506fb1af85`  
		Last Modified: Tue, 07 Oct 2025 20:50:31 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
