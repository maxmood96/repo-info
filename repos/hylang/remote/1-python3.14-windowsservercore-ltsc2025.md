## `hylang:1-python3.14-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:98067c4503ba48759edc27a09927e6b6752ce68603a5ec95160d68f9a3879817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `hylang:1-python3.14-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull hylang@sha256:e58b3c18f0ba6c24125d7f6f0800ba4d7d6289bcc549817493c68f20cfb93d22
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3640906164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b216f5abadee60035b7b4c807d0f223a6a167af009a6b586b6cad8a66b03400`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Tue, 07 Oct 2025 20:38:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Oct 2025 20:38:50 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 07 Oct 2025 20:38:52 GMT
ENV PYTHON_VERSION=3.14.0
# Tue, 07 Oct 2025 20:38:52 GMT
ENV PYTHON_SHA256=52ceb249f65009d936e6504f97cce42870c11358cb6e48825e893f54e11620aa
# Tue, 07 Oct 2025 20:39:58 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 07 Oct 2025 20:39:58 GMT
CMD ["python"]
# Wed, 08 Oct 2025 20:17:07 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 20:17:08 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 20:18:26 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 08 Oct 2025 20:18:26 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b033268fa4f712a337443fd2b61c89968561cff36f7a00321e9d7b90741f217`  
		Last Modified: Tue, 07 Oct 2025 20:47:38 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6d0bf007b1adfcc1f52ffd4f95e577e28eaeeaee22a723b0a5416d574055dd`  
		Last Modified: Tue, 07 Oct 2025 20:47:38 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c8e741c657a33f2559f4b525ff8f3529a010749c9ade376c95c9ffe5e0e8aa`  
		Last Modified: Tue, 07 Oct 2025 20:47:38 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf08c2667cf86ede0fa0cbd773550458db011511164c92b5736dd44f8afb1070`  
		Last Modified: Tue, 07 Oct 2025 20:47:38 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a75fcc53dd08f93ff67101eee642505511481f43eb8805bf6d6d3ec569ddf7`  
		Last Modified: Tue, 07 Oct 2025 20:47:42 GMT  
		Size: 60.8 MB (60848438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae90dfb1fabb7251a71e3739373a17dc57eda28f0aacfd9a2dc821b37c9140d`  
		Last Modified: Tue, 07 Oct 2025 20:47:38 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ab26e3e98865b67a0c84fb2571e42b416ad2aacbf1859d2a8fa78378cd2ccf`  
		Last Modified: Wed, 08 Oct 2025 20:18:54 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c88f1b6cb60845698e122a2afc9ad811a786257e0c8e3d36b24367c14c56871`  
		Last Modified: Wed, 08 Oct 2025 20:18:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcef8b663bff28fb3663914ddaa31fc9d54c71114244a57689951c60f63ba44`  
		Last Modified: Wed, 08 Oct 2025 20:18:56 GMT  
		Size: 8.6 MB (8607364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a8d1692165271f54cc1ec23adba0d91460a46bc169f86c488f6e954d2ff14`  
		Last Modified: Wed, 08 Oct 2025 20:18:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
