## `eclipse-temurin:24-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:3aa9882667b062f06ea45ceb6bd6242bf3c893ee7c51d23c2e1ff6aa96248ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `eclipse-temurin:24-jre-windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull eclipse-temurin@sha256:af3638e745f477bb1839a5e5458663fd3e439448656542d14de76d9d2f7e03cb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3598506507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2bd582d0242e1de1fa8552d4139883cc68ecd80e931fc80f83a6f096fe2423`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:27:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:27:03 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Tue, 12 Aug 2025 20:27:17 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_x64_windows_hotspot_24.0.2_12.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_x64_windows_hotspot_24.0.2_12.msi ;     Write-Host ('Verifying sha256 (701c4d93bec1fd007985518d4e9ca6ba334cb99b0db7c8773c1c8dd1faa24628) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '701c4d93bec1fd007985518d4e9ca6ba334cb99b0db7c8773c1c8dd1faa24628') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 Aug 2025 20:27:23 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92fa5c30a7d294c641a439f9d7ff79b7947b7d47e2f8c359c7b2b3e32ca804ee`  
		Last Modified: Tue, 12 Aug 2025 20:31:06 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b538aa0f16db1a07e4ee49937283731d30ef519ee605d55fe4c27a7a7f5d2f7`  
		Last Modified: Tue, 12 Aug 2025 20:31:07 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6caf8f0fc06ca1a07f834481d362de0546612efd9805fe9c9e9e85810d2522c4`  
		Last Modified: Tue, 12 Aug 2025 20:31:19 GMT  
		Size: 99.3 MB (99301382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8847f725ac27426296a9e1490f4022224548dca466468c8e87eb8b0760ba5b9`  
		Last Modified: Tue, 12 Aug 2025 20:31:08 GMT  
		Size: 372.1 KB (372064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24-jre-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull eclipse-temurin@sha256:1581d2e1d71abb9bffb86ecb42b7a3094308d5382c6e6bc9d4bc7711257aa1c1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2381317415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5abc53701a0be10c83461e490ad4f54130299e795854670a9dce931d6f07b411`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:27:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:27:11 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Tue, 12 Aug 2025 20:27:30 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_x64_windows_hotspot_24.0.2_12.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_x64_windows_hotspot_24.0.2_12.msi ;     Write-Host ('Verifying sha256 (701c4d93bec1fd007985518d4e9ca6ba334cb99b0db7c8773c1c8dd1faa24628) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '701c4d93bec1fd007985518d4e9ca6ba334cb99b0db7c8773c1c8dd1faa24628') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 Aug 2025 20:27:37 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff4ab92ce23b68977e76d8fe57d19c1f9094193386c788a50f3c5d0c55e9452`  
		Last Modified: Tue, 12 Aug 2025 20:29:12 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82912b794341ef98872be6b2ad53444818e36dbe4ebd41e1eea60f6c457bac55`  
		Last Modified: Tue, 12 Aug 2025 20:29:12 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4991ec6231210bc4dc718e1ee69e9e8f96b1ae9cce308d86e876e52da66a4baa`  
		Last Modified: Tue, 12 Aug 2025 20:29:35 GMT  
		Size: 99.3 MB (99273336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f9e53470dc8421ad4a629a3145f7ab760a7f2bc9631b906d7651a91d7a28a1`  
		Last Modified: Tue, 12 Aug 2025 20:29:14 GMT  
		Size: 349.6 KB (349555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
