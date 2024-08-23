## `openjdk:24-jdk`

```console
$ docker pull openjdk@sha256:f4562c137a19123663e733566e6b9781a465dcfa48c108d1472c0405fb537b9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `openjdk:24-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:bb775d80c2d72eb0b92f6421b43d2fc364b09a0f69546732b7d75d426df89605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 MB (300058858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e9f66d2c4901dd8646fd3a46e1ceebbdbddb9d3552a1894c024a0e735f5601`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Aug 2024 18:48:14 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
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
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4322799a14f7d92dd8d8f90e6c46e188ce6e3b737e17c2e3161acaf70f55495`  
		Last Modified: Fri, 23 Aug 2024 01:50:46 GMT  
		Size: 39.1 MB (39068112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5aef70e9107dd2a5aedb40d7dff3ae225d99ff7f3db5546f9b4b9306494a40c`  
		Last Modified: Fri, 23 Aug 2024 01:50:48 GMT  
		Size: 211.8 MB (211756682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:64566d6ea46fd4c0c7fc5590871aec5637c01605f6a3193dbdc64b743bcaa648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3663778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1f3d0527d2d8a6ad78b5f67bfbe91f11b18c2c3dbe237bc0b95277ef6ba075`

```dockerfile
```

-	Layers:
	-	`sha256:226a7da84af435bcc1235e14d3017febaca3eeb68ba1bf8fc1ef58eae4d8701e`  
		Last Modified: Fri, 23 Aug 2024 01:50:45 GMT  
		Size: 3.6 MB (3644251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5da6424fd65399f0b4071453588cb80060de0c3000977bc61e8326df01dd869`  
		Last Modified: Fri, 23 Aug 2024 01:50:45 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:744e8bc9e49b01b99944181afffba42580b871818f6306c9f686d85c24ea35a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (296992268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca59ef5b8f50f2e53fe3b25c8a752f3d516a5c101deff3c6c8db5ef2a2326fb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Aug 2024 18:48:14 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
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
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd1b36cd87201413a78d843fcfb1218c857939c3962a8c46b1f8126a2336f87`  
		Last Modified: Fri, 23 Aug 2024 01:54:37 GMT  
		Size: 39.5 MB (39496829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2890105f9ec25867ee76e02bf36128c83925a3c439045ca5fda24abd81272c9a`  
		Last Modified: Fri, 23 Aug 2024 01:54:42 GMT  
		Size: 209.6 MB (209607648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:a61582f29c7d9f13f2b105bd6beef6c7ccd1c824f10c578024a3e0a5bc10e9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3662637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff4fe6347448ee6a6c7c68b169d72e26185caa36156ceba1a1aaff3c7a4eb39`

```dockerfile
```

-	Layers:
	-	`sha256:fd9bd3a7eec396f182419ee6a73d5780d524378edd94269593e6e4fc6db4b679`  
		Last Modified: Fri, 23 Aug 2024 01:54:36 GMT  
		Size: 3.6 MB (3642634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39b717c0da2dda303d455d4056cad4750a663721ce5b5ce0f355c18e955baddc`  
		Last Modified: Fri, 23 Aug 2024 01:54:36 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk` - windows version 10.0.20348.2655; amd64

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

### `openjdk:24-jdk` - windows version 10.0.17763.6189; amd64

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
