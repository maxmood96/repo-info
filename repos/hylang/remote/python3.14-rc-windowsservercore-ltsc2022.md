## `hylang:python3.14-rc-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:29bac75f05bc222b49fc2862e573166d5a21a6afc368692dcf810f3367a0a002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `hylang:python3.14-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull hylang@sha256:ca7203fda6c68386e078ec0285f4dd7f53d89b56bf190fc323359b934304733a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2351313254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef647904a1f91ea170dac137999944b9399695fcab939b446cf81870e466444`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 22:00:09 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 10 Sep 2025 22:00:10 GMT
ENV PYTHON_VERSION=3.14.0rc2
# Wed, 10 Sep 2025 22:00:11 GMT
ENV PYTHON_SHA256=cf4732baba457a6d444f4c084e0bcf9eab4302730b5cab6031e5767bab3a2a7f
# Wed, 10 Sep 2025 22:00:50 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 22:00:51 GMT
CMD ["python"]
# Wed, 10 Sep 2025 22:22:44 GMT
ENV HY_VERSION=1.1.0
# Wed, 10 Sep 2025 22:22:45 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 10 Sep 2025 22:23:17 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 10 Sep 2025 22:23:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9811425449e84dcbd33b2ae7b7f37c3b7fd53dcd7b0401fd37de5fddd1a09096`  
		Last Modified: Wed, 10 Sep 2025 21:55:58 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbd23738df4c9ead6be4f6e8ee5beb532f0ead207b8ef4930d58b915620e635`  
		Last Modified: Wed, 10 Sep 2025 22:01:31 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b426d36524eb3ed39a15aab6b1d4db63dd17a79f72232077ad0e29ab8e9aeff2`  
		Last Modified: Wed, 10 Sep 2025 22:01:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aaf297d911444b18302f2211d6665838adb2f70fa52931bad21288357e83771`  
		Last Modified: Wed, 10 Sep 2025 22:01:31 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4226f9cc40fdab472d6187f8caa9a99d007afe339bd4247447e8461a721e57`  
		Last Modified: Wed, 10 Sep 2025 22:01:41 GMT  
		Size: 60.7 MB (60651847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536f1956dc0265cbaec04c684fc65cb967e386c13d875e8008e0d1e6c94a5eee`  
		Last Modified: Wed, 10 Sep 2025 22:01:31 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549d61071beb61b6a144e6123bbdca37ff61bb47155a434c4646a7bc87cd2546`  
		Last Modified: Wed, 10 Sep 2025 22:23:38 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ab0845cdb0e2ccb12f9bb1398179c934d3af54ce318cbe7ec586935828f88c`  
		Last Modified: Wed, 10 Sep 2025 22:23:38 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61866db7460303c8817ccf84d2eb1df1f8754c7f3223f0d5e047fa7b50650721`  
		Last Modified: Wed, 10 Sep 2025 22:23:39 GMT  
		Size: 8.5 MB (8505900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f180d5c6333f9858a36b36272044ddccc698472effcd55bb91531914cd3557`  
		Last Modified: Wed, 10 Sep 2025 22:23:38 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
