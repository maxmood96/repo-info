## `eclipse-temurin:11-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:dafad39e9ca0a5bab68fda83596093a09547323f8853c972d13c7c844c3fa15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:11-jre-windowsservercore` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:d1d79be2ea1fd7b26b36daf761a14b924374893c22b3fa1d39c8bd20a6fae06b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2205699386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502bd7a98c827dff130c163f7fc41fdcdb2294964ba72cb8e2cbf806ae489a0d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Wed, 29 Apr 2026 22:46:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 Apr 2026 22:46:44 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 23:01:26 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_windows_hotspot_11.0.31_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_windows_hotspot_11.0.31_11.msi ;     Write-Host ('Verifying sha256 (a047f90b4520cbd53cc74647aff1f23844299e85e3c469159735801e097208ff) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'a047f90b4520cbd53cc74647aff1f23844299e85e3c469159735801e097208ff') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 29 Apr 2026 23:01:32 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a14b1ab823928f463b4116f5097425013fadfeafe8e1197e48a6fc31d0b442f`  
		Last Modified: Wed, 29 Apr 2026 22:48:31 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58ee3f9682c5208560950643c27df8146f711f6a0d2052c02808cb8d06d226d`  
		Last Modified: Wed, 29 Apr 2026 22:48:31 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce0ef27dc50a55f31cdf375059b4a1846697c866d1b202138b6f3cadfae94ff`  
		Last Modified: Wed, 29 Apr 2026 23:01:42 GMT  
		Size: 75.3 MB (75324230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57174b15f56733801f5eee3c9484e1bb60db9ab021c2f1e5f416def7ff6f4b2b`  
		Last Modified: Wed, 29 Apr 2026 23:01:36 GMT  
		Size: 386.5 KB (386522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:ecfdc8f0319dd9bcd3543a581dfd6bcbbcce031ace05fca49e1015a1de5dca96
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2145887649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc3f9a940b75a5712cec639abce9cd2243f2bf68e1ce04b81796bcf6a84e9e0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Wed, 29 Apr 2026 22:49:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 Apr 2026 22:49:59 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 23:06:32 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_windows_hotspot_11.0.31_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_windows_hotspot_11.0.31_11.msi ;     Write-Host ('Verifying sha256 (a047f90b4520cbd53cc74647aff1f23844299e85e3c469159735801e097208ff) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'a047f90b4520cbd53cc74647aff1f23844299e85e3c469159735801e097208ff') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 29 Apr 2026 23:06:38 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881adac9baa303e4738660f9fd178c83fa652492d7841586a9540b0b9e48a059`  
		Last Modified: Wed, 29 Apr 2026 22:51:48 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b1435f2a41e52c0b48b7092d8e05efae8a7f09d9133aea2ed7a9f6f67f770`  
		Last Modified: Wed, 29 Apr 2026 22:51:48 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d43717ff255418775bf3e1b93038c5351aac3f4d6aab6d996d81132a161122`  
		Last Modified: Wed, 29 Apr 2026 23:06:49 GMT  
		Size: 75.3 MB (75307086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97771a0e3f931989a06751d1a91e67de24974c256978de755ee1b2a3882f083`  
		Last Modified: Wed, 29 Apr 2026 23:06:42 GMT  
		Size: 366.7 KB (366698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
