## `eclipse-temurin:11-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:e0fc303dba85aa8972eea2dad138addf46bef15c0fe783bb6d91a28225830d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `eclipse-temurin:11-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull eclipse-temurin@sha256:52ac368ce6ce13c84e0d3d4f27858b1bbb4a856541c40120c6e3b97b6335a6b0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1855312491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f0318b3708470e244e63e86b85b7dc4d75cae962d26d9c03f39a0c7c0c8719`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:40:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:40:41 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 09 Dec 2025 20:41:08 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_windows_hotspot_11.0.29_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_windows_hotspot_11.0.29_7.msi ;     Write-Host ('Verifying sha256 (2113628e4feb65cc5e399c34bd1a070f8c8b931ef2899b8a7f7ac3179a3d24ce) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '2113628e4feb65cc5e399c34bd1a070f8c8b931ef2899b8a7f7ac3179a3d24ce') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 09 Dec 2025 20:41:15 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6381426f6db953d9a70cba6759e20f0456f0b12bdb617e9dc982295e4d1c410`  
		Last Modified: Tue, 09 Dec 2025 20:41:33 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15d3773c489ce3a40d450630348e8ed36187e4b22df8bc2ca8c967fc4cd688a`  
		Last Modified: Tue, 09 Dec 2025 20:41:33 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02a2a9978d254fe910fd1f3ed68e73b6b47e0c1d86e5d1f8327c1b85a426f7f`  
		Last Modified: Tue, 09 Dec 2025 20:41:38 GMT  
		Size: 75.1 MB (75078151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67559498d28819a34e36d82e60a2ab6f3fdaf9fc5f6e2ef0093cfafd5bf4d40c`  
		Last Modified: Tue, 09 Dec 2025 20:41:33 GMT  
		Size: 352.4 KB (352437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
