## `openjdk:24-ea-jdk`

```console
$ docker pull openjdk@sha256:aceb6a0d22bfe605dcfbc0e8f1f514bb772038b65d19324cd1687d4f07d73308
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `openjdk:24-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:ede77f57a86f706ee32f9cf3104dde0c2f1592069975a624ea77ae351441c995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300348765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7319cf9cdad46f69d69c4ba7984a73537b660af158fdf1ee5a8692e48c59aa71`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 01 Nov 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 01 Nov 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+22
# Fri, 01 Nov 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='623a217a8f87e35d4ff793f172e2c66ac4abdd9ff21835d7ad8b1f0e1ad83fe4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='9a0070483615cc2db61a47afaec955cc7be38ec88f75856307bee73c9f601cbd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905fc93d8c6c5cbcfe1e3f43559a25a0a0a529ff4218d76a4e7905c4dbd523cc`  
		Last Modified: Mon, 04 Nov 2024 23:07:41 GMT  
		Size: 39.1 MB (39059547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0abe660239b7729b7ca295c843c45f3b9b6c4055c9977be21b12e92f009366a`  
		Last Modified: Mon, 04 Nov 2024 23:07:44 GMT  
		Size: 212.0 MB (212042276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:8d13b2b55cf036bf472fe908ccafcdb6393638c38c5509c256809eea0969b314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3801951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52848d4331df59b6de67c9f4001e9e20bae093219b339b91f66dc489f74218ec`

```dockerfile
```

-	Layers:
	-	`sha256:38eb47b5ff7cd0135994cbff80d714dfe1f192aad7e0995b9a1d5d6270c60450`  
		Last Modified: Mon, 04 Nov 2024 23:07:41 GMT  
		Size: 3.8 MB (3782205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1268f1e38ef22e657fc7c1f909ba1865c298d12fe1da28f6eba51d81567ca78a`  
		Last Modified: Mon, 04 Nov 2024 23:07:41 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9927b06d333f71e5a096113e8bc2ab8c852a01ebe6549dad7ff67c0d7ae228df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297719771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1c5157d84587cec195c544830b5e282f3820fc2d2e6ac9474e0fdc77abf979`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Fri, 25 Oct 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 25 Oct 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 25 Oct 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Oct 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 25 Oct 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+21
# Fri, 25 Oct 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/21/GPL/openjdk-24-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='c67029681a2f1c745c3a73366080881b2d349b4ffb9ce6a4e1e4b2c423555c5c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/21/GPL/openjdk-24-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='3850e8de3f5cc9a22fabc0963a04d6205a9f242cf2cfc0d67a4399a54deb725e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 25 Oct 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5187f7dd7781df5062b2bba7d82cb17d632e10163993162b9a27e2dc6d310`  
		Last Modified: Fri, 25 Oct 2024 22:58:22 GMT  
		Size: 39.5 MB (39491106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f6972361acb5dc096171d7eaeb6b7067a870716c17b52d1eb22b53b754110d`  
		Last Modified: Fri, 25 Oct 2024 22:58:26 GMT  
		Size: 210.3 MB (210314082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:89fe1d5f07eaa588814e3dc8a4f7a01519bcdbb777059e6e48c7b4f68d8e3a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00de8427d680d0ceaeaa5c0b3a40dbc4f883e35accd273612e9a6e45944aad8f`

```dockerfile
```

-	Layers:
	-	`sha256:36fa0f411137de8096c3245ee2aa3b5b164fec77cabd2690cb75fdfb7ec074e9`  
		Last Modified: Fri, 25 Oct 2024 22:58:22 GMT  
		Size: 3.8 MB (3779341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a5b027dab3a8f68ee631f2fc6eab9724a4d4de423cc54c3d629fdb4cc6b5aab`  
		Last Modified: Fri, 25 Oct 2024 22:58:21 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk` - windows version 10.0.20348.2762; amd64

```console
$ docker pull openjdk@sha256:8d24648e622a86999d1043f1d07c1933b75b15759e6808b7acf494314099eebe
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2008435267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0806fb89796505a4ad3dc450bd658387f7d92a18931fd33c90079fdc47d439`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Mon, 04 Nov 2024 23:07:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 23:08:17 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 04 Nov 2024 23:08:17 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 04 Nov 2024 23:08:24 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 04 Nov 2024 23:08:24 GMT
ENV JAVA_VERSION=24-ea+22
# Mon, 04 Nov 2024 23:08:25 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_windows-x64_bin.zip
# Mon, 04 Nov 2024 23:08:26 GMT
ENV JAVA_SHA256=3ab8853c76cbab5121e3c33e96b120f81d15b6979f56d1b4cc935ec94868413d
# Mon, 04 Nov 2024 23:08:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 04 Nov 2024 23:08:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df525ac0ebc3860930ef72be17bfb43a7cfa8c9535c1856c00b59d94e1f1348`  
		Last Modified: Mon, 04 Nov 2024 23:09:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72310977e90f8dcce705c8d63235f542cc0f3dd7fb1cd20d6cab44d746ec020c`  
		Last Modified: Mon, 04 Nov 2024 23:09:00 GMT  
		Size: 482.8 KB (482758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ae9e5a976f0a9db0a5dd39729ebe8b71d7a8adb34b3729a4c73c2f7805ee5f`  
		Last Modified: Mon, 04 Nov 2024 23:09:00 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb38bdabdfe61a694ca942bc148263fe5f5a13229cc635df17c91691b113140`  
		Last Modified: Mon, 04 Nov 2024 23:09:00 GMT  
		Size: 301.0 KB (301024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0ef8123c63b558e3627020f635753087ec206d903fb2232ea77c5d2d41c89a`  
		Last Modified: Mon, 04 Nov 2024 23:08:59 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af4d3aa4107b80ef4767f1817d7d0f2fd33319211797171aa8d99002502224a`  
		Last Modified: Mon, 04 Nov 2024 23:08:59 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b939bcdabf3399f3d7e39fe33e099ed5ea67513a9cf85c297d2e4d1423716318`  
		Last Modified: Mon, 04 Nov 2024 23:08:59 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb55c3912f573cca7bc688e38a600b4b0bdbbb15bbcf9b08fe79b997e0c3ee7c`  
		Last Modified: Mon, 04 Nov 2024 23:09:10 GMT  
		Size: 208.3 MB (208302219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679f7fce1df5eaff277092e9b574bc0156623d495a4ad2637af2da1981fcf781`  
		Last Modified: Mon, 04 Nov 2024 23:08:59 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-jdk` - windows version 10.0.17763.6414; amd64

```console
$ docker pull openjdk@sha256:5a2d1eb52e73eeb3f6de5828f324255a439f9cca64bda9a7d71f81c9e4578c81
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2110962827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cdddf8dfdf434395b3f0b62c7db6bd51eac66f02bfec5db4fe98328706546d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Mon, 04 Nov 2024 23:07:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 23:09:04 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 04 Nov 2024 23:09:05 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 04 Nov 2024 23:09:17 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 04 Nov 2024 23:09:17 GMT
ENV JAVA_VERSION=24-ea+22
# Mon, 04 Nov 2024 23:09:18 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_windows-x64_bin.zip
# Mon, 04 Nov 2024 23:09:18 GMT
ENV JAVA_SHA256=3ab8853c76cbab5121e3c33e96b120f81d15b6979f56d1b4cc935ec94868413d
# Mon, 04 Nov 2024 23:09:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 04 Nov 2024 23:09:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2eae996a46d273cb03c06eb66cb4f5c91491f932f0e75fd5be174fc0dfe0f20`  
		Last Modified: Mon, 04 Nov 2024 23:10:01 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a0298e3726208dacc3deb1d4d9ec56bb90a3255b7959114da276cdce3501c2`  
		Last Modified: Mon, 04 Nov 2024 23:10:01 GMT  
		Size: 473.9 KB (473862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d80d4f451d5218d787eb07259480da08e383c24be85c8eae06f6c8e2f9dec0`  
		Last Modified: Mon, 04 Nov 2024 23:10:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808c6e1f0f3da9da3982a7e873bd3aa62286af52918960203d2b26f3894b0aea`  
		Last Modified: Mon, 04 Nov 2024 23:10:01 GMT  
		Size: 317.1 KB (317126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbcb4f1e457af82aa4bdf618dcb93d94a990adad2e9e982d329c4d4f59fe491`  
		Last Modified: Mon, 04 Nov 2024 23:10:00 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbd3318bf73a6e7995919a47cf50277db584aed79d9c5b590127b87289a8147`  
		Last Modified: Mon, 04 Nov 2024 23:10:00 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24998f0249770e052cc238dd06756dea9ff11b71f76145c03a71ae08a95962dc`  
		Last Modified: Mon, 04 Nov 2024 23:10:00 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978a212ddd002569afc5d75504b57ac5d31501cb64cc13cea30ac03b3f7f362f`  
		Last Modified: Mon, 04 Nov 2024 23:10:10 GMT  
		Size: 208.3 MB (208338774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528f2832b6bbf2e39d503a3ab61a4611bd508697bb48c58fa3c8a3215f5114b7`  
		Last Modified: Mon, 04 Nov 2024 23:10:00 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
