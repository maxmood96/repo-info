## `eclipse-temurin:25_36-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:1d47f54d511d776328de968f850426bbd5633ba68a7f173ba5eed28115cb8aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `eclipse-temurin:25_36-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:9543e8d2b06ab8ca53eac0f482dc8c86083fa2eae5e2efa0e1a71b1d21508abb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3321627682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9dd15669a04350d510aa59a2045c2e0e2b96c00bd4d46e8e61b2e20c2e690`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:12:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:23:22 GMT
ENV JAVA_VERSION=jdk-25+36
# Fri, 24 Oct 2025 18:23:44 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_windows_hotspot_25_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_windows_hotspot_25_36.msi ;     Write-Host ('Verifying sha256 (eeae2fb19dc8d778a324d9b5c879f7afe9732487516807b75584436b01e0d8c3) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'eeae2fb19dc8d778a324d9b5c879f7afe9732487516807b75584436b01e0d8c3') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-25' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 24 Oct 2025 18:23:51 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5671b9b9319b80bc4a875153412928ecb5a5ecafe14f3becfb08c54de7c6c3b`  
		Last Modified: Fri, 24 Oct 2025 19:07:14 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35420b0ac69c2a7d756d9ab116d8ec6ad1a930d4e1051b01a7599c8ab249baa9`  
		Last Modified: Fri, 24 Oct 2025 18:24:15 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80297a9af1c5e2ca9d2f03b36d0e5243ebab2a660e1a1c5092772ddc2be3fec3`  
		Last Modified: Fri, 24 Oct 2025 18:24:30 GMT  
		Size: 100.9 MB (100933614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55aa27bae798c4a65cf535499c5fdbef2bb44f989c11a1130374ea8783a2b328`  
		Last Modified: Fri, 24 Oct 2025 18:24:15 GMT  
		Size: 344.5 KB (344482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
