## `eclipse-temurin:8-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:12f3754894bfd10b34d34b8390a17ae87cae8fccfd869abbf9bf83874490c2c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `eclipse-temurin:8-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull eclipse-temurin@sha256:4037732169975431114894cfb97fc5ee9f70187cbff9d42c4ad3250c6cfd8cd9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1562012256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ad66e2a517ef87c069a80f5e0b3007dc42da6bb299798ddc9412fc9df62615`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:42:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:46:53 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Tue, 14 Oct 2025 20:47:04 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_windows_hotspot_8u462b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_windows_hotspot_8u462b08.msi ;     Write-Host ('Verifying sha256 (22a64b7531443577dd70eb244c943111121180dbf20a6a867452ed6da99b556d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '22a64b7531443577dd70eb244c943111121180dbf20a6a867452ed6da99b556d') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Oct 2025 20:47:10 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f2742f3144bf637c948400edbc59f380821c3a8b3f6172bcf5adec6fe214c8`  
		Last Modified: Tue, 14 Oct 2025 20:46:40 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead401bead5b35ab629cf6357258c03077a50f1fda1a2006ff114e303cd05d0e`  
		Last Modified: Tue, 14 Oct 2025 20:47:26 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a48179cdd8d02c51509876ce04444bf51ee17f7a176a69dbd300e1639947ee`  
		Last Modified: Tue, 14 Oct 2025 20:47:33 GMT  
		Size: 72.6 MB (72637906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a769d4f82aa304b96e430a38172ff0542dbaf0ef1f234bd0feafa9f770f90a`  
		Last Modified: Tue, 14 Oct 2025 20:47:26 GMT  
		Size: 352.6 KB (352579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
