## `eclipse-temurin:21-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:c4df9c5a84b731f5da7450d1b789357ed33668480bf0197eb28c09276e7db4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:21-jre-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:65c6d6ebc72a948676e9228637028c9954363c50ceab26ea5915f79f5897f0f5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1988714471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c3d75c6dcb1556b6ef834167e49c44db1071f2dfdeb1782e41d5be93ef1574`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Sat, 19 Oct 2024 00:56:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 19 Oct 2024 00:56:18 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Sat, 19 Oct 2024 00:57:38 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_windows_hotspot_21.0.4_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_windows_hotspot_21.0.4_7.msi ;     Write-Host ('Verifying sha256 (cf5b9440680994f1571eb1b83fe017eafbec9e6e8a9cd033b3c099e967c1a553) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'cf5b9440680994f1571eb1b83fe017eafbec9e6e8a9cd033b3c099e967c1a553') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 19 Oct 2024 00:57:50 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:def9d05ebf335f0dc271d07ff2b6982a78099047ad66e9357734bae1357e1c3d`  
		Last Modified: Sat, 19 Oct 2024 00:57:53 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93398bba6243c5b41bcd6836dc0330ab442a705dc9d1f801eecf66f6f61e8611`  
		Last Modified: Sat, 19 Oct 2024 00:57:53 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76aad58eb6f2a6fdd00f1462f06c88b1a0d0fcbfca5901ea0c397df9c12f9cf2`  
		Last Modified: Sat, 19 Oct 2024 00:57:59 GMT  
		Size: 83.2 MB (83249819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fdf301136ad9a2bfbbe7955535e73ebf23816e35b3486a314ebe70d154a210`  
		Last Modified: Sat, 19 Oct 2024 00:57:53 GMT  
		Size: 3.6 MB (3636798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
