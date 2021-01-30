## `adoptopenjdk:openj9-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:4482ac4c58be42492fd81b7f8ab5517149c06c392211961150d230fff24896d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `adoptopenjdk:openj9-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull adoptopenjdk@sha256:9d1ecec75531117a0bb83bed77e7a6d45707a8fdf1194c06daa4c983c2766986
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2818748961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b0c0b98cf230d669b24a3fb4c5f3cc685cc355696ef18de35c8770bf0b8f350`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 30 Jan 2021 02:01:36 GMT
ENV JAVA_VERSION=jdk-15.0.2+7_openj9-0.24.0
# Sat, 30 Jan 2021 02:04:02 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.2%2B7_openj9-0.24.0/OpenJDK15U-jdk_x64_windows_openj9_15.0.2_7_openj9-0.24.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.2%2B7_openj9-0.24.0/OpenJDK15U-jdk_x64_windows_openj9_15.0.2_7_openj9-0.24.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (f366ebd9f9b4243a86bbf72975f9357a7fa6aec5dac40af4edd4c97ddb4d28b8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'f366ebd9f9b4243a86bbf72975f9357a7fa6aec5dac40af4edd4c97ddb4d28b8') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 30 Jan 2021 02:04:04 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle
# Sat, 30 Jan 2021 02:04:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ffb13abd1d90a4766a5d1047adcb1b2622366b5be0a504850c8de2fcb922c7`  
		Last Modified: Sat, 30 Jan 2021 02:51:00 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfbfa46aa649dcf5b0eaaccaab3f846e7095297a7c01f392d5288216b7c33ec`  
		Last Modified: Sat, 30 Jan 2021 02:51:29 GMT  
		Size: 383.0 MB (382971693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f140aec14739ab8b3df53ce8a2947a56b9b7ed185a4e4f0e172937c96a8bff`  
		Last Modified: Sat, 30 Jan 2021 02:51:00 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a70157f5a5b6b889eda763baf53d7320f00c036e92f4f9a82475848ca93a06`  
		Last Modified: Sat, 30 Jan 2021 02:51:00 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
