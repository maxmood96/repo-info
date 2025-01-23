## `hylang:python3.12-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:27d5fe9b435e5363beda1898d1b3687d841397d8243ce4fc644905441fafbc48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `hylang:python3.12-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull hylang@sha256:12d98d761295582d2cf7eb57c1d0fd5222443abdbf89a9485c216a630ec32e70
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2568810423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a32c4e2ecbd0379433c224dca6cf500d43b197513caba513f571f86786bf25`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:35:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:35:07 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 22 Jan 2025 20:35:08 GMT
ENV PYTHON_VERSION=3.12.8
# Wed, 22 Jan 2025 20:35:09 GMT
ENV PYTHON_SHA256=71bd44e6b0e91c17558963557e4cdb80b483de9b0a0a9717f06cf896f95ab598
# Wed, 22 Jan 2025 20:35:48 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:49 GMT
CMD ["python"]
# Thu, 23 Jan 2025 01:32:05 GMT
ENV HY_VERSION=1.0.0
# Thu, 23 Jan 2025 01:32:05 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 23 Jan 2025 01:32:39 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 23 Jan 2025 01:32:39 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e744adeb38ac315f058069dc46fa6184593e46fedcec5b8837129753fa47a6`  
		Last Modified: Wed, 22 Jan 2025 20:35:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f4523a181f8173bac9db92bc79d895125c505b0c86a70bcfe8a6af0f522384`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd79c9297e14fb4872ef852ddb3da31c2c6369cf886b34fed272212b117c3d62`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687842bf821382c23944ad2145b7bfd335a6c09e008d56531d73ac3084061f12`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da25292bf77fdd32c4e87d3ffe10dc129bc46366ac9284c190073c1e21006bd`  
		Last Modified: Wed, 22 Jan 2025 20:35:57 GMT  
		Size: 60.0 MB (59981413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:badeb32f9c7c4a779d4e1ec60951ed1247fdddc74ade3e88712ff2cda2727e07`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3add5a619e38fd8fe55820fe15566e3263e754f0f67aef06885e2e7629d2f504`  
		Last Modified: Thu, 23 Jan 2025 01:32:43 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3367b2736eb6f9a68a154dc4edfa7f50bd889f3281d208f14c3720235f17032`  
		Last Modified: Thu, 23 Jan 2025 01:32:43 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5e1baa87968a0c520c77bf87a50fd62b97161ba8c1cff9474cc70c1cfe364b`  
		Last Modified: Thu, 23 Jan 2025 01:32:45 GMT  
		Size: 8.5 MB (8541055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58445bfdc752453793e043bf2d952722bbf7b05c616a726913013ecaa3eb3d1`  
		Last Modified: Thu, 23 Jan 2025 01:32:44 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
