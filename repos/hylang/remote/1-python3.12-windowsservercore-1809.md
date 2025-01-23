## `hylang:1-python3.12-windowsservercore-1809`

```console
$ docker pull hylang@sha256:4a384af01a24c2eb92b1ce811a6f6b3daed77809544ebb16a5c57a8539c7b10d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `hylang:1-python3.12-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull hylang@sha256:b480e37ce77ac220acb95772a936579fb6d91c71e34ea712283852197f77ed66
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2188002401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f017e4f3795ce6aa5ba987f5cb95e39ced34ed333df8a645c8869284e097fa7`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:44:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:44:41 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 14 Jan 2025 23:44:41 GMT
ENV PYTHON_VERSION=3.12.8
# Tue, 14 Jan 2025 23:44:42 GMT
ENV PYTHON_SHA256=71bd44e6b0e91c17558963557e4cdb80b483de9b0a0a9717f06cf896f95ab598
# Tue, 14 Jan 2025 23:46:16 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:46:17 GMT
CMD ["python"]
# Thu, 23 Jan 2025 01:35:44 GMT
ENV HY_VERSION=1.0.0
# Thu, 23 Jan 2025 01:35:46 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 23 Jan 2025 01:37:08 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 23 Jan 2025 01:37:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d3b60de29b49b64e938dbec1880daf93969744a5d1c4e727ac53e074244964`  
		Last Modified: Tue, 14 Jan 2025 23:46:20 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ceaf8cea4259c9e9d13b89505bba92c7b4c9c35f1b1ea7605b5664b2aaec26`  
		Last Modified: Tue, 14 Jan 2025 23:46:19 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6edc1baaf49f9e279da4990b1cf8004a6e76e8feee167d4c82014d6cb98340`  
		Last Modified: Tue, 14 Jan 2025 23:46:19 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df902afd93697457e0e83522da018f080c4c2b3b602f274e774f858b33865f`  
		Last Modified: Tue, 14 Jan 2025 23:46:19 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50aef5554b9b09b4cc89d774a4e1bfc682b00eb9dda8aa3313d1d200265f385d`  
		Last Modified: Tue, 14 Jan 2025 23:46:24 GMT  
		Size: 58.6 MB (58644908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d821c53c7351f1f18132c3f65b583beb7664ab85c6f6b12e63d9461e69c6bf`  
		Last Modified: Tue, 14 Jan 2025 23:46:19 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e298c3307c7b95791516e03243e655f1be64425a4bd331beb8ad36b3ff2d29a2`  
		Last Modified: Thu, 23 Jan 2025 01:37:11 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa89492a2ce4c78647527d2ed71ea31dca969aaff82f2e64a5a932b4df2b0ad`  
		Last Modified: Thu, 23 Jan 2025 01:37:11 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe835a20f9d3397f4abed86b97bad229c347c16a8bcece6e3da186088c0cf4c`  
		Last Modified: Thu, 23 Jan 2025 01:37:12 GMT  
		Size: 7.1 MB (7134605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2670cea12c8476e15619d41b6a4c414728d2965c21d869e6c6515a3a58174576`  
		Last Modified: Thu, 23 Jan 2025 01:37:11 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
