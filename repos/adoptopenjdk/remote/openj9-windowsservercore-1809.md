## `adoptopenjdk:openj9-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:e87a9e85e08433e3cfa4cb7352969d9f94f1a074adc1e907844b4451cfc4217f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `adoptopenjdk:openj9-windowsservercore-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull adoptopenjdk@sha256:acc35779e269badeecc34b856ab136570b19f973ccccbc04cd165776f1bb1cc4
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2729488377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c082643885fa0eef54da3ed962e2738c1730f9a0e15e445d6e8f8a6b8c124b4d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Tue, 11 Aug 2020 20:36:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 17:37:50 GMT
ENV JAVA_VERSION=jdk-14.0.2+12_openj9-0.21.0
# Wed, 12 Aug 2020 17:40:23 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12_openj9-0.21.0/OpenJDK14U-jdk_x64_windows_openj9_14.0.2_12_openj9-0.21.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12_openj9-0.21.0/OpenJDK14U-jdk_x64_windows_openj9_14.0.2_12_openj9-0.21.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (2e496ce7ca02f7a380fd1902e06d55d52121bb2eee29b21b8e54ad3e2fd3466e) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '2e496ce7ca02f7a380fd1902e06d55d52121bb2eee29b21b8e54ad3e2fd3466e') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Aug 2020 17:40:24 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Wed, 12 Aug 2020 17:40:25 GMT
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
	-	`sha256:5ab9029142c473c80c6e95ee8c6ea7133b7f8c42206387db58125618a60fdd2a`  
		Last Modified: Wed, 12 Aug 2020 18:14:27 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0a2cc206b152d20e712901615abb9f0c5f82830e0ad3266a153543abc99786`  
		Last Modified: Wed, 12 Aug 2020 18:15:14 GMT  
		Size: 393.6 MB (393616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066b2cae8e8462c2e5672ef0fe2f09a029490b01c0fab45579c6a40b2a9d4ea2`  
		Last Modified: Wed, 12 Aug 2020 18:14:27 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c19ecd4fa9d45e928e6b2ab0194e3442e14af2e7848591b7332a1da444430c`  
		Last Modified: Wed, 12 Aug 2020 18:14:27 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
