## `hylang:python3.14-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:fb4dc937b2c98a74a8a904696e2581533473a6528ca59b5d1b8f199a97d151f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `hylang:python3.14-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull hylang@sha256:b632eea196d48a8f09a6f31f9f841ce8d172310aa43eca3fbd014257ff1ad820
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1904972507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d7ef2106b301a3ae7e39bc1aaa0651b9caa56e3024e13bbd1f5732caf2890c`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 04 Feb 2026 20:05:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Feb 2026 20:05:10 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 04 Feb 2026 20:05:11 GMT
ENV PYTHON_VERSION=3.14.3
# Wed, 04 Feb 2026 20:05:11 GMT
ENV PYTHON_SHA256=b68ad91421afbbd1a628105199c8c5f6179b21ba799067a8d8c0bbac3b7defb0
# Wed, 04 Feb 2026 20:06:26 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 04 Feb 2026 20:06:27 GMT
CMD ["python"]
# Wed, 04 Feb 2026 21:04:48 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:04:49 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:05:42 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 04 Feb 2026 21:05:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09f561cc9817aa5a71306c1f7a3185d4427e4552b15b4a465e8b8457f965985`  
		Last Modified: Wed, 04 Feb 2026 20:06:33 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b8630af6c7b0ce1ea7c3a422843d98abcf56718529bc1a38039030b1094970`  
		Last Modified: Wed, 04 Feb 2026 20:06:31 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61254da76d58722ea606dcd714f15cdda3970369a24ebcca39717a9b5271070f`  
		Last Modified: Wed, 04 Feb 2026 20:06:31 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488858954fff995194657bb21432bb2e74ff0df05281e0d0c4b5d216e58476a6`  
		Last Modified: Wed, 04 Feb 2026 20:06:31 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e61b1ffea45b48b500468ef3f2eb69c7916092e68e23c4b8da9b1b861987639`  
		Last Modified: Wed, 04 Feb 2026 20:06:38 GMT  
		Size: 61.0 MB (60986898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429d69ee6c51152cf5cbe1f70b18db0873456e6e061b94185d48b11822a2a828`  
		Last Modified: Wed, 04 Feb 2026 20:06:31 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f2e9de1f2e4a2950fbecc06c2a1819326013dec0052bdfc79517b8f63d58e4`  
		Last Modified: Wed, 04 Feb 2026 21:05:48 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e121dea64c36749cfd98837dfa3cac723b4e729022cb1e338c60731c255a55c3`  
		Last Modified: Wed, 04 Feb 2026 21:05:48 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f9376a7400e45e8de74d0ed4b1982bb85455aa7b2f8b43be8db854e39ff95b`  
		Last Modified: Wed, 04 Feb 2026 21:05:49 GMT  
		Size: 8.3 MB (8315880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed4ff949b8bdd427ccd7964abec9673c1374041b9c34ebfad9f02bb348d3b8c`  
		Last Modified: Wed, 04 Feb 2026 21:05:48 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
