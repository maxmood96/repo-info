## `eclipse-temurin:23_37-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:04b9ce5c38f7235ea3fd0a715c171f403da4dd5f1fa70700e828c1c30e2a40f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `eclipse-temurin:23_37-jre-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull eclipse-temurin@sha256:fb65962b38d03a252fc1bb65bee558477de7a1725c82e42d4aa9b74f02100adc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1808264300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2ac033887abd56626bbae5020c8ce118819c8d21337be8e139b7dd7fb15ba5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 18 Sep 2024 21:19:38 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 21:23:29 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_windows_hotspot_23_37.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_windows_hotspot_23_37.msi ;     Write-Host ('Verifying sha256 (90877250f1f0195cdb241f5c75068e70383d25895567416cde0201abf33efd3c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '90877250f1f0195cdb241f5c75068e70383d25895567416cde0201abf33efd3c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 18 Sep 2024 21:23:51 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:6ee82905aaa1094f1eb535b100b92e463b3af0cd4c3e41322799e86c24b1cc7d`  
		Last Modified: Wed, 18 Sep 2024 21:29:00 GMT  
		Size: 84.2 MB (84177038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088e7e826ce6bf938d80ecb1802d1e7f6828d5e297baf7bdac127ff39d36206b`  
		Last Modified: Wed, 18 Sep 2024 21:28:50 GMT  
		Size: 3.8 MB (3816085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
