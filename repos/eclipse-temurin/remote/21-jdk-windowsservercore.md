## `eclipse-temurin:21-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:73cf3746248105791160140ac31d5c5639db418a7a3979847e89cf998d0cac32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:21-jdk-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:a62d8829ec08e665ec0d50b915f192f6a1bbf2cc2f45eea83029634d384d28c6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2880983735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103ac930ee81b2ed8355e76623c61e4d4ef2b96817a11ce515b8e0f7d37b88ad`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Fri, 31 Jan 2025 01:33:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:33:48 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Fri, 31 Jan 2025 01:34:13 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.6_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.6_7.msi ;     Write-Host ('Verifying sha256 (c361f8a018cffdad1ad0a0ce3e5032fc7314dec3f73642dc626a6121d487008b) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c361f8a018cffdad1ad0a0ce3e5032fc7314dec3f73642dc626a6121d487008b') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:34:23 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Fri, 31 Jan 2025 01:34:24 GMT
CMD ["jshell"]
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
	-	`sha256:63ec8a7a62a5c0b7ea4e8854ad627c12f97f083c92617c355bc39d0a717ae5d1`  
		Last Modified: Fri, 31 Jan 2025 01:34:30 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d2edc7a5fd83bfbad533a7152f92fbe80ffeed538345963814dc40c187c330`  
		Last Modified: Fri, 31 Jan 2025 01:34:30 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa3adc83d4edeeb963fc69b2dc70d4eaec1d541c0baa56e76de6901d54d7eab`  
		Last Modified: Fri, 31 Jan 2025 01:34:48 GMT  
		Size: 380.3 MB (380298694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aabeffcd27546ccbbd0cd7a5575078421317fdfccb8dbcc07380eb298744a2eb`  
		Last Modified: Fri, 31 Jan 2025 01:34:30 GMT  
		Size: 403.6 KB (403563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d104faa5d155c8f92e6a84c845f5ca18806243b2b557345873dc4ec3ea4d566e`  
		Last Modified: Fri, 31 Jan 2025 01:34:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:e87b291d65f398806dd73339b4a98f168b651d764f39b716c9433d63334b0e0d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2642984983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2355c2c9b71a2bd56f0a31d6483e80e42bb48230501082634bf90a42b0583ea4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Fri, 31 Jan 2025 01:30:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:30:27 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Fri, 31 Jan 2025 01:31:59 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.6_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.6_7.msi ;     Write-Host ('Verifying sha256 (c361f8a018cffdad1ad0a0ce3e5032fc7314dec3f73642dc626a6121d487008b) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c361f8a018cffdad1ad0a0ce3e5032fc7314dec3f73642dc626a6121d487008b') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:32:06 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Fri, 31 Jan 2025 01:32:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ef35d8451ff7043288b1d7ea9e46373bb16f6bd4ea644732bddb768a6b09e8`  
		Last Modified: Fri, 31 Jan 2025 01:32:11 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3096365e861edf5e7faa24006f34c11caa7139697a3ab7047be586eb71f8ed09`  
		Last Modified: Fri, 31 Jan 2025 01:32:11 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8cf8a7b4c1fd9d9c9711e7e322ef1108b1fc470841d2c8264158a675d27eac`  
		Last Modified: Fri, 31 Jan 2025 01:32:26 GMT  
		Size: 380.3 MB (380269568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12aac0cd455a50e3c08b2c1d1f1eed1448505900bc5d6f0ea75043684e3717c8`  
		Last Modified: Fri, 31 Jan 2025 01:32:11 GMT  
		Size: 326.3 KB (326257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95ef555b14cae6a07e340a27de41decada96f1976a7233f1c831859de927019`  
		Last Modified: Fri, 31 Jan 2025 01:32:11 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-windowsservercore` - windows version 10.0.17763.6775; amd64

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
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e474a66d2e55e5810d7ae9f19c64745d4070da8f136b3c443676b2d4bc69ae`  
		Last Modified: Fri, 31 Jan 2025 01:33:38 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15c1c0326093ac0ccef60ac7364f31e7f12e78848f4abf63f9881e836f31f60`  
		Last Modified: Fri, 31 Jan 2025 01:33:38 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffef294793c60fbd3e19d4f0c7b95c0868db8d47443657252a87675690c4e570`  
		Last Modified: Fri, 31 Jan 2025 01:33:53 GMT  
		Size: 380.3 MB (380265225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82f6d272e2c4b2826e343d43e30fd5338aa2e900cd4f4612e0df307851f4476`  
		Last Modified: Fri, 31 Jan 2025 01:33:38 GMT  
		Size: 4.0 MB (4042456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9604f5f1f8f84be6a04e4eb91beb260b554ee2fc76067c99987b428f6a2ec685`  
		Last Modified: Fri, 31 Jan 2025 01:33:38 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
