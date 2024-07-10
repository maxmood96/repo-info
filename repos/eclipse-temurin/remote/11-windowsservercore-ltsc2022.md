## `eclipse-temurin:11-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:395ffa172c59c155a52b6b2e07080b96b99776d68f854799c8e1f3439e99ed46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `eclipse-temurin:11-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:575706e986c0dac9c3ea0ba42bcba8cb751dec6779c34ad44c5ccb35a953f48c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2509098267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df62e8fa81a88955402b03b49bedb7bb6ee4b786c14e4d5289557f71f9b5ef3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Wed, 10 Jul 2024 16:34:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 16:42:43 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 10 Jul 2024 16:43:31 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.23_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.23_9.msi ;     Write-Host ('Verifying sha256 (cacbe31a3921e52f4ff6d031d6f37d8a7c58f20a136fccf1754565f8aa403ed8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'cacbe31a3921e52f4ff6d031d6f37d8a7c58f20a136fccf1754565f8aa403ed8') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Jul 2024 16:43:48 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 10 Jul 2024 16:43:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d9de6992053b5598e6e6ffdf2a54d935d71057f5cc79ff86d167df37475ed8`  
		Last Modified: Wed, 10 Jul 2024 17:24:53 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b94af5f035b8d908620e5de7901c26a70405488feba65d86964a93e37fa34aa`  
		Last Modified: Wed, 10 Jul 2024 17:29:17 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e348079271003c87bfca39cb88c0bd1c22d984d4e0245bc5f43f9a0043030d81`  
		Last Modified: Wed, 10 Jul 2024 17:29:38 GMT  
		Size: 369.2 MB (369203253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41b001a5665deaf1759e45da98980b109dbfd1e10620f957f6aeb5a047a3be4`  
		Last Modified: Wed, 10 Jul 2024 17:29:18 GMT  
		Size: 290.5 KB (290477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d49bb5129aa43bd4c9000d54b393d24f9834954a788e0202c158800afc037cf`  
		Last Modified: Wed, 10 Jul 2024 17:29:17 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
