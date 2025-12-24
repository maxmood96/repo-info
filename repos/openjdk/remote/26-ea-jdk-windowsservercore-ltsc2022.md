## `openjdk:26-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:76abb5421bd5a079d99c0a68dd6986e830a56ba2eb92afc8c1ea1b01c78c8916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `openjdk:26-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull openjdk@sha256:db70aa8bcab5dc3e882e9bf979b9198b4ccd0f0a0f4f1b79871045f91e6a7016
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2004963695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb399f82e1b7bfdca8eb23e9da549f588680f399d925a07e23bc0e2995a2e4d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Wed, 24 Dec 2025 05:21:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Dec 2025 05:21:59 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 24 Dec 2025 05:22:00 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 24 Dec 2025 05:22:08 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 24 Dec 2025 05:22:08 GMT
ENV JAVA_VERSION=26-ea+29
# Wed, 24 Dec 2025 05:22:10 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_windows-x64_bin.zip
# Wed, 24 Dec 2025 05:22:11 GMT
ENV JAVA_SHA256=901386b7c2b8f4a23a6158eddfca969dabb4acec8359c9861f538ea3873cf53d
# Wed, 24 Dec 2025 05:23:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 24 Dec 2025 05:23:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5e1e7094f7d15a86b575087b9ef75e5c8056b26b193f2835b0bb746e105e0c`  
		Last Modified: Wed, 24 Dec 2025 05:35:17 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c6c072091e6f8cbfdbba0b2f363767075da4c70a3a6f6a8f284efe5639dc18`  
		Last Modified: Wed, 24 Dec 2025 05:35:18 GMT  
		Size: 504.0 KB (504010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ae30638ce1239ceb7378590f2a8edb80f25f63ea06050dd0b8b1005bd16260`  
		Last Modified: Wed, 24 Dec 2025 05:35:17 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46822cff6f829d862b4c410e084029f0f2d2457f3472ddc72ec05fc9a61ef27f`  
		Last Modified: Wed, 24 Dec 2025 05:35:18 GMT  
		Size: 351.6 KB (351639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d9c736c274100927f6696df4cdc83d983cb95d672bbb43f51f18c898550368`  
		Last Modified: Wed, 24 Dec 2025 05:35:17 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9ce853ad55876bceadb351df5b46da4facac9c69778afcbb4647e98a884c83`  
		Last Modified: Wed, 24 Dec 2025 05:35:17 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052f9856b06d881102b59ad731a29cd00a136b880dc555de685d40cc3ccbdd90`  
		Last Modified: Wed, 24 Dec 2025 05:35:18 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29e086f1005f9cdfb363c12799ba2c0a77cb99e63da0b84366117205f60168a`  
		Last Modified: Wed, 24 Dec 2025 05:35:30 GMT  
		Size: 224.2 MB (224220850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdaa097d97f80f093a723bd16e508cc675bb464986b8a42e1e94ff5943290e3`  
		Last Modified: Wed, 24 Dec 2025 05:35:17 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
