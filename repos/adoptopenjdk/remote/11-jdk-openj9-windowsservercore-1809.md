## `adoptopenjdk:11-jdk-openj9-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:2419a9e024da232c1b8230cd9c053db075a627bcebe9ee9872d68484adc7fa08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `adoptopenjdk:11-jdk-openj9-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull adoptopenjdk@sha256:60e7253bbe69d5634c0e1f61103163ec533f9a27c49cbfedc72bdc3c15c3c940
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2643686898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5707fa4a92f46cfb584b4e89961b45999711e570e9bca143986740d6baeffd46`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Apr 2020 20:55:15 GMT
ENV JAVA_VERSION=jdk-11.0.7+10.1_openj9-0.20.0
# Fri, 24 Apr 2020 20:57:46 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.7%2B10.1_openj9-0.20.0/OpenJDK11U-jdk_x64_windows_openj9_11.0.7_10_openj9-0.20.0.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.7%2B10.1_openj9-0.20.0/OpenJDK11U-jdk_x64_windows_openj9_11.0.7_10_openj9-0.20.0.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (386e33d5b3bb9ed01b3b96e4d68933cc50d87deca7cfbdc8d360929340de16d5) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '386e33d5b3bb9ed01b3b96e4d68933cc50d87deca7cfbdc8d360929340de16d5') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Fri, 24 Apr 2020 20:57:47 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Fri, 24 Apr 2020 20:57:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edc29de224149bd438350512f7a31a67edbd3fcafce757aa60620dc459c184ad`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a685af93d026561da63b43fce230ac34bf02fe05fec296bc697f1b636353cf`  
		Last Modified: Fri, 24 Apr 2020 21:27:08 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be75d1613245c92cf68d316627fc51eb06acd4c6a9aa9f5f5a1272c49f821c4a`  
		Last Modified: Fri, 24 Apr 2020 21:27:35 GMT  
		Size: 373.0 MB (372975156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5a3072a2a85b151f61440ff7ab1a867b5300b785fc7cd495fd733b5751e989`  
		Last Modified: Fri, 24 Apr 2020 21:27:08 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a76da95655801c6838954f2e54d4c5710bdf872940605462354d7761526831e`  
		Last Modified: Fri, 24 Apr 2020 21:27:08 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
