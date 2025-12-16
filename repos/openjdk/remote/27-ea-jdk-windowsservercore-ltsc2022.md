## `openjdk:27-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:dd9faf03414f1f22117adbbb0b31b01b514e96eb63e7694c49aa4c3e145f4c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `openjdk:27-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull openjdk@sha256:15f3c4ecfa6baacb64e996ba4c87373cf2a3bf1a8cf70411f8e3fd14ecb1a150
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2005015435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b659817477a4527f5b6920bf8fba56e3df558b8bcbb616c1ab285b27d7f34cab`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 16 Dec 2025 00:34:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 00:34:51 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 16 Dec 2025 00:34:52 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 16 Dec 2025 00:35:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 16 Dec 2025 00:35:02 GMT
ENV JAVA_VERSION=27-ea+2
# Tue, 16 Dec 2025 00:35:04 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_windows-x64_bin.zip
# Tue, 16 Dec 2025 00:35:05 GMT
ENV JAVA_SHA256=486eb3681d48770501631da706141ae22a0bc408cb4899e2370656479dd8ebfd
# Tue, 16 Dec 2025 00:36:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 16 Dec 2025 00:36:44 GMT
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
	-	`sha256:80e6900165940b67250c33c8a1d9ccdce394d47319cb5ec334325ad76cf52c40`  
		Last Modified: Tue, 16 Dec 2025 00:48:26 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480129b24afef7ee425fce948ebb465044651d7ce74a49e874b2b8d4d2225f73`  
		Last Modified: Tue, 16 Dec 2025 00:48:26 GMT  
		Size: 504.4 KB (504390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc34522d34fa2e2a4b0e8eba2f905d228827a16aa22f46d4aac1059a78d93d8`  
		Last Modified: Tue, 16 Dec 2025 00:48:26 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1998f18910dbab72b963ac2f75615f600719dd98acab946fb519a3a92f502dc3`  
		Last Modified: Tue, 16 Dec 2025 00:48:26 GMT  
		Size: 351.8 KB (351764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c8819b6afe78524d8c0349230cc3310d81737894d7635e28eb15d8101f1eb6`  
		Last Modified: Tue, 16 Dec 2025 00:48:26 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663864309127e1ad86b51b088861da12fd9db26fffdef9868bb8a1eb34086016`  
		Last Modified: Tue, 16 Dec 2025 00:48:26 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9f0618f828d8b77b1da2154ffd198ba6214283001fd8e5aaff966fea0217c2`  
		Last Modified: Tue, 16 Dec 2025 00:48:26 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00ac01c7cc14240868b2c785ce5856fb53d1caf5b6e5912e19475c165fad148`  
		Last Modified: Tue, 16 Dec 2025 00:48:53 GMT  
		Size: 224.3 MB (224272118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9401bfc5a1f241cd3da46796e572255202201349ad9f0f27d5505be5994dbf59`  
		Last Modified: Tue, 16 Dec 2025 00:48:26 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
