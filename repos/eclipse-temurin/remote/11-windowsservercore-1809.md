## `eclipse-temurin:11-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:ba84f7fa2ba26e50699ea0e1f19fe3064792638b75c6a67241340ad6c0a495a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `eclipse-temurin:11-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull eclipse-temurin@sha256:583594989efc2489b8c102ec479a5ed399b903509997ace5fc2126cdbbe7d6d7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2449901906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429dfa1358ffc2738ee14ab5d17819422b5451b02ca536ce225276f0a39448ba`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 19:49:02 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 14 Feb 2024 19:51:02 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.22_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.22_7.msi ;     Write-Host ('Verifying sha256 (a628fdaf29923f4cc2dfd3445369a4c1ce9c205bdf219a8ac33f809d489ffb6f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'a628fdaf29923f4cc2dfd3445369a4c1ce9c205bdf219a8ac33f809d489ffb6f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Feb 2024 19:52:21 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 14 Feb 2024 19:52:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bf91938139ed25d870a6124745064fd0e816088519f4dd240aaa559dfcfd19`  
		Last Modified: Thu, 15 Feb 2024 00:08:52 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1fbfb16e7a03acb37c1f6fd215fba5edf542dc5f2e364da60681bac6da9508`  
		Last Modified: Thu, 15 Feb 2024 00:09:20 GMT  
		Size: 369.2 MB (369161529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17071b38ed1f8c6d0dc2aa63d421bd7db53a02408280171e0920199c05f6490b`  
		Last Modified: Thu, 15 Feb 2024 00:08:52 GMT  
		Size: 287.3 KB (287301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89700f4e5c7ce7b1538caea5374869454ea0efee5806fe65c65ed609db84ae9e`  
		Last Modified: Thu, 15 Feb 2024 00:08:52 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
