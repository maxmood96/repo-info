## `eclipse-temurin:21-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:27fabc4c7e6a17512c2a74ba8a3b4c81dc8b8bccb1be254e6fbb66f19f3e62e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `eclipse-temurin:21-windowsservercore` - windows version 10.0.20348.2529; amd64

```console
$ docker pull eclipse-temurin@sha256:b946bb25b6dc7c90bfa054ebe4b3c8f9b72c83c18b7416bbd620b262c824a45a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2498934507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84730f47206f049be6df64a8828fcdfb61e1cea12087ebdfb382e188914b7030`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Sat, 22 Jun 2024 00:33:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Jun 2024 00:43:37 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Sat, 22 Jun 2024 00:44:42 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_windows_hotspot_21.0.3_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_windows_hotspot_21.0.3_9.msi ;     Write-Host ('Verifying sha256 (264db89e74213f3ea2d7b7379d1c2ac346797d03b4d88cbf4ce72c3ff96477a1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '264db89e74213f3ea2d7b7379d1c2ac346797d03b4d88cbf4ce72c3ff96477a1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 22 Jun 2024 00:45:09 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Sat, 22 Jun 2024 00:45:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4326efd24d64d6a2efa78c581696b3d528dfcf784a3d6605e621e343b62e16`  
		Last Modified: Sat, 22 Jun 2024 00:59:51 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2789df543302a6ab2c7c38b2605ae77577dfe09c69ea045c10ed0f990f72547`  
		Last Modified: Sat, 22 Jun 2024 01:04:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6d41fb5b7ea4c9b4c9a73a43e362e84a3cf4c66292b3cfecbb7f95d546acb1`  
		Last Modified: Sat, 22 Jun 2024 01:04:48 GMT  
		Size: 380.5 MB (380462971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a66472824f7da1bf433a30428250fb8077d96304e22bf0b3fba34ee79109d7`  
		Last Modified: Sat, 22 Jun 2024 01:04:21 GMT  
		Size: 277.0 KB (276983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287810d7e17169fa0f33585bf4fb025fe4c9c74bf9ba66d1a1f1ffa9b3313cfd`  
		Last Modified: Sat, 22 Jun 2024 01:04:21 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull eclipse-temurin@sha256:be8c908ca40c8354e736519d3f4fbedd4a3970de9072a58e1bd8186be9197057
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2605324139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942d14001bf9bf4528f2bbf66c36e4471a8f417f2891765bf2e270600f91f716`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 17:37:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:07:58 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Wed, 12 Jun 2024 18:09:49 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_windows_hotspot_21.0.3_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_windows_hotspot_21.0.3_9.msi ;     Write-Host ('Verifying sha256 (264db89e74213f3ea2d7b7379d1c2ac346797d03b4d88cbf4ce72c3ff96477a1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '264db89e74213f3ea2d7b7379d1c2ac346797d03b4d88cbf4ce72c3ff96477a1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Jun 2024 18:11:02 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 12 Jun 2024 18:11:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04390472505d81fa325a5cfd00620c5caa18dd222dd0a98f7a089b8c65b438b`  
		Last Modified: Wed, 12 Jun 2024 18:39:01 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd22fd39d9cc4b79e4554419d2061f07be851a1e5995390c6fdf8b83fd6c0a0`  
		Last Modified: Wed, 12 Jun 2024 18:48:00 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c11a48ac500c0f4abc4a6a4ddc06cfede72c9145372e363df740a2ab77d78e`  
		Last Modified: Wed, 12 Jun 2024 18:48:28 GMT  
		Size: 380.6 MB (380624744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45b53a18157a52ca1839551dac717c067a3239b2e9cbe430390d1e11a2eff04`  
		Last Modified: Wed, 12 Jun 2024 18:48:01 GMT  
		Size: 4.0 MB (4013918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1c4bc13323d83179a3a0423d80586ef5c2eec78ac73e23e52ef237b474288a`  
		Last Modified: Wed, 12 Jun 2024 18:48:00 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
