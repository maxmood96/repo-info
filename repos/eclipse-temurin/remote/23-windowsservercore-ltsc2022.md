## `eclipse-temurin:23-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:1efd3988a6c6cb5a871fdfea28dbc218fd2e99ed8fa959445a717745defd243e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `eclipse-temurin:23-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull eclipse-temurin@sha256:59b057c36cd2d1fd4a556aa1a57300fe861732edb616d2ec3b2e09b490a0b3cb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2652573215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4535d18bd498ca68153428e10206f926e542aa6c293c763c6b70027f628acf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:39:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:39:23 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 11 Dec 2024 20:39:54 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_windows_hotspot_23.0.1_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_windows_hotspot_23.0.1_11.msi ;     Write-Host ('Verifying sha256 (9ddd8db4b47de9ad2fa1de2db59a5ec2fef891c67eb28cef15c595e8d833ac25) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '9ddd8db4b47de9ad2fa1de2db59a5ec2fef891c67eb28cef15c595e8d833ac25') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Dec 2024 20:40:03 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:40:04 GMT
CMD ["jshell"]
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
	-	`sha256:9d9617f196b3d70661e483c34a7860a23977122a047fe0eea7c6d5f088e5a132`  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb95fc55ffeb62f98efa86d6e2826d633f4b2dd035ad7b508a1677aa298c2f6`  
		Last Modified: Wed, 11 Dec 2024 20:40:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ec8226b8a53845f0aaee96c20432c72f5be7c281d28c1b31cf134143fff338`  
		Last Modified: Wed, 11 Dec 2024 20:40:24 GMT  
		Size: 398.3 MB (398346639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0c942856999ceeed8d1358be8b3fc5f9191d00d9abe647e09842d58fbaf75f`  
		Last Modified: Wed, 11 Dec 2024 20:40:06 GMT  
		Size: 349.0 KB (349023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61701d10e7c949431d246fbf54a7c1445c9571f47144217fa12b450c2dc90177`  
		Last Modified: Wed, 11 Dec 2024 20:40:06 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
