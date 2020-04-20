## `openjdk:15-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:ec0237cd655103fa489f4f0c3730e084059e6e7949e5b3cd23d54d3d8380de14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64
	-	windows version 10.0.14393.3630; amd64

### `openjdk:15-jdk-windowsservercore` - windows version 10.0.17763.1158; amd64

```console
$ docker pull openjdk@sha256:efe96cc5a6a856b7f208479dac73810eb8c9caf7073e68ff665c314d4ceabc3e
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2468109963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c98b8789916150d18285f1ae236e642ba91ae1d9ed295b3f10efc2207cb427`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2020 21:33:26 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Tue, 14 Apr 2020 21:33:27 GMT
ENV JAVA_HOME=C:\openjdk-15
# Tue, 14 Apr 2020 21:33:53 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Mon, 20 Apr 2020 19:21:04 GMT
ENV JAVA_VERSION=15-ea+19
# Mon, 20 Apr 2020 19:21:05 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/19/GPL/openjdk-15-ea+19_windows-x64_bin.zip
# Mon, 20 Apr 2020 19:21:06 GMT
ENV JAVA_SHA256=cedb7660711da3feebdd62bfcc08905de7e0a96ea3a806a8b4acc3e2810cb70e
# Mon, 20 Apr 2020 19:23:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 20 Apr 2020 19:23:09 GMT
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
	-	`sha256:3de6b6e18c57fb613f91d77606e5355771830df52cc6b00e32e74a46a7449d5b`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 4.7 MB (4670665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac510bfbe15bdc6d786e0d3d1e28704fc631e945bcce42fb963d86c2f56d0fd8`  
		Last Modified: Tue, 14 Apr 2020 22:15:54 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0176aea199d3313340042e173fe6b28bc5a463a889d351a42f25db76d678ebf6`  
		Last Modified: Tue, 14 Apr 2020 22:15:55 GMT  
		Size: 295.7 KB (295672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20c87354fa86fe0d473860e6f15e80e716854a2eb442c0889df3427e27c3356`  
		Last Modified: Mon, 20 Apr 2020 19:31:12 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae9bb52b85e446b3de74de2820323174a6cc8215241134dc11dfa402579d24d`  
		Last Modified: Mon, 20 Apr 2020 19:31:12 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb21f360754821d3021527c631892d6aa73fd4553ba1d4b2379571a7fd5338b`  
		Last Modified: Mon, 20 Apr 2020 19:31:12 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06eabdbb04bf27a243ded429cebe10fddd1f4e5b20a5c5f289f9336e194c1ae5`  
		Last Modified: Mon, 20 Apr 2020 19:31:31 GMT  
		Size: 192.4 MB (192429640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eafeaf1bae14bc868a1104fc24687e1ceea015c5647fd3a7cd689fff00e4779`  
		Last Modified: Mon, 20 Apr 2020 19:31:12 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:15-jdk-windowsservercore` - windows version 10.0.14393.3630; amd64

```console
$ docker pull openjdk@sha256:1d86cada6c9d8d1e479df723f8eb7ed417ebe67d815a752f81471c30d3ec6313
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5936350442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc0e3b1f5491f1df4db3fda58d9aac92cd098f861493b57e48dae7056f545f6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Apr 2020 21:35:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2020 21:37:12 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Tue, 14 Apr 2020 21:37:13 GMT
ENV JAVA_HOME=C:\openjdk-15
# Tue, 14 Apr 2020 21:38:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Mon, 20 Apr 2020 19:23:18 GMT
ENV JAVA_VERSION=15-ea+19
# Mon, 20 Apr 2020 19:23:19 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/19/GPL/openjdk-15-ea+19_windows-x64_bin.zip
# Mon, 20 Apr 2020 19:23:20 GMT
ENV JAVA_SHA256=cedb7660711da3feebdd62bfcc08905de7e0a96ea3a806a8b4acc3e2810cb70e
# Mon, 20 Apr 2020 19:25:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 20 Apr 2020 19:25:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ac0134cee91589d04e97f11994235cce86faef5c581d15f2e143ecb90e92572`  
		Last Modified: Tue, 14 Apr 2020 22:16:36 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7792b001970c03ccacbdc7259d0133f320d88e7fdd9394b9c70fe73808fe3ca`  
		Last Modified: Tue, 14 Apr 2020 22:16:39 GMT  
		Size: 5.4 MB (5386185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca3b2979cce17b2f697228c6fc457c3e7099847025fa3aa0cc258fba5a84f6b`  
		Last Modified: Tue, 14 Apr 2020 22:16:37 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99af87d48adcdc7e4a329d2b4d9e50fe2ee23d2596b256f156fc562bb7aba5b1`  
		Last Modified: Tue, 14 Apr 2020 22:16:39 GMT  
		Size: 5.4 MB (5370916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9b7935400da7f502907c39d33439d7f4cd232494228a22b348288feaa189f5`  
		Last Modified: Mon, 20 Apr 2020 19:31:54 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fa031993f91fda2388fc3f3fd6a3afcd6d8a4227572510419b80a8c907518f`  
		Last Modified: Mon, 20 Apr 2020 19:31:54 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79005e2abcfe8113ef89a1b3004d267b02ed7b3a8d099c25dda823fbb821030b`  
		Last Modified: Mon, 20 Apr 2020 19:31:53 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9f7e3218ed9dbbf96979f4d8bff4cf8cf1ba498cddd58fa3818c49f66a847b`  
		Last Modified: Mon, 20 Apr 2020 19:32:14 GMT  
		Size: 197.5 MB (197518971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68347651e92545352bb4a4418d925a5f9c549304a27260a8bbd8e56373a01b86`  
		Last Modified: Mon, 20 Apr 2020 19:31:53 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
