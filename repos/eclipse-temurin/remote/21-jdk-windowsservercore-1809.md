## `eclipse-temurin:21-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:f1b49f7674c3c1c07739822f16055383e1ac6a8187ac2a14d27d9a28323c3552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `eclipse-temurin:21-jdk-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull eclipse-temurin@sha256:085d78d18e4b735213ba6a5df692af681653cd59d66ee37f0f3af218f681d00a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2396737712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde94b224b0f00e9a0b66890c919651ec9ea58fa1e517bfb3dde4230b9ad3781`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:15:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:15:03 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Thu, 14 Nov 2024 20:16:10 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_windows_hotspot_21.0.5_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_windows_hotspot_21.0.5_11.msi ;     Write-Host ('Verifying sha256 (8ef78a37811529d73d37e29a9fa24bf2d46d0d5d97c4f6e403ea9adebc55eaf3) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '8ef78a37811529d73d37e29a9fa24bf2d46d0d5d97c4f6e403ea9adebc55eaf3') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 14 Nov 2024 20:16:19 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:16:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a8aa69ac885e601baf97420b587a4aa575eb82bb925804efbb0a6660b66e9c`  
		Last Modified: Thu, 14 Nov 2024 20:16:23 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7297ece79f1fe2c61997c9e39077a529d6ef2d87aa1f1545fdd3bc5d86186a5`  
		Last Modified: Thu, 14 Nov 2024 20:16:23 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7cb893dcd183d973afb21802973a29ce54e90a2cea157e40c5be90d77cbc98c`  
		Last Modified: Thu, 14 Nov 2024 20:16:39 GMT  
		Size: 382.0 MB (381991059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0b9eb3c2cfa599894c89209a061f14fa101b5296266d6098b0854423cf3d74`  
		Last Modified: Thu, 14 Nov 2024 20:16:24 GMT  
		Size: 4.1 MB (4088986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c6c1d3393b9939bed017a4ae84bc3ff3b54eac6ee51d25d1f87e0414e2c68c`  
		Last Modified: Thu, 14 Nov 2024 20:16:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
