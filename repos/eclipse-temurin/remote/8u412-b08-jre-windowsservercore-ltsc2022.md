## `eclipse-temurin:8u412-b08-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:719283ed42294d90932f52cd470ef182ec1149f876b7efa337762a9ee5a91a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `eclipse-temurin:8u412-b08-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:ac1a130c6b5c216b1f75e5bd65c4943b3660e45c3e179add14f13466766c4039
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2072129008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2418c52414f68532f95a2c927c0bfd938e89c4f4af2bf6b35257aa60d934f2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Apr 2024 18:24:15 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Wed, 24 Apr 2024 18:31:53 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_windows_hotspot_8u412b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_windows_hotspot_8u412b08.msi ;     Write-Host ('Verifying sha256 (d6ab48ee1a4f4fa7f2d64e2ecffd2548b7116f7857f1d6352520ed1bb5fbc8f7) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd6ab48ee1a4f4fa7f2d64e2ecffd2548b7116f7857f1d6352520ed1bb5fbc8f7') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 24 Apr 2024 18:32:15 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae08009ce6846b1be32bf9468bb898d772e37a19009d0d952a0eaf42686dff90`  
		Last Modified: Wed, 24 Apr 2024 19:32:34 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad68f63fdcf43bb65b7dbe2b5351911991d6333dfd036af962ceea93ab0d573`  
		Last Modified: Wed, 24 Apr 2024 19:33:59 GMT  
		Size: 72.5 MB (72467621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea833ec3c613e5cf83ec33ba44992ab45818e0b08435dc901f84e16cebb306aa`  
		Last Modified: Wed, 24 Apr 2024 19:33:51 GMT  
		Size: 285.0 KB (285027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
