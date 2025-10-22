## `openjdk:26-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:e759f1223618b8577444ad54d466ee4485edbd5b778679ad870842b8d18c91c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `openjdk:26-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull openjdk@sha256:75f1e5d59a345186b40e5f279fe68da5c17de7832ae18d54cded610b5999db58
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1711290025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58360239384da85ab175f430450a73f957238cab4d3540a0708338ba7cbfad1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 21 Oct 2025 18:14:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:15:07 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:15:08 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 21 Oct 2025 18:15:16 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:15:17 GMT
ENV JAVA_VERSION=26-ea+20
# Tue, 21 Oct 2025 18:15:18 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_windows-x64_bin.zip
# Tue, 21 Oct 2025 18:15:20 GMT
ENV JAVA_SHA256=dbd547c391f90daa966d5d3a236e5a3cf792dea341d9596eb2a155059fe571a1
# Tue, 21 Oct 2025 18:16:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:16:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1599542500940c0b4e37228fa8a09ae85358f30d28f350aeddfa47b9bad90138`  
		Last Modified: Tue, 21 Oct 2025 18:28:32 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99852693f1f3d4c475ee02cc39e88f9ca2fb89d7e2e50a45766508d632b2261a`  
		Last Modified: Tue, 21 Oct 2025 18:28:32 GMT  
		Size: 369.3 KB (369348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b47ab29c297fb0110eddd84a80abc64b2943dc797d99a5070dc439e431a0a94`  
		Last Modified: Tue, 21 Oct 2025 18:28:32 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6765859afb6ebb46bd35aa19b04d1313c9969c61aef0c76cd40e2cf92ce927a`  
		Last Modified: Tue, 21 Oct 2025 18:28:32 GMT  
		Size: 351.7 KB (351733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71dd2ce81ba383b7a63f5087fd86b4f2250c02569139d5e761bb4c00c1b58ec`  
		Last Modified: Tue, 21 Oct 2025 18:28:32 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03360ec092fc6cafe11f336c74cea97dd59c6ca76e214063631d0e9829c0edc`  
		Last Modified: Tue, 21 Oct 2025 18:28:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f19055eb09dcfe01eb47ba61f60185220ef02260150609e0a20bf23408f787`  
		Last Modified: Tue, 21 Oct 2025 18:28:32 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f82b0d096909333a9163e67c1449614052891016af9de2d7c457739ae86d2c1`  
		Last Modified: Tue, 21 Oct 2025 21:23:55 GMT  
		Size: 221.5 MB (221541998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44373b4189a2a734a43e14ec5e39c929a868410ad31bd41047cdf7d5cd71d9b`  
		Last Modified: Tue, 21 Oct 2025 18:28:32 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
