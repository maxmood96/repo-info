## `openjdk:26-ea-22-windowsservercore`

```console
$ docker pull openjdk@sha256:6122c183262f1bb4566d86d1851d0d25bab6524ff2a882150f98d182c34cd5ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `openjdk:26-ea-22-windowsservercore` - windows version 10.0.26100.6905; amd64

```console
$ docker pull openjdk@sha256:1ec9f169e60d4255b3a5e4aeddd4fb8a31ed3fbed95c8f1f333bed4aef8129d3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3442797825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a24dacd9835f7e58b03c1ebf7fd15d9f49e3d068d262892a27f74cfa7892fb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 31 Oct 2025 20:11:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Oct 2025 20:12:45 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 31 Oct 2025 20:12:46 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 31 Oct 2025 20:12:54 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 31 Oct 2025 20:12:55 GMT
ENV JAVA_VERSION=26-ea+22
# Fri, 31 Oct 2025 20:12:56 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_windows-x64_bin.zip
# Fri, 31 Oct 2025 20:12:57 GMT
ENV JAVA_SHA256=8d5e7c08f721a437ebd1097300a807cf2574e5a2fece94320b0202fc8703ba8f
# Fri, 31 Oct 2025 20:13:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 31 Oct 2025 20:13:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6fa327080882d9e89d7fa2e8059b335954ccd065d5253b5b19934ca6a62bde`  
		Last Modified: Fri, 31 Oct 2025 20:29:04 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2096392c187762baeefcb1588af130383dd1a0010c34e05e5923ae6a71f1287`  
		Last Modified: Fri, 31 Oct 2025 20:29:05 GMT  
		Size: 389.8 KB (389794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a473a83fc970edc5581bc5e20b05ea2ed2acb92cfb742b52595080c75ede621a`  
		Last Modified: Fri, 31 Oct 2025 20:29:05 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bac283b6114c0ec4fbed4eff82d0be76e18fedc45bba9aab724c1b18a711f9`  
		Last Modified: Fri, 31 Oct 2025 20:29:05 GMT  
		Size: 363.4 KB (363437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5403900cd4f6c1415201b62bf9ff3c7c8c6bbdd985634cc48befc26cfa8ccc78`  
		Last Modified: Fri, 31 Oct 2025 20:29:05 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c8f3f35e203be3b104c75d9f26163e368df8c178b487a27b9ec2aa1fa22129`  
		Last Modified: Fri, 31 Oct 2025 20:29:05 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a567356615679b4492f79ecf627c2ec307eed675b5f1b451a393aa37f473ac`  
		Last Modified: Fri, 31 Oct 2025 20:29:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e156c3f6b3e72ea4947e746c8cd4dbf144ed20f32dc519cf83b8250398c0647`  
		Last Modified: Fri, 31 Oct 2025 21:15:07 GMT  
		Size: 221.7 MB (221689697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0e269b44172f92d89667da428a016816fdff5495fc3906482f955d85730ab5`  
		Last Modified: Fri, 31 Oct 2025 20:29:05 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-22-windowsservercore` - windows version 10.0.20348.4297; amd64

```console
$ docker pull openjdk@sha256:ced56f3c09c8a24359c4b3101529a08d358208cf56eb0640536581381c28e066
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1799755209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6f72383caa193141f067856d072cc886b1eae5ef769732685b18a9025e0972`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 31 Oct 2025 20:12:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Oct 2025 20:13:14 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 31 Oct 2025 20:13:15 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 31 Oct 2025 20:13:22 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 31 Oct 2025 20:13:23 GMT
ENV JAVA_VERSION=26-ea+22
# Fri, 31 Oct 2025 20:13:25 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_windows-x64_bin.zip
# Fri, 31 Oct 2025 20:13:27 GMT
ENV JAVA_SHA256=8d5e7c08f721a437ebd1097300a807cf2574e5a2fece94320b0202fc8703ba8f
# Fri, 31 Oct 2025 20:14:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 31 Oct 2025 20:14:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fdc9e4c91313e0d8d35a8bc66a5fcdf64b2fa8df4b6ef66b15bdf501c67c1a`  
		Last Modified: Fri, 31 Oct 2025 20:24:22 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0950f094f0b08d3139550e1d68c2216ce57fb7be8ee0f02cb098d4a6e7251409`  
		Last Modified: Fri, 31 Oct 2025 20:24:22 GMT  
		Size: 521.2 KB (521215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5540843c398e3f7965e0f6a1e7de2f2896b765b58f9a49adbbd3e4652d1e67b0`  
		Last Modified: Fri, 31 Oct 2025 20:24:22 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03a89a3020f584b4810becc7bd5199dc50cf2d148d54c4f6f047cd2b0d20686`  
		Last Modified: Fri, 31 Oct 2025 20:24:22 GMT  
		Size: 360.3 KB (360309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beefec6b03e3434caa6bbec26a0379efcea9161768f56353876d1fe941039caf`  
		Last Modified: Fri, 31 Oct 2025 20:24:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6277ad0ae45b7c48bb5d8aa3e0c63c83a57b7ca145ce745feba7ddc4864e0fc`  
		Last Modified: Fri, 31 Oct 2025 20:24:22 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b424ef3d213c0acb116ab934ecfc66e08ff1683d14a5674b3321a198934f52fe`  
		Last Modified: Fri, 31 Oct 2025 20:24:22 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ade11dcd425d55740af5b4dcf92d98b884a69ac4159214d4c653c3d7f75944`  
		Last Modified: Fri, 31 Oct 2025 21:16:55 GMT  
		Size: 221.7 MB (221672933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9415c007ba84c3b8ed644c6ccf15a1a7d8c9da804ca0377d0c5ab19a0130df75`  
		Last Modified: Fri, 31 Oct 2025 20:24:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
