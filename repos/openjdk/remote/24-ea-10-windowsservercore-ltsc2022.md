## `openjdk:24-ea-10-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:6c4a7c282d6d96ca5cccfed2ce7fc43f01e50b2c2efe09dec403a88c9a9c5227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `openjdk:24-ea-10-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull openjdk@sha256:c606b92c81bf9e58e6863e66707ac9c33ef61c553fc8ff4ea6b93202e53c0a04
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2347170372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0a59243d817a566228f817eda46b4e6f639a5c8a5ddabe46e9de8bce49501f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Mon, 12 Aug 2024 17:58:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Aug 2024 18:00:06 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 12 Aug 2024 18:00:07 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 12 Aug 2024 18:00:14 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 12 Aug 2024 18:00:14 GMT
ENV JAVA_VERSION=24-ea+10
# Mon, 12 Aug 2024 18:00:15 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_windows-x64_bin.zip
# Mon, 12 Aug 2024 18:00:16 GMT
ENV JAVA_SHA256=a4e5b50291add1d88baf1093f1a4822dc3ee939111b1e039214cd2fcd729dc27
# Mon, 12 Aug 2024 18:00:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 12 Aug 2024 18:00:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c37a2c5e07cab9f75cbf47651d57ebb9db25b70d41b8ec35328f548b3210251`  
		Last Modified: Mon, 12 Aug 2024 18:00:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08f91541d43d3e00537b092cb2f704e84c98c18284ee693825f5124461d14ed`  
		Last Modified: Mon, 12 Aug 2024 18:00:48 GMT  
		Size: 360.8 KB (360758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8088bcdbebb8d8c7bc2d60a37b9cd815cec3ebe91783e4a9ee55661ca057b9c0`  
		Last Modified: Mon, 12 Aug 2024 18:00:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96660497eb5877e6409760fabc06b6c0486c9ef3dd79b9e582a29732ab7c6f4d`  
		Last Modified: Mon, 12 Aug 2024 18:00:48 GMT  
		Size: 311.5 KB (311493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac244e0a02348b0ec2313fbbae3a1fc700d9f19955b8806fd153418bedc7ff12`  
		Last Modified: Mon, 12 Aug 2024 18:00:47 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d45e168f8ba4657e293828c90a6e5cad294c9f665ef2bf5375d9304805d8cd`  
		Last Modified: Mon, 12 Aug 2024 18:00:47 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2b66c8e81cf9bdda87a0ef931c92441dc798de39dff6e7bd40b48720fb8633`  
		Last Modified: Mon, 12 Aug 2024 18:00:47 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021c68804ddafa7e8a4c8e96fa8abec87727ab17d080c722537520684516e032`  
		Last Modified: Mon, 12 Aug 2024 18:00:58 GMT  
		Size: 206.9 MB (206890089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b3db08f491266cdb7a4258abb7cddd0dbea7d851ceca4142fa476e18ecacaf`  
		Last Modified: Mon, 12 Aug 2024 18:00:47 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
