## `hylang:python3.12-windowsservercore-1809`

```console
$ docker pull hylang@sha256:4e099bccd384f5cb1f083215a599471400fba3528f8bc3d35aaf0e2918f04531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `hylang:python3.12-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull hylang@sha256:96911e243be3e8d22142a25662863cbe6d15dbd041909928f0e62b135c01a8cf
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2202676061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139af4b04f3fcbd8d07359a006459e998ed9c188c1a0de06c66d41cc22e4867d`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:39:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:39:27 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 13 Feb 2025 00:39:28 GMT
ENV PYTHON_VERSION=3.12.9
# Thu, 13 Feb 2025 00:39:29 GMT
ENV PYTHON_SHA256=2a52993092a19cfdffe126e2eeac46a4265e25705614546604ad44988e040c0f
# Thu, 13 Feb 2025 00:40:31 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:40:32 GMT
CMD ["python"]
# Thu, 13 Feb 2025 01:16:48 GMT
ENV HY_VERSION=1.0.0
# Thu, 13 Feb 2025 01:16:49 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 13 Feb 2025 01:17:58 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 13 Feb 2025 01:17:59 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076d36cea493506eaa213b58874b996f6b2343cf1c3fb797d1f0d3aaf9c3c193`  
		Last Modified: Thu, 13 Feb 2025 00:40:36 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f2174d7c238935ac7a2ff43515c53b761c79c8718e8508cd33c920c364e465`  
		Last Modified: Thu, 13 Feb 2025 00:40:35 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25b6b0f3f122cb38e08184f567baa2b3caf3dcb72d39c1e271281e019c6c09f`  
		Last Modified: Thu, 13 Feb 2025 00:40:35 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a32bca3f311e2aab471466c217089697529c04e1225c9261b7d9888b2a228e`  
		Last Modified: Thu, 13 Feb 2025 00:40:35 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420e5f3ea586db58038950218b42c5fd8b49b06b40537c121c3fd87b59da8c9a`  
		Last Modified: Thu, 13 Feb 2025 00:40:40 GMT  
		Size: 58.6 MB (58627806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88db513b5afb552cf2a0b82720b8f2108b47d7bab82c6eb076c08d785190866e`  
		Last Modified: Thu, 13 Feb 2025 00:40:35 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73049ab606638cb3a67a4a147623385cc1c08cc51739bd3b68836f49e13856d2`  
		Last Modified: Thu, 13 Feb 2025 01:18:02 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12f5f5e16469643a15e4769357214abf37b01f30aba81e8280216c7b026d0ad`  
		Last Modified: Thu, 13 Feb 2025 01:18:02 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d9e79bcbb634c6752d5052036cdbb172cdcea0fcbf813bec8f5fde9b67bab3`  
		Last Modified: Thu, 13 Feb 2025 01:18:03 GMT  
		Size: 7.1 MB (7128884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4d7990e542f514821037a72571f8a66599e7e5760f122f7ecac1f093f37f2d`  
		Last Modified: Thu, 13 Feb 2025 01:18:02 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
