## `openjdk:24-jdk`

```console
$ docker pull openjdk@sha256:cad76ed03825f2d21243c2b6b39f4e3796490df2ac660772564b877e915b4228
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `openjdk:24-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:838f22543b34fd67795e9637f4ac26a598c1adb5b72e57b15d84e6c276e0d5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 MB (300130979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe6cc2eb5f63eaad2b901c0eb328019fbde3ed6360edf541b2de72b5de28880`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 06 Sep 2024 18:48:13 GMT
ADD file:d8a38112d165940510d5cfd57f316139caf4069546c97dfc10a08f33f3f1ca9f in / 
# Fri, 06 Sep 2024 18:48:13 GMT
CMD ["/bin/bash"]
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 06 Sep 2024 18:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+14
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='e3cf94d73e0ca63c536e901858cb97a0053c62606f8bb9d5b2ca20e1cc573d0c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='0d13500ae2e96601c70e90fca2ad928c3bf541afc71c293aed33924a2361d97a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:12d7e45337f84111b352ed27b6a21ab109dec7571b23ebc522b6bb6b318d883b`  
		Last Modified: Mon, 09 Sep 2024 22:21:36 GMT  
		Size: 49.2 MB (49237791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48d62797a6a657cc627514abd40304456b8c9e3ff6e10c63f2e19f48bf69bd4`  
		Last Modified: Mon, 09 Sep 2024 23:02:11 GMT  
		Size: 39.1 MB (39060878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3d408aa04717d10c404fb4967df73c20cae4b77bdf8dfe24e9209951e1fc69`  
		Last Modified: Mon, 09 Sep 2024 23:02:14 GMT  
		Size: 211.8 MB (211832310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:73f448f1b035a3f6ecee9ef68074aafe65ff0cf51099109d582337f8c8b50684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3663807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fdcca585882c5ded34996bb8308b442b2d900caa4d16eb378bc77e8cf5b5fdd`

```dockerfile
```

-	Layers:
	-	`sha256:056b21e384a5ebd724271502ab62da272d9911e4685469a084c742988c26c771`  
		Last Modified: Mon, 09 Sep 2024 23:02:10 GMT  
		Size: 3.6 MB (3644279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26b5cb4c339f25c6dca563e26f52bfabcba2e4e750dd386e6c33d2dc82d90b63`  
		Last Modified: Mon, 09 Sep 2024 23:02:09 GMT  
		Size: 19.5 KB (19528 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7e4ac73aafbdceded98958093807e138f3cb2d2e1de041ee687c9bc2b79d2e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297059318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71b53d67a6b28cd6331c14652cf3e908863b758f86ceebbf1627d4598d5d0a2`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Aug 2024 00:40:26 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Fri, 23 Aug 2024 00:40:27 GMT
CMD ["/bin/bash"]
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 06 Sep 2024 18:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+14
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='e3cf94d73e0ca63c536e901858cb97a0053c62606f8bb9d5b2ca20e1cc573d0c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='0d13500ae2e96601c70e90fca2ad928c3bf541afc71c293aed33924a2361d97a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d43f5ded4088b46b5f902d592d52c2a52fe637a75fa3f5875e873ef3c66794`  
		Last Modified: Fri, 06 Sep 2024 22:24:26 GMT  
		Size: 39.5 MB (39489040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d7fa6da34451efda3c1a92cd10668e1a134ca1405ab43685514606fba6d5db`  
		Last Modified: Fri, 06 Sep 2024 22:24:31 GMT  
		Size: 209.7 MB (209682487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:936533b61d2992156efad41e06a4ce1caa66d2d45235602ab318d6a52345e28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3662636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f969693b433324783afb49977e3e26de49933ac60d68deb52e126d716b93ca`

```dockerfile
```

-	Layers:
	-	`sha256:2e0f6396590117672fe8bfd5afb11fef6f159c4f42f4165a83bfc2052b8ffd39`  
		Last Modified: Fri, 06 Sep 2024 22:24:25 GMT  
		Size: 3.6 MB (3642634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8e10d7a56aa517e82008b3b58f731e128e98cc2cd37faecdff4a90b856e896b`  
		Last Modified: Fri, 06 Sep 2024 22:24:25 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk` - windows version 10.0.20348.2655; amd64

```console
$ docker pull openjdk@sha256:cb6638979cc02322af20871bba12eed44d8ef02995d6578ab7f044a2945a36f6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2350454022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6d20700bed0d225624e1c2cabfd6ca49ff2b98e7f2d54fc2e7d9879ac8eec6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Fri, 06 Sep 2024 22:00:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Sep 2024 22:01:28 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 06 Sep 2024 22:01:29 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 06 Sep 2024 22:01:40 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 06 Sep 2024 22:01:40 GMT
ENV JAVA_VERSION=24-ea+14
# Fri, 06 Sep 2024 22:01:41 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_windows-x64_bin.zip
# Fri, 06 Sep 2024 22:01:42 GMT
ENV JAVA_SHA256=d302c4d8be4955ea17267c66b8321f205212748df83273e4e0d9ccc0d1c4b1a2
# Fri, 06 Sep 2024 22:02:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 06 Sep 2024 22:02:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af83db2d09f0dbd517e78c2c32c1889ca9b84aa301ab4a2f1180204a3ad80867`  
		Last Modified: Fri, 06 Sep 2024 22:02:19 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af8a177ebebd2410378b7f8daeff093af9d1870183f0bcf5e34d59ef3085b83`  
		Last Modified: Fri, 06 Sep 2024 22:02:19 GMT  
		Size: 374.1 KB (374110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e4a2b2a8530a0dc404b9fc4b3fbd89e37acc9921f6cc082bdfe0da2ee525a1`  
		Last Modified: Fri, 06 Sep 2024 22:02:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0330adff9c58975286c882786b7bd8d2bbfbd75c34a2b99b2aba8d03018cbe7`  
		Last Modified: Fri, 06 Sep 2024 22:02:19 GMT  
		Size: 321.5 KB (321508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c438adf9c12442fcb3c2c10a7eb87bf2f9c34647afc3355b140710530e0a4b7c`  
		Last Modified: Fri, 06 Sep 2024 22:02:18 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e6028c0b02b44dc8097f71e99cb3700370e63c26f35e128c465996b93cfe92`  
		Last Modified: Fri, 06 Sep 2024 22:02:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4292ac3338c779aa3d76c92fee7ae91b42f19711996b2b3090c64d18553d27`  
		Last Modified: Fri, 06 Sep 2024 22:02:18 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f23b977eb1536446ac9c110494a44ad8f00623b244e701ed5bf8f8d1f6b9b`  
		Last Modified: Fri, 06 Sep 2024 22:02:29 GMT  
		Size: 208.0 MB (207985641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ef8839a1c446caa094f2d9a4ff559d2be599500bd759490829355c5aacef9e`  
		Last Modified: Fri, 06 Sep 2024 22:02:18 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-jdk` - windows version 10.0.17763.6189; amd64

```console
$ docker pull openjdk@sha256:2206af543fe149f27e9768b8a681d657ae24a182f8d747c68cae9cc76f7b6e63
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2454065444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431d91e354b9da5bd5c77818510bbda44e53e4c063deeac7770f76582a24efba`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Fri, 06 Sep 2024 22:00:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Sep 2024 22:02:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 06 Sep 2024 22:02:26 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 06 Sep 2024 22:02:51 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 06 Sep 2024 22:02:51 GMT
ENV JAVA_VERSION=24-ea+14
# Fri, 06 Sep 2024 22:02:52 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_windows-x64_bin.zip
# Fri, 06 Sep 2024 22:02:52 GMT
ENV JAVA_SHA256=d302c4d8be4955ea17267c66b8321f205212748df83273e4e0d9ccc0d1c4b1a2
# Fri, 06 Sep 2024 22:03:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 06 Sep 2024 22:03:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a85539afafa4fd5c7cff928b9651e0ad5e977e24bc2f01a9b8d3bef5fea504`  
		Last Modified: Fri, 06 Sep 2024 22:03:48 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30bd183cd6bf2e89ae1801679c2cd36558a985f6627e5a7923993831ad9b11db`  
		Last Modified: Fri, 06 Sep 2024 22:03:48 GMT  
		Size: 500.9 KB (500915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8b834bfb2671db352ab9c7bf877bfb395837c650262beb0c1dfddb1d8d2c6b`  
		Last Modified: Fri, 06 Sep 2024 22:03:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed62d59192ed801af12eff4faa9e78682a1d64180b0263899cee8ede1bff2f8d`  
		Last Modified: Fri, 06 Sep 2024 22:03:48 GMT  
		Size: 346.6 KB (346567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b76a5c8ce16e1f122d4700b423b51ebdd77a77b23257a133d87db7a2684c38`  
		Last Modified: Fri, 06 Sep 2024 22:03:47 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abf20b02eb8464f5d632f2d7e6c41c6d91fa7f59fd1992e7809e12f06ad9a32`  
		Last Modified: Fri, 06 Sep 2024 22:03:47 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c8bcf86a1fd2dd90d9d520a25b5e59676ffa657ae2ef56931aebf23a787c43`  
		Last Modified: Fri, 06 Sep 2024 22:03:47 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a361e1dd41c4cc57f54bf6f55ca3efa9484432155481795409397fd98792c2fc`  
		Last Modified: Fri, 06 Sep 2024 22:03:58 GMT  
		Size: 208.0 MB (208006955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2454f4607c6812877021c59b1e5e318701a093d4dee3385a821fba802f087b9`  
		Last Modified: Fri, 06 Sep 2024 22:03:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
