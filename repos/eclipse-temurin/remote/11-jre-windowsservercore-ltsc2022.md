## `eclipse-temurin:11-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0a27683c657a3d096b15d6c1ba28d96d52a5b80f2c4c7bf397f8eaf4ce762d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:11-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

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
