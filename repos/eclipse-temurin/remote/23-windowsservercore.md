## `eclipse-temurin:23-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:c4deb07ece8cea158cdd83ebd1f9bb98e59134652c21e4fd6caefe5a1fbfb9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:23-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:999bd0e191ad5b4c1fb10eff920083202c8ae43a26e3fba85db1adfc41fa7e8e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3305885775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d153fec67dbd995cb68bd7e2a7df793b85b0c34f6d16485154a050e00ea5d0d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:49:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:49:47 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Wed, 12 Mar 2025 18:50:16 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_windows_hotspot_23.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_windows_hotspot_23.0.2_7.msi ;     Write-Host ('Verifying sha256 (e4ef33439c2dc725387fce4d57ed63794785c0d3ab55726bdc9861c0387dc3a0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e4ef33439c2dc725387fce4d57ed63794785c0d3ab55726bdc9861c0387dc3a0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:50:26 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:50:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c19d6ff5ef5a6b71d5d12bfbbbc663cf8d5da211c661f5587dd472f0493333`  
		Last Modified: Wed, 12 Mar 2025 18:50:31 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d53c13638e874ab1df43b31000efe393d4dc6547d2f88307eae67767f00d0cc`  
		Last Modified: Wed, 12 Mar 2025 18:50:31 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aadeb93262369fb38a7ce94488ef20da1005e52388006c5924b778e6e650c0`  
		Last Modified: Wed, 12 Mar 2025 18:50:50 GMT  
		Size: 396.9 MB (396861815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e3bb3814ffd032ec3fc39a6e91722ed5c70a87690d8c70590f8d39e67e1a38`  
		Last Modified: Wed, 12 Mar 2025 18:50:31 GMT  
		Size: 372.3 KB (372332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e467189fa0d0e04d51b0a815c9a45d71ab9f33df5c12ba1434fdfe363ea003`  
		Last Modified: Wed, 12 Mar 2025 18:50:31 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:1bfa4ee4aff46edd459860547bd931897ee1eb52a9177d6cac6ff2d6f607694c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2667143494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10dc57ef82d7e2ab87d6a8ac52a44a50d2db308a85f5b7efc2850fbeae31b545`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:54:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:54:02 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Wed, 12 Mar 2025 18:54:32 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_windows_hotspot_23.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_windows_hotspot_23.0.2_7.msi ;     Write-Host ('Verifying sha256 (e4ef33439c2dc725387fce4d57ed63794785c0d3ab55726bdc9861c0387dc3a0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e4ef33439c2dc725387fce4d57ed63794785c0d3ab55726bdc9861c0387dc3a0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:54:40 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:54:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeaaeab7c07295058f8e21763e6f8202a941f8a4945a98941f42abf41afdafa7`  
		Last Modified: Wed, 12 Mar 2025 18:54:43 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e9e7ac07839ecacd17177e0a844006fefb6b83937f23f0069d1bf40bb82767`  
		Last Modified: Wed, 12 Mar 2025 18:54:43 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213e3c2d4e8d797c0b7c0444c0ef1edd6ac3127d2453e4f18c950cec81d0df4d`  
		Last Modified: Wed, 12 Mar 2025 18:54:59 GMT  
		Size: 396.8 MB (396839396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5f9747909aa6376a0407ccdbbecc2b806c5e0fc30f34a1bbe1a3bb4405d240`  
		Last Modified: Wed, 12 Mar 2025 18:54:43 GMT  
		Size: 359.0 KB (358985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bdc276842dd7dd6c20f9a9a491d841a88dad3970dd29b583344a2ee07aa6c5`  
		Last Modified: Wed, 12 Mar 2025 18:54:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:8a33d6c986eff28409965e266201cd7397b12e609133ef1ec61ec9872183d49d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2552855372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9b19748635e7772b0f62751f900c7ee5d64b5e755fbe1f07d598194562f47c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:49:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:49:43 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Wed, 12 Mar 2025 18:50:46 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_windows_hotspot_23.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_windows_hotspot_23.0.2_7.msi ;     Write-Host ('Verifying sha256 (e4ef33439c2dc725387fce4d57ed63794785c0d3ab55726bdc9861c0387dc3a0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e4ef33439c2dc725387fce4d57ed63794785c0d3ab55726bdc9861c0387dc3a0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:51:01 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:51:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc451c3bcd98cd4d390e0794757811b5a78322acff722636d5ac2c686de8734`  
		Last Modified: Wed, 12 Mar 2025 18:51:07 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468cb03b340452c7e8142c91182d390259044a0387b76e731e1da4df78487eb7`  
		Last Modified: Wed, 12 Mar 2025 18:51:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbf53e62395e893ec06af77488c974fc68c72c74fedf3bd7eb588bc35ec3298`  
		Last Modified: Wed, 12 Mar 2025 18:51:24 GMT  
		Size: 396.9 MB (396859888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484116a22a7b76ff327fc000deac2120574c1d9a838ede99ff3aa358a97353b1`  
		Last Modified: Wed, 12 Mar 2025 18:51:08 GMT  
		Size: 4.4 MB (4356803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af269c85567427ce2e93a8af0bb4429d6235b2a5b8e3020dc6f4ec934b7cc14`  
		Last Modified: Wed, 12 Mar 2025 18:51:07 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
