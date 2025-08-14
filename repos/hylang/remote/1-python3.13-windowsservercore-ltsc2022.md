## `hylang:1-python3.13-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:d067b83260b60baf0ba7efdb9ff1631553172658320a3d9d667b9a5d1a90c31b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `hylang:1-python3.13-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull hylang@sha256:005e2e3c1cf6a9aede9849c16c52f0dc751333805cfbe18760dfd644a40f4826
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348773478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913e3124b16a9b825a50abd0b688e63d8bcb077dd0ce307eaafb53c39ded2310`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:35:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:35:34 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 12 Aug 2025 20:35:35 GMT
ENV PYTHON_VERSION=3.13.6
# Tue, 12 Aug 2025 20:35:36 GMT
ENV PYTHON_SHA256=5edce6f0597a9b250c72790dc076649b06c1dc4754f3c68d7c284a1f10c33f36
# Tue, 12 Aug 2025 20:36:22 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:36:23 GMT
CMD ["python"]
# Wed, 13 Aug 2025 21:23:54 GMT
ENV HY_VERSION=1.1.0
# Wed, 13 Aug 2025 21:23:55 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 13 Aug 2025 21:24:27 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 13 Aug 2025 21:24:28 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa7f9525e97f7d2a3c9a29045c1d1ab724b1af6b18f662e26f86e3889f8ee2e`  
		Last Modified: Tue, 12 Aug 2025 20:37:50 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6793d162379082f44e69d9f658be63c3cbabcbb18ce0e566ef587fe3368d9d5c`  
		Last Modified: Tue, 12 Aug 2025 20:37:51 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40da388cd57f137fdb0c437a43c976bc2e872d24b653d805a773b26f06f95cb1`  
		Last Modified: Tue, 12 Aug 2025 20:37:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d2423ab72b055e64a1475ac8f61984647f912e8664ccb9a99adb5185a8fa77`  
		Last Modified: Tue, 12 Aug 2025 20:37:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e7b6f568b83b94c098114042757bd77ab3a15cb19bba2f1112d4a5f774bb8e`  
		Last Modified: Tue, 12 Aug 2025 20:37:58 GMT  
		Size: 58.6 MB (58594538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa07893126836d480560f77652230045864b6363894e658cea532abac50aace`  
		Last Modified: Tue, 12 Aug 2025 20:37:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700bf80acf321aa3986a6b1c4fb4ebd0bae1459d30206129d532fc267643ee23`  
		Last Modified: Wed, 13 Aug 2025 21:25:08 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db5b881a83435a1e46cb7aa7ceae7bc8ae15b93dc977c6946b0698ea851f3c2`  
		Last Modified: Wed, 13 Aug 2025 21:25:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0001613f3fd81079dd6562b2fae2c4434d7d4eb63e0693f26bc3c34b32a6cb1`  
		Last Modified: Wed, 13 Aug 2025 21:25:10 GMT  
		Size: 8.5 MB (8476687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ec3344d1f4681b6c2ecc65f30214364cfb063a08c21bcaf90d3e594efead6a`  
		Last Modified: Wed, 13 Aug 2025 21:25:09 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
