## `hylang:python3.12-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:e380619971e1709dc35b8ba2a377814e03a11c535f4dc9bd022d1c372bb3bec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `hylang:python3.12-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull hylang@sha256:c124d20a04e70cc3d385fc4625677c165ca21445e3c2d0155ebd65bac4965dd2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330876487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887d324be7ca70d3e9b03063882ca2422c77084158dbf71b5158734d8da65efa`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Thu, 06 Feb 2025 23:26:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 Feb 2025 23:26:23 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 06 Feb 2025 23:26:24 GMT
ENV PYTHON_VERSION=3.12.9
# Thu, 06 Feb 2025 23:26:24 GMT
ENV PYTHON_SHA256=2a52993092a19cfdffe126e2eeac46a4265e25705614546604ad44988e040c0f
# Thu, 06 Feb 2025 23:27:18 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 06 Feb 2025 23:27:19 GMT
CMD ["python"]
# Fri, 07 Feb 2025 00:27:53 GMT
ENV HY_VERSION=1.0.0
# Fri, 07 Feb 2025 00:27:54 GMT
ENV HYRULE_VERSION=0.8.0
# Fri, 07 Feb 2025 00:29:21 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 07 Feb 2025 00:29:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc52aa793c63e6aaf63df8fc0ef66921646a06ac41cccf1dd83481c1fd710b33`  
		Last Modified: Thu, 06 Feb 2025 23:27:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3fb38c47c230b7016575035938b2951cb1869329351236422cf07016289750`  
		Last Modified: Thu, 06 Feb 2025 23:27:23 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988b1d873db1d7dc95ef93495fa3a6733b3407c5fdfece6929c2128ea7215840`  
		Last Modified: Thu, 06 Feb 2025 23:27:23 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbe06907a4a1f8c2da9b583d19bb98bee1cf948547873616f6276e76b3e6a65`  
		Last Modified: Thu, 06 Feb 2025 23:27:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f7a435063ed8d89a1ba8be77f3c3a98618f21f8633e9d3698516573336ecb1`  
		Last Modified: Thu, 06 Feb 2025 23:27:28 GMT  
		Size: 60.0 MB (59958203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432c0fc8d7e5b5f9971a9e98e409eb73e31e5cc0c419d8d3c2e008f56b8d5f0b`  
		Last Modified: Thu, 06 Feb 2025 23:27:23 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61d1515d507dae3904a717fc63a4b7e67aee57edeaf85e593254cb5a8def163`  
		Last Modified: Fri, 07 Feb 2025 00:29:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b5545dbb70963e0a24fd665e376c967a1020088c2db0c7a1d5c2dc6fb29968`  
		Last Modified: Fri, 07 Feb 2025 00:29:24 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f62f14849cb6716b33ea49095f4bea4366390fdab040b20ae49f5ca3e860c9e`  
		Last Modified: Fri, 07 Feb 2025 00:29:25 GMT  
		Size: 8.5 MB (8522668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9e7bcb70fd2a991750b7a690493e3da6941bf64a9241bbdd72bce5ea32afe2`  
		Last Modified: Fri, 07 Feb 2025 00:29:24 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
