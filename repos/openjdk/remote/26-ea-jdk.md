## `openjdk:26-ea-jdk`

```console
$ docker pull openjdk@sha256:75857b3ff2a6c97dc15c5d8bc45b3baffc530990d3886642dabf4d21d0bffe2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `openjdk:26-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:7803308aedc53372df7c8cecee2d6ede9482d4cc8af96aeb59ff2a079f02b728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313430828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8666b31dfea20b99dd84bbc30cc919f34ff9fee6b8f1ea37c6f3a6feb0ecb75`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Sat, 06 Dec 2025 00:33:43 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Dec 2025 00:33:55 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 06 Dec 2025 00:33:55 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:33:55 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:33:55 GMT
ENV JAVA_VERSION=26-ea+27
# Sat, 06 Dec 2025 00:33:55 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='c219dd04012af56a87523d69c6dd07a66adce846ff11981335a361ae9e0b4472'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b59cc8266e8d1eadc2919567b907da7098542b2c0d602eb73484728a0e7b2f7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:33:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4ff58ab1572230750b4a7fb82dbb75c767faa983eb2b1a4d6af78c78a6271`  
		Last Modified: Sat, 06 Dec 2025 00:34:41 GMT  
		Size: 38.3 MB (38298004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c2ecb57ff10f1e0cdbab7155c062e99458befe51b1408e7b91390cffb84041`  
		Last Modified: Sat, 06 Dec 2025 00:36:08 GMT  
		Size: 227.8 MB (227818076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:e84a8d95ecd11ae992f56fc72e754b100a25b25af18d2aa5829146aa38c913c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f1b4e5a198ddc627dd839e302205512f324518b6fed4623ef28ca5be1a7e5c`

```dockerfile
```

-	Layers:
	-	`sha256:4c9e2f716df8d0fadbe87849add970f2646fc7f5b94b6bc93e8576bed3b6df2b`  
		Last Modified: Sat, 06 Dec 2025 01:23:32 GMT  
		Size: 3.7 MB (3655331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbc3668237ef6bbafa8aa107c8b87035c5c77661abba690b02872a5b395705e0`  
		Last Modified: Sat, 06 Dec 2025 01:23:33 GMT  
		Size: 17.8 KB (17838 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7c1dd0a94111750f906beb74cbb825bce07cb161e2f06f567383c376aed1f69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.3 MB (310332373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b11da68091eca3fbf8d27b0a34e8e86152e1f017a04e8d33da12fb4402dab6`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Sat, 06 Dec 2025 00:34:40 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Dec 2025 00:35:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 06 Dec 2025 00:35:07 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:35:07 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:35:07 GMT
ENV JAVA_VERSION=26-ea+27
# Sat, 06 Dec 2025 00:35:07 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='c219dd04012af56a87523d69c6dd07a66adce846ff11981335a361ae9e0b4472'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b59cc8266e8d1eadc2919567b907da7098542b2c0d602eb73484728a0e7b2f7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:35:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8090318bfe3ef046daf7ec1e15088d12210fd6439a6ea2487afcfe38cd22f7c3`  
		Last Modified: Sat, 06 Dec 2025 00:35:43 GMT  
		Size: 38.7 MB (38700224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921ee30cbbd1ade4361d00a0bb9a1d54ce6d2635e9b602db7412792acf6e7217`  
		Last Modified: Sat, 06 Dec 2025 00:37:42 GMT  
		Size: 225.7 MB (225735117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:5618cab5a33beb8194ccf6408189aeb0dc258dd68eb6eb6240a2456d11069fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daaa861c4352a655da4ad9fd7f82cbb2168ad6c051782c9ec25b4e6446261e3a`

```dockerfile
```

-	Layers:
	-	`sha256:5dac55075565d376b2d9dd92da6b22c536b8bf3d6ed62ba7ad1d0552dcde7f23`  
		Last Modified: Sat, 06 Dec 2025 01:23:37 GMT  
		Size: 3.7 MB (3653021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2a3e517e38d008e0837d60e65dbcf8784abd5eefc36985eff517867919ed6dd`  
		Last Modified: Sat, 06 Dec 2025 01:23:38 GMT  
		Size: 18.1 KB (18053 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk` - windows version 10.0.26100.7171; amd64

```console
$ docker pull openjdk@sha256:6bbb49fb77386a335da6bd43997dc48b378b14f027b656360bd7a396e6927a25
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3461802924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb938c2dd4c78849dbe6376f57f89bfa2a1fcfc327285adad8a8f50098b00355`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Sat, 06 Dec 2025 00:40:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 06 Dec 2025 00:41:38 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 06 Dec 2025 00:41:39 GMT
ENV JAVA_HOME=C:\openjdk-26
# Sat, 06 Dec 2025 00:41:45 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 06 Dec 2025 00:41:46 GMT
ENV JAVA_VERSION=26-ea+27
# Sat, 06 Dec 2025 00:41:47 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_windows-x64_bin.zip
# Sat, 06 Dec 2025 00:41:47 GMT
ENV JAVA_SHA256=5fc8523fafe0bbe81e010d1bd57b12836c42cdd1f017e4492f67d56bde06f86a
# Sat, 06 Dec 2025 00:42:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 06 Dec 2025 00:42:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d491b064d08a64d94dcb03d80d556f4a1ba7a494f3762485661160f954d6ca`  
		Last Modified: Sat, 06 Dec 2025 01:00:17 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010d7cdade1e0cb34ee9aff67aa859146fa0787f28c26935e9493391c1a9a9e7`  
		Last Modified: Sat, 06 Dec 2025 01:00:17 GMT  
		Size: 392.0 KB (392004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d7c1e4d2b4eb18d0de48b2534dc228d0109411789a7ff557d5414f81de7822`  
		Last Modified: Sat, 06 Dec 2025 01:00:17 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736b240bc5c784f6e99fa25c5cb00b7a003f3f7893816981e33d5fc39c5520b7`  
		Last Modified: Sat, 06 Dec 2025 01:00:17 GMT  
		Size: 364.8 KB (364830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3a7d46e547a01cd0cf46ac0dbc7ee148d47ee4b105a68ee550fbf7c1404cff`  
		Last Modified: Sat, 06 Dec 2025 01:00:17 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46926f79000d266664eb73df67f91260bc080e122af2c0ca7d356a879b822a48`  
		Last Modified: Sat, 06 Dec 2025 01:00:17 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f6b09c2b479f9916ad26c427ac992a6555696b15ecfecfa2126a2a00a4513a`  
		Last Modified: Sat, 06 Dec 2025 01:00:17 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ea24ab29c5df3e1a421d68afa37b2d5a0bf52ca08065a0e0b2e5fa4bb80a1f`  
		Last Modified: Sat, 06 Dec 2025 01:00:43 GMT  
		Size: 225.6 MB (225582415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863c0b04b07e1cd4e3fa445ff7f9cbc2cc13e80714b56bb98c8cb91ea3adead0`  
		Last Modified: Sat, 06 Dec 2025 01:00:17 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-jdk` - windows version 10.0.20348.4405; amd64

```console
$ docker pull openjdk@sha256:47bee49942bd227a9e99119c4fd1bbaf7b86d1ff667f2fb964dba7ccdb8c1f64
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1996398069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d153ec78e11124ef7400d45ce9722a37b4309d157997a19a07d6bd14dbf068`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Sat, 06 Dec 2025 00:35:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 06 Dec 2025 00:36:13 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 06 Dec 2025 00:36:14 GMT
ENV JAVA_HOME=C:\openjdk-26
# Sat, 06 Dec 2025 00:36:21 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 06 Dec 2025 00:36:22 GMT
ENV JAVA_VERSION=26-ea+27
# Sat, 06 Dec 2025 00:36:24 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_windows-x64_bin.zip
# Sat, 06 Dec 2025 00:36:24 GMT
ENV JAVA_SHA256=5fc8523fafe0bbe81e010d1bd57b12836c42cdd1f017e4492f67d56bde06f86a
# Sat, 06 Dec 2025 00:37:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 06 Dec 2025 00:38:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8462076761531ece541cabbff8aa81904d45ff8a160c631ad6c756c28992e1c1`  
		Last Modified: Sat, 06 Dec 2025 00:45:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8504190794f5132138626e0d39aa6ce0ab2f2ea2b6097c6a0f0a9a46bd9fa5`  
		Last Modified: Sat, 06 Dec 2025 00:45:14 GMT  
		Size: 503.4 KB (503450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6b5f8d98f40b65f69ab8cab35c598883e94cac6ff276fb4f3ca26d843e41ea`  
		Last Modified: Sat, 06 Dec 2025 00:45:15 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b34eb090ef28780069b786a3fc78acd5351a4ed41b59355d32ebf2bab9a16a`  
		Last Modified: Sat, 06 Dec 2025 00:45:14 GMT  
		Size: 350.4 KB (350408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ce898cb9986365a8bd5cf55ce6fbc64841de2ad892b399ec872b0423f0d822`  
		Last Modified: Sat, 06 Dec 2025 00:45:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a688f845b597995cc8fbdeb016b93a4e6e2b703701455024f7d16c64fe40cbbf`  
		Last Modified: Sat, 06 Dec 2025 00:45:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2bbed5d893c469cfd0a51ca4278e1214afc683aaf76b1744190f29aa2ced43d`  
		Last Modified: Sat, 06 Dec 2025 00:45:14 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0195d684db06b7aff47c6bdcb2dacef9d691dccaaa757924d10d31a9e6a91c42`  
		Last Modified: Sat, 06 Dec 2025 00:45:32 GMT  
		Size: 225.6 MB (225574825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8d5b08796e1e5944fcedfe5d0dd6c786d2281633635a7f39509ff33e481253`  
		Last Modified: Sat, 06 Dec 2025 00:45:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
