## `python:3-windowsservercore-ltsc2025`

```console
$ docker pull python@sha256:3ef630fdb67869912e50ca657784568bbc1da33e03ae010dd0d7348f757fbaa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `python:3-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull python@sha256:cd442fed2a6871f6b2125724fbe0c902ce3733406eb99a46f75db6fd8dca9081
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2967869383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4ecf9f132e88d03fa6a5b1274148b9791e53254ecc050f25eb971ba13c17b3`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:48:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:48:07 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 12 Mar 2025 18:48:07 GMT
ENV PYTHON_VERSION=3.13.2
# Wed, 12 Mar 2025 18:48:08 GMT
ENV PYTHON_SHA256=9aaa1075d0bd3e8abd0623d2d05de692ff00780579e1b232f259028bac19bb51
# Wed, 12 Mar 2025 18:48:45 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:48:46 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db05ebafac5b0fb7dfa4ed97cc8b2683be4b287bba5e884a0a5e1e13057cfe7`  
		Last Modified: Wed, 12 Mar 2025 18:48:49 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cd8e49651a452d31e3a3a7a7f4def3fdcb2c7e50b25a4b73fff3fc5cbfeac0`  
		Last Modified: Wed, 12 Mar 2025 18:48:48 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb0a44871b4a0b85a7d8842de002af943c755e89a56a55e938cb82f1bb27b3a`  
		Last Modified: Wed, 12 Mar 2025 18:48:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debf2ff1ef0c7393113b5fc5d7c95015e4488ea283411bb029236334bbceacc2`  
		Last Modified: Wed, 12 Mar 2025 18:48:48 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097f71ff76ec962ef08c9a66553840cf263f1263f2764877bfa28038280c63c2`  
		Last Modified: Wed, 12 Mar 2025 18:48:53 GMT  
		Size: 59.2 MB (59215131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc46af2be7643fc9d0674f87668a6ac672b920e08ec9e61ef2066c25469151f`  
		Last Modified: Wed, 12 Mar 2025 18:48:48 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
