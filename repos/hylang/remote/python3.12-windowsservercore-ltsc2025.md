## `hylang:python3.12-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:9ed782ce1879408a0e7b9328e8f505fff19b0f92551223facb3f499ba255cdc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `hylang:python3.12-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull hylang@sha256:62f6af6668a88694f60eca51672cf5925bf9b537109e6175e1b289753d20345f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2568850701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2aa999614d641c05039f9a7db3f15247ea317d5d4ff5ce48ad55ba80bf407f`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 06 Feb 2025 22:31:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 Feb 2025 22:31:04 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 06 Feb 2025 22:31:05 GMT
ENV PYTHON_VERSION=3.12.9
# Thu, 06 Feb 2025 22:31:06 GMT
ENV PYTHON_SHA256=2a52993092a19cfdffe126e2eeac46a4265e25705614546604ad44988e040c0f
# Thu, 06 Feb 2025 22:31:44 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 06 Feb 2025 22:31:45 GMT
CMD ["python"]
# Thu, 06 Feb 2025 23:30:29 GMT
ENV HY_VERSION=1.0.0
# Thu, 06 Feb 2025 23:30:29 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 06 Feb 2025 23:31:03 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 06 Feb 2025 23:31:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44086744a54cab3c06d35a081f70d5a8f9fc9bfd1d71913c910751a4e5d21f0`  
		Last Modified: Thu, 06 Feb 2025 22:31:51 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4c587373522fda9fdb0cfb7b0aa2891f92b03938ed6d795cbd3ebecfee2947`  
		Last Modified: Thu, 06 Feb 2025 22:31:49 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec17189e14b0a31adf44d017472339557fbef03484068b49db6132a656c5c13`  
		Last Modified: Thu, 06 Feb 2025 22:31:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6750c5ec3e419f17d0bb0de4f7d59b2cab9845e08b56e43b595bca29954c40`  
		Last Modified: Thu, 06 Feb 2025 22:31:49 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37b185802c43c46fde8fc062f76b5811e6c918190f788c4796eb4c974134972`  
		Last Modified: Thu, 06 Feb 2025 22:31:54 GMT  
		Size: 60.0 MB (60021653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefc2df2fdfb97bfc6f53c4665c8eccffc107006f8d41299a5c7c564bac6bd3f`  
		Last Modified: Thu, 06 Feb 2025 22:31:49 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2ee26a218aa2922455a7859ede4de2594438ec62b29814546192ad00fb889d`  
		Last Modified: Thu, 06 Feb 2025 23:31:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cd5224c1ec1b9dcb723b5d5e0b6258cd0db66f5f74acf3f982b5b017ba4e3c`  
		Last Modified: Thu, 06 Feb 2025 23:31:08 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00c174fcb801c1904444fc6c514c4e757750a0a20428e0704078516386b4d15`  
		Last Modified: Thu, 06 Feb 2025 23:31:09 GMT  
		Size: 8.5 MB (8541055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b516b38eb7b6415ccd300a3ef9b46d81b63566f29685547fb0040c969877c65`  
		Last Modified: Thu, 06 Feb 2025 23:31:08 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
