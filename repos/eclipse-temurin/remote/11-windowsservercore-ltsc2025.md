## `eclipse-temurin:11-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:b145291a2c21ada7737847da4519c14dbef46127ec752b21981f9c6731561103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `eclipse-temurin:11-windowsservercore-ltsc2025` - windows version 10.0.26100.4652; amd64

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
