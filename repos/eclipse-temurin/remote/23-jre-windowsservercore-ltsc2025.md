## `eclipse-temurin:23-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:a11eeb76102bbcad7d8e96fa4dbb18dc55fdcdf39ff1704d0be24a267b04e4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `eclipse-temurin:23-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:1d5b3d38fd32389f18d68c265385c5ba28f7290eba0e38ddf96d62b2b323a359
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2584500660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e68ba5dced4d4d62da444a5583c186d3218fd8b4a0a38d8f87c4ca4b89ba43`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Fri, 31 Jan 2025 01:35:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:35:13 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Fri, 31 Jan 2025 01:35:29 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_windows_hotspot_23.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_windows_hotspot_23.0.2_7.msi ;     Write-Host ('Verifying sha256 (07ddf8b8d004692261d0ab769a31176abd22b5203cee44317328f9113a99e486) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '07ddf8b8d004692261d0ab769a31176abd22b5203cee44317328f9113a99e486') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:35:38 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4feda805cc910b20ad35875f9c399f5e411b198d10001e2933e4411c0c5c5ef`  
		Last Modified: Fri, 31 Jan 2025 01:35:40 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea937d872eb81b11103320fa34507a345f81b6e8a240cd938a60951a0e695aa`  
		Last Modified: Fri, 31 Jan 2025 01:35:40 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb37ab49d6f95950941963cda5bcd58d2e96858e311c498d93f995d443b67ed`  
		Last Modified: Fri, 31 Jan 2025 01:35:48 GMT  
		Size: 83.8 MB (83826556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd5589b0894a703c313129106b22f6f9001eb64e7323e6428a70d6cb44a55b2`  
		Last Modified: Fri, 31 Jan 2025 01:35:40 GMT  
		Size: 393.9 KB (393936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
