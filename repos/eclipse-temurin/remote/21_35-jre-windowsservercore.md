## `eclipse-temurin:21_35-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:28b6f31ed458fef9631f12469c6f52495ceb9549b3a91fe8d83feb283f3f19ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2031; amd64
	-	windows version 10.0.17763.4974; amd64

### `eclipse-temurin:21_35-jre-windowsservercore` - windows version 10.0.20348.2031; amd64

```console
$ docker pull eclipse-temurin@sha256:13a26e338ba3525cf1c2b73406e3ecadbf2421828955d0a9777a10060bf78c44
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1943499793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f30948d94a275e7e2c007044cb65c7dc7f376858476ee3490d80e3f35ecee3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 17:33:14 GMT
ENV JAVA_VERSION=jdk-21+35
# Wed, 11 Oct 2023 17:39:00 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jre_x64_windows_hotspot_21_35.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jre_x64_windows_hotspot_21_35.msi ;     Write-Host ('Verifying sha256 (8668c6733296da59d38c140d692539be4f2e9b19a2360685ef8612273de065a0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '8668c6733296da59d38c140d692539be4f2e9b19a2360685ef8612273de065a0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Oct 2023 17:39:20 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75fd06c305b130cd43db7daa07edec8ba83ad9b9012fcd6d6dd88a717f4f1e2`  
		Last Modified: Wed, 11 Oct 2023 17:46:50 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4fb883f53710a2a84190227593aae4dcac4c198a22a5945877e6a32d41a303`  
		Last Modified: Wed, 11 Oct 2023 17:49:02 GMT  
		Size: 83.4 MB (83375603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1f0b3916245a2d61064f3035ae84525c10e8000b986942ccd802e5a4d6c00f`  
		Last Modified: Wed, 11 Oct 2023 17:48:51 GMT  
		Size: 278.4 KB (278401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21_35-jre-windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull eclipse-temurin@sha256:b93914473c5590caea34f55f8c2645856306ddc422f271b5cc6dc762801b1bd7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2118582988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ee001728308578fc53e662a7b02f4de57fb82399ae5c9fe56d789295c23c83`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 17:34:42 GMT
ENV JAVA_VERSION=jdk-21+35
# Wed, 11 Oct 2023 17:40:49 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jre_x64_windows_hotspot_21_35.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jre_x64_windows_hotspot_21_35.msi ;     Write-Host ('Verifying sha256 (8668c6733296da59d38c140d692539be4f2e9b19a2360685ef8612273de065a0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '8668c6733296da59d38c140d692539be4f2e9b19a2360685ef8612273de065a0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Oct 2023 17:41:55 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26c12848d469db2241a06d186840577de0744b88357c91115183b9974ddeaf3`  
		Last Modified: Wed, 11 Oct 2023 17:47:32 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf203f1cae6bbedbd99853446d14441b534349180d7017d728f73e15e3909be`  
		Last Modified: Wed, 11 Oct 2023 17:49:22 GMT  
		Size: 83.4 MB (83415629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57eb7ef16ba7ed7a009a93d6663a3ddb4722cc8aa2f6b0024d73f8cc1c9501d6`  
		Last Modified: Wed, 11 Oct 2023 17:49:12 GMT  
		Size: 3.6 MB (3574133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
