## `eclipse-temurin:11-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:e55a8651604a1c3366e8e1112577e77a8c36c097037dbb6438afb1d0dbbdcf14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1607; amd64
	-	windows version 10.0.17763.4131; amd64

### `eclipse-temurin:11-jdk-windowsservercore` - windows version 10.0.20348.1607; amd64

```console
$ docker pull eclipse-temurin@sha256:5144d632a7cd89e5571e0955e5e92fc6ecac86641586299bc3da775fee72b40a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2081768504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b3c879d3ba8afb04f39c994a38c824cd5fe51ce29ab5f3144401acce1daf76`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 10 Mar 2023 06:37:36 GMT
RUN Install update 10.0.20348.1607
# Thu, 16 Mar 2023 00:38:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Mar 2023 00:52:12 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 00:53:27 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_x64_windows_hotspot_11.0.18_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_x64_windows_hotspot_11.0.18_10.msi ;     Write-Host ('Verifying sha256 (71e84c14606d1478147b46c3687486af0b51886192ff3b6239e51c1af413c688) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '71e84c14606d1478147b46c3687486af0b51886192ff3b6239e51c1af413c688') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 16 Mar 2023 00:54:15 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 16 Mar 2023 00:54:16 GMT
CMD ["jshell"]
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
	-	`sha256:261e1c3fb2972d931b5850548b01c79e749653ccc48039b83c0a6cad3ff54552`  
		Last Modified: Thu, 16 Mar 2023 01:44:27 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5ae49c1a060c49b8ab7315a320caf57ff1b1e9476dea2cff06761cc69cdd8`  
		Last Modified: Thu, 16 Mar 2023 01:45:01 GMT  
		Size: 367.3 MB (367272162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62411bc19a9f486bc5add8e5e1aa46cd2b94d8653630c48f119ab9744934d46e`  
		Last Modified: Thu, 16 Mar 2023 01:44:28 GMT  
		Size: 552.2 KB (552250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3dababbf52c255edd20e3b5edc48b4f0a41bb5a0bc77f14059086abb3acf54a`  
		Last Modified: Thu, 16 Mar 2023 01:44:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-windowsservercore` - windows version 10.0.17763.4131; amd64

```console
$ docker pull eclipse-temurin@sha256:e2f30f09a4ef17ca95fb17d15a08f7d69699729cc8d04f1179ab18928b7ce787
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2380875279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7deafc9ef90acfe92c5b67dbfaa5e5ab9e9e1fa08616e9e5add9d95086b0e235`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Sat, 11 Mar 2023 10:37:22 GMT
RUN Install update 10.0.17763.4131
# Thu, 16 Mar 2023 00:41:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Mar 2023 00:54:28 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 00:56:35 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_x64_windows_hotspot_11.0.18_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_x64_windows_hotspot_11.0.18_10.msi ;     Write-Host ('Verifying sha256 (71e84c14606d1478147b46c3687486af0b51886192ff3b6239e51c1af413c688) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '71e84c14606d1478147b46c3687486af0b51886192ff3b6239e51c1af413c688') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 16 Mar 2023 00:58:01 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 16 Mar 2023 00:58:02 GMT
CMD ["jshell"]
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
	-	`sha256:a94e129a3e0ede25a4750b66c42029a23d59fc3bec0f224978bef6cbefbc12fd`  
		Last Modified: Thu, 16 Mar 2023 01:45:14 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc10961cfaa0e6c8e809a73dc8fc7055f65314ab69d2ce8f72d6c494fde67167`  
		Last Modified: Thu, 16 Mar 2023 01:45:49 GMT  
		Size: 367.0 MB (367046143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c4fbe0cd30db63ce6926a9310337d7a645cc0988acd253fe3378e4815aa5aa`  
		Last Modified: Thu, 16 Mar 2023 01:45:14 GMT  
		Size: 315.9 KB (315901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14530e730f8cabc922d402f4d9849d760df8cffa59fdbc6bf9728db4c7122fba`  
		Last Modified: Thu, 16 Mar 2023 01:45:14 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
