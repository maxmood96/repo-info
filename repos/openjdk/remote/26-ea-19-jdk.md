## `openjdk:26-ea-19-jdk`

```console
$ docker pull openjdk@sha256:fea1dee0364700522ecc4d51aa4da8893b05c50cc272f6c1d7f2e10f1ca09338
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `openjdk:26-ea-19-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:a836fd2f61a5c61be8cb6fa05b386ab9d682fe6e39cc7390290d331405e66754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.3 MB (313276012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936ed279b76256479bc4ac2a1bc764020603cca02469f6ddc42d5d9449015c57`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
CMD ["/bin/bash"]
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 11 Oct 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+19
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='9a89dcca644d59f40b82f6712c854e416d5b5fe80808c40868e1ba2d6d8e1e9e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='2841b9fa0e22671fc0ee3e6ba1e87237d895446e7548021004f201a1ff5abd99'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93c8878a2cdfd2dc50032c3572c9b627079c5632261fd3256ee3992dc0e12b6`  
		Last Modified: Mon, 13 Oct 2025 21:03:29 GMT  
		Size: 38.1 MB (38082794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb02e6489f4563d93b520919c701424762c708ea1d5d6ad0e6f8ed21d92a74c`  
		Last Modified: Mon, 13 Oct 2025 21:44:01 GMT  
		Size: 225.7 MB (225696222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-19-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:d66e37dac03b419ecec68d0d407fcfc2f1693cb661b122f24ac3e2e733ab52fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b787fc8b4860bc71972d0fbf8494979521f8ff7a7a7f769e2767adaf4eb66610`

```dockerfile
```

-	Layers:
	-	`sha256:3f33e79370ec6c6ac28ccf77a860af7b9c07136e99688903dde1a82a23101dbb`  
		Last Modified: Mon, 13 Oct 2025 21:23:26 GMT  
		Size: 3.6 MB (3640737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf64b528cd98eb4959c88ada35227ace8388eb3967fe3f245baf9bf24d415163`  
		Last Modified: Mon, 13 Oct 2025 21:23:27 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-19-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:518992b4523d828058fae037c21b2f4a2b0f448fded31cf05965c024c855c949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310131876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b4fd0300a1d7fa5bb4e3da8d35551153745a8f31d3fab7e81cdcb145d50d74`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
CMD ["/bin/bash"]
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 11 Oct 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+19
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='9a89dcca644d59f40b82f6712c854e416d5b5fe80808c40868e1ba2d6d8e1e9e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='2841b9fa0e22671fc0ee3e6ba1e87237d895446e7548021004f201a1ff5abd99'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09dde7f62f08c4f419f5b4d9cd6e8ca61653d876c53d501862e61f852e10141b`  
		Last Modified: Mon, 13 Oct 2025 18:20:13 GMT  
		Size: 38.5 MB (38490273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21451a66ce259cf7b8828e9dceb273999673d5d91342ac8c2fd51c435bdb3031`  
		Last Modified: Mon, 13 Oct 2025 18:18:18 GMT  
		Size: 223.6 MB (223553306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-19-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:a05b68b68de53980544b431212583f470fc021f423a57939446dc9db862d4b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3658532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87be79be9029cb84fed66f4dd49199a56b5ef92605d76c0b2c06c480a15a3fb`

```dockerfile
```

-	Layers:
	-	`sha256:1133a1bfbbf5192f569fd287b981ea74c90ab2b4550b126572fe941d862eb8f1`  
		Last Modified: Mon, 13 Oct 2025 21:23:31 GMT  
		Size: 3.6 MB (3638499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f709a2b22ef7542e335a7be86690575871a59b7dd9183d0d3e28235954d31e36`  
		Last Modified: Mon, 13 Oct 2025 21:23:32 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-19-jdk` - windows version 10.0.26100.6584; amd64

```console
$ docker pull openjdk@sha256:a11c28b420da137ff35ccec4aae692b550e32e59f7d29c0895b8a55d266cd7cb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3793803273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d596865be71e465de566632b9dde974cf112de10a448bc71aba277060f8ada17`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Mon, 13 Oct 2025 18:21:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 13 Oct 2025 18:22:32 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 13 Oct 2025 18:22:33 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 13 Oct 2025 18:22:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 13 Oct 2025 18:22:39 GMT
ENV JAVA_VERSION=26-ea+19
# Mon, 13 Oct 2025 18:22:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_windows-x64_bin.zip
# Mon, 13 Oct 2025 18:22:41 GMT
ENV JAVA_SHA256=b31dc1d0afdaba4c6b7a399e0a932fb1a4f5a61e7624aaad8ca40b85400f966a
# Mon, 13 Oct 2025 18:23:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 13 Oct 2025 18:23:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac58c0234c584817a261d280a90a93a32dcdff4099bfeae26d9cc974f8779939`  
		Last Modified: Mon, 13 Oct 2025 18:37:21 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d00ae36bb0ebef162f8a3563d9df78c2b405a328f61049d59d6b692cde3b4c`  
		Last Modified: Mon, 13 Oct 2025 18:37:21 GMT  
		Size: 389.2 KB (389178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8359e608c98bdd70e4f7d158dc8bfe26b2408404ed492ad61bdfb60125ea20e0`  
		Last Modified: Mon, 13 Oct 2025 18:37:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea9e6a7e3492342a227e657e8fa825b76a4dfa55fe2098381494df88e185bd2`  
		Last Modified: Mon, 13 Oct 2025 18:37:21 GMT  
		Size: 362.6 KB (362609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e961f49153bf991b3312cb08ac4f7f4bc9fb35fb3ee3b23cd5d51351037982b8`  
		Last Modified: Mon, 13 Oct 2025 18:37:20 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be929c303663995905a5cbbead1cf0f74ae3e3665ea2e2e79adafa5d0a159c5`  
		Last Modified: Mon, 13 Oct 2025 18:37:20 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757e62759d0e5e7fc449e486542e4d73d97192f6bca59cfaec8b144f236b8a68`  
		Last Modified: Mon, 13 Oct 2025 18:37:21 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d4cba39ce9f4205b28adb15e2d5a0f07f8717a28287c9866df0dbd0cbc42c9`  
		Last Modified: Mon, 13 Oct 2025 19:23:30 GMT  
		Size: 221.6 MB (221603955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf618fb4b482343fd5ba9a6ee056c6701d2cff103b7a68e1e8023df0b9b01cc`  
		Last Modified: Mon, 13 Oct 2025 18:37:21 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-19-jdk` - windows version 10.0.20348.4171; amd64

```console
$ docker pull openjdk@sha256:97343f988df496cd0efe696bdd7a1efaa075669764447ea4b61870244268337e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2504453667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a5738284ed6d6b75ea7bbdd1f7c866ca99c40956edf687112f8a6c7ff7d911`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Mon, 13 Oct 2025 18:21:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 13 Oct 2025 18:22:26 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 13 Oct 2025 18:22:27 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 13 Oct 2025 18:22:34 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 13 Oct 2025 18:22:35 GMT
ENV JAVA_VERSION=26-ea+19
# Mon, 13 Oct 2025 18:22:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_windows-x64_bin.zip
# Mon, 13 Oct 2025 18:22:37 GMT
ENV JAVA_SHA256=b31dc1d0afdaba4c6b7a399e0a932fb1a4f5a61e7624aaad8ca40b85400f966a
# Mon, 13 Oct 2025 18:23:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 13 Oct 2025 18:23:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Thu, 09 Oct 2025 10:32:05 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bb7dfcb21f637059e920895867272f6b5844269335225d912fd2c1c1f672f2`  
		Last Modified: Mon, 13 Oct 2025 18:34:23 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b602b2ce8095b05453a05481e04cee3f1320a02e300e093bae790d5abb11c62`  
		Last Modified: Mon, 13 Oct 2025 18:34:23 GMT  
		Size: 369.3 KB (369252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e36f72e2357a8545af99a74fa42b99190d692e240780234c476b7f9119f6cb`  
		Last Modified: Mon, 13 Oct 2025 18:34:23 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88770b40d9bfe1cc8d660c447d682003eaebbdf9dd7e06a9a1d10081bb0e4bec`  
		Last Modified: Mon, 13 Oct 2025 18:34:23 GMT  
		Size: 344.6 KB (344626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb606e0f0e306a112a7ae303c544c7c823c07ef6578f33d8a05554d38cc87560`  
		Last Modified: Mon, 13 Oct 2025 18:34:23 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3521842abf0442cb29c50df890d8cbee7eea5c1db9607ad2fde440e49e915f00`  
		Last Modified: Mon, 13 Oct 2025 18:34:23 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f868c3df2262bc1d2b6da516738171320a0c5e33aab40e7aee720df6942bf9ee`  
		Last Modified: Mon, 13 Oct 2025 18:34:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2818a4bbd44a88c3d895fc3fb6d2a27eb79548c70a0e09d040e3b757fa29015`  
		Last Modified: Mon, 13 Oct 2025 20:18:21 GMT  
		Size: 221.6 MB (221586912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ac1aee8213cc281f1bc814ebe3df548df4545336d38822dc56e6ae3e60bbfe`  
		Last Modified: Mon, 13 Oct 2025 18:34:23 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
