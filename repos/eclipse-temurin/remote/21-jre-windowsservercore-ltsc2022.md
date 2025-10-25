## `eclipse-temurin:21-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:cbc637c87c455f260235016e8862a14243873ad010fd9e50d53df61d6f4b527c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:21-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:b21e7d080104c5d4e547d38816965364de4bae32de547b0f1006faae08128fe8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1661254476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c0f22683350e71d3dddd162b0e687fb3d407acbe0f4e9c0b723bce4fb0eca3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:21:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:22:07 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 24 Oct 2025 18:22:24 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_windows_hotspot_21.0.8_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_windows_hotspot_21.0.8_9.msi ;     Write-Host ('Verifying sha256 (9e38a94eed115fb834c2c4375bc493cef1a47e28c82bd83f623efe3fca017e7a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '9e38a94eed115fb834c2c4375bc493cef1a47e28c82bd83f623efe3fca017e7a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 24 Oct 2025 18:22:31 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:0be850ed281f5fa2f86d2844f03995e9477820d84349da6d62f3b664e565028e`  
		Last Modified: Fri, 24 Oct 2025 18:21:57 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf5ceddb2359fe2b46b634a7433eee256ead26cf95a4243d1841dfc263e971f`  
		Last Modified: Fri, 24 Oct 2025 18:22:51 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99c4cb0a49bfeb9cdcea102d20b6b07a8d0e0289cdd049c4538c340cd71a933`  
		Last Modified: Fri, 24 Oct 2025 18:23:00 GMT  
		Size: 83.7 MB (83706579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ea5e061c7012949a7f8088eb53f5d0c6561e877b674b750aa78a357b21d357`  
		Last Modified: Fri, 24 Oct 2025 18:22:51 GMT  
		Size: 352.3 KB (352308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
