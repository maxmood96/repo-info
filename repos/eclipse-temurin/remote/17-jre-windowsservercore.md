## `eclipse-temurin:17-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:c8ea546a62a4a456bc3fe968e980ad8a4af794199f676a3d4f9cbc1d5dce8385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:17-jre-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:14eec0487aa73556f7aad5cb3f73a417392838b273f81e1aaacc393f1a9238ae
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1874148922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0d4e85c91e256ddfb5273ff2123ca4290f4ab5d9dd8a229445cd91708a4175`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Wed, 09 Oct 2024 23:33:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:48:55 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 09 Oct 2024 23:54:01 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_windows_hotspot_17.0.12_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_windows_hotspot_17.0.12_7.msi ;     Write-Host ('Verifying sha256 (62caaa23b88545099612ae77455fe2ac888ad3731ac0758f5cbedad406fd3c6c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '62caaa23b88545099612ae77455fe2ac888ad3731ac0758f5cbedad406fd3c6c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Oct 2024 23:54:23 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dd7a167e5d8024c2db3283a385811103c47c1e1349528ae29d41d1aa3117ae`  
		Last Modified: Thu, 10 Oct 2024 00:18:53 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6222f88e95e2ade54fc72bc5b001168d2b8f9d4dfe8790c7a9d98d096500b66e`  
		Last Modified: Thu, 10 Oct 2024 00:24:33 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9a09351468fa5586f8725913556677c171e76fe10f5e02cd60b02e62697104`  
		Last Modified: Thu, 10 Oct 2024 00:27:12 GMT  
		Size: 74.5 MB (74538038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81a3e5b50a4b3c4d91e6b0c9ac9678b6449e2c01e54f786a9604df9cf822826`  
		Last Modified: Thu, 10 Oct 2024 00:27:03 GMT  
		Size: 266.5 KB (266497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:7a96696930d61a1c3d2fa779079fbf59d09d822235f24ee4da994c3bbb983067
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1979546520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9992b1fa4e9548351e9dc8b031ba7775f9c5c06a922d92e2dc04b2a25104ac15`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Wed, 09 Oct 2024 23:35:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:50:24 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 09 Oct 2024 23:55:33 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_windows_hotspot_17.0.12_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_windows_hotspot_17.0.12_7.msi ;     Write-Host ('Verifying sha256 (62caaa23b88545099612ae77455fe2ac888ad3731ac0758f5cbedad406fd3c6c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '62caaa23b88545099612ae77455fe2ac888ad3731ac0758f5cbedad406fd3c6c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Oct 2024 23:56:13 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71416d65806874920ade48cad9fe9e847b67ca207c59353ff136f87da9c117ce`  
		Last Modified: Thu, 10 Oct 2024 00:19:58 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec183f8c91ef88858125b806eb4896cdc12f748961d5134ebf50daf472609879`  
		Last Modified: Thu, 10 Oct 2024 00:25:09 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5f955f7b5c0e97b11e4281e5eb8b5d4bb7157ddaa6fc25ae504c27d951886b`  
		Last Modified: Thu, 10 Oct 2024 00:27:30 GMT  
		Size: 74.6 MB (74559986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be45f80045292c5a405d181ab83b8c2bd637bbe1e466a5b202b5555ea1ff47d1`  
		Last Modified: Thu, 10 Oct 2024 00:27:21 GMT  
		Size: 3.2 MB (3158392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
