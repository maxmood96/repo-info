## `eclipse-temurin:8-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:80bd329b85751493c11dcdd42873b2b90170d4bb19a6213b62ad6550c856c2bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.825; amd64

### `eclipse-temurin:8-windowsservercore-ltsc2022` - windows version 10.0.20348.825; amd64

```console
$ docker pull eclipse-temurin@sha256:fd25942da11827091cb101da60ff4a376778c35151ae5e4fb9f9f449d6b713de
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2490900971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b11f056961687cf3206ec4cb5a30fafa579c0884a7f06df1b2d1e2d59261a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Aug 2022 18:16:17 GMT
ENV JAVA_VERSION=jdk8u342-b07.1
# Tue, 02 Aug 2022 18:17:11 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07.1/OpenJDK8U-jdk_x64_windows_hotspot_8u342b07.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07.1/OpenJDK8U-jdk_x64_windows_hotspot_8u342b07.msi ;     Write-Host ('Verifying sha256 (b13aea54b44802bf5caacc829e20e521659107331715aa6683e6926c67939133) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b13aea54b44802bf5caacc829e20e521659107331715aa6683e6926c67939133') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 02 Aug 2022 18:17:44 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da18b9f2fed96ac9c619df2e3c5b9f7843c52d1032f49f54f452f3cb3ece7d18`  
		Last Modified: Tue, 02 Aug 2022 18:41:47 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4ded67399627205ef5f0d8837a41da39fff3b17a1befcc71bbb6a0a0b08c88`  
		Last Modified: Tue, 02 Aug 2022 18:42:04 GMT  
		Size: 190.1 MB (190095614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab96e3e098d715b4ef2bcb9c82d17d02638981ae889e1b42b8d92b2660f3204`  
		Last Modified: Tue, 02 Aug 2022 18:41:47 GMT  
		Size: 571.0 KB (570984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
