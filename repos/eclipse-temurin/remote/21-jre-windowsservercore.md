## `eclipse-temurin:21-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:a05b358e646140cb5afb05f025d915b7628772ce118659acc91b9fd45cc627b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `eclipse-temurin:21-jre-windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull eclipse-temurin@sha256:2dcfb83a294c78a6b97059761748d527866e96857757dcd2b02ce2259b8f0d3e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3655362208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165cf15e7724b2377dc58c5cda80f9fa811e5a551cc933a9520d75c41b568471`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 10 Sep 2025 21:49:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:57:03 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Wed, 10 Sep 2025 21:57:22 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_windows_hotspot_21.0.8_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_windows_hotspot_21.0.8_9.msi ;     Write-Host ('Verifying sha256 (9e38a94eed115fb834c2c4375bc493cef1a47e28c82bd83f623efe3fca017e7a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '9e38a94eed115fb834c2c4375bc493cef1a47e28c82bd83f623efe3fca017e7a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Sep 2025 21:57:27 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39bf991b65b005f2b7f122bb8e11deadf02225b06438805e32f109fda66c1ea`  
		Last Modified: Wed, 10 Sep 2025 21:57:04 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605e60c6ef50eabb1d6c103cfa7320c262ee187aff40652018569052e3f431de`  
		Last Modified: Wed, 10 Sep 2025 21:57:48 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333f5312d68e5ee5b2cd7c5acd043fb7f8fac4d8ba367bde49cd4be5264e58c5`  
		Last Modified: Wed, 10 Sep 2025 21:57:56 GMT  
		Size: 83.6 MB (83574765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305ee4b2cc09801870f21dca8ca6ff1b119c3442d40e7d64583c3fd3f7d110f3`  
		Last Modified: Wed, 10 Sep 2025 21:57:48 GMT  
		Size: 345.1 KB (345074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull eclipse-temurin@sha256:97580a0f8430d0d6e711c8c01b5e60fd101c0fb2d73e2443848da4110ab17565
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2366060603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318b47059960b261a64d774ca1ddf87b05a19b0bcda69958ce5d7452e80691aa`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 20:20:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 20:21:23 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Wed, 10 Sep 2025 20:42:26 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_windows_hotspot_21.0.8_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_windows_hotspot_21.0.8_9.msi ;     Write-Host ('Verifying sha256 (9e38a94eed115fb834c2c4375bc493cef1a47e28c82bd83f623efe3fca017e7a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '9e38a94eed115fb834c2c4375bc493cef1a47e28c82bd83f623efe3fca017e7a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Sep 2025 20:42:32 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbe60f506e392727a189c473ed3077c57345b082b3f502c4e12299121d8a339`  
		Last Modified: Wed, 10 Sep 2025 21:43:44 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf478d5a24e6075683437ec147526cf583589b551018d6d33269596375d3dc7`  
		Last Modified: Wed, 10 Sep 2025 21:53:31 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3951bd898a6bbcdb742ad00c4167192fae996843ff6ab405c3d9449aaf040a`  
		Last Modified: Wed, 10 Sep 2025 21:53:53 GMT  
		Size: 83.6 MB (83561214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100babe34efd63b991dc2df2d6bd300cabd436530aab2255c09dd32dd50cd5c9`  
		Last Modified: Wed, 10 Sep 2025 21:53:45 GMT  
		Size: 351.8 KB (351811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
