## `eclipse-temurin:8u472-b08-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:27ba781c055877f6d7fff8ce9bb877c666c0cbc7fce2b53a50dd2beffae3be8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:8u472-b08-jre-windowsservercore` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:2c487f73f71caaa15cff6e90f75c4ed7999dc8946d0a06ffc626c1671d87f99f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1650364936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714524f33e24d1f71c376c2041c8ac56ccff5b1dabb7d462d2006abb3a809937`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Sat, 08 Nov 2025 17:55:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 08 Nov 2025 18:06:05 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 18:06:35 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_windows_hotspot_8u472b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_windows_hotspot_8u472b08.msi ;     Write-Host ('Verifying sha256 (2099c63f97bab0dea8c70fb2f32a7a8a2ad8e53167f0523f42c8f62d03bcc66a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '2099c63f97bab0dea8c70fb2f32a7a8a2ad8e53167f0523f42c8f62d03bcc66a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 08 Nov 2025 18:06:42 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc465f19c1be9fa244763193421ce6a938df14e90c8844c65c79ad3b5cca4e6`  
		Last Modified: Sat, 08 Nov 2025 18:05:13 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3577035f25bfd7297e7cce16ea2be7202e8c2bceac315ca3dd169de317f72313`  
		Last Modified: Sat, 08 Nov 2025 18:07:03 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cbcbdb32f4a185471d8f7125a6b32c0c73ebd3ffc5efd50573f0daab8c40e12`  
		Last Modified: Sat, 08 Nov 2025 18:07:09 GMT  
		Size: 72.8 MB (72802827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f0f5a1d32de466969b5b05681c102eb616d42c33070595db4c2ed9a7e10431`  
		Last Modified: Sat, 08 Nov 2025 18:07:04 GMT  
		Size: 366.5 KB (366537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
