## `openjdk:27-ea-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:9f035c5992b9fb99d515683e96012983b501721b48df1d6e73fd253e2422d64b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `openjdk:27-ea-jdk-windowsservercore` - windows version 10.0.26100.32370; amd64

```console
$ docker pull openjdk@sha256:5985fc0e4ab580eae9b1c39d066a72d8cd303afc2abeb0d96b690585a231ff3a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190361780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599980f6181742f82ab596f186a6601e5ad705fd95fb40412a2306278b74ecb7`
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
# Tue, 17 Feb 2026 19:32:46 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 17 Feb 2026 19:32:51 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 17 Feb 2026 19:32:51 GMT
ENV JAVA_VERSION=27-ea+9
# Tue, 17 Feb 2026 19:32:52 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_windows-x64_bin.zip
# Tue, 17 Feb 2026 19:32:52 GMT
ENV JAVA_SHA256=8f50a6f1fbb252ea650c31da6e40bdd95a1b286d715b84748ef20d251ac46b76
# Tue, 17 Feb 2026 19:33:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 17 Feb 2026 19:33:16 GMT
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
	-	`sha256:4a3d2efb5f3de8eb070c292173985fec703d3164365588ac24efb5193c82d6ae`  
		Last Modified: Tue, 17 Feb 2026 19:33:24 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970fc10841555fb4d3116301e24ceeb7c32e0d954d96730437094aaa1e2ce035`  
		Last Modified: Tue, 17 Feb 2026 19:33:24 GMT  
		Size: 370.7 KB (370720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8f6a438e5c03cdaf6f60a3d3e0545c801cf8832032c0bae7bd34aaaa3b2d24`  
		Last Modified: Tue, 17 Feb 2026 19:33:22 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13473e3e2be3d1256eb47d0ac6ae4c9c2e68038a7b632daaceb91cb879351115`  
		Last Modified: Tue, 17 Feb 2026 19:33:22 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bf13050a823b7e242fe212cd8fc3c40facec7534908154c45e25205f5f9082`  
		Last Modified: Tue, 17 Feb 2026 19:33:22 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbae85cc3137429a1e439744dcbb4637ba5252bba431cdfe779faa94870d0b0`  
		Last Modified: Tue, 17 Feb 2026 19:33:37 GMT  
		Size: 224.8 MB (224840872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9215a7d8fe27da41f4dcf03e070393a524a17180deade4db6d0e9abae12ad19`  
		Last Modified: Tue, 17 Feb 2026 19:33:22 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-jdk-windowsservercore` - windows version 10.0.20348.4773; amd64

```console
$ docker pull openjdk@sha256:8b1a0b7e57c8b28fa80c63d0c17d41ef96d7b0a81d8bb3075ad4b0013f0cd6c2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2088342551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2ec5a0ca6d92f80bf677b7248049284b8c79cf4d8df31b560432b16e4ad768`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Tue, 17 Feb 2026 19:45:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 17 Feb 2026 19:46:12 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 17 Feb 2026 19:58:49 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 17 Feb 2026 19:58:55 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 17 Feb 2026 19:58:55 GMT
ENV JAVA_VERSION=27-ea+9
# Tue, 17 Feb 2026 19:58:56 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_windows-x64_bin.zip
# Tue, 17 Feb 2026 19:58:57 GMT
ENV JAVA_SHA256=8f50a6f1fbb252ea650c31da6e40bdd95a1b286d715b84748ef20d251ac46b76
# Tue, 17 Feb 2026 19:59:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 17 Feb 2026 19:59:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537c87dc79dd0988a4104b7c89e38ad000e2354ad04b242a5e7c0febe517e1f7`  
		Last Modified: Tue, 17 Feb 2026 19:47:41 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c365cc66df2c402fb4def346ed016c3253688d4764a39dce6906f20709c0f815`  
		Last Modified: Tue, 17 Feb 2026 19:47:41 GMT  
		Size: 505.6 KB (505601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e8f9796fc1887885cc90473ef01c9e2773b481187a4c7f88c4ec761b42b9f9`  
		Last Modified: Tue, 17 Feb 2026 19:59:41 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7039622b8be9e454036a24447b09c505f9aa34293f90a26c9d15cc3c85dca6a1`  
		Last Modified: Tue, 17 Feb 2026 19:59:42 GMT  
		Size: 352.1 KB (352082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df39cfe705319acf93de6479e46e5c2c5dfd131965df09e9dd765b4ec49babb`  
		Last Modified: Tue, 17 Feb 2026 19:59:40 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b23b9b389d8a647920ffbba6e34fadc6a53c46925b180380498281a5aa10057`  
		Last Modified: Tue, 17 Feb 2026 19:59:40 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5282b2e3b2a2d42d23592bcefa4f0e3cb58f0d268ef37c0437180273038b64`  
		Last Modified: Tue, 17 Feb 2026 19:59:40 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23c9a1a65046399f5211b933f037d06af10146795ec7dc47e317920081bc3a5`  
		Last Modified: Tue, 17 Feb 2026 19:59:55 GMT  
		Size: 224.8 MB (224819860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0511a3c4c58c2d8a53e7a5199c959937a95a7c5406786ce68a3aa5471a407c`  
		Last Modified: Tue, 17 Feb 2026 19:59:40 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
