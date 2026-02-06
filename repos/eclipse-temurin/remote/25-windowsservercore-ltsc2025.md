## `eclipse-temurin:25-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:0ed32f407cb213d4053a66741afd8b55a21acee9290649f633cfb0d1a6e6e502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:25-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:e2b8ef4a3086c60294fa59717b1c1b5e77ef74af5622346beefe7b234ca6f874
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1749736432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d242af8acd330250c16149fe067488cbdc701ddedf4a31570743f42a459236a9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Thu, 05 Feb 2026 22:21:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Feb 2026 22:21:02 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:22:01 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_windows_hotspot_25.0.2_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_windows_hotspot_25.0.2_10.msi ;     Write-Host ('Verifying sha256 (c433b59ab42630634657ae273940183c2f95a115dd5bf6846a70dcd0a42b9c0d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c433b59ab42630634657ae273940183c2f95a115dd5bf6846a70dcd0a42b9c0d') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-25' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 05 Feb 2026 22:22:07 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 05 Feb 2026 22:22:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca757c7ea41e4227529ce38856c7839aa2b082427fa3cff69504cd31f47fc1f6`  
		Last Modified: Thu, 05 Feb 2026 22:22:12 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8286988760cc133eb263c463a0fd2202de326180a6881a8f992fc7748dc3c22d`  
		Last Modified: Thu, 05 Feb 2026 22:22:12 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50940b9690111ac307baef5514d8996d23033d0047014d95ae037e3fd4967a0c`  
		Last Modified: Thu, 05 Feb 2026 22:22:30 GMT  
		Size: 253.6 MB (253572518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0857f6e20c4c11a38c822b98d2189fff35d7cebd0da365d10d9876c91244d14`  
		Last Modified: Thu, 05 Feb 2026 22:22:13 GMT  
		Size: 399.7 KB (399736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88ec58546217aad252efb04fd27f57900166f79d635f60aac0ac11bb43c73cf`  
		Last Modified: Thu, 05 Feb 2026 22:22:12 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
