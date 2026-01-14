## `hylang:windowsservercore`

```console
$ docker pull hylang@sha256:bbd3358d909f01d66b625eac095ec5542b5004b8d2abc9c3f354e8de1793a1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `hylang:windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull hylang@sha256:05617f239933515c17087ddc91c8a56ffb1b021af2faac5139562bea276bc2dc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1565256279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964680701eadf32513310c6b2a4f6869729cb9ee8ba4568ca81e14c0979b85f6`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:53:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 22:53:11 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 13 Jan 2026 22:53:12 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 13 Jan 2026 22:53:13 GMT
ENV PYTHON_SHA256=9db919cefe30a0051658c600a9912acb0cd2b872aaf35842c9ec2bf401efa848
# Tue, 13 Jan 2026 22:54:02 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 22:54:03 GMT
CMD ["python"]
# Tue, 13 Jan 2026 23:42:31 GMT
ENV HY_VERSION=1.1.0
# Tue, 13 Jan 2026 23:42:32 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 13 Jan 2026 23:43:06 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 13 Jan 2026 23:43:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:56:33 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4c348082658f8a5ab278a6856dfa04fa2a0bb282804f2a57c36436a6688e78`  
		Last Modified: Tue, 13 Jan 2026 22:58:08 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7406e948e74291cdc5905b66f33026f1ad4de3e9480650c627fc1f6b4d2497`  
		Last Modified: Tue, 13 Jan 2026 22:58:01 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a9bbd5a9a7ccac63082093a7ec5833b388af4dd276a46a5a9fc4b83c1fa23`  
		Last Modified: Tue, 13 Jan 2026 22:58:00 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b5338ec1f2fb294bb5ab6f8422587814fd49b59f1e971d96595182b03f163b`  
		Last Modified: Tue, 13 Jan 2026 22:58:01 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09b3ced76e049cd23a977f60ab2e553df2cf0030ca556474076910ea1c68e6c`  
		Last Modified: Tue, 13 Jan 2026 22:58:09 GMT  
		Size: 60.9 MB (60921665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cf9876fd6e51157ded13cccea948367966f638ef559198342a82406ad08702`  
		Last Modified: Tue, 13 Jan 2026 22:58:00 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec8695e27431e4533690e65449917e76eef6a28bb3a2394b5d36691e86a45cf`  
		Last Modified: Tue, 13 Jan 2026 23:43:19 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6884510002d3a58ab7c031b1df6822b666554ae9eb8bf0762e4a425e508c266`  
		Last Modified: Tue, 13 Jan 2026 23:43:19 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50339854aa6fc9269d2955763c47431d346a19e12651d3d36f1d40fd6e18dfac`  
		Last Modified: Tue, 13 Jan 2026 23:43:20 GMT  
		Size: 8.6 MB (8563777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9192f698f47e2cbcffe8b55b74b3a461e83636aa1e8965443fef72f6014f404e`  
		Last Modified: Tue, 13 Jan 2026 23:43:19 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull hylang@sha256:9925633ea5154f70f4b115922a4e167e00ea6d5376cbd3a10780a8c5f0c0f69c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1905065578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267a46090fc57caedd14f165a9321e8c55f3747271c436eb7b411854182e52b0`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 22:53:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 22:53:32 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 13 Jan 2026 23:12:32 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 13 Jan 2026 23:12:32 GMT
ENV PYTHON_SHA256=9db919cefe30a0051658c600a9912acb0cd2b872aaf35842c9ec2bf401efa848
# Tue, 13 Jan 2026 23:13:20 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:13:21 GMT
CMD ["python"]
# Tue, 13 Jan 2026 23:39:34 GMT
ENV HY_VERSION=1.1.0
# Tue, 13 Jan 2026 23:39:34 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 13 Jan 2026 23:40:04 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 13 Jan 2026 23:40:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:28:58 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b66bcc5dc6d3aaa7c66e1e850b7913643ad68c20c1b5e2f0a0f33bc0b2abc19`  
		Last Modified: Tue, 13 Jan 2026 23:01:21 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4c7a2c73fbb702a7634e591a8deffb401988837f04b065770a17cdd6eb5f57`  
		Last Modified: Tue, 13 Jan 2026 23:01:21 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5de4e88f071073922fa3cadd4835f4e12a9bd94e18c7f841ec7a724a73a9f5e`  
		Last Modified: Tue, 13 Jan 2026 23:13:40 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38dd83fa0cf30718e5b9fae5a8ceadc74aa91fa7a9f56f3b292752aa90010f14`  
		Last Modified: Tue, 13 Jan 2026 23:13:40 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b46e72ea394959370b557dc126eed00cf920910d311268c79281f18b6d6f557`  
		Last Modified: Tue, 13 Jan 2026 23:13:47 GMT  
		Size: 60.9 MB (60945328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4efc477f332b9523229810f82131c13b8aea792db5a920bf731cb4e0ed0f952`  
		Last Modified: Tue, 13 Jan 2026 23:13:40 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80eb82eabbb91b3aa659873bcff182ba67056df793e15fbaa672d2f8e877db14`  
		Last Modified: Tue, 13 Jan 2026 23:40:16 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3fa33341e46d255b9f1889bdd0687d51538b3d37ca15c50cb29015fa1b0856`  
		Last Modified: Tue, 13 Jan 2026 23:40:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6213528db312da9d30a94078142e2ce1c259ed29f6c2e5e3c373a9e21b30ddb8`  
		Last Modified: Tue, 13 Jan 2026 23:40:17 GMT  
		Size: 8.5 MB (8450526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50121d9d2a72dc5896dbb24b947775acc7ffbc82c7ae58a7058d32a972c3e123`  
		Last Modified: Tue, 13 Jan 2026 23:40:16 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
