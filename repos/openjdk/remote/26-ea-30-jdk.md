## `openjdk:26-ea-30-jdk`

```console
$ docker pull openjdk@sha256:0a11bf2a29094f5c95c4b986bdfdc5bda1ac464f3215d68507ef3689d6338a31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `openjdk:26-ea-30-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:fc8c4b3885c26019892dee4f911d5bf987513ff28a83c5338f80d71aa2927c45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313452269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36dabeb5f2e920192c2a513931db5eed70ee7b630679be560b58b5edb1c3ef4a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:28:27 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:28:36 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 16 Jan 2026 23:28:36 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 23:28:36 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jan 2026 23:28:36 GMT
ENV JAVA_VERSION=26-ea+30
# Fri, 16 Jan 2026 23:28:36 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Jan 2026 23:28:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fc6b1a1157059ffbac02377f85d44d8960a6d085ce336f896c6736e2579640`  
		Last Modified: Fri, 16 Jan 2026 23:28:57 GMT  
		Size: 38.3 MB (38295769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb26f8bced4f28a1377822f78e4ee81a2fd8a1662a6b2bc441b0d7032b22abf8`  
		Last Modified: Fri, 16 Jan 2026 23:29:01 GMT  
		Size: 227.8 MB (227841962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-30-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:e56f0fa74434ff3fc4cad8b4d0d8095ead8333d532b8a2ade55e3d027f9f932b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff74983ca25d96c37c02e948cb106681b4dc782c9889c533cb914461f589045`

```dockerfile
```

-	Layers:
	-	`sha256:a32ec14f2c478c8ddc4bd337ff50cf7be357b989e7a6360054edd68db979c2e6`  
		Last Modified: Sat, 17 Jan 2026 00:07:51 GMT  
		Size: 3.7 MB (3655371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dd8d94640c73ad245406f6d62fef1141130595dad944873074cd1c7153b205c`  
		Last Modified: Sat, 17 Jan 2026 00:07:47 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-30-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8cffdb6e3efe96aadd2c5308d41dfcb9cdc19a9342bd607b4daa1651e04d8b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310358638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afc87fda6faeba27fde3ed60824f2af6f596c4326dca89332e0664a5980697a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:31:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:31:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 16 Jan 2026 23:31:16 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 23:31:16 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jan 2026 23:31:16 GMT
ENV JAVA_VERSION=26-ea+30
# Fri, 16 Jan 2026 23:31:16 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Jan 2026 23:31:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:29:32 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c993bdf110f826a9133d09627e93d2f6fbc63b05c7486e6cc798ec0b27a29b4`  
		Last Modified: Fri, 16 Jan 2026 23:31:39 GMT  
		Size: 38.7 MB (38697994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ee0e35d152abf65e410de9f73a4037d066826911656aa15ceceb1f6aab42de`  
		Last Modified: Fri, 16 Jan 2026 23:31:43 GMT  
		Size: 225.8 MB (225758741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-30-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:38b921bac7aeb7f40c5bd735801d7f49beff9b26d112e037903b17e72d42355e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb09aead8caac7eb8f73f2a78468fcb48825c17ff9a45a380637e2f6b3aa5b7`

```dockerfile
```

-	Layers:
	-	`sha256:cf7cac28a9bd2c1ad3878d6a0f894b720ada23eb95bbf19fa28f88fd43e016f5`  
		Last Modified: Fri, 16 Jan 2026 23:31:38 GMT  
		Size: 3.7 MB (3653061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cc1179a90c273a972d7939f3709a1b23852b99453b8cde88e1ef376b48d4b57`  
		Last Modified: Fri, 16 Jan 2026 23:31:38 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-30-jdk` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:d626308a8e9d586920c980b220b6e5cce6f599e4a5acc2ddc27ad7724ea163e7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1720742556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fda4209441fd0907673be2cae910afd30184d7534f73eabe5ea241e0de009c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:53:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:00:32 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:00:32 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 13 Jan 2026 23:00:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:00:38 GMT
ENV JAVA_VERSION=26-ea+30
# Tue, 13 Jan 2026 23:00:38 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_windows-x64_bin.zip
# Tue, 13 Jan 2026 23:00:39 GMT
ENV JAVA_SHA256=43834141dc2e692e91f2f08c4cdfcbe91d8e33dea1abaace5b34ca7b14913f44
# Tue, 13 Jan 2026 23:01:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:01:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed7aff12eed6d468fbfd98c5cdb643204448d37e6b4376b4863d715fe54870b`  
		Last Modified: Tue, 13 Jan 2026 22:57:56 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c149fad9357b5cdfcaca55fcd6ac7b3399f61fa714b3956cbec0b4c06b4382`  
		Last Modified: Tue, 13 Jan 2026 23:01:39 GMT  
		Size: 370.7 KB (370713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b03aaceef5b42143ec9573a6b449d152d970c7390ce8f7615e52f6b977cda97`  
		Last Modified: Tue, 13 Jan 2026 23:01:17 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec79522e69a65c91961f53e5b585669223744461fe90f17ee9bb5836cf2ac5b4`  
		Last Modified: Tue, 13 Jan 2026 23:01:17 GMT  
		Size: 361.5 KB (361491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0001e60a3ec4f482d2c986a4df8cea5b6fcce24a854858a529394065c9ed6767`  
		Last Modified: Tue, 13 Jan 2026 23:01:39 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518236d5eb7376b4a396a89e2ad8f817e3d76756412c5953de43444869914da0`  
		Last Modified: Tue, 13 Jan 2026 23:01:39 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0caa44bc401c391a9f67c6b59f7bab66cb5771c02ff5c850db9028a1021b013`  
		Last Modified: Tue, 13 Jan 2026 23:01:39 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8a22031c61675746137a45345c39171c6b084247b0dfccafd02d8de9b2407b`  
		Last Modified: Tue, 13 Jan 2026 23:01:31 GMT  
		Size: 224.2 MB (224242160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0724d7401125beb7cfa4fa750652b1e73154325ef78a1c6df2f2a054c8b29ac8`  
		Last Modified: Tue, 13 Jan 2026 23:01:15 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-30-jdk` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:d8dd373304d857e9907f49a50ad59b6d5d5eca66fe848bd22ad1f8dbf37339fc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2060708795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef3c0143d5b8f270a7e20db71bef97f74d2a2caa9b3783178c0e6a958271e5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 22:54:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:10:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:10:45 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 13 Jan 2026 23:10:50 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:10:50 GMT
ENV JAVA_VERSION=26-ea+30
# Tue, 13 Jan 2026 23:10:51 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_windows-x64_bin.zip
# Tue, 13 Jan 2026 23:10:52 GMT
ENV JAVA_SHA256=43834141dc2e692e91f2f08c4cdfcbe91d8e33dea1abaace5b34ca7b14913f44
# Tue, 13 Jan 2026 23:11:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:11:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f08760e06519dd29e9a52391dac11e5952f68046c79c4bdea23cb54196c9897`  
		Last Modified: Tue, 13 Jan 2026 23:04:06 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4808f5095eed5048da9d8c0297b6117383db4a47baf032f33f6144af28df6a01`  
		Last Modified: Tue, 13 Jan 2026 23:11:22 GMT  
		Size: 483.6 KB (483585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da961f082c8915158eb3dd9db2ca6dff8cb2e4778f7b39570ce3f9c1336fff60`  
		Last Modified: Tue, 13 Jan 2026 23:11:43 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46840288a57e1c13393653027c3697419c9d380cdddec99f9c9da07ca41d857e`  
		Last Modified: Tue, 13 Jan 2026 23:11:43 GMT  
		Size: 334.1 KB (334145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588998e1f6701f51445f12d78df1794cd9a50ef26520ac7f95c3961cf0c7ad68`  
		Last Modified: Tue, 13 Jan 2026 23:11:20 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e598e22c53f3d96d467870ba47a825c366b9f241e97bf0d493534d5c6ef201`  
		Last Modified: Tue, 13 Jan 2026 23:11:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5040b122641d59e1883ae53152cdff153d8de6acdc108f1a68a268654f026c1`  
		Last Modified: Tue, 13 Jan 2026 23:11:44 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e189b5645be5c659967d8db1a6af08614d911433ad61c14debafc63225b475`  
		Last Modified: Tue, 13 Jan 2026 23:11:36 GMT  
		Size: 224.2 MB (224224077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4ea3423cba7bfe0e45216bd72344c90aee8080a01df3ac10734c26c2e4958d`  
		Last Modified: Tue, 13 Jan 2026 23:11:44 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
