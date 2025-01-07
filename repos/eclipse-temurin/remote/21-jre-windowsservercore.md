## `eclipse-temurin:21-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:1229041cb2d02edbd2c98092fabf3251e20eb0c08c544a50227c4e43ec29b45c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `eclipse-temurin:21-jre-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull eclipse-temurin@sha256:60e229be4dc601d633f96d564beaae67de82403f03031b13ca7cd313288ce02a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338529451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46b8a1f246d3d57c1393151fd0eacb0a6b43012acf1d4ba9b894d9b3e76bc1d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:38:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:38:17 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 11 Dec 2024 20:38:39 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_windows_hotspot_21.0.5_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_windows_hotspot_21.0.5_11.msi ;     Write-Host ('Verifying sha256 (baa356843cbe2cbc8e49bad1cfef27eaaf5e59748a1627be40492804753c706a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'baa356843cbe2cbc8e49bad1cfef27eaaf5e59748a1627be40492804753c706a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Dec 2024 20:38:45 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2344c998e44cbbe25c00477391b425cf43013ed4a5ed66b6a3306fe10f63e050`  
		Last Modified: Wed, 11 Dec 2024 20:38:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095eb3928a39d3f2aa9ba196d515799a5bde8c4de6da12c9421ce89f8b89e98b`  
		Last Modified: Wed, 11 Dec 2024 20:38:47 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f364d334dbc2db304d04dbe067d61b1ba86941f22544a0866c9e4658e14ea5b6`  
		Last Modified: Wed, 11 Dec 2024 20:38:54 GMT  
		Size: 84.3 MB (84293074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f06e54e8b7b30c3e8e6497d6bfd03fca7960b9198955e015c2d4a2c5f58bd0a`  
		Last Modified: Wed, 11 Dec 2024 20:38:48 GMT  
		Size: 360.2 KB (360183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull eclipse-temurin@sha256:8b7c7240e3d91acdb423a159167a7a9e8a28ffa6654d1ff7e75d62e07f1b1958
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2102200876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d5c0e866c98b88e0501558df5b9707bf0b38b001d8d3ff86c3b6d5a5a119c1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:34:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:34:45 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 11 Dec 2024 20:35:31 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_windows_hotspot_21.0.5_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_windows_hotspot_21.0.5_11.msi ;     Write-Host ('Verifying sha256 (baa356843cbe2cbc8e49bad1cfef27eaaf5e59748a1627be40492804753c706a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'baa356843cbe2cbc8e49bad1cfef27eaaf5e59748a1627be40492804753c706a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Dec 2024 20:35:38 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b4a70a021def97f2942726c2a480986d39cf486b23ab2af138e46ea961f5f1`  
		Last Modified: Wed, 11 Dec 2024 20:35:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448065c567973356fd5d4aef7988493ec20f17e1ec460ca0a57d7799d7a85b1d`  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4ef64652264f96f31d04604c9611fa303257a18b02aa676adb5cdd91b8ab76`  
		Last Modified: Wed, 11 Dec 2024 20:35:49 GMT  
		Size: 84.4 MB (84424298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27c4f73db9b5b7a071838591cfaf12ccac159c925c2308697a1be4aca3b92cf`  
		Last Modified: Wed, 11 Dec 2024 20:35:43 GMT  
		Size: 3.6 MB (3603802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
