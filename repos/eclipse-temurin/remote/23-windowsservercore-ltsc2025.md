## `eclipse-temurin:23-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:67fbc2de27d549d7d80e8ca9a7ef9ec369f05d657094c05fc5b25aee3f9302f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `eclipse-temurin:23-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:3bb1f49a47f9f245d9f2d42d72998506b0c1befbac4a0bb9fe58a03371d31b86
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2899078422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bacfcbf8bd5f40333d4c2f87efca04af2340f00a581e6bfcbdd7d12078a81033`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 18:31:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 18:31:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 22 Jan 2025 18:31:58 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_windows_hotspot_23.0.1_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_windows_hotspot_23.0.1_11.msi ;     Write-Host ('Verifying sha256 (9ddd8db4b47de9ad2fa1de2db59a5ec2fef891c67eb28cef15c595e8d833ac25) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '9ddd8db4b47de9ad2fa1de2db59a5ec2fef891c67eb28cef15c595e8d833ac25') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 22 Jan 2025 18:32:09 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 22 Jan 2025 18:32:10 GMT
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
	-	`sha256:1930f12eee6418df702f0fd736e641fbd62c4008523bb20ec159cefbcfd96131`  
		Last Modified: Wed, 22 Jan 2025 18:32:14 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83d695a446a1c88e3b1ae92306022ff51f9161f2ac5f28c31876f02550d64ed`  
		Last Modified: Wed, 22 Jan 2025 18:32:14 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa50e3b9161e54440e4697073768a37c8e3fa3789e1a224ddc942c87c9cf441`  
		Last Modified: Wed, 22 Jan 2025 18:32:33 GMT  
		Size: 398.4 MB (398394151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150fb8bc78b69f3e024f444fc984db46939c042d68c075e17282aa05d45c0e7b`  
		Last Modified: Wed, 22 Jan 2025 18:32:14 GMT  
		Size: 402.7 KB (402702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9cb616de1d279a2c9634b6054a73807a42d37d7420c99b703a2c873157b575`  
		Last Modified: Wed, 22 Jan 2025 18:32:14 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
