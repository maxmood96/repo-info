## `hylang:1-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:26f9e6e973e618d430a1da5417ca045780c7dade00d2eea7f00465ef03d25171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `hylang:1-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull hylang@sha256:2d1d85146e5d249356b8d396e64d66030a4d94a3169f558005aaba013677066e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1839372961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f111b81b5214487c839937e978c1976aba74e81cf4fa6f16edd6f2e7d0a2a11`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Wed, 03 Dec 2025 01:05:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 01:05:27 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 03 Dec 2025 01:05:28 GMT
ENV PYTHON_VERSION=3.14.1
# Wed, 03 Dec 2025 01:05:30 GMT
ENV PYTHON_SHA256=74e1516408744190fcc12307c150de30902898444f77f85f4c2ac18f36788a80
# Wed, 03 Dec 2025 01:06:39 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 03 Dec 2025 01:06:40 GMT
CMD ["python"]
# Wed, 03 Dec 2025 02:10:17 GMT
ENV HY_VERSION=1.1.0
# Wed, 03 Dec 2025 02:10:18 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 03 Dec 2025 02:11:10 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 03 Dec 2025 02:11:11 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27be210d6833cdc827bfc15972f5d728f0d871b50e3aa17e152f86594cb31ba`  
		Last Modified: Wed, 03 Dec 2025 01:12:24 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14fddf0b287656bd22c11db1941d0dac9b8298027d4deeb2f20f0c2fc07c4bd`  
		Last Modified: Wed, 03 Dec 2025 01:12:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735d45cf80e1838869461b613b84034ebde2378b5dde4341d8c26e4e2e327500`  
		Last Modified: Wed, 03 Dec 2025 01:12:37 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f5801afbbb07dc121162a03ec40e37be0764f8fcd90a307293e563c5982cb7`  
		Last Modified: Wed, 03 Dec 2025 01:12:24 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638d982268f0601a8853f4a723db335bdade0cf5f3b69e75f7b3b848c63eedec`  
		Last Modified: Wed, 03 Dec 2025 01:12:29 GMT  
		Size: 60.9 MB (60945374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcdb429ddbeeaadd3b01bc240bdafbd232bbc3b52821c1e897c9b07dfd6af5f`  
		Last Modified: Wed, 03 Dec 2025 01:12:24 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447f63a8f616de6f7f24ceb502eb089b53f6e7cae0e3d6d434948084c590890f`  
		Last Modified: Wed, 03 Dec 2025 02:11:24 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dfd2756efd198cc14fb8a36a3248c5b3bf161598bf6d30701ffdfb4491dbe7b`  
		Last Modified: Wed, 03 Dec 2025 02:11:25 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139dc52e0c09ba6ff8db0a8d02adbf47eb85d813f57cfe60ee9117ba23fb71bc`  
		Last Modified: Wed, 03 Dec 2025 02:11:26 GMT  
		Size: 8.5 MB (8455599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13793799c4a26c04c919badfae48558e61d25c86c0f86bde64c564360fadfb1b`  
		Last Modified: Wed, 03 Dec 2025 02:11:25 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
