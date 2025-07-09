## `hylang:1-python3.14-rc-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:1cdab11e6d776addb781f2e95c5c1c4170a1876fbe0f40962885316af7832815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `hylang:1-python3.14-rc-windowsservercore-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull hylang@sha256:c5173da4a659f51c35fbecb724ea7ad10c3d8f37e3b0276c673f205a5d0a97b7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3561024187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca68b131af31128c8c051036c3351db845fe74d8423b80cf6b6c9e6ab1168961`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Wed, 09 Jul 2025 18:11:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:11:39 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 09 Jul 2025 18:11:40 GMT
ENV PYTHON_VERSION=3.14.0b4
# Wed, 09 Jul 2025 18:11:41 GMT
ENV PYTHON_SHA256=0f8bbdfd7d1f99a0b8df86278a99e4c0248582b93e9d7d4d6e63e787098dad00
# Wed, 09 Jul 2025 18:12:20 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:12:21 GMT
CMD ["python"]
# Wed, 09 Jul 2025 19:14:46 GMT
ENV HY_VERSION=1.1.0
# Wed, 09 Jul 2025 19:14:48 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 09 Jul 2025 19:15:20 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 09 Jul 2025 19:15:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f47c8f2e806aab12fb78910d840d3cbc910a556c488e965813af4452f3b2e6`  
		Last Modified: Wed, 09 Jul 2025 19:08:54 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a89c4c8747ec466eb3af290e3d909e0cdcc5cc33259e2dbed121d451f2f536`  
		Last Modified: Wed, 09 Jul 2025 19:08:55 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70a64621c6e67338acead431a6f2be71e59b7e894a09b6b660a86c8f991733d`  
		Last Modified: Wed, 09 Jul 2025 19:08:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60578e16b4920ef37ad3d8089293c4a6bdd7ae581700d3021bc7585e6c95beeb`  
		Last Modified: Wed, 09 Jul 2025 19:08:58 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f6fe09584d835bca520875c7e47410f7b2b46281b0d462274ecaa74650b839`  
		Last Modified: Wed, 09 Jul 2025 19:09:04 GMT  
		Size: 61.3 MB (61252237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f174737cd3007f6f1ade2eb46d4715ca66406d2abcf852746bbf81c1aa5fd13`  
		Last Modified: Wed, 09 Jul 2025 19:09:05 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0001ffbcd261772b31cf3c11f9aa63508e3e284f11bba0761a331f71388b382c`  
		Last Modified: Wed, 09 Jul 2025 19:15:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9efdb8068d15242a0d8acd17296bc7c7dfdbe4c30ea6f8b0e9da297cf02bb26`  
		Last Modified: Wed, 09 Jul 2025 19:15:35 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639a964589cde2e8ae56a2449bd698e3a50b69e2d1a4ceddbe437aa177397142`  
		Last Modified: Wed, 09 Jul 2025 19:15:36 GMT  
		Size: 8.6 MB (8588079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca990ddb2dc6edf8c18f573bffc993ceadb9a65b2e704cb2769a49c9b02158f`  
		Last Modified: Wed, 09 Jul 2025 19:15:35 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
