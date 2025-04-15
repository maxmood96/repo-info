## `openjdk:25-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:d1e3063cfa8f72e6fcb15ec2b0630f8c6b305c3c77b9d92189be07572ba98343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `openjdk:25-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull openjdk@sha256:82b9115d9ce19bac431f29d461d9cf41366b7eae62c5dca30f149e0693bc59be
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2371376094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd68f374460b19e7d00f97eafe7ff3db49beabbefa4f1196fcd4fbb36235443`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Mon, 14 Apr 2025 23:01:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Apr 2025 23:01:58 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 14 Apr 2025 23:01:59 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 14 Apr 2025 23:02:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 14 Apr 2025 23:02:06 GMT
ENV JAVA_VERSION=25-ea+18
# Mon, 14 Apr 2025 23:02:07 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_windows-x64_bin.zip
# Mon, 14 Apr 2025 23:02:08 GMT
ENV JAVA_SHA256=41f24482b5d173e5a8f242d81909835bd7e85fdb131b901bff9a150186c3c03c
# Mon, 14 Apr 2025 23:02:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 14 Apr 2025 23:02:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901c4f6499be32d72d03acd1b077f303c36f9e02549df1e19e93e6f970009e2e`  
		Last Modified: Mon, 14 Apr 2025 23:02:37 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6b8435c9a9649b98ba88785e7bf6465520b54419856cf1fc5db334b067d2ad`  
		Last Modified: Mon, 14 Apr 2025 23:02:37 GMT  
		Size: 341.7 KB (341685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842b230d555934e825a14324149c16f66c7014b6e8bb7651a898041ee671e45d`  
		Last Modified: Mon, 14 Apr 2025 23:02:37 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f43866e1dcafdf28f4228409e7ba028feb8636b24ff7f354045ae263091c14`  
		Last Modified: Mon, 14 Apr 2025 23:02:37 GMT  
		Size: 333.1 KB (333086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1ccac9761890f7f40a1d1f6dff046a49acef0e861085317fcedff81f3bfd42`  
		Last Modified: Mon, 14 Apr 2025 23:02:35 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728d117ea3c13782050bb4a5f47e6dd5262c2b8ac6fed617a386a78ebf37b227`  
		Last Modified: Mon, 14 Apr 2025 23:02:35 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f101e1391c24c0c7c48aae7c9ad7c7041f39b242c99fe1ea34338ff5647e557`  
		Last Modified: Mon, 14 Apr 2025 23:02:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7704872e5346a4a65f26e58a263307eab434bc65fe32064a6461f9bbc161cf3d`  
		Last Modified: Mon, 14 Apr 2025 23:02:46 GMT  
		Size: 208.0 MB (207967651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd85a721ad333995528bd0b2888dbac19cbf4830018f77b6f2d724f226a5b2c5`  
		Last Modified: Mon, 14 Apr 2025 23:02:35 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
