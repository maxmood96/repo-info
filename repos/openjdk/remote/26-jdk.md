## `openjdk:26-jdk`

```console
$ docker pull openjdk@sha256:0f7fb77054eb74479b4cd9d53087da4fb5accc73a42e572c5266fa10ba75a7d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `openjdk:26-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:0d5b9570c8894efd1f4177404d20d4d2ba63d8e451847224ee3ae694fe64db32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313387385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79c652f7b9b6d93383f09aa129966cc508732aec99ec3fd7a8bc86244e8d3cb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 20:29:08 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 31 Oct 2025 20:29:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 31 Oct 2025 20:29:18 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:29:18 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 20:29:18 GMT
ENV JAVA_VERSION=26-ea+22
# Fri, 31 Oct 2025 20:29:18 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Oct 2025 20:29:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f52671d8640f78fb620835252e9bb17ede1f1ffe1d006b52689eccc020a81f9`  
		Last Modified: Fri, 31 Oct 2025 20:29:51 GMT  
		Size: 38.1 MB (38088664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e9256083390a62a4cd490d39471961833a586e8a03335840305f11c7680198`  
		Last Modified: Fri, 31 Oct 2025 21:26:04 GMT  
		Size: 225.8 MB (225802216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:8f9ad98cd841f05c46b832db67a084c7af9566d764fce090ec680cfb3d79f093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3658573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20953d97fc19157c86b180501890067983aa83743d965eea3c155f9cd1cd6dbc`

```dockerfile
```

-	Layers:
	-	`sha256:7f989b46ef1730f4dc8e3c9667ae6374cdd4d09c7e9837c26cb227989bd8bc0c`  
		Last Modified: Fri, 31 Oct 2025 21:23:27 GMT  
		Size: 3.6 MB (3638870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8911474527fa2abe19b2b3e33d6734a5639de9c187cc2ea4321cc4a3e6508596`  
		Last Modified: Fri, 31 Oct 2025 21:23:28 GMT  
		Size: 19.7 KB (19703 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:370113cfafc6796c1bfdb5ee27d86ede54095ef93030660853cb93788d49c8fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 MB (310219284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b971c8b6443a76930cf758dacdfa55e6979d71a9064afaef392f1b0b4b4ddfe9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 20:09:43 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 31 Oct 2025 20:09:53 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 31 Oct 2025 20:09:53 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:09:53 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 20:09:53 GMT
ENV JAVA_VERSION=26-ea+22
# Fri, 31 Oct 2025 20:09:53 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Oct 2025 20:09:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e330f617d80d4f200463c938ad131223d4f568895e3d18972993148c9cd7c8`  
		Last Modified: Fri, 31 Oct 2025 20:10:29 GMT  
		Size: 38.5 MB (38491320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21da5f6ea4336817b8bcb3323204c0a6ae9bf5a30f896762eed7114094f2fdfd`  
		Last Modified: Fri, 31 Oct 2025 21:26:28 GMT  
		Size: 223.6 MB (223641063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:d0eea96def5df3b13f675765cd13f4df271981c963a3079db90e9407690410e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3656622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bd7ab94463d30ea710ebd75ca89295fe18d6d452be08b5240bd6a94dd7cbcf`

```dockerfile
```

-	Layers:
	-	`sha256:e5dae7e5f4145771ca550b778cc6fdb7d3786533ecccb29eecee0b99f68fa6bd`  
		Last Modified: Fri, 31 Oct 2025 21:23:32 GMT  
		Size: 3.6 MB (3636632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff8b683dd0e12906f196f838cdb537a55fe4b2fe9097f3d43f18120201b4c5a`  
		Last Modified: Fri, 31 Oct 2025 21:23:33 GMT  
		Size: 20.0 KB (19990 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk` - windows version 10.0.26100.6905; amd64

```console
$ docker pull openjdk@sha256:1ec9f169e60d4255b3a5e4aeddd4fb8a31ed3fbed95c8f1f333bed4aef8129d3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3442797825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a24dacd9835f7e58b03c1ebf7fd15d9f49e3d068d262892a27f74cfa7892fb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 31 Oct 2025 20:11:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Oct 2025 20:12:45 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 31 Oct 2025 20:12:46 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 31 Oct 2025 20:12:54 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 31 Oct 2025 20:12:55 GMT
ENV JAVA_VERSION=26-ea+22
# Fri, 31 Oct 2025 20:12:56 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_windows-x64_bin.zip
# Fri, 31 Oct 2025 20:12:57 GMT
ENV JAVA_SHA256=8d5e7c08f721a437ebd1097300a807cf2574e5a2fece94320b0202fc8703ba8f
# Fri, 31 Oct 2025 20:13:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 31 Oct 2025 20:13:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6fa327080882d9e89d7fa2e8059b335954ccd065d5253b5b19934ca6a62bde`  
		Last Modified: Fri, 31 Oct 2025 20:29:04 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2096392c187762baeefcb1588af130383dd1a0010c34e05e5923ae6a71f1287`  
		Last Modified: Fri, 31 Oct 2025 20:29:05 GMT  
		Size: 389.8 KB (389794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a473a83fc970edc5581bc5e20b05ea2ed2acb92cfb742b52595080c75ede621a`  
		Last Modified: Fri, 31 Oct 2025 20:29:05 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bac283b6114c0ec4fbed4eff82d0be76e18fedc45bba9aab724c1b18a711f9`  
		Last Modified: Fri, 31 Oct 2025 20:29:05 GMT  
		Size: 363.4 KB (363437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5403900cd4f6c1415201b62bf9ff3c7c8c6bbdd985634cc48befc26cfa8ccc78`  
		Last Modified: Fri, 31 Oct 2025 20:29:05 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c8f3f35e203be3b104c75d9f26163e368df8c178b487a27b9ec2aa1fa22129`  
		Last Modified: Fri, 31 Oct 2025 20:29:05 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a567356615679b4492f79ecf627c2ec307eed675b5f1b451a393aa37f473ac`  
		Last Modified: Fri, 31 Oct 2025 20:29:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e156c3f6b3e72ea4947e746c8cd4dbf144ed20f32dc519cf83b8250398c0647`  
		Last Modified: Fri, 31 Oct 2025 21:15:07 GMT  
		Size: 221.7 MB (221689697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0e269b44172f92d89667da428a016816fdff5495fc3906482f955d85730ab5`  
		Last Modified: Fri, 31 Oct 2025 20:29:05 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-jdk` - windows version 10.0.20348.4297; amd64

```console
$ docker pull openjdk@sha256:ced56f3c09c8a24359c4b3101529a08d358208cf56eb0640536581381c28e066
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1799755209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6f72383caa193141f067856d072cc886b1eae5ef769732685b18a9025e0972`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 31 Oct 2025 20:12:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Oct 2025 20:13:14 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 31 Oct 2025 20:13:15 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 31 Oct 2025 20:13:22 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 31 Oct 2025 20:13:23 GMT
ENV JAVA_VERSION=26-ea+22
# Fri, 31 Oct 2025 20:13:25 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_windows-x64_bin.zip
# Fri, 31 Oct 2025 20:13:27 GMT
ENV JAVA_SHA256=8d5e7c08f721a437ebd1097300a807cf2574e5a2fece94320b0202fc8703ba8f
# Fri, 31 Oct 2025 20:14:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 31 Oct 2025 20:14:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fdc9e4c91313e0d8d35a8bc66a5fcdf64b2fa8df4b6ef66b15bdf501c67c1a`  
		Last Modified: Fri, 31 Oct 2025 20:24:22 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0950f094f0b08d3139550e1d68c2216ce57fb7be8ee0f02cb098d4a6e7251409`  
		Last Modified: Fri, 31 Oct 2025 20:24:22 GMT  
		Size: 521.2 KB (521215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5540843c398e3f7965e0f6a1e7de2f2896b765b58f9a49adbbd3e4652d1e67b0`  
		Last Modified: Fri, 31 Oct 2025 20:24:22 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03a89a3020f584b4810becc7bd5199dc50cf2d148d54c4f6f047cd2b0d20686`  
		Last Modified: Fri, 31 Oct 2025 20:24:22 GMT  
		Size: 360.3 KB (360309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beefec6b03e3434caa6bbec26a0379efcea9161768f56353876d1fe941039caf`  
		Last Modified: Fri, 31 Oct 2025 20:24:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6277ad0ae45b7c48bb5d8aa3e0c63c83a57b7ca145ce745feba7ddc4864e0fc`  
		Last Modified: Fri, 31 Oct 2025 20:24:22 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b424ef3d213c0acb116ab934ecfc66e08ff1683d14a5674b3321a198934f52fe`  
		Last Modified: Fri, 31 Oct 2025 20:24:22 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ade11dcd425d55740af5b4dcf92d98b884a69ac4159214d4c653c3d7f75944`  
		Last Modified: Fri, 31 Oct 2025 21:16:55 GMT  
		Size: 221.7 MB (221672933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9415c007ba84c3b8ed644c6ccf15a1a7d8c9da804ca0377d0c5ab19a0130df75`  
		Last Modified: Fri, 31 Oct 2025 20:24:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
