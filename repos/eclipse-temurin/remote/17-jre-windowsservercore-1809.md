## `eclipse-temurin:17-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:40041ebfedd5e01e154a8d7df5a8fa63a37d08cf0f46287d3d504252641be1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:17-jre-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:a2ea0408b47fc7e522a14ba59f46704076e71c8f0f8c4d6f00ba6e1e70eedde6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2200572563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b4e35445426addedbca6cc495c51ffc413b5b0279fc25d6fd0a534f93e7a1b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 31 Jan 2025 01:29:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:29:31 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 31 Jan 2025 01:30:37 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_windows_hotspot_17.0.14_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_windows_hotspot_17.0.14_7.msi ;     Write-Host ('Verifying sha256 (6a81df58247baeec4153e746b68af5b8618e50ed51a59b4c9e0c1b025edd4ad8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6a81df58247baeec4153e746b68af5b8618e50ed51a59b4c9e0c1b025edd4ad8') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:30:47 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 20:54:32 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2ab6ec680291fceadd8103b9f5bbad1baed7814d3043299e33ad042c4ce638`  
		Last Modified: Wed, 05 Feb 2025 22:44:29 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b06d2db8a1d2e53b02f217cd5bd660ece62f7fc0516630db7c8274dcbb13b42`  
		Last Modified: Wed, 05 Feb 2025 22:44:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45b1f7ef5bed886a078156e6cc2b822ec5083eb3435dbcb6768296e2643074c`  
		Last Modified: Wed, 05 Feb 2025 22:44:35 GMT  
		Size: 75.1 MB (75098654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972dcccadc00ca03db7954b757c3c1766c2226ea692f0fa48ca2b93c06c241d8`  
		Last Modified: Wed, 05 Feb 2025 22:44:35 GMT  
		Size: 3.3 MB (3259118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
