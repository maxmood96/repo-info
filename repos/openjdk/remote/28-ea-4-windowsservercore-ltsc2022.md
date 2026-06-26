## `openjdk:28-ea-4-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:3a25658441393a937ec98c28c7adb0226d3d3bd2d996a4523879196908e8b658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `openjdk:28-ea-4-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull openjdk@sha256:38775a76a4ab6261a6a863489534dfe43f2fd07dcdbf6f9b127178c8e8d54919
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2357421003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15822d9500cf82d9d5c2b4a681e541dc723572976130bf954b7993ace7368511`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Fri, 26 Jun 2026 22:43:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Jun 2026 22:43:54 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 26 Jun 2026 22:43:55 GMT
ENV JAVA_HOME=C:\openjdk-28
# Fri, 26 Jun 2026 22:44:02 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 26 Jun 2026 22:44:02 GMT
ENV JAVA_VERSION=28-ea+4
# Fri, 26 Jun 2026 22:44:03 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_windows-x64_bin.zip
# Fri, 26 Jun 2026 22:44:04 GMT
ENV JAVA_SHA256=b85f4b0c1313453fc760c198dec39f0c3a27e386671a184a123c19fcfb46c776
# Fri, 26 Jun 2026 22:45:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 26 Jun 2026 22:45:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6abaff06b6cf8d216a7cd97ba106d8b7fff77fd20dd23f8b011085d795dedb`  
		Last Modified: Fri, 26 Jun 2026 22:45:59 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce2cd747a577ffed1599ea67899827f4db92db1edeae4f67de272e5fec1d0cf`  
		Last Modified: Fri, 26 Jun 2026 22:45:59 GMT  
		Size: 502.9 KB (502856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9090a0352da1996214a8fc740c6e23e2bbab6dde1ced339c3c0b30fe72be7a0d`  
		Last Modified: Fri, 26 Jun 2026 22:45:58 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32ad2d94825c4e1b134e3e5a48ac35fa1f98a908728fde6a270b03206734890`  
		Last Modified: Fri, 26 Jun 2026 22:45:59 GMT  
		Size: 351.9 KB (351886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d8dfb02e6af436f55e266423d5e1f045a2abfe1323986f43c65c859adbc409`  
		Last Modified: Fri, 26 Jun 2026 22:45:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9021843611160965c7d4201b79f6336006a9efe82a335d80018c89cd0ab5d579`  
		Last Modified: Fri, 26 Jun 2026 22:45:57 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54537bdf3282a6b77f0c47bed33d2064bc1f0c8749582a664f3d812a42853c70`  
		Last Modified: Fri, 26 Jun 2026 22:45:57 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1b2d5f8e0e7c7ff167c844a2dc9eb050cd4509e8c322ca9776804ea2e1bea7`  
		Last Modified: Fri, 26 Jun 2026 22:46:13 GMT  
		Size: 224.4 MB (224432834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3007c94ba763e47716d2e6ef9ff6e6e85f6cec5fc92654f983ab8b544cd4d1`  
		Last Modified: Fri, 26 Jun 2026 22:45:57 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
