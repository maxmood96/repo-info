## `hylang:python3.12-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:44eb6cbd5e50ebe86d9b75121005a00744eb026d9e0331c73d4b174b645f756c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `hylang:python3.12-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull hylang@sha256:30b6d286471c67d404835315b9cae46b5bfeacd6738892e9813079e71195d7e8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2977425519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ec2dab804cde36fb62e8066522c7226eee88d59a6b28ed53fc320855889b1f`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:48:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:48:19 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 12 Mar 2025 18:48:20 GMT
ENV PYTHON_VERSION=3.12.9
# Wed, 12 Mar 2025 18:48:21 GMT
ENV PYTHON_SHA256=2a52993092a19cfdffe126e2eeac46a4265e25705614546604ad44988e040c0f
# Wed, 12 Mar 2025 18:48:59 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:48:59 GMT
CMD ["python"]
# Wed, 19 Mar 2025 23:05:20 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 23:05:22 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 23:06:01 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 19 Mar 2025 23:06:02 GMT
CMD ["hy"]
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
	-	`sha256:fa6ab578ec8491b47ec39e11a79eeac738d23b741f5f2d9480e6f8f35366e9c8`  
		Last Modified: Wed, 12 Mar 2025 18:49:05 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095ddf14630b8b7dcff9dbdf09047657aa0f426431be631646cf7a5f04d5b3cc`  
		Last Modified: Wed, 12 Mar 2025 18:49:03 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6732778a9d15b5ceedc87d2fd5974a16ecc0f3f3aba789df74feeb38c278b2`  
		Last Modified: Wed, 12 Mar 2025 18:49:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab72a92e0ac0561e7ecf182a29d3bd6a8fb17976e172558e51a5fd99ac666fe`  
		Last Modified: Wed, 12 Mar 2025 18:49:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48feb201ade569bac5347a5e18f93cb3c2392d976e9a90a2fdbf31fec8f5557e`  
		Last Modified: Wed, 12 Mar 2025 18:49:09 GMT  
		Size: 60.1 MB (60096959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512c0c087e203eae3cbd53618793e3bc1ce757df8be0d04c962dc392579b9e55`  
		Last Modified: Wed, 12 Mar 2025 18:49:03 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415436b4e30d51281adffbdd9984c4042ec10a08c1ccf0649d86ec8e29b691d3`  
		Last Modified: Wed, 19 Mar 2025 23:06:06 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8141103a38520bae936eda5e70561cc7845328ee46a1f3ebb166a8f013ed4bfa`  
		Last Modified: Wed, 19 Mar 2025 23:06:06 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eabeb709d83505f74f886bd5b526b9f18e66f94e300d9a53bf3a9530319b330`  
		Last Modified: Wed, 19 Mar 2025 23:06:07 GMT  
		Size: 8.7 MB (8670321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea7f874de3cf7a9911c641bc342f73efe32cb27a08aac8ae7ad7e0b9f116e63`  
		Last Modified: Wed, 19 Mar 2025 23:06:06 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
