## `openjdk:24-ea-11-jdk`

```console
$ docker pull openjdk@sha256:b543447bb0bb6620ae8864ae22aaae20d01d1f29b65ecf27e31049a4f7f28d96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `openjdk:24-ea-11-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:f3b69cb3fa172881d2ea9f0e4788527d6ea6bf1c45c8ca66e16af0a6b96c528c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299798285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03a7361f764af255d8281fe056724929bfc3b71cdf890674c887a454f76c041`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Aug 2024 18:48:14 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
# Fri, 16 Aug 2024 18:48:14 GMT
CMD ["/bin/bash"]
# Fri, 16 Aug 2024 18:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 Aug 2024 18:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 16 Aug 2024 18:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Aug 2024 18:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 16 Aug 2024 18:48:14 GMT
ENV JAVA_VERSION=24-ea+11
# Fri, 16 Aug 2024 18:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/11/GPL/openjdk-24-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='c8cc4f7709c86eca1eb249323b8502416afffc54ddffc85278182dc222b1dcd8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/11/GPL/openjdk-24-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='cd79e2e9877e5f8efa2324bc78851af99fbd9dc936c41c7c07ba928efd889c21'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Aug 2024 18:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51423d70752a8af6f46da49d1118e48f7eacad87fa460cea855c86e7abe5150`  
		Last Modified: Wed, 21 Aug 2024 01:06:28 GMT  
		Size: 39.0 MB (39046709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7bc51f9c1a3ee526f4045af4c37ddd049cb6734fd1c7919275492b85c0c849`  
		Last Modified: Wed, 21 Aug 2024 01:06:31 GMT  
		Size: 211.8 MB (211756755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-11-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:2a467feeae15383bac92b89d0b3807e5cfd21c146774a97eb19656690233e468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58e538fccda0031b07627ea9583c3f80abb9e304aab07916cb1253f2e1138da`

```dockerfile
```

-	Layers:
	-	`sha256:0a2aa2ba8bc82097a860a64a80af3017ccd57ccf40bc74baeb29a0eab830e1e4`  
		Last Modified: Wed, 21 Aug 2024 01:06:27 GMT  
		Size: 3.5 MB (3545985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d44fe02863cbfb265ccf653f79716fc0f625dd89f566a1a5dd8862041232fa8`  
		Last Modified: Wed, 21 Aug 2024 01:06:27 GMT  
		Size: 19.5 KB (19528 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-11-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a235be72d2da585c19de02e23d39608ade2c6dc3508d6b703db18138194c6dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296741247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28486793e9c481b73b573b4564b1e5064fed9e5c5daaeefaddb5028b8b8e396`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Aug 2024 18:48:14 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
# Fri, 16 Aug 2024 18:48:14 GMT
CMD ["/bin/bash"]
# Fri, 16 Aug 2024 18:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 Aug 2024 18:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 16 Aug 2024 18:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Aug 2024 18:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 16 Aug 2024 18:48:14 GMT
ENV JAVA_VERSION=24-ea+11
# Fri, 16 Aug 2024 18:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/11/GPL/openjdk-24-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='c8cc4f7709c86eca1eb249323b8502416afffc54ddffc85278182dc222b1dcd8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/11/GPL/openjdk-24-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='cd79e2e9877e5f8efa2324bc78851af99fbd9dc936c41c7c07ba928efd889c21'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Aug 2024 18:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64a371a7ad1ff13a4dded4febe3bd91f6ddf3dac8b18dc7feef6e025c2943f3`  
		Last Modified: Wed, 21 Aug 2024 01:11:51 GMT  
		Size: 39.5 MB (39478981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d843b766bf93c7faa6e0eb014ff3ba6dc299de0fefa821aa723ac47ac4c591`  
		Last Modified: Wed, 21 Aug 2024 01:11:55 GMT  
		Size: 209.6 MB (209607700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-11-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:b554ec1cce800f3afc56954d457e95bf63195e70aee184401f21f0a82afac1d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3564371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60842824e85ebcf9160738ba2e3c3790341d60783907da99434bc403fae77a30`

```dockerfile
```

-	Layers:
	-	`sha256:edc1f213df313cdb112646ef05aba2f536f683d138fca0acca5bcead2b803582`  
		Last Modified: Wed, 21 Aug 2024 01:11:50 GMT  
		Size: 3.5 MB (3544368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a767213f1986303c48f27f4f2587b687bb09c945c13625a231e65083fe746ab9`  
		Last Modified: Wed, 21 Aug 2024 01:11:50 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-11-jdk` - windows version 10.0.20348.2655; amd64

```console
$ docker pull openjdk@sha256:fd1f4ca12c3f5a54e98065445a57a2bdc94ecd4d170c43f96847cc6d11ec77bc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2350396889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6baa243b23bb563e614d5a4dd2c4c17294b7b3f80514d07c155bd728dc61f4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Fri, 16 Aug 2024 22:08:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Aug 2024 22:08:47 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 16 Aug 2024 22:08:47 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 16 Aug 2024 22:08:54 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 16 Aug 2024 22:08:55 GMT
ENV JAVA_VERSION=24-ea+11
# Fri, 16 Aug 2024 22:08:55 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/11/GPL/openjdk-24-ea+11_windows-x64_bin.zip
# Fri, 16 Aug 2024 22:08:56 GMT
ENV JAVA_SHA256=7a69063e699bfa886323d4d41aebe553be53c68819b952fb7342fd73cc735697
# Fri, 16 Aug 2024 22:09:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 16 Aug 2024 22:09:20 GMT
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
	-	`sha256:020e0ad155fc185910867d71ec2eaa6ced1ad78cca2c59bba04d7c4c132253de`  
		Last Modified: Fri, 16 Aug 2024 22:09:25 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9389a83a13943f501a85aa2cb04c84ccef96a696240aa326db6420977d56ba`  
		Last Modified: Fri, 16 Aug 2024 22:09:25 GMT  
		Size: 360.9 KB (360894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6dc9bc6f3c47f209179c8d477c0e49ba1c64e634497698777045d122a6cc10`  
		Last Modified: Fri, 16 Aug 2024 22:09:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d77e1caf493ae8554e0c6a24fcc7d36a97097e41a7961cbf3273cc75a7e3063`  
		Last Modified: Fri, 16 Aug 2024 22:09:25 GMT  
		Size: 341.1 KB (341150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a0e976bcc25e6e514f995827973d660cf6413a0044c2f8d2d2694800d89102`  
		Last Modified: Fri, 16 Aug 2024 22:09:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c8db328e59bf440ce329e374c5063e7c7cde702716976026c2c33b6137ba60`  
		Last Modified: Fri, 16 Aug 2024 22:09:23 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2764b6d53e353cdbb3c6b06165be7ac2b63155ef0c3a0faf4307b1e06aa8d41`  
		Last Modified: Fri, 16 Aug 2024 22:09:23 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f942b077f2fa4373551bb6c248563d185cc6a577973e372faa9ce45fa9b9ac`  
		Last Modified: Fri, 16 Aug 2024 22:09:34 GMT  
		Size: 207.9 MB (207922132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd5888b353a4afa69195bd1d926ca7b3fc13d221caec0e2c7819541ece1978f`  
		Last Modified: Fri, 16 Aug 2024 22:09:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-11-jdk` - windows version 10.0.17763.6189; amd64

```console
$ docker pull openjdk@sha256:6b62abb3cfe281137ebff9a86a9235e84e3ee7763c424a4922672de2fcf44062
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2453974553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65de2250d32227b878fd7574a6a3c9ecd9b39ebef946a81ebc0eace90ab867d6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Fri, 16 Aug 2024 22:02:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Aug 2024 22:02:38 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 16 Aug 2024 22:02:39 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 16 Aug 2024 22:02:56 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 16 Aug 2024 22:02:57 GMT
ENV JAVA_VERSION=24-ea+11
# Fri, 16 Aug 2024 22:02:57 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/11/GPL/openjdk-24-ea+11_windows-x64_bin.zip
# Fri, 16 Aug 2024 22:02:58 GMT
ENV JAVA_SHA256=7a69063e699bfa886323d4d41aebe553be53c68819b952fb7342fd73cc735697
# Fri, 16 Aug 2024 22:03:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 16 Aug 2024 22:03:31 GMT
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
	-	`sha256:a9d25b119927bcfe5d32e85c7c17a6226207ca07b071d14beb6dc05db6850ba8`  
		Last Modified: Fri, 16 Aug 2024 22:03:39 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1266b3d9b99476f2dd66849d966507de5a78efea31bc1d7a39894608f037dc4`  
		Last Modified: Fri, 16 Aug 2024 22:03:39 GMT  
		Size: 488.7 KB (488749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfebf4a8c1c09851868e8172d616595590024210e407ca97ba45c12d5fdd235b`  
		Last Modified: Fri, 16 Aug 2024 22:03:38 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f967beb5c367d05757412c7c7b58a425a522df56e58f9d47080400dc7ad5c8af`  
		Last Modified: Fri, 16 Aug 2024 22:03:38 GMT  
		Size: 335.8 KB (335840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71c9d4c72f740a9eb61107afa23b15d8885494cd7eab927e56b42b7c1bfb0da`  
		Last Modified: Fri, 16 Aug 2024 22:03:36 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162edac2a55bb4b6ba7587b17c17dfe214324f0ba53f9b0b8c1a32e14592a70c`  
		Last Modified: Fri, 16 Aug 2024 22:03:36 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca708901375b06abb7391c6ba4e3b6e579b836482ea3dbf167aaedb182d6db8a`  
		Last Modified: Fri, 16 Aug 2024 22:03:36 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c30263b3af1d6e9c4d62d0b8c26b8043d2ac248020bab4ac7e3e3616c5f229`  
		Last Modified: Fri, 16 Aug 2024 22:03:47 GMT  
		Size: 207.9 MB (207938921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7a1ca3570c5dfc9e7efd943bc836f42761c244617ce344d1be0d7b2b06aa7b`  
		Last Modified: Fri, 16 Aug 2024 22:03:36 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
