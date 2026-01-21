## `openjdk:27-ea-5-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:4b306b2b48dc587b4ae37dfd9a164d39fe266563b8a5f898eb3d315ccd9769a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `openjdk:27-ea-5-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:36f4ca3dbb5838e1bd200eee72c5ea9460157364de3edd95a48ffcb466c77a3d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2061004440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983bb2d518ed2afd1c8e299edd57e7849f0b69231b79c051bc6f14b818c56a35`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 20 Jan 2026 18:54:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 20 Jan 2026 18:55:58 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:55:59 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 20 Jan 2026 18:56:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:56:07 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 18:56:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_windows-x64_bin.zip
# Tue, 20 Jan 2026 18:56:10 GMT
ENV JAVA_SHA256=350ca51cd4321274f6557de42448fd4fc6e845cfe0695800868857f13f89a2fc
# Tue, 20 Jan 2026 18:56:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:56:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12503e819e94357068d715ad8ecf83f339bd5889b12d224bfd56b14fc18ed03`  
		Last Modified: Tue, 20 Jan 2026 19:07:44 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3734874d8df4d7d771d6b1069ee7161637b1c85f22f98b4159d6b88d52986f32`  
		Last Modified: Tue, 20 Jan 2026 19:07:44 GMT  
		Size: 513.0 KB (512968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a40ed685c42672d72a2ca56606735d97bbb3e73fb3efffd84f5dc98f83175c`  
		Last Modified: Tue, 20 Jan 2026 18:56:52 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d298107636bc92dd10715ab2e90da677425c7ef68a7ee07eb9ca510adf2958`  
		Last Modified: Tue, 20 Jan 2026 19:26:23 GMT  
		Size: 360.2 KB (360169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286b4060bec13e685f9eabab1eb4aac12f72419b9a03cc08e06d8721eca263e9`  
		Last Modified: Tue, 20 Jan 2026 18:56:51 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a2735f865a5901c5e0d56b5c640cca88ed7a07e5be27a93ff7cf9dd6362b91`  
		Last Modified: Tue, 20 Jan 2026 18:56:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf5658709f37c40a3845d61f68860c77c7d902a98f5c2909661d2568c4b3f58`  
		Last Modified: Tue, 20 Jan 2026 18:56:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21bd7fe4f4bae5fc8e5338fddc1e340eadb8313fbb3e3038c89d4e544e288765`  
		Last Modified: Tue, 20 Jan 2026 19:26:37 GMT  
		Size: 224.5 MB (224464285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6cecd6b7b9ff1f44fcab2283976b2e06e2c9218eb6f1e613530da7e757264b`  
		Last Modified: Tue, 20 Jan 2026 18:56:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
