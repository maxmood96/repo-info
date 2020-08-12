## `adoptopenjdk:14-jdk-hotspot-windowsservercore`

```console
$ docker pull adoptopenjdk@sha256:ec5cffb76ccf665b130e5619b54dd47cbdbaa55b4b0abf1ddee39de520ffcbc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3866; amd64
	-	windows version 10.0.17763.1397; amd64

### `adoptopenjdk:14-jdk-hotspot-windowsservercore` - windows version 10.0.14393.3866; amd64

```console
$ docker pull adoptopenjdk@sha256:87198c9e3e5adfe011d3130af161b0f9f6ec225bbdfb05c1b03a55f7e4b08c47
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 GB (6133150519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7658dafba442bcefec7c067c59a888465c010d95f07a196d22c82b87d4822a26`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Aug 2020 20:31:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 16:55:28 GMT
ENV JAVA_VERSION=jdk-14.0.2+12
# Wed, 12 Aug 2020 16:58:46 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_x64_windows_hotspot_14.0.2_12.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_x64_windows_hotspot_14.0.2_12.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (9cbd03600e58ad8d2383c15e596396fbdfbc9655ba0019f5bc74c910e4082c7c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '9cbd03600e58ad8d2383c15e596396fbdfbc9655ba0019f5bc74c910e4082c7c') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Aug 2020 16:58:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:32838d9637dc39d4acee78700b0f93d6c8c9d2db755f12c8009c1b51687d3fbd`  
		Last Modified: Tue, 11 Aug 2020 20:54:28 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c978e1ac9975ef8ef38080b6f67b130c8a22752931908c388958d905e0b016`  
		Last Modified: Wed, 12 Aug 2020 18:01:47 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8798160e90455c0f86f47f18b0ccc72210d3c0b69691d1c4980bf6bcb578a78a`  
		Last Modified: Wed, 12 Aug 2020 18:02:48 GMT  
		Size: 395.0 MB (394999681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3889261a30ccdf513c211b17e7b719161913a7daba7087fe95736b3ad023e75`  
		Last Modified: Wed, 12 Aug 2020 18:01:46 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:14-jdk-hotspot-windowsservercore` - windows version 10.0.17763.1397; amd64

```console
$ docker pull adoptopenjdk@sha256:49c573afcf9e2cd279c7b5cbd751b038ce69e1c750d4e1565bbee20ed6e8ca61
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2730196309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13773b57ee038727991f5b1e98e19574ac553bfaddb70f2bcc8a145a3908573`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Tue, 11 Aug 2020 20:36:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 16:58:54 GMT
ENV JAVA_VERSION=jdk-14.0.2+12
# Wed, 12 Aug 2020 17:01:30 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_x64_windows_hotspot_14.0.2_12.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_x64_windows_hotspot_14.0.2_12.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (9cbd03600e58ad8d2383c15e596396fbdfbc9655ba0019f5bc74c910e4082c7c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '9cbd03600e58ad8d2383c15e596396fbdfbc9655ba0019f5bc74c910e4082c7c') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Aug 2020 17:01:31 GMT
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
	-	`sha256:8819af825e098fdf494065c262fe675b42e36a3d26aaf6c1fa8e462b2dd370fb`  
		Last Modified: Wed, 12 Aug 2020 18:03:03 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7419cf74500b73ac0fb8056d7d4698bebd7f3d42590cf45f5bebe2ef7a3716da`  
		Last Modified: Wed, 12 Aug 2020 18:04:01 GMT  
		Size: 394.3 MB (394325908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622a83fb057f482d0d549e91bd4e963b41424879ef0613e4cf20249dd77c2d16`  
		Last Modified: Wed, 12 Aug 2020 18:03:03 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
