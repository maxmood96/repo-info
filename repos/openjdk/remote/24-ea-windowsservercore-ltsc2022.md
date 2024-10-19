## `openjdk:24-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:c0a335948acc8f91d20756d3732427141967f1caa71431d755c0e5bd576aa3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `openjdk:24-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

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
