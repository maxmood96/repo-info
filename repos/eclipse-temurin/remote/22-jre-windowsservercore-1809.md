## `eclipse-temurin:22-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:a6bab3f7ea790615e7ae5b00227074d3606e40e6d88f347d1a3bf9863e9438b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:22-jre-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:04ac93d9a7f7016e48c200d4e22ba0f72e00a143f9f8800f519e6b73d7b0c152
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325259791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ad0a1c344f3615e661fd2407161f2f90f33756e079af114febab74457c34a1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 16:36:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 17:10:01 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Wed, 10 Jul 2024 17:15:44 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jre_x64_windows_hotspot_22.0.1_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jre_x64_windows_hotspot_22.0.1_8.msi ;     Write-Host ('Verifying sha256 (6d918aa3c1cbad4c70afe9563f057dcf39b3c2dff2ae01e44e1e89f237399d96) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6d918aa3c1cbad4c70afe9563f057dcf39b3c2dff2ae01e44e1e89f237399d96') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-22' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Jul 2024 17:16:39 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396e1b977f1ec2790de6e1bcdd9b0272d3ab46f70fdbef2ae277b7f99b83d0b3`  
		Last Modified: Wed, 10 Jul 2024 17:26:34 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e373da1aea31b6837945fcfd0b8d5686a47d1941334576e282ba2eaaf851e6`  
		Last Modified: Wed, 10 Jul 2024 17:36:59 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a63ed268e8dec12a6cce9e3c97d0d439f731bd8b61235a2517d641044df0aba`  
		Last Modified: Wed, 10 Jul 2024 17:38:25 GMT  
		Size: 83.2 MB (83239400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf808d494710005c302bef651a4646328d469833ea581ab5f496d4fbec02a8b`  
		Last Modified: Wed, 10 Jul 2024 17:38:17 GMT  
		Size: 3.6 MB (3588189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
