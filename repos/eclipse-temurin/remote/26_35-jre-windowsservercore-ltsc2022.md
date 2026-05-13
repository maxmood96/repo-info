## `eclipse-temurin:26_35-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:88227a63582b4cce400fbb624c3af276f1222b497d40f1238328d5bd678230e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `eclipse-temurin:26_35-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull eclipse-temurin@sha256:3681268094eb3a1523425f2fa3ffde056b0deb3a8379c892dbc15abe8ebfae55
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2226901218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9310dd4df872203a9780b03b780d6621d6951f245ed2ef34c25f16726e442a38`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:37:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:50:51 GMT
ENV JAVA_VERSION=jdk-26+35
# Tue, 12 May 2026 23:51:20 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_windows_hotspot_26_35.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_windows_hotspot_26_35.msi ;     Write-Host ('Verifying sha256 (891d4a89535cb0d0451428aa9ce6d87908cc147113b38eef896de6a429052507) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '891d4a89535cb0d0451428aa9ce6d87908cc147113b38eef896de6a429052507') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-26' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 May 2026 23:51:30 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7a01241dffc0255c0d740f91d9866138ed91aa4d50cf1d48faeb8ec0d7ed11`  
		Last Modified: Tue, 12 May 2026 23:38:54 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc483dc6963280f1deee0bd2b0329fd5404857f94beb911d3fc9fe3f375df09`  
		Last Modified: Tue, 12 May 2026 23:51:34 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7c16823b5fc1a67dd189f569db0dd8db180821024bb6fa394361b018c9caf6`  
		Last Modified: Tue, 12 May 2026 23:51:44 GMT  
		Size: 104.1 MB (104124973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4ef39e2212115e1096d8feec9f20dd520c01082c6a80c0b546234b2a8fc085`  
		Last Modified: Tue, 12 May 2026 23:51:34 GMT  
		Size: 353.0 KB (353021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
