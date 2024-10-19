## `openjdk:24-ea-20-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:83ffe65e72b40d1fc2f4805d38779854f16f08636bb339a9110cb82cf58cc732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `openjdk:24-ea-20-jdk-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull openjdk@sha256:8ea442b197a52b82db43c78b99324ff1ac0524413c2d38f64bfcca57e742a992
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2008754799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63145827ab026662aef9b9ac4acf45e88ed8e08f4a5cda5f6682754f32e27ddd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Sat, 19 Oct 2024 01:03:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 19 Oct 2024 01:03:58 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 19 Oct 2024 01:03:59 GMT
ENV JAVA_HOME=C:\openjdk-24
# Sat, 19 Oct 2024 01:04:04 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 19 Oct 2024 01:04:05 GMT
ENV JAVA_VERSION=24-ea+20
# Sat, 19 Oct 2024 01:04:06 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/20/GPL/openjdk-24-ea+20_windows-x64_bin.zip
# Sat, 19 Oct 2024 01:04:07 GMT
ENV JAVA_SHA256=c2245e984dab93fa5690a08ea6c0470f006119857a9ab15c0a84cd55bb0687fd
# Sat, 19 Oct 2024 01:04:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 19 Oct 2024 01:04:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58644dcc05d4477f383ee52dd8384e729fb9d397a44901e53d35a9ae67b171c1`  
		Last Modified: Sat, 19 Oct 2024 01:04:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba704f47459e8387e4f208a6a43a355288b87b970445545c83eb9c1756ed70`  
		Last Modified: Sat, 19 Oct 2024 01:04:34 GMT  
		Size: 490.3 KB (490316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb98981c8327d0e886541b4fb2ad9fe7f3bc8a130dd0dae21767c2252d60c4d`  
		Last Modified: Sat, 19 Oct 2024 01:04:34 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3ee64247737dea3c623fd383f8a2fb6ba88db18fd2a22eacec32a0cee4ce81`  
		Last Modified: Sat, 19 Oct 2024 01:04:34 GMT  
		Size: 343.8 KB (343815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1faec35c6bdaa7c86715fe2c0c2e15aa4bc79fd25c3db4b5a22c909aed096e1b`  
		Last Modified: Sat, 19 Oct 2024 01:04:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5f5d77c4c249998f7ad10f54029327086426f414a437f3910d2590a8b3d37a`  
		Last Modified: Sat, 19 Oct 2024 01:04:32 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7868ba5dfac2c0a9c7c936990932541eb5116262022958a80ae84c2b77f2f08d`  
		Last Modified: Sat, 19 Oct 2024 01:04:32 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6938fe5016f43ad48bfc24dae03831e953aaaa6470ba96b5689a686c932231b4`  
		Last Modified: Sat, 19 Oct 2024 01:04:43 GMT  
		Size: 208.6 MB (208571386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0af3447475657eb9b84eccd4e2bec18d19b39594a246597cb5e4b406a2d497`  
		Last Modified: Sat, 19 Oct 2024 01:04:32 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-20-jdk-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull openjdk@sha256:475b82c44e43885f8e40ae857ed5cc1da3ef0f8aca2a9b210664bcc3bc17c165
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2111217437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5929498abfac09460980adcb11acd87d16b223afc15a382a9b7e3d1990687817`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Sat, 19 Oct 2024 00:56:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 19 Oct 2024 00:56:52 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 19 Oct 2024 00:56:53 GMT
ENV JAVA_HOME=C:\openjdk-24
# Sat, 19 Oct 2024 00:57:01 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 19 Oct 2024 00:57:02 GMT
ENV JAVA_VERSION=24-ea+20
# Sat, 19 Oct 2024 00:57:02 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/20/GPL/openjdk-24-ea+20_windows-x64_bin.zip
# Sat, 19 Oct 2024 00:57:03 GMT
ENV JAVA_SHA256=c2245e984dab93fa5690a08ea6c0470f006119857a9ab15c0a84cd55bb0687fd
# Sat, 19 Oct 2024 00:57:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 19 Oct 2024 00:57:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b9159860d285b1633cd4006a35d0dd03c64804025e81e4d4f4719641317bb6`  
		Last Modified: Sat, 19 Oct 2024 00:57:37 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a68334851dd5d9f9e9aa921aa3f40c760c2e6f05724e88ad981127c35604ea9`  
		Last Modified: Sat, 19 Oct 2024 00:57:37 GMT  
		Size: 484.5 KB (484540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1afa13cddb942854be940a1575fad319d33038b009e164bf0d5cfdeb8f61901`  
		Last Modified: Sat, 19 Oct 2024 00:57:37 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef11f8ffbf0f12e414ad983b6e670ff8fc0758dfa5c24ca418cdb76d21cf6fe`  
		Last Modified: Sat, 19 Oct 2024 00:57:37 GMT  
		Size: 328.0 KB (327976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b1f009909ee60f633128c0117b86e876a77cdf37e3d7d0ff9731b21400bc0b`  
		Last Modified: Sat, 19 Oct 2024 00:57:35 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f133e9ac46c00ab4e25fbd1315acc529d73940ca3fa2392c6da7ed13e674d6`  
		Last Modified: Sat, 19 Oct 2024 00:57:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e55c0a1858c0301f7bb583279152184249239ba69577ccfe4005acd9d490e0c`  
		Last Modified: Sat, 19 Oct 2024 00:57:35 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae39bd4423d94ffb995a0b70a0682d6d43c5400bc38e0fc8653fc7e9badeef5`  
		Last Modified: Sat, 19 Oct 2024 00:57:45 GMT  
		Size: 208.6 MB (208571878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30a9f09076316468ff6675dbebe899772ceb4b4e6701340107fb1c3f8a7c82c`  
		Last Modified: Sat, 19 Oct 2024 00:57:35 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
