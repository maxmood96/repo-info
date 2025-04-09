## `python:3-windowsservercore-1809`

```console
$ docker pull python@sha256:0e8b728feb20a4a1620693f44f8224e5ea9f17350bdb76be6f05feeb05741b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `python:3-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull python@sha256:54e99589c934dab3b5938afd2794e3cc3641afbc0e51480700b4eaa759816e09
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2209525299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43c095b64b018d70eee56ac96e09cb38deedf8dd32e9dc2bdae9d9746c7c9fa`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 09 Apr 2025 00:44:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:44:51 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 09 Apr 2025 00:44:51 GMT
ENV PYTHON_VERSION=3.13.3
# Wed, 09 Apr 2025 00:44:52 GMT
ENV PYTHON_SHA256=698f2df46e1a3dd92f393458eea77bd94ef5ff21f0d5bf5cf676f3d28a9b4b6c
# Wed, 09 Apr 2025 00:46:27 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:46:29 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7cbdca28b891cc10a9cf739642e4676d3cc4b157359c51f2fbf6c33d48ca84`  
		Last Modified: Wed, 09 Apr 2025 00:46:33 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548ec4da30f9701611b2c5029276fa7f2558af7dda179a88aec4fd75b453d36a`  
		Last Modified: Wed, 09 Apr 2025 00:46:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699782ce3de5df4ee661da4cf8ac218089128b8803fe03a9ce713a7281045127`  
		Last Modified: Wed, 09 Apr 2025 00:46:32 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b11632a0f7a2ff4393459a2601c90ccaf0f3fbdf664af1175746df48bc552bb`  
		Last Modified: Wed, 09 Apr 2025 00:46:31 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c7794dd05200ff655acca76c25f98bab407b1beb91007e6c86f91250efe2f9`  
		Last Modified: Wed, 09 Apr 2025 00:46:37 GMT  
		Size: 57.9 MB (57884195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f4016024c2988d21f51b343d3e72fbd5d8c0369598fead465c6bab5b2a0c78`  
		Last Modified: Wed, 09 Apr 2025 00:46:32 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
