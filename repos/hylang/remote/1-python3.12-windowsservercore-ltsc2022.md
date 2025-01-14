## `hylang:1-python3.12-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:f2b38ff81914781439a76d4dd32134a39d3b9d1c140d862f2d89df7cc96fa471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `hylang:1-python3.12-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull hylang@sha256:1178a9c0396b1c35d12c1b1e9aa215cde9b6ec2fec7a071a86a896491f86fb25
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2322350536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176cd329819245b0bb5706fdfd9dee31df51c240c1fd619404267fcec54c8520`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:42:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:42:58 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 11 Dec 2024 20:42:59 GMT
ENV PYTHON_VERSION=3.12.8
# Wed, 11 Dec 2024 20:43:00 GMT
ENV PYTHON_SHA256=71bd44e6b0e91c17558963557e4cdb80b483de9b0a0a9717f06cf896f95ab598
# Wed, 11 Dec 2024 20:43:43 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:43:43 GMT
CMD ["python"]
# Thu, 09 Jan 2025 23:10:35 GMT
ENV HY_VERSION=1.0.0
# Thu, 09 Jan 2025 23:10:36 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 09 Jan 2025 23:12:05 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 09 Jan 2025 23:12:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Fri, 13 Dec 2024 16:30:53 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da926f5375939d9dc382c854fc5da819e00a1ff2c7406fcddc8ba05f26ecb34`  
		Last Modified: Wed, 11 Dec 2024 20:43:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f58adc4231c3bbc7df9a3546d8ab43372f4dc9d70529b3c92f3366cb9b3a5db`  
		Last Modified: Wed, 11 Dec 2024 20:43:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fbdbe634f9ad8487a6fa24162448cacc4dc0dfd61ce1c1298c2ac24f78d976`  
		Last Modified: Wed, 11 Dec 2024 20:43:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010caa98cd1cce422bc61b1062237b35a780a9f4ac262cfb1477e4359133b089`  
		Last Modified: Fri, 13 Dec 2024 18:32:59 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2eb60fc7589b6813d8b88bb56a4e9a6557740d9e4a6231cc24b9b00823857d`  
		Last Modified: Fri, 13 Dec 2024 22:14:03 GMT  
		Size: 59.9 MB (59935423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff6b0046ebd10376ac0bf3af702b085b098fab88ae08b318aeee4c0584d4aa7`  
		Last Modified: Fri, 13 Dec 2024 16:26:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76be316adfd0e23ead718839887b77e3dd7cbc27570935a6ce28ca598db93996`  
		Last Modified: Thu, 09 Jan 2025 23:12:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e9d84ccc1b2effc6e1fb269e321f2dfa2d2065c638ae34789fb7e62bb5c4a1`  
		Last Modified: Thu, 09 Jan 2025 23:12:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f623b909728f4cc4807a699e6ef69d2d2920d79a80f16b46c48342368e616e2b`  
		Last Modified: Thu, 09 Jan 2025 23:12:10 GMT  
		Size: 8.5 MB (8531189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064b0f954001b84240261a61efbf65ec580ef9ba3be70b7bdf79116fdacfbe58`  
		Last Modified: Thu, 09 Jan 2025 23:12:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
