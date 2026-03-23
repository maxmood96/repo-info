## `openjdk:27-ea-14-windowsservercore`

```console
$ docker pull openjdk@sha256:ddf66905ab85cea35ba49de0aa26d51d2a082133f07508e4ba9547392afd6325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `openjdk:27-ea-14-windowsservercore` - windows version 10.0.26100.32522; amd64

```console
$ docker pull openjdk@sha256:3760d5261532ac45f98b7a94e43a57a6cace6c267974f4217605d178175a2402
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2306787858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712d3ca60d5bb8d2d994e6ab67596c306db94417ff673114d52f9c5e78226b75`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Mon, 23 Mar 2026 17:59:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2026 18:00:20 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 23 Mar 2026 18:00:20 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 23 Mar 2026 18:00:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 23 Mar 2026 18:00:27 GMT
ENV JAVA_VERSION=27-ea+14
# Mon, 23 Mar 2026 18:00:28 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_windows-x64_bin.zip
# Mon, 23 Mar 2026 18:00:29 GMT
ENV JAVA_SHA256=036103af3a6b6a7fb78955d438f100e620132a28640df5277dd69e8678a924a5
# Mon, 23 Mar 2026 18:00:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 23 Mar 2026 18:00:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d965dd410e3195b9ae57caf4f1c339e13a22baf8f46191f070f943dc14aa66f`  
		Last Modified: Mon, 23 Mar 2026 18:01:06 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091abd0bee8579150e2a66dc763d1226bb48d8fe4779f411027f54ebd320ac8a`  
		Last Modified: Mon, 23 Mar 2026 18:01:06 GMT  
		Size: 403.9 KB (403875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fbe3771ce949f77e8d85416219d1ddc6f8b25bcf431aaa259e5eac24f135296`  
		Last Modified: Mon, 23 Mar 2026 18:01:07 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5dbfa0b1c6d05c5c2d5612a095e1f9e04579ad630ca79b441ae5b4e09953db`  
		Last Modified: Mon, 23 Mar 2026 18:01:06 GMT  
		Size: 385.3 KB (385341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364088be8a50446eb4ac1eb3dac1e98be63efe912c8f012a82e15d795b8d9a81`  
		Last Modified: Mon, 23 Mar 2026 18:01:04 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70f0466cf371da550758f7e6f5442dea965406b4f180439bdc54b023d49d1c4`  
		Last Modified: Mon, 23 Mar 2026 18:01:04 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a06caa864b0c79cca2719bbdbfb548efd2eea63f64c5246a56ccc0ec7810e6`  
		Last Modified: Mon, 23 Mar 2026 18:01:04 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85aa6acc09d5b2852ca57f66ba97eb72cc4aef9a4113a7266e89e141695d3f2e`  
		Last Modified: Mon, 23 Mar 2026 18:01:37 GMT  
		Size: 224.8 MB (224794734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58e8a04d0fafe12399768a744ebc1560e6e028635a06fcd2b63a5b7674adad8`  
		Last Modified: Mon, 23 Mar 2026 18:01:04 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-14-windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull openjdk@sha256:dfd43e0ea001df8280569c9fdb26891ccba845e3905974e95d561ff996303b4e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2207912078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b21859f72b107d29c32a5bdad732657b448f6fe8e20b6d6d3d27dcf4d807d0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Mon, 23 Mar 2026 18:21:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2026 18:22:21 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 23 Mar 2026 18:22:22 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 23 Mar 2026 18:22:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 23 Mar 2026 18:22:31 GMT
ENV JAVA_VERSION=27-ea+14
# Mon, 23 Mar 2026 18:22:31 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_windows-x64_bin.zip
# Mon, 23 Mar 2026 18:22:32 GMT
ENV JAVA_SHA256=036103af3a6b6a7fb78955d438f100e620132a28640df5277dd69e8678a924a5
# Mon, 23 Mar 2026 18:23:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 23 Mar 2026 18:23:41 GMT
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
	-	`sha256:a5e70bdc88dd20cec2da9e31448ebb1ef7e1cae0295119642e4c9b963bff73d9`  
		Last Modified: Mon, 23 Mar 2026 18:23:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115d67259ed24f89a0a4aebc56c8a2ea60f124af392f46d71d282f42191e08d0`  
		Last Modified: Mon, 23 Mar 2026 18:23:53 GMT  
		Size: 505.2 KB (505249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba144e8d8da234e91983e03b3083fa516b6e60f6389dbcc8cec0ceec61281b4`  
		Last Modified: Mon, 23 Mar 2026 18:23:52 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca10d54bd002a2f8739e979f174281036c7e88ecd45fdd222c80de2a54064a4`  
		Last Modified: Mon, 23 Mar 2026 18:23:52 GMT  
		Size: 345.3 KB (345310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcba2fa6db45de5dcb1424dd4d82069c5f59a62a43eb52649319f236e27805ce`  
		Last Modified: Mon, 23 Mar 2026 18:23:50 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c73186d90f627106e2fd69251dbbe9ed9a1620d20e7ec7a66c92a58bb6b4311`  
		Last Modified: Mon, 23 Mar 2026 18:23:50 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec9bce3698367ea02c6b137e2988ba352d670037abc27328fe964c108fcbf98`  
		Last Modified: Mon, 23 Mar 2026 18:23:50 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e3ba7b530164e099c41e8722c4461962d9d54caa01549933df8773894b88ad`  
		Last Modified: Mon, 23 Mar 2026 18:24:06 GMT  
		Size: 224.8 MB (224772256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56f16b7a64d76621414703b64a64e3f130ad99f095bad86cf7b539a881459bb`  
		Last Modified: Mon, 23 Mar 2026 18:23:50 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
