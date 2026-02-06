## `eclipse-temurin:11-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:bffcf38aaef475b3988578b0ae18a22bdc67c387bbcf087666a2da8185c80f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:11-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:007f569642bec356913e11dabbc1d74c843d3accbfdb2c47f25b73aecf2cda86
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1865769596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff81411f106005272233e2877b0270e707b166701f041239cb42c01f32942d0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Thu, 05 Feb 2026 22:16:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Feb 2026 22:16:15 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:17:06 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.30_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.30_7.msi ;     Write-Host ('Verifying sha256 (5a7e985d6e89c864cf176c9ebf919ab1e97b40877b8e5290e4c51f532e37d1c2) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '5a7e985d6e89c864cf176c9ebf919ab1e97b40877b8e5290e4c51f532e37d1c2') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 05 Feb 2026 22:17:13 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 05 Feb 2026 22:17:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1e0ce08e6c73cde467e407194ecbb0f5fa417d35a5760864c23004fb38e5ca`  
		Last Modified: Thu, 05 Feb 2026 22:17:17 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f164f684fda543aa221000673c51dc3e37c5a85346c0274779857369d0def549`  
		Last Modified: Thu, 05 Feb 2026 22:17:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1384370c46a6b0f02963720773118c384c7007a051b2ae5f3aed8987f369935d`  
		Last Modified: Thu, 05 Feb 2026 22:17:37 GMT  
		Size: 369.6 MB (369595519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6a7976e68a84ec605dd3809835ca48e9275a2cfb8c375b80f2e29b477c5ece`  
		Last Modified: Thu, 05 Feb 2026 22:17:18 GMT  
		Size: 409.9 KB (409850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09466828393ef4bb04ddb5302c2e5aa28543e0525ac0a5a179f342f4a6dfd4b`  
		Last Modified: Thu, 05 Feb 2026 22:17:18 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:6bfb5db872b546855e5272527098d2d57325439a6aaf436d30948b644d2f79e6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2205687777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1b8c819d78269b6f02c6dc75d432010014d47446b7e212a8858ab3027ef970`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Thu, 05 Feb 2026 22:17:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Feb 2026 22:17:44 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:18:58 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.30_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.30_7.msi ;     Write-Host ('Verifying sha256 (5a7e985d6e89c864cf176c9ebf919ab1e97b40877b8e5290e4c51f532e37d1c2) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '5a7e985d6e89c864cf176c9ebf919ab1e97b40877b8e5290e4c51f532e37d1c2') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 05 Feb 2026 22:19:03 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 05 Feb 2026 22:19:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13aea86ebfc8b62e40288794b04f1db17a58538a5841b2c6c05e0f5f262cd5dc`  
		Last Modified: Thu, 05 Feb 2026 22:19:08 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0225a3903a776ff92d7bdd9ec7f331ff95a6a2b227da41e061bc9fc17e200d8`  
		Last Modified: Thu, 05 Feb 2026 22:19:08 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea2ac6a2e2c6523efcdba702042e391da23b8a7a670bcc082ff588412b4c36d`  
		Last Modified: Thu, 05 Feb 2026 22:19:26 GMT  
		Size: 369.7 MB (369669324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ca038053708cff02c8317eed289fb23dce2ab6805f82f02f25c784dc1ed41a`  
		Last Modified: Thu, 05 Feb 2026 22:19:08 GMT  
		Size: 355.4 KB (355404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636369f2f30ccb7a8531244458f86bc5692e9747c17f67998efa576fc9e6363b`  
		Last Modified: Thu, 05 Feb 2026 22:19:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
