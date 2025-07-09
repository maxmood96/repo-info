## `eclipse-temurin:11-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:89b5ce37b9ed8b2691fceebb9f43bef37303771d5c5a6ed209a2acf6403cf57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4652; amd64
	-	windows version 10.0.20348.3932; amd64

### `eclipse-temurin:11-jdk-windowsservercore` - windows version 10.0.26100.4652; amd64

```console
$ docker pull eclipse-temurin@sha256:8982bb40da70d82953803bc059b3e830ca12410e4d64733a135c34ca2d1d7cb1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3860918748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce31a389877c3526e2900b03ac50387e78a23c84425ca403d82806d52414057`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Wed, 09 Jul 2025 18:08:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:08:45 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 09 Jul 2025 18:09:09 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_windows_hotspot_11.0.27_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_windows_hotspot_11.0.27_6.msi ;     Write-Host ('Verifying sha256 (b34003048c6c3341ff0911663dc5d80822ffdb895b2fe4b6640ae39afa89b4ad) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b34003048c6c3341ff0911663dc5d80822ffdb895b2fe4b6640ae39afa89b4ad') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jul 2025 18:09:18 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:09:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f56408cf68d0471cc97623bef863553013a62827ffe7f756c8f59c7781472df`  
		Last Modified: Wed, 09 Jul 2025 19:09:15 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73538c0e95c144f5b4883384efad6b6744e9a3bc31563bfea41bec01fb7e5037`  
		Last Modified: Wed, 09 Jul 2025 19:09:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f750b2794b7a6f393954d5ee1386ccbed7b2dd1b58a472bf33a3e0f54596849a`  
		Last Modified: Wed, 09 Jul 2025 19:09:29 GMT  
		Size: 369.4 MB (369364255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57aa38eb7be7f32ee921010f5a63870553620e03417cdff6980876fb84fef7f`  
		Last Modified: Wed, 09 Jul 2025 19:09:31 GMT  
		Size: 377.3 KB (377324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed043111dcb3b2ece037200e48e5c446d1432ad43ced579abcb02c0610c8181e`  
		Last Modified: Wed, 09 Jul 2025 19:09:34 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-windowsservercore` - windows version 10.0.20348.3932; amd64

```console
$ docker pull eclipse-temurin@sha256:70e0fdf5a60eb5874e5377254fb418dfc6ad2126ad2dd3531c184bc35841da5e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2650275278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9be402b56583f837cf062cf954cce30a4c3a7c18c6d29394fad41110292cca5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Wed, 09 Jul 2025 18:07:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:07:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 09 Jul 2025 18:07:28 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_windows_hotspot_11.0.27_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_windows_hotspot_11.0.27_6.msi ;     Write-Host ('Verifying sha256 (b34003048c6c3341ff0911663dc5d80822ffdb895b2fe4b6640ae39afa89b4ad) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b34003048c6c3341ff0911663dc5d80822ffdb895b2fe4b6640ae39afa89b4ad') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jul 2025 18:07:37 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:07:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223b45c41b9524d6dd731f85f2d5a673eaeafa3e0fb8fcaf78524cff8da9a009`  
		Last Modified: Wed, 09 Jul 2025 19:08:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17fc76e02e9040430be223b8d7c3b356cd1231b77b258345ef2ac448e1e6686`  
		Last Modified: Wed, 09 Jul 2025 19:08:19 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf13c19d6aa036f98fe9a2571cdf60390fb2fec8faeb99f77bde72d3c48b8766`  
		Last Modified: Wed, 09 Jul 2025 19:08:51 GMT  
		Size: 369.3 MB (369318954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99476f6478492ae3f392f7548ee5f16b086905d2534004033e3376767a758cbe`  
		Last Modified: Wed, 09 Jul 2025 19:08:20 GMT  
		Size: 349.0 KB (348985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7b5f7fa45e3bc729fdcba12132c415bd05bbea3b56962a0ad6d21f5eddb566`  
		Last Modified: Wed, 09 Jul 2025 19:08:20 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
