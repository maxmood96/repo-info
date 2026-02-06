## `eclipse-temurin:25-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:d9440049755dd736402057eb1f5937e458d26565d64ecfc0ea843f2f4a769de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:25-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:05cfef4fcb09b47e9a2697cf90e7e4beeb13bc46409d5fb810c83567f95c2044
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1597169410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebd7ae4ef38abf687d486486b5e7f973f470ade26117393b77303888bea6f5d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Thu, 05 Feb 2026 22:21:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Feb 2026 22:21:09 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:21:56 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_windows_hotspot_25.0.2_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_windows_hotspot_25.0.2_10.msi ;     Write-Host ('Verifying sha256 (8344bfe9d2e161276f4956f6e8444dec444b631ca5d80c36657d9df4ba5643a2) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '8344bfe9d2e161276f4956f6e8444dec444b631ca5d80c36657d9df4ba5643a2') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-25' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 05 Feb 2026 22:22:02 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0115f8c37833a4648e1ed04b8b5ee8db788402d5d86e00d5c72d31cc892569fb`  
		Last Modified: Thu, 05 Feb 2026 22:22:07 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e720d70dd71980c08857be804809e470c8b10c51c77aac678947784a358c2220`  
		Last Modified: Thu, 05 Feb 2026 22:22:07 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4a99d426012ea8276b3c83e9017b94ddf86583264bc7ccca9fbb76733453ac`  
		Last Modified: Thu, 05 Feb 2026 22:22:17 GMT  
		Size: 101.0 MB (101006388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634501e21f39a598b925fec3bbd9b02e16576746b54d8149137bc9fa28aef10c`  
		Last Modified: Thu, 05 Feb 2026 22:22:07 GMT  
		Size: 400.1 KB (400138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
