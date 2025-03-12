## `eclipse-temurin:21-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:09f140b581291127414462cdcd7d369bf123fcba3bc5417f38f258b4def49f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `eclipse-temurin:21-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:e1556e55dd6d8ce6a9702347ec571b589aa71b65948f5d0647594e9f58a79d17
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3289317412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed0264f4fea478d53e23fcbccec7593f02b5afe4949667ba80b23932bf6c109`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:48:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:48:19 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 12 Mar 2025 18:48:45 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.6_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.6_7.msi ;     Write-Host ('Verifying sha256 (c361f8a018cffdad1ad0a0ce3e5032fc7314dec3f73642dc626a6121d487008b) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c361f8a018cffdad1ad0a0ce3e5032fc7314dec3f73642dc626a6121d487008b') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:48:53 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:48:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df8daf6a650f2bc06e062c5cec319d9210ed269c0556597ccd6343764604993`  
		Last Modified: Wed, 12 Mar 2025 18:48:58 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8388d3eaaa5368118865dc0540c29759901dd1187dff19fff95fc41f32167f5`  
		Last Modified: Wed, 12 Mar 2025 18:48:57 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b8417d3f7cd49ece52c6f08cba2771c21a05675ffeb0025ef91f9dd6f07093`  
		Last Modified: Wed, 12 Mar 2025 18:49:16 GMT  
		Size: 380.3 MB (380284999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32c1b47df85e2abd6df5fdb689ba4d335d5a23cb54b2aac8b6ad9fb7dd2caf4`  
		Last Modified: Wed, 12 Mar 2025 18:48:58 GMT  
		Size: 380.7 KB (380711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028f273bc09dd24e62d1b347f4c0480746d8ec8967eb002e49fbedb75196a01a`  
		Last Modified: Wed, 12 Mar 2025 18:48:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
