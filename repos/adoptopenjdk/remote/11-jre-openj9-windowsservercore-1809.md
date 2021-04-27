## `adoptopenjdk:11-jre-openj9-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:9514937499c89a39df2c0f33624e61b6673c103bcb7be7eaa6b70ac2d01304f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `adoptopenjdk:11-jre-openj9-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull adoptopenjdk@sha256:3d2b95e1ae80ecb8f0e6a1296d2d1adf5be268f0fd74f2060e463f74439938bf
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2546029459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edc814c7e8933d7d802321b67706d1bcc37583fa3b9664e8dcab28f961c783b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 18:42:20 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Mon, 26 Apr 2021 20:09:49 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_windows_openj9_11.0.10_9_openj9-0.24.0.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_windows_openj9_11.0.10_9_openj9-0.24.0.msi ;     Write-Host ('Verifying sha256 (66bf50f000c1803a66ccd00ccb24dbfd18a69a14731e6eb8be48f9813a6cd841) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '66bf50f000c1803a66ccd00ccb24dbfd18a69a14731e6eb8be48f9813a6cd841') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {             Write-Host 'FAILED installing MSI!' ;             exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Mon, 26 Apr 2021 20:09:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841852f873b13d3dd878133ddab68b4cf2df29150ea67480397a1ee2060c3fc4`  
		Last Modified: Wed, 14 Apr 2021 19:36:02 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f21b9e30d649682c57aba8a11cbb0f750daaa7f735388df1c47c3dfb7a0e03d`  
		Last Modified: Mon, 26 Apr 2021 20:45:53 GMT  
		Size: 76.3 MB (76271289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75abc7f45e90921361fab0156c2c8be40ad60f4db81480b824c93669fbb781c5`  
		Last Modified: Mon, 26 Apr 2021 20:45:38 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
