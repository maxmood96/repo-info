## `openjdk:27-ea-jdk`

```console
$ docker pull openjdk@sha256:7e00c23f59882a9d3fe20b44523612fcfae5e32811a72f5d17a6d424d4c015d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `openjdk:27-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:1c09b28e8c9c22a522b09a837644a52f87282ebbbf82845f959eb9db6b69ec25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309602874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774922288ce36e5d6992d1a708f26e8acfda8df9765f9513474a186f46118487`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:51 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:51 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:12:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:23 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 18 Apr 2026 00:12:23 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Apr 2026 00:12:23 GMT
ENV LANG=C.UTF-8
# Sat, 18 Apr 2026 00:12:23 GMT
ENV JAVA_VERSION=27-ea+17
# Sat, 18 Apr 2026 00:12:23 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9052972f914c38a9c00c5d8104a0b58217438f9a672ae7abead7c12347bb0d7c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c2be8295243785a5077e17817615b5f355a643367e44eef5972e58fcbd8bde4b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 18 Apr 2026 00:12:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:59f98efa373e352e94c44103a934ba322d4b0d08d660faa4e8642d56b03dd4fe`  
		Last Modified: Fri, 17 Apr 2026 23:39:02 GMT  
		Size: 43.1 MB (43074999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f98796d55173168f20ae2a0e8ad60c5dbf836e09a8699591532eba7b10b74da`  
		Last Modified: Sat, 18 Apr 2026 00:12:46 GMT  
		Size: 37.7 MB (37678693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d7440525b54cae165ecc4a4ce5e8a0e250c84fe38cad3d75ecf949aca65e14`  
		Last Modified: Sat, 18 Apr 2026 00:12:50 GMT  
		Size: 228.8 MB (228849182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:33464708453f30e92a813b6600d68bc3a3bd0e1aaec51df12a7bd58d2d481b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c83440c177805e337423f0d2e2836a2c3a0de7220c8426c216ab0bb66537bb8`

```dockerfile
```

-	Layers:
	-	`sha256:c61ab1676e5ba1b6718182437fc64b3bdb0991701ca27d574d5a269ba5724273`  
		Last Modified: Sat, 18 Apr 2026 00:12:44 GMT  
		Size: 2.4 MB (2369035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d8fcc075f9d8f47a4fc8ab805511bcc50f26dc2fb72f2a79f1d77fa18ac1203`  
		Last Modified: Sat, 18 Apr 2026 00:12:44 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:13e634aa394c86a0dacf33dd409e7d963a320c0a38a738d4fbfa776ed00ad1e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (305983881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd6d540cc18f07df60365baaa6219612fd0dd2af043039893a4df3dfb537d92`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:18 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:18 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:12:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:36 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 18 Apr 2026 00:12:36 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Apr 2026 00:12:36 GMT
ENV LANG=C.UTF-8
# Sat, 18 Apr 2026 00:12:36 GMT
ENV JAVA_VERSION=27-ea+17
# Sat, 18 Apr 2026 00:12:36 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9052972f914c38a9c00c5d8104a0b58217438f9a672ae7abead7c12347bb0d7c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c2be8295243785a5077e17817615b5f355a643367e44eef5972e58fcbd8bde4b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 18 Apr 2026 00:12:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b998cd5b08c06e4f5efb16eb3e3a01c0e5c56b8b33a94e55d1a919f120c4e0ab`  
		Last Modified: Fri, 17 Apr 2026 23:38:28 GMT  
		Size: 41.5 MB (41476716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7a48a62ee8098e7cf4c52b2d58dbac7dae97753b6b5255807d6081ea21edd1`  
		Last Modified: Sat, 18 Apr 2026 00:12:59 GMT  
		Size: 37.7 MB (37698921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f6446b3bf63c4490af3e9befab67080afc04ca4517175920cbb0bf9e41a94e`  
		Last Modified: Sat, 18 Apr 2026 00:13:03 GMT  
		Size: 226.8 MB (226808244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:663f0425982bdbe281ced2acf036f6b071db8c212ce6652571f0e469fe96ca09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83dd4755a14127b290fecd8db705d1aa2dd4720a9961155d431ce97a5e57a45`

```dockerfile
```

-	Layers:
	-	`sha256:4756b65362479b47c7e0b3cd3527f30f0319a920c2f33a7092a0b0e1b9414010`  
		Last Modified: Sat, 18 Apr 2026 00:12:57 GMT  
		Size: 2.4 MB (2368563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d85db03892a5369dee9656f38c2bcd7628994bfc1932eabf675d071ce7fbb7d8`  
		Last Modified: Sat, 18 Apr 2026 00:12:57 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk` - windows version 10.0.26100.32690; amd64

```console
$ docker pull openjdk@sha256:97dc3acf18cd6596af901b936e875bfe91f3bea67e2a7d30b831dbeb2b2c1d27
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2355832628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509d0b8e511e479b2eadb22b0e2349a26defbca1348e5c3c771ba777d95c2335`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:02:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:14:56 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:14:57 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 14 Apr 2026 21:15:03 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:15:04 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 21:15:05 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_windows-x64_bin.zip
# Tue, 14 Apr 2026 21:15:05 GMT
ENV JAVA_SHA256=3cc253c247f136b430f6f42ac667120512f18fff012cfbf20817c6425edf15c7
# Tue, 14 Apr 2026 21:15:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:15:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285db92ff03740292d2e70ef81a1ebcda5d964ee8082b3dfae77c36c2f844e8e`  
		Last Modified: Tue, 14 Apr 2026 21:03:02 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6468b137e203035156b6ca55eff762c1938470eb825a3e58e70c36e93a0d1734`  
		Last Modified: Tue, 14 Apr 2026 21:15:39 GMT  
		Size: 338.6 KB (338603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88108e0d2e427fb6d6189ab2ac49a91e47f2438e85ea306fb87109f5fd94e420`  
		Last Modified: Tue, 14 Apr 2026 21:15:38 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add33a389d114549c294126d3ce1a07378dbebff29c455c1fec9774be18d5813`  
		Last Modified: Tue, 14 Apr 2026 21:15:38 GMT  
		Size: 330.7 KB (330702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36443e614f71773b88bc04f5e2e839661d482382808cbeb8ffb420804bbc9de3`  
		Last Modified: Tue, 14 Apr 2026 21:15:34 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8cbe7a774f3b0a336e3238584430153716bc8d4354c41a1a38c7e536690494`  
		Last Modified: Tue, 14 Apr 2026 21:15:34 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e089af2623e5ed1965e0147ccab3e6d3a8957c5327e151dc5b2232b140c52c9e`  
		Last Modified: Tue, 14 Apr 2026 21:15:34 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704e40e5696448a72b5699e09772fb696745dadac07bce4ed9a7020808c3009`  
		Last Modified: Tue, 14 Apr 2026 21:15:48 GMT  
		Size: 225.2 MB (225169413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7342a74566c58554bedfbae4beeffaff81d5ed38516a59fb5e90de2e287eb1f5`  
		Last Modified: Tue, 14 Apr 2026 21:15:34 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-jdk` - windows version 10.0.20348.5020; amd64

```console
$ docker pull openjdk@sha256:82a1e3b2456a44cb3c7cda1e7cad70926a42db10057a8480036b07fb1615555f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296241918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8710eed708c01f046c91f118281e1b8fbf8d1412eea4b736910482d904bd730d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:27:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:28:01 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:28:03 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 14 Apr 2026 21:28:10 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:28:12 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 21:28:13 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_windows-x64_bin.zip
# Tue, 14 Apr 2026 21:28:13 GMT
ENV JAVA_SHA256=3cc253c247f136b430f6f42ac667120512f18fff012cfbf20817c6425edf15c7
# Tue, 14 Apr 2026 21:29:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:29:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a7714c59919c6d44b28cf949bd217d46331d307a2e65ee104808286d94e42d`  
		Last Modified: Tue, 14 Apr 2026 21:29:26 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c3b0b3d2577cbf533fea0da989b44db0c4d3517aa9be19594e7498351686ad`  
		Last Modified: Tue, 14 Apr 2026 21:29:26 GMT  
		Size: 498.0 KB (497977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3686f058a0872f704d42eaec54442f986f56c3f54b436baf160194f7d32417c`  
		Last Modified: Tue, 14 Apr 2026 21:29:26 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc6ebceebf7adaefa0f4e550b5b37607999f707505431435d2699b5204aade5`  
		Last Modified: Tue, 14 Apr 2026 21:29:27 GMT  
		Size: 344.3 KB (344333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba0b905db28010609a00e5647a94f27d5c64155c70bbbf1a50623fe04ccf517`  
		Last Modified: Tue, 14 Apr 2026 21:29:25 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e70d0045bdfd8ef733b1fe499f0fe50d8516eeef6a6556296d43390484317d`  
		Last Modified: Tue, 14 Apr 2026 21:29:25 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f8fb0859c184b9cdd81c522accd01484d857babd9c5e560bf06a0ee2fb15a6`  
		Last Modified: Tue, 14 Apr 2026 21:29:25 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae97122d31259f7791675d94a05e21ba7971565d0efd458705ffb92368f84d03`  
		Last Modified: Tue, 14 Apr 2026 21:29:41 GMT  
		Size: 225.2 MB (225180440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4035c286f1de5c9f4bb9d5c1288d03d05748e680a7ec469a879810e566945263`  
		Last Modified: Tue, 14 Apr 2026 21:29:25 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
