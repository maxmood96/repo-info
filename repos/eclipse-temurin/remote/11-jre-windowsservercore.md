## `eclipse-temurin:11-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:279f4728b19262a7285f9c036468608891b6fef7db96a10383e703cab72d83cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `eclipse-temurin:11-jre-windowsservercore` - windows version 10.0.20348.2849; amd64

```console
$ docker pull eclipse-temurin@sha256:ce395cf244f3c422b6c1ca40879334bba06100710079c32b9464132cef7c4e9c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328633020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af8501eccd9894673379c8c7fbd37bc5a4c0a11ae0c29f6229b5f018adda50a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 20:18:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:18:35 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 14 Nov 2024 20:18:55 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_windows_hotspot_11.0.25_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_windows_hotspot_11.0.25_9.msi ;     Write-Host ('Verifying sha256 (577f448ffe2737633bdc2a02e5c53ecccaf3317274b7013b6eb25e9de1934a79) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '577f448ffe2737633bdc2a02e5c53ecccaf3317274b7013b6eb25e9de1934a79') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 14 Nov 2024 20:19:04 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b8b6467eab66d67f4d1ef5e828de45929ba55d89426054a3c32c71ba0d4220`  
		Last Modified: Thu, 14 Nov 2024 20:19:06 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4beb746d935d538f64ce621e387b583efeb743e01cf63e5d392afcc563d718`  
		Last Modified: Thu, 14 Nov 2024 20:19:06 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204175a1491eae1dd298b247d0a358a46043e00b58d2da3ee30b47ca79f7ecb3`  
		Last Modified: Thu, 14 Nov 2024 20:19:12 GMT  
		Size: 75.8 MB (75784220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b83023574e5830d204bc05ebe92a27f7094c225fda6e32e066f7c746b249637`  
		Last Modified: Thu, 14 Nov 2024 20:19:07 GMT  
		Size: 362.0 KB (362000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull eclipse-temurin@sha256:33cb3b633820107ead831c12736b6b25962784cffc6fbbe1d77e242f4739a97d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2086918565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83845b6487600065d8ea2ec845dc24fdd2f483c8691f3c3ed9726021559a896e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:11:14 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 14 Nov 2024 20:11:44 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_windows_hotspot_11.0.25_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_windows_hotspot_11.0.25_9.msi ;     Write-Host ('Verifying sha256 (577f448ffe2737633bdc2a02e5c53ecccaf3317274b7013b6eb25e9de1934a79) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '577f448ffe2737633bdc2a02e5c53ecccaf3317274b7013b6eb25e9de1934a79') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 14 Nov 2024 20:11:52 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834f176126dd2e5af491ab069e71c6f6fa1e80c713dce34770e4528666343f19`  
		Last Modified: Thu, 14 Nov 2024 20:11:56 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84396109cb56b77c86ae50f2c86069180884056d54a958bc6a3edab4f65c1ce`  
		Last Modified: Thu, 14 Nov 2024 20:11:56 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed361b9d22848c19670033d14aabed3ec88f66b1602dc4739608d36525d538a1`  
		Last Modified: Thu, 14 Nov 2024 20:12:02 GMT  
		Size: 75.9 MB (75925117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec07b6e809a5996bc13bc2a60fb824609eb26cba509c07117cc1c260bb9000af`  
		Last Modified: Thu, 14 Nov 2024 20:11:56 GMT  
		Size: 337.1 KB (337052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
