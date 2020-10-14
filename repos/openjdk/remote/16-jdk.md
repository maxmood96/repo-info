## `openjdk:16-jdk`

```console
$ docker pull openjdk@sha256:94ec7569e433be16c7589b370cb601651dab24b028976b162dfdaad4dc1f8e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1518; amd64
	-	windows version 10.0.14393.3986; amd64

### `openjdk:16-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:1f1d62f8f4037f7bc9a78acb4d6d441e38a53521ce92ca956d637b48eed3d637
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264203028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd198485fdcbb9eef389549b564fda26d89a85aafbef2fbe7e6cc50356befa5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Sep 2020 21:22:07 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-amd64/8-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 8 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Tue, 15 Sep 2020 21:22:13 GMT
ADD file:8011e31575cbf4b8ebb243821b300ba24330e02cab925024aa98f4ce27997846 in / 
# Tue, 15 Sep 2020 21:22:13 GMT
CMD ["/bin/bash"]
# Tue, 15 Sep 2020 21:41:02 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 15 Sep 2020 21:41:02 GMT
ENV LANG=C.UTF-8
# Tue, 15 Sep 2020 21:41:02 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Tue, 15 Sep 2020 21:41:02 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Oct 2020 17:34:41 GMT
ENV JAVA_VERSION=16-ea+19
# Mon, 12 Oct 2020 17:35:22 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/19/GPL/openjdk-16-ea+19_linux-aarch64_bin.tar.gz; 			downloadSha256=9e7094e0dcba61b6b8111f48934cb7395e6dafb1d1ddea7d2296cb0872d67d66; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/19/GPL/openjdk-16-ea+19_linux-x64_bin.tar.gz; 			downloadSha256=487e44f1ec92106437a96f8af07a83ac314dee51dfd46838c23657e550bc616f; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Oct 2020 17:35:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:79701ada7495177c292979fd69d41eee91dc93ef0feea5ff95bb453f4ab7a1c5`  
		Last Modified: Mon, 14 Sep 2020 18:35:00 GMT  
		Size: 54.2 MB (54164063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47708145bbc56f1e73084e03c4662a6b29535708cfe5d51510cdae37bc363ba3`  
		Last Modified: Tue, 15 Sep 2020 21:47:10 GMT  
		Size: 13.5 MB (13491818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499afc7d5d1fe83ff9daf193859ad32eccfb8d949a94313bede60b88640dc280`  
		Last Modified: Mon, 12 Oct 2020 17:39:30 GMT  
		Size: 196.5 MB (196547147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a638e5e534f08414316e8e62d16370579fdaee7d28a8eff195717fe6e788af5a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243898205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3c8a7ace8ce90c746dd9701122a177aadfffc92f6cf390da292fc57335e8d5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Sep 2020 20:40:54 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-arm64v8/8-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 8 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Tue, 15 Sep 2020 20:41:01 GMT
ADD file:b3bd5c2ec8ff0efe8a0b1384563b42f02d6bcf7531132d9ec4748ecfe264d476 in / 
# Tue, 15 Sep 2020 20:41:02 GMT
CMD ["/bin/bash"]
# Tue, 15 Sep 2020 20:58:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 15 Sep 2020 20:58:31 GMT
ENV LANG=C.UTF-8
# Tue, 15 Sep 2020 20:58:37 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Tue, 15 Sep 2020 20:58:39 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Oct 2020 17:45:55 GMT
ENV JAVA_VERSION=16-ea+19
# Mon, 12 Oct 2020 17:46:39 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/19/GPL/openjdk-16-ea+19_linux-aarch64_bin.tar.gz; 			downloadSha256=9e7094e0dcba61b6b8111f48934cb7395e6dafb1d1ddea7d2296cb0872d67d66; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/19/GPL/openjdk-16-ea+19_linux-x64_bin.tar.gz; 			downloadSha256=487e44f1ec92106437a96f8af07a83ac314dee51dfd46838c23657e550bc616f; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Oct 2020 17:46:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a805b9845b615e5963d09def3e5e9919b39e76b5122c2abecc98d4a4bb358394`  
		Last Modified: Mon, 14 Sep 2020 17:43:27 GMT  
		Size: 54.3 MB (54266593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f893975677f1e890e793bb79d6684177489551bc055499096c3c153bc305e940`  
		Last Modified: Tue, 15 Sep 2020 21:04:39 GMT  
		Size: 14.4 MB (14366569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b559be1e73192a25483c03e133e5019d8d615a52508eee13d766036f45acbb06`  
		Last Modified: Mon, 12 Oct 2020 17:50:37 GMT  
		Size: 175.3 MB (175265043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-jdk` - windows version 10.0.17763.1518; amd64

```console
$ docker pull openjdk@sha256:6e23b9f7e44ca9bdccef6986c51bd3fae6c6192c03013bd2945ce1a2fbf10a40
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2580594494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e53a64aae95fe11a5e78a896263f566a1a8326fc8193d3fec13fce8f781e299`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 17:38:17 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 14 Oct 2020 17:38:18 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 14 Oct 2020 17:38:40 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 14 Oct 2020 17:38:41 GMT
ENV JAVA_VERSION=16-ea+19
# Wed, 14 Oct 2020 17:38:42 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk16/19/GPL/openjdk-16-ea+19_windows-x64_bin.zip
# Wed, 14 Oct 2020 17:38:42 GMT
ENV JAVA_SHA256=de05d9fe7d118efc99ecd1a98754da35dd41bbb167f67f27793c7429653178d2
# Wed, 14 Oct 2020 17:40:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 14 Oct 2020 17:40:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5f8e5825cfa7b4f8c5a50657da7a44c0547d90306b4fa11bbf82021b684262`  
		Last Modified: Wed, 14 Oct 2020 18:26:50 GMT  
		Size: 9.2 MB (9230486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e034563561e5379df3a00fd4da250e977243aacd8623dc768db3ef40497b87`  
		Last Modified: Wed, 14 Oct 2020 18:26:42 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24997a5d1f99495d60fc79a47ec6d7bcf172f637b322078eccbc230cebf01c74`  
		Last Modified: Wed, 14 Oct 2020 18:26:42 GMT  
		Size: 307.8 KB (307821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d222aa35b29acc7700925154b67606df5a40013ce378e3de7457ded1815a98`  
		Last Modified: Wed, 14 Oct 2020 18:26:39 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e36d70a3749360746db977698d39d4260c9a88d93f787dbd19a45e1a7a55ae`  
		Last Modified: Wed, 14 Oct 2020 18:26:39 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d17f6ae3a6c5aa4a716f6db8a4d56cd5f323e1e62661d857b3abd0dcccfeeef`  
		Last Modified: Wed, 14 Oct 2020 18:26:40 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed58c25f3204744f6c6c7cc5d1bcd6b81656c4f068be64d39f7d6fb78d4ec25c`  
		Last Modified: Wed, 14 Oct 2020 18:30:17 GMT  
		Size: 197.0 MB (196959225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c877514b5220a5ed638309e191608fd786775082878518ec73e8fc51765db40`  
		Last Modified: Wed, 14 Oct 2020 18:26:39 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-jdk` - windows version 10.0.14393.3986; amd64

```console
$ docker pull openjdk@sha256:0ebd8253981b93210e9f0607aa989e2294c068e247ea2adf9565d5f8b7c149d3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5958758908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8683ea4d2353ca76e95f7a1ef225f7e03f3fbe14b6bac5c9d3e86b8c19932392`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 17:42:04 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 14 Oct 2020 17:42:05 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 14 Oct 2020 17:43:23 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 14 Oct 2020 17:43:23 GMT
ENV JAVA_VERSION=16-ea+19
# Wed, 14 Oct 2020 17:43:24 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk16/19/GPL/openjdk-16-ea+19_windows-x64_bin.zip
# Wed, 14 Oct 2020 17:43:25 GMT
ENV JAVA_SHA256=de05d9fe7d118efc99ecd1a98754da35dd41bbb167f67f27793c7429653178d2
# Wed, 14 Oct 2020 17:45:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 14 Oct 2020 17:45:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48f75bae068c25f8a226647b58c0be2010ed0c8cd6921bdc70e67addcbf5a03`  
		Last Modified: Wed, 14 Oct 2020 18:30:55 GMT  
		Size: 9.9 MB (9914428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380be8c20c0be6ed94b2345de72a72dc8fa948cfb66f819ea06dbad3715e9431`  
		Last Modified: Wed, 14 Oct 2020 18:30:50 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2abbe75cd492fbd42e73733a282a661cb8caf898389b66479838c9d6a12bf93`  
		Last Modified: Wed, 14 Oct 2020 18:30:53 GMT  
		Size: 5.4 MB (5376495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c3237c44740eca9d5e3739fa337cf16483759d465df6956982fdb7b40380b9`  
		Last Modified: Wed, 14 Oct 2020 18:30:46 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47c2cbcead399a81c1d2603ac94418dbca3a0a89f3f5122777a9cc968e8efea`  
		Last Modified: Wed, 14 Oct 2020 18:30:46 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b18f8fcd164acc0596deaab273e14d4000fd8c4da2f71dae5ca99b5b2d3ace`  
		Last Modified: Wed, 14 Oct 2020 18:30:46 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c88970d8e9fd985d5b945055eb27f7389438f9558e54f226c5509432e5e439`  
		Last Modified: Wed, 14 Oct 2020 18:31:12 GMT  
		Size: 202.1 MB (202109470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404cf1fa6a8facece90cee70c67f28127335d2349656328bbd2fb3fa27f40791`  
		Last Modified: Wed, 14 Oct 2020 18:30:47 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
