## `eclipse-temurin:8-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:91ae99848a287740d010e7209ebba55fd3776c12d9f570a624e5099d31cc1983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:8-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:0a37fa0def53d80061cb5c4a0ced0005c2ac2bf9a32a188b3fc8da641a5f1514
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2465354694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cc99ebaf0ce5bfd591c2d439d46946a116e8fef9c0bf6df73e12b36dd4c87d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Mon, 28 Apr 2025 20:16:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 28 Apr 2025 20:16:30 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 28 Apr 2025 20:16:58 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u452b09.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u452b09.msi ;     Write-Host ('Verifying sha256 (989f085584ca58701eab2d2b2f5576b7594325f0a6f85572b34586774963c46c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '989f085584ca58701eab2d2b2f5576b7594325f0a6f85572b34586774963c46c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Mon, 28 Apr 2025 20:17:05 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841c1837aaf4e097c06cf73170e665d8b313122d7f4280773de65804e8a64511`  
		Last Modified: Mon, 28 Apr 2025 20:17:08 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8c322a3cda57cca43426c84f861914768e15e887482f3583d1dd2961464223`  
		Last Modified: Mon, 28 Apr 2025 20:17:08 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62257b16b9c450d090574c2ac7ef36e38ab53b991c89eca79a7936864ce75a2`  
		Last Modified: Mon, 28 Apr 2025 20:17:16 GMT  
		Size: 191.4 MB (191397193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7e7566d7165354df76d7005779ae8e40f55710fb60797155916887ef53830a`  
		Last Modified: Mon, 28 Apr 2025 20:17:08 GMT  
		Size: 372.4 KB (372391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
