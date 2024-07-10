## `eclipse-temurin:17-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:82346826a911d18a5bd100ce8355b61aca5e7a674b6612ce049de1a5e259e829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `eclipse-temurin:17-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:e7052fa69e9e4bad58b4d51564dff03a1fa79d9395551f29dc3ef8ac5398f815
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2214670947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6224e595c0952c4f2279b8ab1da9c84e4ee83411e20b0759ada4a465871fb808`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Wed, 10 Jul 2024 16:34:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 16:51:07 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 10 Jul 2024 16:55:59 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_windows_hotspot_17.0.11_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_windows_hotspot_17.0.11_9.msi ;     Write-Host ('Verifying sha256 (1244a2fc43e502758f16bd49de01fa60e89a94247eee41fa449db8f90ed5e682) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '1244a2fc43e502758f16bd49de01fa60e89a94247eee41fa449db8f90ed5e682') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Jul 2024 16:56:15 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d9de6992053b5598e6e6ffdf2a54d935d71057f5cc79ff86d167df37475ed8`  
		Last Modified: Wed, 10 Jul 2024 17:24:53 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c9319abca7932f83ef0014a5e4aa12b772428d475d6678faf1d6930f7becc6`  
		Last Modified: Wed, 10 Jul 2024 17:31:34 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a5108c52dd74e62f250c1f848e9491f2c477b2eae4a64d973350c76c701a91`  
		Last Modified: Wed, 10 Jul 2024 17:33:16 GMT  
		Size: 74.8 MB (74768475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2553fc57bdb3ebfea153c7164874478a026210ce7ed3f860d8672593922a13`  
		Last Modified: Wed, 10 Jul 2024 17:33:07 GMT  
		Size: 299.4 KB (299381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
