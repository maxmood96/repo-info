## `openjdk:26-rc-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:4a4edbcaf70dc3e2d324fab694e83957c35d3787140e8a740d34b6175bf3b790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `openjdk:26-rc-windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull openjdk@sha256:d10c95e855e7bd2b8ffdf733c85a731633cf1fce0c2b44704dc33af77df4f275
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2189868723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f480a11a1539605103330ff728e152d25a85b52629ef94a74b076137dfb644a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 17 Feb 2026 19:27:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 17 Feb 2026 19:27:22 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 17 Feb 2026 19:27:23 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 17 Feb 2026 19:27:28 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 17 Feb 2026 19:27:30 GMT
ENV JAVA_VERSION=26
# Tue, 17 Feb 2026 19:27:31 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_windows-x64_bin.zip
# Tue, 17 Feb 2026 19:27:32 GMT
ENV JAVA_SHA256=2dd2d92c9374cd49a120fe9d916732840bf6bb9f0e0cc29794917a3c08b99c5f
# Tue, 17 Feb 2026 19:27:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 17 Feb 2026 19:27:56 GMT
CMD ["jshell"]
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
	-	`sha256:47376505e9774f463250f38092b0512796232df85683d4e85beeb9bfb4eb1563`  
		Last Modified: Tue, 17 Feb 2026 19:28:02 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f65ca361387030a79fd0a8b6bce97ba03d6f4c05eafab7bbb336b0cc8f197cd`  
		Last Modified: Tue, 17 Feb 2026 19:28:02 GMT  
		Size: 382.4 KB (382425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f37df38d1c234facf16f742605afd2f30ffe2a683d4898283cccdeba19d29dc`  
		Last Modified: Tue, 17 Feb 2026 19:28:01 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bfa8f7d43592689764184ffcd83a77fb281171ddf21b3fa3147fc780ac940`  
		Last Modified: Tue, 17 Feb 2026 19:28:02 GMT  
		Size: 369.8 KB (369776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ccc2b7ee6af9ace51cd113b2268bfe3b63e84c66f244b92eebd23e3a59a336`  
		Last Modified: Tue, 17 Feb 2026 19:28:00 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7fe7c082ad7376d584f2472f2216b7d29d4d0e7975bf43e3b3377a4c6b648a`  
		Last Modified: Tue, 17 Feb 2026 19:28:00 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a92c2ae67644019a80860909d27d1b6b36ea95012602a337bffe0743476587`  
		Last Modified: Tue, 17 Feb 2026 19:28:00 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea39550b2ccf4e35d8eeb73645076fcf88616c2268df9dde560dd64f27234f39`  
		Last Modified: Tue, 17 Feb 2026 19:28:14 GMT  
		Size: 224.3 MB (224348796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a580d0bbacc4c89dca72f78181ecff323b75ad3fc6ef08de0a4d115ec6e9f8dc`  
		Last Modified: Tue, 17 Feb 2026 19:28:00 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
