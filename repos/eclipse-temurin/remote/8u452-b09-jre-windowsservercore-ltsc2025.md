## `eclipse-temurin:8u452-b09-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:02038cba5fb8f1f05c53815b7a78504d9f80b7dfdf0289466847d4e1b9c5e8a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `eclipse-temurin:8u452-b09-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull eclipse-temurin@sha256:ab19eb8b5804f5f5e6aae47e5fef99f07bab357160507b0c4f6f0349d45e8e85
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3564357623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6492bd7255382a7b6e00c370269fed8d95adc46e0d453cf0c29276fc6410e1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Wed, 09 Jul 2025 18:08:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:08:28 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Wed, 09 Jul 2025 18:08:43 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_windows_hotspot_8u452b09.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_windows_hotspot_8u452b09.msi ;     Write-Host ('Verifying sha256 (aa75823c6dee1d65b53da6b1e9bd7de8a521e01f7e95dea2b5f104be0ee58242) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'aa75823c6dee1d65b53da6b1e9bd7de8a521e01f7e95dea2b5f104be0ee58242') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jul 2025 18:08:50 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
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
	-	`sha256:20ac8f4cf94500ed2bef53699a736302d0252c013726485bdb865c981d4cffaf`  
		Last Modified: Wed, 09 Jul 2025 19:09:39 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec5c6bc140135db7621d22f176ce8376c3b9af0b98e78fbc057dbb82663ab80`  
		Last Modified: Wed, 09 Jul 2025 19:09:40 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2af3ef37fe79919e201fec224b57bab7f6cc20ddd2c38f104d25b8999273f1`  
		Last Modified: Wed, 09 Jul 2025 19:09:48 GMT  
		Size: 72.8 MB (72791758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb12f70ffbe817abb7bf51cdec4cab1a57951ed0ce95cd20b4a4e0ee1ef4c45f`  
		Last Modified: Wed, 09 Jul 2025 19:09:48 GMT  
		Size: 389.9 KB (389919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
