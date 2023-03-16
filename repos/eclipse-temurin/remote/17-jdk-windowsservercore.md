## `eclipse-temurin:17-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:205232a50f3feb2a8884cf6edd889b72a1d9931f05e490a88b55d7ce1dc064c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1607; amd64
	-	windows version 10.0.17763.4131; amd64

### `eclipse-temurin:17-jdk-windowsservercore` - windows version 10.0.20348.1607; amd64

```console
$ docker pull eclipse-temurin@sha256:c82b862701a320623ada378697f8818cf3d5c374677da944450b63b71e2ff161
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2067396424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c63ee794ab5d470d4d0d1b9d97dfcf479963091fde09af9a00085aca8badcb1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 10 Mar 2023 06:37:36 GMT
RUN Install update 10.0.20348.1607
# Thu, 16 Mar 2023 00:38:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Mar 2023 01:04:40 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 01:05:57 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_windows_hotspot_17.0.6_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_windows_hotspot_17.0.6_10.msi ;     Write-Host ('Verifying sha256 (943152d548f8dd24e3c07e67ddc17262d15dc390197cb4ef330867fe4130e590) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '943152d548f8dd24e3c07e67ddc17262d15dc390197cb4ef330867fe4130e590') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 16 Mar 2023 01:06:40 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 16 Mar 2023 01:06:41 GMT
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
	-	`sha256:00d537d7bcb9d23bb02da2dfc233a58c92f00582883661ec289c68fea2e5623d`  
		Last Modified: Thu, 16 Mar 2023 01:47:36 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad021785670538523a1b19b1b1b6ad2ddbe9548b9781518121f58c361ba0b7a3`  
		Last Modified: Thu, 16 Mar 2023 01:48:09 GMT  
		Size: 352.9 MB (352899612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b7060b1efe42f58e8b46e38d7224baebceacbbe76a5fe32321d771c883bff6`  
		Last Modified: Thu, 16 Mar 2023 01:47:37 GMT  
		Size: 552.5 KB (552459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b52f373f577bfbd7b0d5f53890660e364035fbd5173d1321bf1e726fed0f14a`  
		Last Modified: Thu, 16 Mar 2023 01:47:36 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-windowsservercore` - windows version 10.0.17763.4131; amd64

```console
$ docker pull eclipse-temurin@sha256:c1d2c1887b1f67ad69eafeeabcf23b12e960faaafd0418c009cc61e19245ac62
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2370068887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b16ed090d1173d9ce00e42d234a176eef90562428542e7b39e2e23ddda724a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Sat, 11 Mar 2023 10:37:22 GMT
RUN Install update 10.0.17763.4131
# Thu, 16 Mar 2023 00:41:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Mar 2023 01:06:55 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 01:08:56 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_windows_hotspot_17.0.6_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_windows_hotspot_17.0.6_10.msi ;     Write-Host ('Verifying sha256 (943152d548f8dd24e3c07e67ddc17262d15dc390197cb4ef330867fe4130e590) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '943152d548f8dd24e3c07e67ddc17262d15dc390197cb4ef330867fe4130e590') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 16 Mar 2023 01:10:24 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 16 Mar 2023 01:10:25 GMT
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
	-	`sha256:1b633a3b48ab859b05839c561735503362ab7f1c8ed880ff5207414e135a8505`  
		Last Modified: Thu, 16 Mar 2023 01:48:21 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d496ae2e11abb1a2905955624fd96d4b5de9bd52b8ff63e7a09586d45fccb6`  
		Last Modified: Thu, 16 Mar 2023 01:48:53 GMT  
		Size: 352.7 MB (352666511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16bf9fa945ae84016e893eb8062a6bc88989c9d3c48d2c93ab77f779e4065de`  
		Last Modified: Thu, 16 Mar 2023 01:48:22 GMT  
		Size: 3.9 MB (3889139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cdf00297a6d298240bfec6df9ab96b964d272dca72fa6e88744cc9267cf9bf`  
		Last Modified: Thu, 16 Mar 2023 01:48:21 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
