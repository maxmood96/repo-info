## `eclipse-temurin:25-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:3aa7a9d6f67ba9900a8ab5e557889f9b7a0cd9e28e289f34ed5b31bbcb45b972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `eclipse-temurin:25-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull eclipse-temurin@sha256:cb03c245c2a910bc09447d40b34b4b78f34dc97ea0017cef8330135715abaa53
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1964066945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb19161260bbeff051dd3187d32db0bccf5ea4f1d80c8f68e9a9d80e65f7a74`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Tue, 10 Feb 2026 23:03:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 23:03:05 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 10 Feb 2026 23:04:06 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_windows_hotspot_25.0.2_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_windows_hotspot_25.0.2_10.msi ;     Write-Host ('Verifying sha256 (8344bfe9d2e161276f4956f6e8444dec444b631ca5d80c36657d9df4ba5643a2) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '8344bfe9d2e161276f4956f6e8444dec444b631ca5d80c36657d9df4ba5643a2') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-25' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Feb 2026 23:04:13 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c278d4f704add38ce9a551afe6146e2259f519e8e9f3d39fcc43830804d0d5`  
		Last Modified: Tue, 10 Feb 2026 23:04:17 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5bc77cf30a4e005c4cfcadc3e344eaa2ec4380320412dc0422f115a6957833`  
		Last Modified: Tue, 10 Feb 2026 23:04:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8eedf6e6cb01ab9dac9c930b3525fac2445a1a3cdafa9dd35fd9e2957be7bd3`  
		Last Modified: Tue, 10 Feb 2026 23:04:27 GMT  
		Size: 101.1 MB (101065900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf2c033cfeb96f08422919e5d20429b30c5e30f085a739e3cc426477e4a3f36`  
		Last Modified: Tue, 10 Feb 2026 23:04:17 GMT  
		Size: 341.3 KB (341272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
