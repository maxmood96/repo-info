## `eclipse-temurin:23-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:51a43054508467cbd2652bbbdd6a0a04d116050e01bc4901f3e4db8448fd22c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:23-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:8a33d6c986eff28409965e266201cd7397b12e609133ef1ec61ec9872183d49d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2552855372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9b19748635e7772b0f62751f900c7ee5d64b5e755fbe1f07d598194562f47c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:49:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:49:43 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Wed, 12 Mar 2025 18:50:46 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_windows_hotspot_23.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_windows_hotspot_23.0.2_7.msi ;     Write-Host ('Verifying sha256 (e4ef33439c2dc725387fce4d57ed63794785c0d3ab55726bdc9861c0387dc3a0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e4ef33439c2dc725387fce4d57ed63794785c0d3ab55726bdc9861c0387dc3a0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:51:01 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:51:03 GMT
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
	-	`sha256:9fc451c3bcd98cd4d390e0794757811b5a78322acff722636d5ac2c686de8734`  
		Last Modified: Wed, 12 Mar 2025 18:51:07 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468cb03b340452c7e8142c91182d390259044a0387b76e731e1da4df78487eb7`  
		Last Modified: Wed, 12 Mar 2025 18:51:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbf53e62395e893ec06af77488c974fc68c72c74fedf3bd7eb588bc35ec3298`  
		Last Modified: Wed, 12 Mar 2025 18:51:24 GMT  
		Size: 396.9 MB (396859888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484116a22a7b76ff327fc000deac2120574c1d9a838ede99ff3aa358a97353b1`  
		Last Modified: Wed, 12 Mar 2025 18:51:08 GMT  
		Size: 4.4 MB (4356803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af269c85567427ce2e93a8af0bb4429d6235b2a5b8e3020dc6f4ec934b7cc14`  
		Last Modified: Wed, 12 Mar 2025 18:51:07 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
