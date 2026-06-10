## `hylang:python3.14-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:b1f253f2cfef42f53ebf1ac306e5be61ba272b67f4be789cbe73461cf71de95f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `hylang:python3.14-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull hylang@sha256:c00e933ada2c8022c46f1351a52a9ae8a33755885c9949c7c612728dbb0d008a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2203003271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ce3414e6879e7d80384558ef626cb4ec80ed995a4b01ce47d6ddf99a55b656`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Wed, 10 Jun 2026 20:37:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jun 2026 20:37:28 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 10 Jun 2026 20:37:29 GMT
ENV PYTHON_VERSION=3.14.6
# Wed, 10 Jun 2026 20:37:29 GMT
ENV PYTHON_SHA256=14b3e9a710a3fcf0bd9b55ab6b60412bd91227563f813fc49040cabc0209e0bd
# Wed, 10 Jun 2026 20:38:22 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 10 Jun 2026 20:38:22 GMT
CMD ["python"]
# Wed, 10 Jun 2026 20:41:30 GMT
ENV HY_VERSION=1.3.0
# Wed, 10 Jun 2026 20:41:31 GMT
ENV HYRULE_VERSION=1.1.0
# Wed, 10 Jun 2026 20:42:00 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 10 Jun 2026 20:42:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efdeb7b9257507127f091d76dedd48b4e9315c618931c7843fe791444fef5e2`  
		Last Modified: Wed, 10 Jun 2026 20:38:29 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbef0a9ed23b87025e4bcaa41890235aa60e301f69c19c22582258ac5cb619dd`  
		Last Modified: Wed, 10 Jun 2026 20:38:27 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9afac6236488dffd5eb3bd308bd6036968c8c074899c92120bef7921084b6bc7`  
		Last Modified: Wed, 10 Jun 2026 20:38:27 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ee807f1d9fd2ce4482fd975e84e54c1902301af2eb573cfc2012a1415177bb`  
		Last Modified: Wed, 10 Jun 2026 20:38:28 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def964152d8d19e60c468d2e475afb609fbf2652ed2a16ab3c224396effc6ea7`  
		Last Modified: Wed, 10 Jun 2026 20:38:34 GMT  
		Size: 62.6 MB (62587974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d08759384096f4909eaec98732c51c4cc9e2e86f98a0dab1b6b51c5d70f0652`  
		Last Modified: Wed, 10 Jun 2026 20:38:27 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d24524b000bfdd859bacf5def87afeb4eb33bd0d90e1d2f3238dee17ec5c1ec5`  
		Last Modified: Wed, 10 Jun 2026 20:42:05 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358dcf95399fdfef3b7db3aa2b1a1b78d0d0927a788a4d50a23ed123674e767c`  
		Last Modified: Wed, 10 Jun 2026 20:42:05 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e739c2f9dbca3b754e6e2e16bcfa3efd438fbecde198ba3e2cffafaa032832ea`  
		Last Modified: Wed, 10 Jun 2026 20:42:06 GMT  
		Size: 8.3 MB (8279223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54184a88082c5bad85c2b7e644377e5e347e5ef024917b3d856b24b22ad1f8df`  
		Last Modified: Wed, 10 Jun 2026 20:42:05 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
