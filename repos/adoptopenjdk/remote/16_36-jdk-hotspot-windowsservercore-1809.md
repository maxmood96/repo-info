## `adoptopenjdk:16_36-jdk-hotspot-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:5cbee5fa6e0695ca4b14e75a4f2ea632be60f5d06ee750843b1acb552fc16b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `adoptopenjdk:16_36-jdk-hotspot-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull adoptopenjdk@sha256:92bcc4f9baa58f9f88b6b02169ff4828be5b83c1767d1c6d790f8b2a0d1c7d6b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2852387810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e341558c029ecf66bcc1005061eed8f40c71592162f5f1f1fd0827fd126e0da3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 18:25:11 GMT
ENV JAVA_VERSION=jdk-16+36
# Wed, 14 Apr 2021 18:26:59 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16%2B36/OpenJDK16-jdk_x64_windows_hotspot_16_36.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16%2B36/OpenJDK16-jdk_x64_windows_hotspot_16_36.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (7e10ec7e61baad6293c8b2812eee7d049450602c9493f658f5476c48f0c450b1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '7e10ec7e61baad6293c8b2812eee7d049450602c9493f658f5476c48f0c450b1') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Apr 2021 18:27:01 GMT
CMD ["jshell"]
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
	-	`sha256:ae53fc385dc9efa1e7b61ba503d543de9ed12cb2bdcea828d2125a31847e3611`  
		Last Modified: Wed, 14 Apr 2021 19:25:42 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3157ebce9ec2dddaab0fc5e15399d19b40fbb9db1faeb44d0b75334096510f56`  
		Last Modified: Wed, 14 Apr 2021 19:26:15 GMT  
		Size: 382.6 MB (382629648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb273bf11354163aa8b9f43d38d56aed7e6f36fee182767675f0de8895c3bbe`  
		Last Modified: Wed, 14 Apr 2021 19:25:42 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
