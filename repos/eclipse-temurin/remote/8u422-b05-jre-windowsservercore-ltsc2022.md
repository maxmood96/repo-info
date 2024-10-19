## `eclipse-temurin:8u422-b05-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:30677db16cc1ae501e778c68ce48ebc19c389fa81c50e8da26dcb448cb230010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `eclipse-temurin:8u422-b05-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:ea2edbc8811ceee599a0c78a95373c2f36c9754395163a825a8dd917c7a79305
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1871650842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4415caf6fceeeae2808672363882eaba6a850ef53a790c75fda10db1c06f0d50`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Sat, 19 Oct 2024 01:01:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 19 Oct 2024 01:01:50 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Sat, 19 Oct 2024 01:02:19 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_x64_windows_hotspot_8u422b05.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_x64_windows_hotspot_8u422b05.msi ;     Write-Host ('Verifying sha256 (6a53b2e2e0eee6b238d79999e4de2fac70efc03922d48ea6d1007f50e7c11307) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6a53b2e2e0eee6b238d79999e4de2fac70efc03922d48ea6d1007f50e7c11307') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 19 Oct 2024 01:02:25 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977f76d957e3ecf8cf9341943f1b4a87fca8e9d6e93332497c4ae56dd8d49925`  
		Last Modified: Sat, 19 Oct 2024 01:02:29 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e6d7a9cadcd3d9e5e0c963c95b4c17ae663a6abfb6d69b3d33f05e8e3f2c4c`  
		Last Modified: Sat, 19 Oct 2024 01:02:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7599ff1b976ca46f68927e91cda4ec43ae714681f55b13cc677d2609e60245`  
		Last Modified: Sat, 19 Oct 2024 01:02:33 GMT  
		Size: 71.9 MB (71944913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25db15e966bf4a676e408c4ba85b23843c26e4b66214acece488a8f8a03c6908`  
		Last Modified: Sat, 19 Oct 2024 01:02:29 GMT  
		Size: 361.8 KB (361807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
