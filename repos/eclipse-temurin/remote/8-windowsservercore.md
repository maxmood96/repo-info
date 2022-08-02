## `eclipse-temurin:8-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:5aa1a76be76c063f97f87f32def294a74eea92272358041e42396ebd5447f97b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.825; amd64
	-	windows version 10.0.17763.3165; amd64

### `eclipse-temurin:8-windowsservercore` - windows version 10.0.20348.825; amd64

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

### `eclipse-temurin:8-windowsservercore` - windows version 10.0.17763.3165; amd64

```console
$ docker pull eclipse-temurin@sha256:fa620c7c93b5a67233ee1edcefce94109dd14f4c2548642a7737118bd930a45d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2862237964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1e5f73669c010d6820370a1156122968b62244d5a167a46834f646a68a4178`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Aug 2022 18:18:00 GMT
ENV JAVA_VERSION=jdk8u342-b07.1
# Tue, 02 Aug 2022 18:19:41 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07.1/OpenJDK8U-jdk_x64_windows_hotspot_8u342b07.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07.1/OpenJDK8U-jdk_x64_windows_hotspot_8u342b07.msi ;     Write-Host ('Verifying sha256 (b13aea54b44802bf5caacc829e20e521659107331715aa6683e6926c67939133) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b13aea54b44802bf5caacc829e20e521659107331715aa6683e6926c67939133') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 02 Aug 2022 18:20:48 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92297cee9eff9d29a76894f6eb33574fc2d54f50a15d5768d85234919e6a82f5`  
		Last Modified: Tue, 02 Aug 2022 18:42:16 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b20c1b96af86a84a6507c1c1b8c02255a1b127b2ece6ce16122befcf7119ff0`  
		Last Modified: Tue, 02 Aug 2022 18:42:33 GMT  
		Size: 189.9 MB (189850743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401d08b70c66ffcf5e22f49d3be7cd48525b860e4c388449eb0423b209337d46`  
		Last Modified: Tue, 02 Aug 2022 18:42:16 GMT  
		Size: 340.6 KB (340627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
