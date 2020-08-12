## `adoptopenjdk:13-hotspot-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:b4bd8d5e9d5f8dee6822a11007477afef971054de0e859356bf15da50f5da0d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `adoptopenjdk:13-hotspot-windowsservercore-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull adoptopenjdk@sha256:5a469c27f5bfc53dd381d563c8a66c634139868249bbbdf00357a1b2f9f74ef8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2735936728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e48131c9d763ecbfb9495589207e773c4dd79a7fbb390e944b12436855a5b0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Tue, 11 Aug 2020 20:36:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 16:48:39 GMT
ENV JAVA_VERSION=jdk-13.0.2+8
# Wed, 12 Aug 2020 16:51:24 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_x64_windows_hotspot_13.0.2_8.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_x64_windows_hotspot_13.0.2_8.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (422a4ce0668df53cd891ea38e6c472941893b26c9eb4121787d7c1eee123abee) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '422a4ce0668df53cd891ea38e6c472941893b26c9eb4121787d7c1eee123abee') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 12 Aug 2020 16:51:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:43065500f09f35124a5d71517aa493fd23ad75660682600f7f6b40aa7629ac78`  
		Last Modified: Tue, 11 Aug 2020 20:54:54 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77668552cdd1ff24f36f7a0341ac5eee74353184b2235df085fc4e1232caa59c`  
		Last Modified: Wed, 12 Aug 2020 18:00:05 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a207ff3ed753dc60114d9ef98a96bf434cb61ab0c6c4eaf2fbeebb824c181ff`  
		Last Modified: Wed, 12 Aug 2020 18:00:41 GMT  
		Size: 400.1 MB (400066287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e811f701ff3e219d8a82ee6523319cfa19b3978f68ea75126c7f808b746e0d97`  
		Last Modified: Wed, 12 Aug 2020 18:00:04 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
