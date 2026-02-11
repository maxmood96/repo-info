## `hylang:1-python3.13-windowsservercore`

```console
$ docker pull hylang@sha256:e892bc23640470f4b43d8df51f30fa742dc8870ec39e4b206b6c1b7a2e7cb057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `hylang:1-python3.13-windowsservercore` - windows version 10.0.26100.32370; amd64

```console
$ docker pull hylang@sha256:2cc67be69ef9c7e89ab33a11278e8d2c1309a6936213d0b72fc2d8034e017cf6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2032684420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c75a35b5a956df4217e1f71990dab7b36a18445c755bfdea173678ff4d229e`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:52:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 23:00:51 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 10 Feb 2026 23:00:51 GMT
ENV PYTHON_VERSION=3.13.12
# Tue, 10 Feb 2026 23:00:52 GMT
ENV PYTHON_SHA256=96159fcb523ae404b707186a75b4104ee23851e476a5e838e14584cf1e03f981
# Tue, 10 Feb 2026 23:01:33 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 10 Feb 2026 23:01:34 GMT
CMD ["python"]
# Tue, 10 Feb 2026 23:39:03 GMT
ENV HY_VERSION=1.2.0
# Tue, 10 Feb 2026 23:39:03 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 10 Feb 2026 23:39:31 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 10 Feb 2026 23:39:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c98dbe9f1f0558e249573b12845ab1eecd63a28b82c4d7dd0c89342195382d`  
		Last Modified: Tue, 10 Feb 2026 22:53:53 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19adb6c218ad01c348ecf5040b869a039fbb9ffb206b02a9e3ab16a30b7e6cb3`  
		Last Modified: Tue, 10 Feb 2026 23:01:38 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a99515b9d6552abb4f60548ac11c295ee3c95a30234f0f21e1f1b10f46fddb1`  
		Last Modified: Tue, 10 Feb 2026 23:01:38 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc53ef9b1ea23d3de468d7cc3ffa650a4f8fd8853015fad914116feb3bdac062`  
		Last Modified: Tue, 10 Feb 2026 23:01:38 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c88d3f41cc8aef04ce6bb181f9cb3d157761f4f4b0dbff67ffbea33d4798aa`  
		Last Modified: Tue, 10 Feb 2026 23:01:43 GMT  
		Size: 59.3 MB (59273000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0928ca5f850f0db4bb917b7c0a025f8856ccc03b3dff47b59608715f8d7be5`  
		Last Modified: Tue, 10 Feb 2026 23:01:38 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6728d47d330d676ff93691f6af7d6ce7b11f2ff93913c787f00500c19d033cf`  
		Last Modified: Tue, 10 Feb 2026 23:39:36 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f4aff4b0b87cc3a83274919f1a80650272f1e2e81bea3e69d0a1bffac7915b`  
		Last Modified: Tue, 10 Feb 2026 23:39:36 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe10f30b4700a73bb1ff62ef33ab8fe7e79cb93c2dce991187b24ba156049743`  
		Last Modified: Tue, 10 Feb 2026 23:39:37 GMT  
		Size: 8.6 MB (8641021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b037ddede9ca6264953e9815b350d50dad90a5870c0d5cb174469e0569fa3b6`  
		Last Modified: Tue, 10 Feb 2026 23:39:36 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
