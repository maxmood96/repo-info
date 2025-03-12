## `eclipse-temurin:11-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:02142d01b470c0646e35659d70f24fb7aaeb5e225949ba88e7bef6e155a60fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:11-jdk-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:946675874a7b32e3a552dbc386c2e2a397cc764bcd32116e6b43cd87a3a1ce09
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2521262488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5d44eb2ab950fc87930f469aa6da961e842a7a05df744190c29bd6755de49c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:53:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:53:08 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 12 Mar 2025 18:54:25 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_windows_hotspot_11.0.26_4.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_windows_hotspot_11.0.26_4.msi ;     Write-Host ('Verifying sha256 (25bc11bd05e4dad95ebefde017bd5eb29dfe8624bbd46beeca8eba4b4d77fae1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '25bc11bd05e4dad95ebefde017bd5eb29dfe8624bbd46beeca8eba4b4d77fae1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:54:35 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:54:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce318b55d5f1209100356531104716e5ad9b6fa793de69b47bb1e7fd68fe9d0`  
		Last Modified: Wed, 12 Mar 2025 18:54:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2728cd3d6b1bdf80335f86aa5e6cce91b5369b29aa8a8fbbc4d97bbcffff6fab`  
		Last Modified: Wed, 12 Mar 2025 18:54:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9efea3979f6b9e5a7c6bf749d29a6cd2af60690cf750c26d650a3ea9bf7e585e`  
		Last Modified: Wed, 12 Mar 2025 18:54:54 GMT  
		Size: 369.3 MB (369293803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d853b29989d9dac5424a62edbec05ea6a40eaba4ae6ac3e49c1259433b3187a3`  
		Last Modified: Wed, 12 Mar 2025 18:54:39 GMT  
		Size: 330.2 KB (330170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bfc4d2c839a1f0865c2b77e3dfae65a6422aad1c02708d81165a0807ffe569`  
		Last Modified: Wed, 12 Mar 2025 18:54:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
