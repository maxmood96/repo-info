## `eclipse-temurin:23-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:6679a8cf9cad72cfe91baf3beb11ab4a2a333209dd61ca5389e9353ae0ef0b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `eclipse-temurin:23-jdk-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull eclipse-temurin@sha256:2edfb4186637bd8a8c02ca4fa80e49aafd0ade9a5ed4650b8122d47d52216aa9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1860075659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f341d04b33600b60ea6dd786f0040fa5b8079292b5157b49d96c046247d8645f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:35:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 18 Sep 2024 21:17:40 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 21:18:58 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_windows_hotspot_23_37.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_windows_hotspot_23_37.msi ;     Write-Host ('Verifying sha256 (39b7594580597ab85b3b4769d945e70d1665b3b8167c70039db407d2fb36803f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '39b7594580597ab85b3b4769d945e70d1665b3b8167c70039db407d2fb36803f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 18 Sep 2024 21:19:23 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 18 Sep 2024 21:19:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0ff9a79ca5aec0b3e3be0c49c873a237847a9d74342acad1818e3f10647107`  
		Last Modified: Wed, 11 Sep 2024 01:13:29 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e7842774e6f3b7aa5d5da5f10556d5ee58d2ed3bcbaf492d583620158d1f45`  
		Last Modified: Wed, 18 Sep 2024 21:27:11 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27864acc7337b7cb76fc5edec0eebd608c60b1f2ca1f264dcb535b9a9e6627df`  
		Last Modified: Wed, 18 Sep 2024 21:27:39 GMT  
		Size: 397.6 MB (397589115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6907dc9c302cdb719291d9dbf059b8b0ee33455d1cb0f1bca646ef82863210b9`  
		Last Modified: Wed, 18 Sep 2024 21:27:11 GMT  
		Size: 289.9 KB (289930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92c8526b9b474e291135a9711122b994b95a8190f94175cf4853ce6461ac151`  
		Last Modified: Wed, 18 Sep 2024 21:27:11 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jdk-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull eclipse-temurin@sha256:9aab8f7c158779cb9f719aaab6f5acb4fc73050036a99c28314f7f3865dc6e9e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2122167023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a59b2b5285df578786ffb83348aae6f2a95664d0c275db96414e7dfcc072cec`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 18 Sep 2024 21:19:38 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 21:20:51 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_windows_hotspot_23_37.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_windows_hotspot_23_37.msi ;     Write-Host ('Verifying sha256 (39b7594580597ab85b3b4769d945e70d1665b3b8167c70039db407d2fb36803f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '39b7594580597ab85b3b4769d945e70d1665b3b8167c70039db407d2fb36803f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 18 Sep 2024 21:21:14 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 18 Sep 2024 21:21:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b681a22e2ab818abdc55dff7075266cbdad9e0c1d79f16a962cabde9559b4bc1`  
		Last Modified: Wed, 11 Sep 2024 01:17:09 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192c9af22a70bd2ee1407e227c80f7c4934714b6d6214e1008bb26b348abea39`  
		Last Modified: Wed, 18 Sep 2024 21:27:50 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de95d83b4e17ecaf1288e44541967dfe96fa5b8d1413dfa652797e798df2d37`  
		Last Modified: Wed, 18 Sep 2024 21:28:18 GMT  
		Size: 397.6 MB (397599420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d732337b574d8da4221f2c5031bd100c0174f7e3b7789febeb2b6eabb0f9af8e`  
		Last Modified: Wed, 18 Sep 2024 21:27:51 GMT  
		Size: 4.3 MB (4295034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12a6d345662dfc2e4b15deab3a384f423050710aa1a82389b245e140edc78ed`  
		Last Modified: Wed, 18 Sep 2024 21:27:50 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
