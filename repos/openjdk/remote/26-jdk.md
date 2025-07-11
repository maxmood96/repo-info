## `openjdk:26-jdk`

```console
$ docker pull openjdk@sha256:7344acb2af2f5d12fb8b2939f4ec265d9e3bac7e7a704f251cce91ecc4a99403
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.4652; amd64
	-	windows version 10.0.20348.3932; amd64

### `openjdk:26-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:7e818fc65441af6afb28a269f990c9c5abc74c13e61237d1a4c91321b85cb031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310531368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:481dcd0af8c3231f1ccd767a2b49712717e0691aab59d07c26c742b4ee608f00`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 05 Jul 2025 00:54:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 00:54:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 05 Jul 2025 00:54:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 00:54:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Jul 2025 00:54:13 GMT
ENV JAVA_VERSION=26-ea+5
# Sat, 05 Jul 2025 00:54:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b43bfaf18ccd153838dbb7979ebf2f4be031eb16da6a977823c2422eefa279e7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='94cab2a012f104ef5ae8201f05912bf495c9f696b58e2f255bf10d6d018fb0c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:90dac1e734aa2e08c0e4e8bb7d30232985487cf8abfb490025986f98bc2e5382`  
		Last Modified: Thu, 10 Jul 2025 23:20:44 GMT  
		Size: 49.5 MB (49500230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6483f9c15a4efd5e153cead57406bbca7391b3a395ace4d59b65f7ee90a147fe`  
		Last Modified: Fri, 11 Jul 2025 00:09:23 GMT  
		Size: 38.1 MB (38093387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a868c353f94ff44e834a112788787ec3212d520303f1686b97120d409e2691`  
		Last Modified: Fri, 11 Jul 2025 04:27:11 GMT  
		Size: 222.9 MB (222937751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:99421b5dd0b5362edb1ffc4b21fbb8414bcadee37b5f0e06695bd2cdda70806c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3661014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e19282a560d271c8f6c857ecacc049b890c80091abc45227e64d5759d04c7d`

```dockerfile
```

-	Layers:
	-	`sha256:5fc7253c2327a3de482c0d88e06e9d595fdeae4e10772bbf908a6fc6635ad120`  
		Last Modified: Fri, 11 Jul 2025 03:24:10 GMT  
		Size: 3.6 MB (3641294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80ef956d80d70a4961575d5c5bde238e3dee4877b68ca377ad993b231d918085`  
		Last Modified: Fri, 11 Jul 2025 03:24:11 GMT  
		Size: 19.7 KB (19720 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b5addc84246b4ed846d57bd5f80e66bb9e537c69c167f5695364adb3e4043dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.3 MB (307270235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f728e838d8688e47b587e0e1e08a6ec223eff31736c94fb5f9ed65194c15504`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 05 Jul 2025 00:54:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 00:54:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 05 Jul 2025 00:54:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 00:54:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Jul 2025 00:54:13 GMT
ENV JAVA_VERSION=26-ea+5
# Sat, 05 Jul 2025 00:54:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b43bfaf18ccd153838dbb7979ebf2f4be031eb16da6a977823c2422eefa279e7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='94cab2a012f104ef5ae8201f05912bf495c9f696b58e2f255bf10d6d018fb0c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4447c51b3bde441b803aaaf0a684a8bbac02d7fce9167a7c1e87c313add07cf4`  
		Last Modified: Thu, 10 Jul 2025 23:23:17 GMT  
		Size: 48.1 MB (48085739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971f07a392e04b4b6e3af0d916043d20304174997e2490b9db70ba78668b2551`  
		Last Modified: Fri, 11 Jul 2025 00:13:53 GMT  
		Size: 38.5 MB (38493030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66999f1be9ff06af7486e93242c4d193691b57c748b895cd3ed0d14e9c5cae2`  
		Last Modified: Fri, 11 Jul 2025 04:54:59 GMT  
		Size: 220.7 MB (220691466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:2429d2d49cc4625b5986ebaf4168e8293a44b3048fbb54bb1d0557bdbda11386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3659064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461929500f59712d76b0218f79e3da96250d49e189ec36e0a71007af3f1c9baa`

```dockerfile
```

-	Layers:
	-	`sha256:7d133c11cfd1c0c44b0e7bd50a2c988a758aaef809a304a3472bea39bd50d5b5`  
		Last Modified: Fri, 11 Jul 2025 03:24:15 GMT  
		Size: 3.6 MB (3639056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e709db1c7466526955a7fa65f6198078ba877fdd14e8988844d5bf18928a6479`  
		Last Modified: Fri, 11 Jul 2025 03:24:16 GMT  
		Size: 20.0 KB (20008 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk` - windows version 10.0.26100.4652; amd64

```console
$ docker pull openjdk@sha256:f7ba37f27f987642d0df4e8306d6f7320a8d7660b655c232c986aa2b6d81512b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3710833205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae14b9b4564aa8e416943839e9efdd51764a82cc0c3dc50ceee3ba455500296`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Wed, 09 Jul 2025 18:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:09:43 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:09:44 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 09 Jul 2025 18:09:50 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:09:51 GMT
ENV JAVA_VERSION=26-ea+5
# Wed, 09 Jul 2025 18:09:52 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_windows-x64_bin.zip
# Wed, 09 Jul 2025 18:09:53 GMT
ENV JAVA_SHA256=884a05860f9ed48a9a26e95900c90750b220618efe84857aa27061fd3657fee3
# Wed, 09 Jul 2025 18:10:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:10:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f7d7e7b74d17a3a394e43e6fc08aa4ae8e9ac6b0d8868e014e74d1617b2a21`  
		Last Modified: Wed, 09 Jul 2025 19:09:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4908098a74bdc5a385c002b7d3d64a8a92e3163a8c27f70ed6f9d96b044973c6`  
		Last Modified: Wed, 09 Jul 2025 19:09:29 GMT  
		Size: 391.1 KB (391108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee377c238d243697b29d9d96e4b068c10110db519d39f4ea4b4ffcb32add8b2`  
		Last Modified: Wed, 09 Jul 2025 19:09:30 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a2c6262721621531ff32c8fa8e56c908bea6250df4210781edeb769f0e768e`  
		Last Modified: Wed, 09 Jul 2025 19:09:33 GMT  
		Size: 375.1 KB (375062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27487be9b1cda83f642d4dc075a21628efb78d71bceee618978394c2d46cf891`  
		Last Modified: Wed, 09 Jul 2025 19:09:34 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb646b13ab8c4fdb021be772b164088ef14e35e2ccd9a6c141eb91b1f7dc11c5`  
		Last Modified: Wed, 09 Jul 2025 19:09:36 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8841445d721659485ecd7312a69c7a799028195ffc05b65215beef5a18019a`  
		Last Modified: Wed, 09 Jul 2025 19:09:37 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afc54772b30e36a3d952380debe6749f8440c8d41005ebd7f544d97cd953128`  
		Last Modified: Wed, 09 Jul 2025 19:09:49 GMT  
		Size: 218.9 MB (218885902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ae451d09b6531c75d7b1fc70cfdc4ee788b2ab0ed21397bbd16c943178b176`  
		Last Modified: Wed, 09 Jul 2025 19:09:50 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-jdk` - windows version 10.0.20348.3932; amd64

```console
$ docker pull openjdk@sha256:e7c2a11e347f5497d6d8eb2d6f527368b1f1143e04c92fe7e8ae8632e746d790
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2500144940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae9df4aba3d2b7a06cf9a94cf7c1570a5b8961b777653b388514660f495e3c5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Wed, 09 Jul 2025 18:11:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:12:02 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:12:02 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 09 Jul 2025 18:12:08 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:12:10 GMT
ENV JAVA_VERSION=26-ea+5
# Wed, 09 Jul 2025 18:12:10 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_windows-x64_bin.zip
# Wed, 09 Jul 2025 18:12:11 GMT
ENV JAVA_SHA256=884a05860f9ed48a9a26e95900c90750b220618efe84857aa27061fd3657fee3
# Wed, 09 Jul 2025 18:12:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:12:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667a2f19db58eb97b8ce399e49f60b27e7ca4c34e9499d99b48b78dec3ec3041`  
		Last Modified: Wed, 09 Jul 2025 19:08:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63594e3ed0c698b89ae34ec9b5a724d2ab730fabe3f50b84d16ed306a8743bac`  
		Last Modified: Wed, 09 Jul 2025 19:08:31 GMT  
		Size: 347.4 KB (347431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d197d178bc1f08b97ba3a936f73d9ac730fad558064cdf67a29d1f5d7419026a`  
		Last Modified: Wed, 09 Jul 2025 19:08:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccc9b4105910f91a0478b17761b32eac10d1362c64037750a35ee1b684d86f8`  
		Last Modified: Wed, 09 Jul 2025 19:08:33 GMT  
		Size: 334.3 KB (334334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0716a8f184e1b31023888dfa0098d92fb24dd3178a48c4f7b73ab597922fcdf6`  
		Last Modified: Wed, 09 Jul 2025 19:08:34 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5cb36861622dfd74ef80c5367277f5012bf91e408892fccf0d54c6fb682911`  
		Last Modified: Wed, 09 Jul 2025 19:08:34 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98b04c9e44392061d44b299789edd891c706c8bcd58a99a9767aac2402deaab`  
		Last Modified: Wed, 09 Jul 2025 19:08:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257a1d932a42111bb37066d36c44ab62faa379831b05d4359e879e6c1a02847b`  
		Last Modified: Wed, 09 Jul 2025 19:09:33 GMT  
		Size: 218.9 MB (218851895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1432cfbaae9ba585e16c2258251e745ec906196090a7c0b57209e6e018a2d5fb`  
		Last Modified: Wed, 09 Jul 2025 19:08:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
