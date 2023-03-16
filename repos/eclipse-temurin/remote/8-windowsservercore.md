## `eclipse-temurin:8-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:b7a69f004d537b640124394dbdc66b17092cfe3ce5a14209e71782cf2b9305e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1607; amd64
	-	windows version 10.0.17763.4131; amd64

### `eclipse-temurin:8-windowsservercore` - windows version 10.0.20348.1607; amd64

```console
$ docker pull eclipse-temurin@sha256:210888179ce06ef5faed5db91ea0d57342d417cb67be25ceee40962837f5f55a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1905882084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ed9a87e3b55f779bd05089557b3fc49b8de83d3af5404ed705d9ea62c7e8ad`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 10 Mar 2023 06:37:36 GMT
RUN Install update 10.0.20348.1607
# Thu, 16 Mar 2023 00:38:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Mar 2023 00:38:32 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 16 Mar 2023 00:39:57 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u362b09.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u362b09.msi ;     Write-Host ('Verifying sha256 (07d6ff7bb5400a618e7e8c6e6104c04c1df6141fa85026526676aa8af011e44c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '07d6ff7bb5400a618e7e8c6e6104c04c1df6141fa85026526676aa8af011e44c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 16 Mar 2023 00:41:05 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c921d7eac594f5e3ce3ef10adb8fd0f71bdbb713c4854336b995d25f89c44d42`  
		Last Modified: Thu, 16 Mar 2023 01:41:04 GMT  
		Size: 327.9 MB (327911088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bca4593035ae0e8d1b6e6eb1b053fddc6a6824b28f45f99de726d752d2c0f72`  
		Last Modified: Thu, 16 Mar 2023 01:39:50 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448c166f14e4abf65c0e92797b07f0b212e712b28fc6e4ed71942cb9f59c752c`  
		Last Modified: Thu, 16 Mar 2023 01:39:50 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07601296624cd2d4dffd08afc9be41aacb89deb1f6a20166367c6a532194166`  
		Last Modified: Thu, 16 Mar 2023 01:40:20 GMT  
		Size: 191.4 MB (191386720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85813707946c8eb4a4af9af7c462ab02efc31adfd339cc190a111491e5d270ec`  
		Last Modified: Thu, 16 Mar 2023 01:39:50 GMT  
		Size: 552.6 KB (552557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-windowsservercore` - windows version 10.0.17763.4131; amd64

```console
$ docker pull eclipse-temurin@sha256:5ba76b2a45e256d754e5e298c0b2f991404d2450d0099c038f1c391a9ac94b56
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2204986448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4391b74ccf0d1660bf8a66a0f7368447f1c7581cecc8a09cf1550ff3f871c8f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Sat, 11 Mar 2023 10:37:22 GMT
RUN Install update 10.0.17763.4131
# Thu, 16 Mar 2023 00:41:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Mar 2023 00:41:19 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 16 Mar 2023 00:43:40 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u362b09.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u362b09.msi ;     Write-Host ('Verifying sha256 (07d6ff7bb5400a618e7e8c6e6104c04c1df6141fa85026526676aa8af011e44c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '07d6ff7bb5400a618e7e8c6e6104c04c1df6141fa85026526676aa8af011e44c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 16 Mar 2023 00:45:31 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92048040b3b13af10f8287baabaddbb2759dfc77b1fb43f89b38b3275467f93`  
		Last Modified: Thu, 16 Mar 2023 01:42:29 GMT  
		Size: 305.6 MB (305565048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8e4e0836091bdd33e8adb56d1e13b8096550727a20534e2a2ab9298c86fa09`  
		Last Modified: Thu, 16 Mar 2023 01:41:16 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397814120347f984a9317518ce2e0d48f8e86e4ec090c37143e646b5855692cb`  
		Last Modified: Thu, 16 Mar 2023 01:41:16 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff7a37a2686520cb1dedb45592b3c68c8e5e87c70bbeee2d370731f5604cc6a`  
		Last Modified: Thu, 16 Mar 2023 01:41:46 GMT  
		Size: 191.2 MB (191157575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d36641e983a6cf6efc60989aa845631b4e5461191baa7fe70f67c05e140e6e5`  
		Last Modified: Thu, 16 Mar 2023 01:41:18 GMT  
		Size: 317.0 KB (317046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
