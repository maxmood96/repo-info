## `openjdk:14-jdk`

```console
$ docker pull openjdk@sha256:5f69fd17f746cbcd44820abb47dcf0c8a3fdec3fa823f149d85feba8449c58aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	windows version 10.0.17763.914; amd64
	-	windows version 10.0.14393.3384; amd64

### `openjdk:14-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:b34101282111943443f789f41ae77970497157a8c7b2ae78bb285ad062e4a7c9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.5 MB (256538822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09215ccd4b0871be4de9c3e526c2ed46fcea3f23003b6c91915877c1ac73daf3`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 20 Dec 2019 01:46:43 GMT
ADD file:e662b0d428c91ed028fec1db2cccbeddea848eb36b32c8bfad324619b8e57d9f in / 
# Fri, 20 Dec 2019 01:46:44 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2019 02:05:13 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 20 Dec 2019 02:05:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2019 02:06:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-14
# Fri, 20 Dec 2019 02:06:57 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Dec 2019 23:24:28 GMT
ENV JAVA_VERSION=14-ea+29
# Mon, 30 Dec 2019 23:24:28 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk14/29/GPL/openjdk-14-ea+29_linux-x64_bin.tar.gz
# Mon, 30 Dec 2019 23:24:28 GMT
ENV JAVA_SHA256=16981e7212ed6035580dff619f93356f707b75f6abfca9a3df7b45a290e8f521
# Mon, 30 Dec 2019 23:24:48 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Mon, 30 Dec 2019 23:24:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:822ace0353cbeeb23baa4e10b00916d8aae76c005023f5807d16cd97e6339b9b`  
		Last Modified: Fri, 20 Dec 2019 01:48:50 GMT  
		Size: 42.7 MB (42725372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf4d0631bf4e4c98ff5629cdf7958d9db134bbabd5a323f89f8fd783ca4c524`  
		Last Modified: Fri, 20 Dec 2019 02:10:52 GMT  
		Size: 14.8 MB (14793038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d6c2a0457e32c05d85b431b7ee7fa1d500d358ad6971ebf355ca768fba4aa4`  
		Last Modified: Mon, 30 Dec 2019 23:30:31 GMT  
		Size: 199.0 MB (199020412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:14-jdk` - windows version 10.0.17763.914; amd64

```console
$ docker pull openjdk@sha256:9c4e6ff28098683bdb101983de637104c90bc93957b7dec5c145de41ca038d27
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2415375284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c76b77ecc75375bcbf24481add23ca93df2019d449ca7f8a18b52180e7a3df`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 29 Nov 2019 04:34:15 GMT
RUN Install update 1809-amd64
# Tue, 10 Dec 2019 21:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 18:41:29 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 11 Dec 2019 18:41:30 GMT
ENV JAVA_HOME=C:\openjdk-14
# Wed, 11 Dec 2019 18:41:52 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Mon, 30 Dec 2019 23:30:20 GMT
ENV JAVA_VERSION=14-ea+29
# Mon, 30 Dec 2019 23:30:22 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk14/29/GPL/openjdk-14-ea+29_windows-x64_bin.zip
# Mon, 30 Dec 2019 23:30:23 GMT
ENV JAVA_SHA256=083c06147216ce2163d4e6e0fdbad095c35769bf98f8020b20801660b22c38e0
# Tue, 31 Dec 2019 00:03:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 31 Dec 2019 00:03:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:faf31ee0aa3d3c60a38dd03c7554d632065cef50eab052ef1444590786249d07`  
		Size: 681.6 MB (681618026 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e147f14e0d6a9cbd5261162dea8f3aac7a34db5d9f6a587a9aac6b88722a2da4`  
		Last Modified: Tue, 10 Dec 2019 22:07:34 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0c4a671756d1396180ecdf66a8d6708b4290b154606229618d94780b6ab6b3`  
		Last Modified: Wed, 11 Dec 2019 19:58:31 GMT  
		Size: 4.6 MB (4578585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dd93d5d22657024ea3906380498894b3ebdd06d5348c4adcd4061becd49e45`  
		Last Modified: Wed, 11 Dec 2019 19:58:29 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68816793ae0ca8336d60c4283925c035fea988d4e1648ed0c7f3d724dfe1aae7`  
		Last Modified: Wed, 11 Dec 2019 19:58:30 GMT  
		Size: 314.7 KB (314698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b42b06415e8bfd8b7a9f7071b886a51c41e95eab0251ff33e822ace520c8d3`  
		Last Modified: Tue, 31 Dec 2019 00:20:08 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f3b38e3bed6333ed5388e001f97f50f427004a67af5c4011e09e6783300bcb`  
		Last Modified: Tue, 31 Dec 2019 00:20:08 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ed98d6c5b99b98d91ca9ba7c26fd243bc2a56fc70ce46cb39e549ba3a3e3ad`  
		Last Modified: Tue, 31 Dec 2019 00:20:09 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e6dc70768391e634a28157055992e4f4e10cce457a2c841a46dd8f453b7c0b`  
		Last Modified: Tue, 31 Dec 2019 00:23:15 GMT  
		Size: 194.2 MB (194171452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338caab9880adcbdd738358816bc0b67f3f02b696d7d2515136acaf9219cb986`  
		Last Modified: Tue, 31 Dec 2019 00:20:09 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:14-jdk` - windows version 10.0.14393.3384; amd64

```console
$ docker pull openjdk@sha256:ad1f54eceefdf2812908ec5995c3f52ea9a073936738bcff2c1662bd6f87f9dc
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5937091136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133ca6fea7e137cb049fac9723a83671c9f1bacb4c4341c12a740734d952bcf0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 00:35:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 18:45:32 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 11 Dec 2019 18:45:34 GMT
ENV JAVA_HOME=C:\openjdk-14
# Wed, 11 Dec 2019 18:46:45 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Tue, 31 Dec 2019 00:03:23 GMT
ENV JAVA_VERSION=14-ea+29
# Tue, 31 Dec 2019 00:03:24 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk14/29/GPL/openjdk-14-ea+29_windows-x64_bin.zip
# Tue, 31 Dec 2019 00:03:25 GMT
ENV JAVA_SHA256=083c06147216ce2163d4e6e0fdbad095c35769bf98f8020b20801660b22c38e0
# Tue, 31 Dec 2019 00:06:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 31 Dec 2019 00:06:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:530e4240d4261ce165890648d1df6230dc4f9ce5df2e6cf9f0d5876694c3d4f0`  
		Last Modified: Wed, 11 Dec 2019 01:14:39 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ba7ecb82646b9454a7a416c149a513479fd0ab29aaa2dfbe96281b62668931`  
		Last Modified: Wed, 11 Dec 2019 19:59:59 GMT  
		Size: 5.4 MB (5365131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3eaf34da6eedc1087e3f8e21af3d549b7e85b0e1f93c4275a7569076c67f12`  
		Last Modified: Wed, 11 Dec 2019 19:59:55 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef9e5659d610b4fc02e08dc2d00b5d97d8f9e0d0ca73681a31acbef3f3e00a5`  
		Last Modified: Wed, 11 Dec 2019 19:59:58 GMT  
		Size: 5.3 MB (5345980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84af87ab9d1b71b1e6131ed1c53df8704170febb2941814d8da2fd094e5d314`  
		Last Modified: Tue, 31 Dec 2019 00:24:14 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ced9aed42717ad7915fce285edf80a961e89907cb0f3350fb5d818c0ad0315`  
		Last Modified: Tue, 31 Dec 2019 00:24:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf493bad33edd3fa7fe0113d737011f9d7adb69aecbd7816c14126d99980e44`  
		Last Modified: Tue, 31 Dec 2019 00:24:14 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e359947fffb1860e53d921df990ef484390775bbfb5f0e907c2eaa7e154b2def`  
		Last Modified: Tue, 31 Dec 2019 00:24:39 GMT  
		Size: 203.7 MB (203668980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a80814be613268cbfccb3d5172b591bde112ffb1eae5fc53607e3111cf78a8`  
		Last Modified: Tue, 31 Dec 2019 00:24:14 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
