## `eclipse-temurin:21-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:95884cd99e2c013e3fc610adee1e5f3b979bc1a17a8b2d215a542416d0770959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:21-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:b20b65e217baca257b882e8d395a7c1a0f4dabf2ad37a9fd41141115929a55e8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2506523756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608c84fab69a4a88cda0cb9d726fafcfe7b31e47a292e2869fa1b767ec57328a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 31 Jan 2025 01:30:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:30:39 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Fri, 31 Jan 2025 01:33:23 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.6_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.6_7.msi ;     Write-Host ('Verifying sha256 (c361f8a018cffdad1ad0a0ce3e5032fc7314dec3f73642dc626a6121d487008b) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c361f8a018cffdad1ad0a0ce3e5032fc7314dec3f73642dc626a6121d487008b') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:33:34 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Fri, 31 Jan 2025 01:33:35 GMT
CMD ["jshell"]
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
	-	`sha256:67e474a66d2e55e5810d7ae9f19c64745d4070da8f136b3c443676b2d4bc69ae`  
		Last Modified: Wed, 05 Feb 2025 05:11:12 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15c1c0326093ac0ccef60ac7364f31e7f12e78848f4abf63f9881e836f31f60`  
		Last Modified: Wed, 05 Feb 2025 19:18:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffef294793c60fbd3e19d4f0c7b95c0868db8d47443657252a87675690c4e570`  
		Last Modified: Tue, 04 Feb 2025 03:06:25 GMT  
		Size: 380.3 MB (380265225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82f6d272e2c4b2826e343d43e30fd5338aa2e900cd4f4612e0df307851f4476`  
		Last Modified: Wed, 05 Feb 2025 04:40:01 GMT  
		Size: 4.0 MB (4042456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9604f5f1f8f84be6a04e4eb91beb260b554ee2fc76067c99987b428f6a2ec685`  
		Last Modified: Wed, 05 Feb 2025 04:36:55 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
