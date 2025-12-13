## `eclipse-temurin:21-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:94e9a30790efb7e5e2a4a70f74ea1315ab8d24ef23d6a5b6628c9dd82a642f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `eclipse-temurin:21-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull eclipse-temurin@sha256:75f881e7e44eb4028c6d74eee9200c23e93de9dd959698f9aaa2de0c90ccbf7d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1863969410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeac427cba82a0bbf0f1d2e1042e5f629536bd5190290da311e5230b701e0785`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:40:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:41:12 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Tue, 09 Dec 2025 20:41:33 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_windows_hotspot_21.0.9_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_windows_hotspot_21.0.9_10.msi ;     Write-Host ('Verifying sha256 (56b167659821fe125ea3b2974b0da1bac725b886b77193629d8ef880d38517e1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '56b167659821fe125ea3b2974b0da1bac725b886b77193629d8ef880d38517e1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 09 Dec 2025 20:41:40 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8168617ee10fc15e3adb5c56ebdabfa52e263ba4a71565a1bb5e5a80bf05dad0`  
		Last Modified: Tue, 09 Dec 2025 20:41:03 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab96a6bead4425e00e395d8ee613c31e1799ea3ed529b9bfdd40e30e35bd2e4c`  
		Last Modified: Tue, 09 Dec 2025 20:42:00 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b79cbf410212efe57db9d4cb3b6c41e751e6d3e3d7c237d6b665a35f18443cf`  
		Last Modified: Tue, 09 Dec 2025 20:42:10 GMT  
		Size: 83.7 MB (83735433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46458dcc6515cdef37810ff001503439b4af102b7473ea76e7f456748f2594e`  
		Last Modified: Tue, 09 Dec 2025 20:42:01 GMT  
		Size: 352.1 KB (352078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
