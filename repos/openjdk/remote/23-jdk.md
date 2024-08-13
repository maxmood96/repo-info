## `openjdk:23-jdk`

```console
$ docker pull openjdk@sha256:99f14abcb0128306ddae2aa65d0abe33cc9bd8b31fb7a299b6733c4500289587
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `openjdk:23-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:0f458e3b47d16ffdb8089e6e35b0da7d4c9a78bb0a6f7eb8d9585f3962e678d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.3 MB (299345608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1e7c80537140db57e5635ff65203c9fd3f0ddf2826ebe965caa1937c8877c6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
CMD ["/bin/bash"]
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 09 Aug 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='d8d169ae7a0285e09872565bc3044ad97697d3780e678d2a5ae9f8451c207cfc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5cad336e22d64a4a578f59d089223c226d67455c410cbaeb91f5fa0503ce2f96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd99a730f2ce347114a97667e995d24883880ce844e1e3a1fee2a4d5193dccf9`  
		Last Modified: Mon, 12 Aug 2024 17:59:23 GMT  
		Size: 39.0 MB (39047159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ee034621b4a9cfec94c8fb4f91561a108732a3f5addb24aa00c3755a03a872`  
		Last Modified: Mon, 12 Aug 2024 17:59:25 GMT  
		Size: 211.3 MB (211304713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:e9b145f0940c48e91444e14f88619a6ca4f6c86d2b0a82a461372462023403e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3561701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c64de40233849ff148439c2de052e6ca99a9c0a5d2bbc54a9a715275ae80a279`

```dockerfile
```

-	Layers:
	-	`sha256:0426d3fdc471bd6e8a7fdb47b3f8fe394f1c323da9df0be9c67c3b9d0fa4613f`  
		Last Modified: Mon, 12 Aug 2024 17:59:22 GMT  
		Size: 3.5 MB (3544037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6be9f5d06355d8877cee1084fd8593ddf67d06380303de117cae7567c58b72c`  
		Last Modified: Mon, 12 Aug 2024 17:59:22 GMT  
		Size: 17.7 KB (17664 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f8b0713f6b0b0da3d2685d2d03f172799874e5e5f0003590cfc14f592c4d4dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296313741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dc91c35c7a7ff6928f1e83207e578c3fd604f450aebd6b1dd7647acdfc20d7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 22:40:25 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Mon, 08 Jul 2024 22:40:26 GMT
CMD ["/bin/bash"]
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 09 Aug 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='d8d169ae7a0285e09872565bc3044ad97697d3780e678d2a5ae9f8451c207cfc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5cad336e22d64a4a578f59d089223c226d67455c410cbaeb91f5fa0503ce2f96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e12335bb1126bd80cd31b34b4fde93f2ccb7bb979403e778624cb60c3ece28c`  
		Last Modified: Mon, 29 Jul 2024 16:56:31 GMT  
		Size: 39.5 MB (39479870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4dae405cd0c91e2db058ab92394a314cccbe643a8759a6d82f5c7c1ee0284c7`  
		Last Modified: Mon, 12 Aug 2024 18:35:17 GMT  
		Size: 209.2 MB (209181210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:48f4f599bc3bccbc2adf6010f3af185be854772c0ac2614bf60da2ca9e1715c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3560415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31abd35de71948a94bc1b44f3b020acfd95928834ed7ffb157df26b2374bcca0`

```dockerfile
```

-	Layers:
	-	`sha256:fec81f5b75b52b42aeb0d2ebfd7176ffb68ec861a6652bed4a66cd20483d683f`  
		Last Modified: Mon, 12 Aug 2024 18:35:12 GMT  
		Size: 3.5 MB (3542348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2116a519cfc1286dfb3d1d4f52ada0852decc469c5340a3d4c6afb3a0cedf2d9`  
		Last Modified: Mon, 12 Aug 2024 18:35:12 GMT  
		Size: 18.1 KB (18067 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk` - windows version 10.0.20348.2655; amd64

```console
$ docker pull openjdk@sha256:edd86d0e7b1693f1060413d050c6e28e6a222600f286145c70355ecd8186f936
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348869833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb4d90a52e58f83029de0cfa10d1fc46d17109f05a92f0a637e22708404325e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Tue, 13 Aug 2024 20:10:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Aug 2024 20:10:46 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:10:46 GMT
ENV JAVA_HOME=C:\openjdk-23
# Tue, 13 Aug 2024 20:10:52 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:10:53 GMT
ENV JAVA_VERSION=23
# Tue, 13 Aug 2024 20:10:54 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_windows-x64_bin.zip
# Tue, 13 Aug 2024 20:10:54 GMT
ENV JAVA_SHA256=b18897bec6b1c6e0f639d95757eb0e3b0ec3d69720f6e4631874f2f9408075c5
# Tue, 13 Aug 2024 20:11:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:11:13 GMT
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
	-	`sha256:fc09bc75d43c40557b22c06f0797f0b469b59124226671e8464342862ffcfa16`  
		Last Modified: Tue, 13 Aug 2024 20:11:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fc8d20f0c792799b77e2395c660f2f548cb63d09b774f288d529b7120b9d46`  
		Last Modified: Tue, 13 Aug 2024 20:11:20 GMT  
		Size: 352.8 KB (352765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9c356654843ef09a161332cb9bc27274ec9adefe5507536c89c6bf73e46176`  
		Last Modified: Tue, 13 Aug 2024 20:11:20 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e7a4b35caa762efc0fc6096103d5eebcc5468d137259b7ad1d7f1783c2caa7`  
		Last Modified: Tue, 13 Aug 2024 20:11:20 GMT  
		Size: 334.5 KB (334515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451683ffe7e1a3ba0c8a58221021555f28cecfbed0b32828784f1c27915091f5`  
		Last Modified: Tue, 13 Aug 2024 20:11:18 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544217591296445b2ec212778acc0ad69493be69224f5f8573585ca1ee5b034a`  
		Last Modified: Tue, 13 Aug 2024 20:11:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f3d49d3ba66709e9ef33481c58bb94e1b3ae841f3d010e19e577e8e681a60f`  
		Last Modified: Tue, 13 Aug 2024 20:11:18 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5fec82d7a6a88bb50ee7a3dd8514b6017b1a91072e465824923ae23eb6aa91`  
		Last Modified: Tue, 13 Aug 2024 20:11:29 GMT  
		Size: 206.4 MB (206409867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfccad77c2dfd6e45ba7f99818bdc308e795b081d41f5178ad3f758d69334ac1`  
		Last Modified: Tue, 13 Aug 2024 20:11:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-jdk` - windows version 10.0.17763.6189; amd64

```console
$ docker pull openjdk@sha256:88df5d409ff9a181a8cdaa4fe0762e0cbec0917afe9848277bf12b4fe9c24e07
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2452447898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb40c197d597dcbb7bdd23555f81eea2f0a4db5462e7e4fbff58b725ed8d838`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:22:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Aug 2024 20:23:42 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:23:43 GMT
ENV JAVA_HOME=C:\openjdk-23
# Tue, 13 Aug 2024 20:24:01 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:24:01 GMT
ENV JAVA_VERSION=23
# Tue, 13 Aug 2024 20:24:01 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_windows-x64_bin.zip
# Tue, 13 Aug 2024 20:24:02 GMT
ENV JAVA_SHA256=b18897bec6b1c6e0f639d95757eb0e3b0ec3d69720f6e4631874f2f9408075c5
# Tue, 13 Aug 2024 20:24:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:24:39 GMT
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
	-	`sha256:93ea461e47505e6d80552039fa353c061374ee1e4a787b8fd39eae413b00d676`  
		Last Modified: Tue, 13 Aug 2024 20:24:43 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec235f678c457b9b63f4e3063293dd09753f918af8277fb45e18eb1e94f7d1d`  
		Last Modified: Tue, 13 Aug 2024 20:24:43 GMT  
		Size: 488.5 KB (488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65a4db3505ecdfcd7fe910a9582573e43d4a9f2232b23f707133b0d4796e3fe`  
		Last Modified: Tue, 13 Aug 2024 20:24:42 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0f8b9b20c346f4830189f12333c883cbc5c98fc3509db14da10ef2244010c2`  
		Last Modified: Tue, 13 Aug 2024 20:24:42 GMT  
		Size: 335.5 KB (335471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8a877757de33a773a410ec7974470fcf0b736b8931599faf05f54a8a30416f`  
		Last Modified: Tue, 13 Aug 2024 20:24:42 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af6053cb92cb5642dfba8066acc9c6710733a8b0f40b39f33cb7b08257fa178`  
		Last Modified: Tue, 13 Aug 2024 20:24:42 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78dbd5233bee791b33177018960430cd7a4f3d60fb4aa071f4aa91c2deeb4b62`  
		Last Modified: Tue, 13 Aug 2024 20:24:41 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa829cd0ca01150e87729e82f589c595186ca7a8f636b467eecc2ff3bc9998f`  
		Last Modified: Tue, 13 Aug 2024 20:24:53 GMT  
		Size: 206.4 MB (206412834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1221680068eb05cf37ad39445aa0577e9e64fc3f723794cee69cff2062efdfa`  
		Last Modified: Tue, 13 Aug 2024 20:24:41 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
