## `eclipse-temurin:8u412-b08-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:1390b9a2a88f4456b7a7372f2dfc53592942bce7a5a4c3f1cc94d858446636bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `eclipse-temurin:8u412-b08-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:98d1dcac62b47e2a36838894a8c7948d6ecb6c721b99c0ed325e46703131c527
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212227553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea2c6ad94652c7bd99b6fb6858ca6772e1e28d26a794c6de71d6f060c3dbc08`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Wed, 10 Jul 2024 16:34:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 16:34:48 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Wed, 10 Jul 2024 16:39:48 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_windows_hotspot_8u412b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_windows_hotspot_8u412b08.msi ;     Write-Host ('Verifying sha256 (d6ab48ee1a4f4fa7f2d64e2ecffd2548b7116f7857f1d6352520ed1bb5fbc8f7) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd6ab48ee1a4f4fa7f2d64e2ecffd2548b7116f7857f1d6352520ed1bb5fbc8f7') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Jul 2024 16:40:04 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d9de6992053b5598e6e6ffdf2a54d935d71057f5cc79ff86d167df37475ed8`  
		Last Modified: Wed, 10 Jul 2024 17:24:53 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4dfd2309dea904665a300103ec26f9e01b82b4bd0b6e41b5c0b404d75d2111`  
		Last Modified: Wed, 10 Jul 2024 17:24:53 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f5aa67b87168b48b745b6ace8826a79b492aba1d0c0c07bd157596bd222c61`  
		Last Modified: Wed, 10 Jul 2024 17:28:41 GMT  
		Size: 72.3 MB (72333828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18aa4c58872d15c6fcbdca07c16bb9caad7a2f9d4134feafe73e170c41dcb393`  
		Last Modified: Wed, 10 Jul 2024 17:28:35 GMT  
		Size: 290.6 KB (290589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
