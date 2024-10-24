## `eclipse-temurin:17-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:90246a35ff3acb042b5f8a91a476efe66b84e51fa6cb1934962290c446b1b3bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:17-jre-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:2fa82c0ee32d08f2696de7c04b5aa93d458d7b548cdc113851e5e927609d4b74
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1981016427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63686c2d54a17fbd5582d2e4e640b4313730d8dd1046212ae0133d8edee4303c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 24 Oct 2024 00:56:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 24 Oct 2024 00:56:42 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Thu, 24 Oct 2024 00:57:39 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_windows_hotspot_17.0.13_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_windows_hotspot_17.0.13_11.msi ;     Write-Host ('Verifying sha256 (457194f803be9129eaa2f0d50ac62bbd6182bf4923f91000199d936fa04e40e4) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '457194f803be9129eaa2f0d50ac62bbd6182bf4923f91000199d936fa04e40e4') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 24 Oct 2024 00:57:50 GMT
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
	-	`sha256:4f945977e3d252bfe5c1a05ea49e33db9b160d48d0d6ff54dfbc1852a27f0052`  
		Last Modified: Thu, 24 Oct 2024 00:57:53 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e04fba0598c7d611ba6bac5ad2ed3d1cadd559e29acb87dfb53018e1c976dd`  
		Last Modified: Thu, 24 Oct 2024 00:57:53 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd92f0fdaf0f48b572ea783159a4f29b77d480f86712c110867eedcabdb8c30`  
		Last Modified: Thu, 24 Oct 2024 00:57:58 GMT  
		Size: 75.9 MB (75949102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23eb8c4e5aa94daef69480f37d8124e0d88e27f55e456f97f2dd0a6cc675c249`  
		Last Modified: Thu, 24 Oct 2024 00:57:53 GMT  
		Size: 3.2 MB (3239472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
