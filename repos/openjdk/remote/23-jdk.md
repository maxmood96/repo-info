## `openjdk:23-jdk`

```console
$ docker pull openjdk@sha256:d6932e1d2681750b082126ed5f595cb0604ee25454781cd0fd29d92f55f839da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

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

### `openjdk:23-jdk` - windows version 10.0.20348.2582; amd64

```console
$ docker pull openjdk@sha256:3d5f49168b53daa46c74b66255519690b9e1a41a40d8958256fd532e610ddc15
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346726226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd78b686d518b28aa7e77bd1f2083261fbff025cbefae4fdfed745a6433625a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Mon, 12 Aug 2024 17:58:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Aug 2024 17:59:07 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 12 Aug 2024 17:59:08 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 12 Aug 2024 17:59:14 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 12 Aug 2024 17:59:15 GMT
ENV JAVA_VERSION=23
# Mon, 12 Aug 2024 17:59:16 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_windows-x64_bin.zip
# Mon, 12 Aug 2024 17:59:16 GMT
ENV JAVA_SHA256=b18897bec6b1c6e0f639d95757eb0e3b0ec3d69720f6e4631874f2f9408075c5
# Mon, 12 Aug 2024 17:59:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 12 Aug 2024 17:59:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1c9a02e3c8f8cb45b925d1c139e2ff509dc1f6e1782725286cdc09a41be716`  
		Last Modified: Mon, 12 Aug 2024 17:59:48 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48af13aa08e66390b1585c6370dc8b7325cb85edffda7548a28b88d26224f436`  
		Last Modified: Mon, 12 Aug 2024 17:59:48 GMT  
		Size: 358.0 KB (357958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9f4a6965f57f0a2710b219b543b2ce754cb755a90e2798476b54850ac0e9aa`  
		Last Modified: Mon, 12 Aug 2024 17:59:48 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818c8d2c75047be0c5680a738161ad0afba30702d65f51b5df725ed8c730d233`  
		Last Modified: Mon, 12 Aug 2024 17:59:48 GMT  
		Size: 344.1 KB (344133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228422811aaf5c8e6d93cfbe98cf48522a7f6eee8994d8d436e578fc532adf70`  
		Last Modified: Mon, 12 Aug 2024 17:59:46 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0538bb7ec51bd46a824a0b2b6c7cf99b426121ad22d61d758152a1fd408d61f`  
		Last Modified: Mon, 12 Aug 2024 17:59:46 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a206f37244844cb90b5ce972c3bcfed0c1fbe5b82e38d2b4a14220cc09e1aa8e`  
		Last Modified: Mon, 12 Aug 2024 17:59:46 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d867588610fd6f723b8f672009b4c40a90af1052c60f3ff1e5935e1013cd1c`  
		Last Modified: Mon, 12 Aug 2024 17:59:56 GMT  
		Size: 206.4 MB (206415936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb1d86c840e66900d109b6dc2cfdf3324f70d601fa1de819503ef1020e9b17e`  
		Last Modified: Mon, 12 Aug 2024 17:59:46 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-jdk` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:5f24c3eaf9f83a0373d4976784e9dbf8f4ceae066f61411b8fa660a15f543d26
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2445676504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128cc257453e32c23c5f11f7efcbcb6d0b402f67982a27cf04c05b7cd8b2ff11`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Mon, 12 Aug 2024 17:58:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Aug 2024 18:00:19 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 12 Aug 2024 18:00:20 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 12 Aug 2024 18:00:40 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 12 Aug 2024 18:00:40 GMT
ENV JAVA_VERSION=23
# Mon, 12 Aug 2024 18:00:41 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_windows-x64_bin.zip
# Mon, 12 Aug 2024 18:00:41 GMT
ENV JAVA_SHA256=b18897bec6b1c6e0f639d95757eb0e3b0ec3d69720f6e4631874f2f9408075c5
# Mon, 12 Aug 2024 18:01:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 12 Aug 2024 18:01:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0485a52b2750c5edb17d3e85e3529319914f5b22cf8753766e55ee20f3ec11eb`  
		Last Modified: Mon, 12 Aug 2024 18:01:28 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee8b218b15bb28346580cc025ad46cf8bd48e0b5f561b9fb420a13326b3658c`  
		Last Modified: Mon, 12 Aug 2024 18:01:28 GMT  
		Size: 488.7 KB (488659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d59080640177d6c33655e895233c773a865c183f452b6b89323d832196d22f`  
		Last Modified: Mon, 12 Aug 2024 18:01:28 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33acef4986e1e973579075c0e3092c491897e0d32a87c3ba740154d6e9d356c7`  
		Last Modified: Mon, 12 Aug 2024 18:01:28 GMT  
		Size: 332.3 KB (332262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433fda61ae3b2a8228a886b1796366b5c46e36065bb4b8735b7f3f97daf05cb4`  
		Last Modified: Mon, 12 Aug 2024 18:01:27 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d398a322c8bd668f7e6178eff7ee8fe86a5689f3a469ad0a129081ff958cff18`  
		Last Modified: Mon, 12 Aug 2024 18:01:27 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a41fd79f637eb5202ef4f323f815caeaa80569733f6a50e58092627d06bb1d3`  
		Last Modified: Mon, 12 Aug 2024 18:01:27 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534566af8484c380ad5fc3a1178e8b4f3d25823ea358b7988ec9abdd7013dd75`  
		Last Modified: Mon, 12 Aug 2024 18:01:37 GMT  
		Size: 206.4 MB (206418401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e905f3ed9d1ae9b89f53d995b8c4168eead00609a3819b1ad3d779f98d96c2d`  
		Last Modified: Mon, 12 Aug 2024 18:01:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
