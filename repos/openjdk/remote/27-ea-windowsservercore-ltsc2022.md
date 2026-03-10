## `openjdk:27-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:f5b2aa53dfc174aa92bcb71223b4e13eee0f7235ab973fae9ea9cb56b8a2e9e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `openjdk:27-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull openjdk@sha256:31a45f414475b13be910281335a95649582bbe68be8e1cc0a20daa3024b80e95
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2207834880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dfd5103361edf759fe471582fe5282ee736b0ffddb48552cf02c72a0b1197c2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:57:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:14:54 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:14:55 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 10 Mar 2026 22:15:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:15:01 GMT
ENV JAVA_VERSION=27-ea+12
# Tue, 10 Mar 2026 22:15:01 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_windows-x64_bin.zip
# Tue, 10 Mar 2026 22:15:02 GMT
ENV JAVA_SHA256=bb5331abf59ac46c0dd11cefa00cc052f8d7cf6384d850b919591cb3346acbe4
# Tue, 10 Mar 2026 22:15:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:15:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f982b44695c6c1cca851e9238aa8eceda2f7522e65a6a1df319239f66b3610fe`  
		Last Modified: Tue, 10 Mar 2026 22:00:31 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7ce18d39c8fd66409b6df095755d7331405577028a781dc62022f4be4f7df`  
		Last Modified: Tue, 10 Mar 2026 22:15:49 GMT  
		Size: 491.8 KB (491764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9709e89de0f771446b0addeb48003e703cd5533b39b78b867272bbee78b1c7`  
		Last Modified: Tue, 10 Mar 2026 22:15:49 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b95ef2b220dc5350cda21f1947f8cccb26a0e52134b48ef8a486a531295a7e0`  
		Last Modified: Tue, 10 Mar 2026 22:15:49 GMT  
		Size: 337.9 KB (337886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47e5a03efb8d1c3b42cc3156c2b9730011599ba4962e9e81912ebde2663441d`  
		Last Modified: Tue, 10 Mar 2026 22:15:47 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5f28235feef5e3517512792b835dcf99ee050da565821b0d860974e9f87d68`  
		Last Modified: Tue, 10 Mar 2026 22:15:47 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe20410c761248631018d174892c6830bb72938a6d9a926f3df3543dcb71aec`  
		Last Modified: Tue, 10 Mar 2026 22:15:47 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0c74df48da9f323c40c6c6350831c5c307b337f2349b51479d48d807e1a556`  
		Last Modified: Tue, 10 Mar 2026 22:16:03 GMT  
		Size: 224.7 MB (224715958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b91cbaadd0667bffc39536877ca56f2d47430ee31074c95a6f5cb57f982f65`  
		Last Modified: Tue, 10 Mar 2026 22:15:47 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
