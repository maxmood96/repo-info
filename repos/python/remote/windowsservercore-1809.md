## `python:windowsservercore-1809`

```console
$ docker pull python@sha256:3910a53c096d2b29d200cbcc11d7a21fa134288b108a2281b644cd7220befa5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `python:windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull python@sha256:1b5b9f4d7122143b565ba94da61a28a2f0d946831b3275fcd8529f842c45ab32
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778566854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897a2f80dc5279ac0d4e3fe0ec973b5a3ae7ab257b49c2cafe1c516b3f4eb3e0`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 01 Oct 2024 22:21:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 01 Oct 2024 22:21:07 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 01 Oct 2024 22:21:08 GMT
ENV PYTHON_VERSION=3.12.7
# Tue, 01 Oct 2024 22:23:28 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 01 Oct 2024 22:23:29 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d60466f388349362ce8b2dc02f5f3014b2030a0ad31a4c9a1caf39454f7b7f`  
		Last Modified: Tue, 01 Oct 2024 22:23:32 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f8b3151c2bcd4fc4e9e9817d7c61ef713477c640262723232edf8d74570df7`  
		Last Modified: Tue, 01 Oct 2024 22:23:32 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9050d570781708e062d7abc4973a27aef29f97dea5850555a97bed6352b0fc62`  
		Last Modified: Tue, 01 Oct 2024 22:23:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226daf498520a1457179f15a26c5c95b7ff9b03e47e925d60937960fa786abbb`  
		Last Modified: Tue, 01 Oct 2024 22:23:36 GMT  
		Size: 58.3 MB (58293274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c188e8c574fc93c860542c258b5a9c8c4ec40953e617aed3529175fdbed2300c`  
		Last Modified: Tue, 01 Oct 2024 22:23:32 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
