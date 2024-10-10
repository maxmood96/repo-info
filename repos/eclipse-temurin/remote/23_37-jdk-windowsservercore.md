## `eclipse-temurin:23_37-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:1df4d925c26d5311ab9cb06249978cca607929c037623dd1e20091a13a868f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:23_37-jdk-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:7091351ef5099dd1b85289aa4ab28b37b7c2df2585cb00470a59f9abbec88232
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2197344556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6642097cafe5603b6b6ffeee06c9be341c632b2103ee646184cc6e24ac40bfe3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Wed, 09 Oct 2024 23:33:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Oct 2024 00:04:36 GMT
ENV JAVA_VERSION=jdk-23+37
# Thu, 10 Oct 2024 00:05:36 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_windows_hotspot_23_37.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_windows_hotspot_23_37.msi ;     Write-Host ('Verifying sha256 (39b7594580597ab85b3b4769d945e70d1665b3b8167c70039db407d2fb36803f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '39b7594580597ab85b3b4769d945e70d1665b3b8167c70039db407d2fb36803f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 10 Oct 2024 00:05:59 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 10 Oct 2024 00:06:00 GMT
CMD ["jshell"]
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
	-	`sha256:f6dd7a167e5d8024c2db3283a385811103c47c1e1349528ae29d41d1aa3117ae`  
		Last Modified: Thu, 10 Oct 2024 00:18:53 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b382d6d68061f3371be6f50b9b98bf213d56f8a3d84748b96d1d8aedb166a5d`  
		Last Modified: Thu, 10 Oct 2024 00:30:48 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa5962a6ee97cb71e6b190c38268166a54e657a332a64c77c9481a0827b8063`  
		Last Modified: Thu, 10 Oct 2024 00:31:16 GMT  
		Size: 397.7 MB (397711216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfcc433e08fc021b50ac6e01e08408460349ce1d42113d68d2636aa445dcfb1`  
		Last Modified: Thu, 10 Oct 2024 00:30:49 GMT  
		Size: 287.6 KB (287578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ae14abf3c3d4938bd1b477728a648b373d15bc6cc1205cafb0b476fb6677de`  
		Last Modified: Thu, 10 Oct 2024 00:30:48 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23_37-jdk-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:5b386f9723df3b53aaaf6984ab44fe5b7548858068062bed15e5835b2261df66
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303782206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025eef96b0ffc4d2e28764398e1ea64e33d9b37258e1ea8d69f2666262c5bd12`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Wed, 09 Oct 2024 23:35:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Oct 2024 00:06:19 GMT
ENV JAVA_VERSION=jdk-23+37
# Thu, 10 Oct 2024 00:07:32 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_windows_hotspot_23_37.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_windows_hotspot_23_37.msi ;     Write-Host ('Verifying sha256 (39b7594580597ab85b3b4769d945e70d1665b3b8167c70039db407d2fb36803f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '39b7594580597ab85b3b4769d945e70d1665b3b8167c70039db407d2fb36803f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 10 Oct 2024 00:08:12 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 10 Oct 2024 00:08:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71416d65806874920ade48cad9fe9e847b67ca207c59353ff136f87da9c117ce`  
		Last Modified: Thu, 10 Oct 2024 00:19:58 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874ec34a182588fcd8627fb781040f6f0b5dd20245d43f68e2dfd39c36f5222d`  
		Last Modified: Thu, 10 Oct 2024 00:31:26 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425231eb41ca02205326e1a362d74e6d0e3a35455910e52416f74cd120170bda`  
		Last Modified: Thu, 10 Oct 2024 00:31:56 GMT  
		Size: 397.7 MB (397693655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75fc3ec8248af47ccf590824afde4d34e8694b260acc508457d4460c5f44711`  
		Last Modified: Thu, 10 Oct 2024 00:31:27 GMT  
		Size: 4.3 MB (4259077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029703b883ff8c5c19d03663ee5ed3ae547646be8b66cbdc8d4eedc32c5815fd`  
		Last Modified: Thu, 10 Oct 2024 00:31:26 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
