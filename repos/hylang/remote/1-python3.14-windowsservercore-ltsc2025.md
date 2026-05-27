## `hylang:1-python3.14-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:353534fe90c416d7eca9b23cb01f13cb5966df72583a1b4b644fed437f3f4efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `hylang:1-python3.14-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull hylang@sha256:3303ab876ad208ecac78238bc423850e2a84e71f4ac1bfe127f5c36f949d5453
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2275804814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357c74bcb233d1feb9ee0b65dfb9213279b3f30277a9529605a4597714382d8a`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:50:01 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 12 May 2026 23:50:01 GMT
ENV PYTHON_VERSION=3.14.5
# Tue, 12 May 2026 23:50:02 GMT
ENV PYTHON_SHA256=f9c09f5ed6f796fd1a8bc5ddfa41715a494b453c4781f0e35d5077cf9fa58f6d
# Tue, 12 May 2026 23:50:43 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:50:44 GMT
CMD ["python"]
# Wed, 27 May 2026 00:12:51 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:12:54 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:14:19 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 27 May 2026 00:14:20 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d188d7f4a5421b58c277ec337ae635de99e29dcb259e15d0521f9f034b9389`  
		Last Modified: Tue, 12 May 2026 23:40:52 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c855b0a869238548e35027126893ffdaca30a464fd624c1620934f52c0959ecd`  
		Last Modified: Tue, 12 May 2026 23:50:49 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92122d749a5d51e526ebf6aada6f98e9e35c40733efb71ccf2a229b20c34bcb3`  
		Last Modified: Tue, 12 May 2026 23:50:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08824b384a0da70df6c9f9f748a7aefe5bdb0b9cbbc2c1618e24036a8c546b95`  
		Last Modified: Tue, 12 May 2026 23:50:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb50e2e31ecbae4894b157e17cb692176f5a3d79a0bf9346ecfb3362426195b`  
		Last Modified: Tue, 12 May 2026 23:50:55 GMT  
		Size: 61.3 MB (61338866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e53701d2b2b04d99f34efdb0a69c516cf8fcfc08f12203223dab1b275ca746`  
		Last Modified: Tue, 12 May 2026 23:50:49 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a345f28b2ec34e448e909a23ddd7dd871dc71fdb9093176234dd9cfae76068c`  
		Last Modified: Wed, 27 May 2026 00:14:24 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d4abcd2fd5fcfb6881ceffe0b87a85b7fc0830d0504b2930bc610effaa01c3`  
		Last Modified: Wed, 27 May 2026 00:14:24 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bf857635dc503ef38fa03fb1e7ef65f1cae3c58df0df711320db04874f6f8f`  
		Last Modified: Wed, 27 May 2026 00:14:26 GMT  
		Size: 8.5 MB (8513594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6d7fa9412d2e4451ecb40456f60b20d384d86e816ebdce28f19a391404c183`  
		Last Modified: Wed, 27 May 2026 00:14:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
