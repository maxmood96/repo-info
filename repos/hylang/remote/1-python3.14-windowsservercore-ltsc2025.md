## `hylang:1-python3.14-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:e6fd6d5c7b120255c63cc79de8dada69fb6bab82d7388b9c9f4e611ff9471d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `hylang:1-python3.14-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull hylang@sha256:53c794831f1935a24a3189ea90e58ba217cd39908da5b78f40923f4bf448c07d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3304851284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8db909c24b94aa5c45b27339720c2d8fae14c07bbd2f3a9e605fa48d99bbb0`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Mon, 08 Dec 2025 20:10:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 08 Dec 2025 20:10:35 GMT
ENV PYTHONIOENCODING=UTF-8
# Mon, 08 Dec 2025 20:10:36 GMT
ENV PYTHON_VERSION=3.14.2
# Mon, 08 Dec 2025 20:10:37 GMT
ENV PYTHON_SHA256=9db919cefe30a0051658c600a9912acb0cd2b872aaf35842c9ec2bf401efa848
# Mon, 08 Dec 2025 20:12:29 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Mon, 08 Dec 2025 20:12:29 GMT
CMD ["python"]
# Mon, 08 Dec 2025 21:12:56 GMT
ENV HY_VERSION=1.1.0
# Mon, 08 Dec 2025 21:12:57 GMT
ENV HYRULE_VERSION=1.0.1
# Mon, 08 Dec 2025 21:13:41 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Mon, 08 Dec 2025 21:13:41 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb84e1f28d34adc94a68681490a6a32c77b70d09eb548ee0a0f5aa4f8ad439d`  
		Last Modified: Mon, 08 Dec 2025 20:29:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2dceb91a25e3c36ec2f9ed3e169d502dfacda739d5addd6538fa3ebdab1715`  
		Last Modified: Mon, 08 Dec 2025 20:29:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39276ab0f8de5a7106d2c9acd4c4738b3d9eebde3ffede18721bf3f512c5d256`  
		Last Modified: Mon, 08 Dec 2025 20:29:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d674b24e3bc89cb302e130e25c75ed29942e2c4025d7dea5f136ffbb713711`  
		Last Modified: Mon, 08 Dec 2025 20:29:16 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5582356be3c38b8f90b73689f3a15536a77894068f78b39d986ef7209b18c3e`  
		Last Modified: Mon, 08 Dec 2025 20:29:24 GMT  
		Size: 60.9 MB (60883023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7999c5b06f3add40b6211a52a3be5843b29d422a7101a4c7d5297c1855b4aed8`  
		Last Modified: Mon, 08 Dec 2025 20:29:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be1189d23652a845d65f201b95e63428b3c5cabaeae1cfbd0129654c4bda8f9`  
		Last Modified: Mon, 08 Dec 2025 21:13:56 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698ff7f5f2bb06155302dd77544cf4b60dd63f1d47cf9adeef7aea8498ea9bd6`  
		Last Modified: Mon, 08 Dec 2025 21:13:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12687410233d01960585f13416765228a95fad0325b07adf57f8377e4dcad1f`  
		Last Modified: Mon, 08 Dec 2025 21:13:57 GMT  
		Size: 8.5 MB (8502071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d25eaf7c86033bd93cc4913306595aa1cc8d56d21e5bde0e7f6caae74431c4`  
		Last Modified: Mon, 08 Dec 2025 21:13:56 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
