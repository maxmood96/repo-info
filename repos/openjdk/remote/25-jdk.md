## `openjdk:25-jdk`

```console
$ docker pull openjdk@sha256:b64a126821ca0b9259f7b662df4fd54f113a7a13fb043af4a67b19420c428838
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64

### `openjdk:25-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:45cb451ba4e40cf623accd08dc6c335ee5dc16838f7ef02cee7e04631eb3db2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310559409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01572da91492b75b0c04d71ffcda999c44017a0d1646b8027ac07afc8b3000e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 30 May 2025 16:24:46 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 May 2025 16:24:46 GMT
CMD ["/bin/bash"]
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Mon, 09 Jun 2025 06:48:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 06:48:11 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_VERSION=25-ea+26
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='bec0201fc359c9fa1075d95f49a422113ce6aa004345eb6af1b6945a56880994'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c5be9b0a161ba87ed6632b21490aa7556cf615a4794dafe2dc87c93dd0ea9b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9845df06f911da943784ccfba2249144e9c16f5ad081b3583ac643cc30b49df0`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 49.5 MB (49497893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23d8df8cc87f696bbb58f025d825b1a8c79930e21bce87f21d52e6e1ac7ed98`  
		Last Modified: Mon, 09 Jun 2025 22:07:01 GMT  
		Size: 38.1 MB (38083311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc2e6cc5b1befaf3bc3acc92011301a29a9f6d8772722d555bfbb21c3f98bfb`  
		Last Modified: Tue, 10 Jun 2025 00:48:48 GMT  
		Size: 223.0 MB (222978205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:883c9db60db0f9decf9d2e780a2cc85bf9b09d0315c89c01d070ec9acf235754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69428b8c5cdd0787412502ba77432cfa7172df5eb3122a32c61300ce56ac9908`

```dockerfile
```

-	Layers:
	-	`sha256:ac7e80061f157736c0fb2745f5346913c17c03d011752e2c5dc975895069b4b4`  
		Last Modified: Tue, 10 Jun 2025 00:23:27 GMT  
		Size: 3.6 MB (3641236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37314215768d539e802b648a5e873218ef841e5e07f6e851e38e43691fbcbd6f`  
		Last Modified: Tue, 10 Jun 2025 00:23:27 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5fc02520792e6ef05ac16d9f5bdbd31f5852dbfbd288ec33b77b15b8b05bdd2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307355571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2fb726af5b83fe7f4e356adbc82e6d8339f64dc22c4fcf995db2db27bd9c2f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 30 May 2025 16:25:38 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 May 2025 16:25:38 GMT
CMD ["/bin/bash"]
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Mon, 09 Jun 2025 06:48:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 06:48:11 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_VERSION=25-ea+26
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='bec0201fc359c9fa1075d95f49a422113ce6aa004345eb6af1b6945a56880994'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c5be9b0a161ba87ed6632b21490aa7556cf615a4794dafe2dc87c93dd0ea9b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cfd988351345b9f04447fdf8c2c46e73b5a5a2afdfe346ff0026d0c170ac82`  
		Last Modified: Tue, 03 Jun 2025 13:49:29 GMT  
		Size: 38.5 MB (38495973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b5aa78add0916ace39c3afa9cf14b69ebc9e6f691b5df9d5dfb3ed1c4c96ec`  
		Last Modified: Mon, 09 Jun 2025 22:30:59 GMT  
		Size: 220.8 MB (220769019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:f6c257f44d721e62cd6214b0f04b22e438af8f06960c8e833442bee2c49bd6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3659031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9315bf9ddcb5a96017890fea7fd7a4299cfb9b4f3bf9a38264c9941a7373d520`

```dockerfile
```

-	Layers:
	-	`sha256:7926f16f05de0ae2987b10996586cb5a9efc7a9023bf37ab07ba67011feeb519`  
		Last Modified: Tue, 10 Jun 2025 00:23:32 GMT  
		Size: 3.6 MB (3638998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e28e7299dd798acd06c9e6d0206568c7715ccc1e8ebc251d8c869c1a1f7340c`  
		Last Modified: Tue, 10 Jun 2025 00:23:33 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk` - windows version 10.0.26100.4061; amd64

```console
$ docker pull openjdk@sha256:26e2dceedd7fde64c9c6b6d8ee16bd9a3a201ca9cf14fca63157f0a4015f7953
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3650396329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37741a49b057171051478776fb1fbb3dc95cb21551b7451bd3e6c862ecd174d4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Mon, 09 Jun 2025 22:11:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Jun 2025 22:11:27 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 09 Jun 2025 22:11:28 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 09 Jun 2025 22:11:34 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 09 Jun 2025 22:11:34 GMT
ENV JAVA_VERSION=25-ea+26
# Mon, 09 Jun 2025 22:11:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_windows-x64_bin.zip
# Mon, 09 Jun 2025 22:11:35 GMT
ENV JAVA_SHA256=6600725ff08e343ea49db5bdac0cc8ef756053c899efb6a504b5f9e4a2fcc69d
# Mon, 09 Jun 2025 22:11:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 09 Jun 2025 22:11:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d20626c5356d286dc015bfc02a35c7439fa6a1fdd0f0e1c3154150718ff7a4`  
		Last Modified: Mon, 09 Jun 2025 22:15:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cd14ae314c9c9b272c7f402fd6496b43000a857368a520a42adc83233191b4`  
		Last Modified: Mon, 09 Jun 2025 22:15:18 GMT  
		Size: 392.6 KB (392600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf47c0531eb0639c8eccc653ad181edae4490fe18edf26320730c4d0c2e5b455`  
		Last Modified: Mon, 09 Jun 2025 22:15:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516cfd8c532eb4e0995446c98ff9eaf65b106b2c247cfdfa8bd22edfa9d9397b`  
		Last Modified: Mon, 09 Jun 2025 22:15:19 GMT  
		Size: 376.7 KB (376681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45f464e18614be4653f31ea5378c4f1bb5d7d2133ddc6fd9081451d2250913`  
		Last Modified: Mon, 09 Jun 2025 22:15:19 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d512a3814ce42a725be31ba0409e56c4b1dc6f9cc45a33c1e7bd61d5357ccb01`  
		Last Modified: Mon, 09 Jun 2025 22:15:20 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73a0d78a720374bd1625e54ddc2371212a47abd1717d57723789efa3c4b14c5`  
		Last Modified: Mon, 09 Jun 2025 22:15:20 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7a562c357564c25f10e19a0bcb09dfd845bf42f02efc1b144c648a54605923`  
		Last Modified: Mon, 09 Jun 2025 23:07:05 GMT  
		Size: 218.9 MB (218853417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d339aa7fb9e8388ef037a23b3ea9a4a0272b81464a3e0b9fdfdb58500a5436b2`  
		Last Modified: Mon, 09 Jun 2025 22:15:21 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-jdk` - windows version 10.0.20348.3692; amd64

```console
$ docker pull openjdk@sha256:815bdd54d54a708b45e4fc93296f82e1fe5dbea124f310720bd8a609cde787ab
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2493098474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94fa12805567ebd6cf6e5155e67e88f65e879f0341a92330860b64d2188edce9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Mon, 09 Jun 2025 22:06:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Jun 2025 22:07:54 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 09 Jun 2025 22:07:55 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 09 Jun 2025 22:08:03 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 09 Jun 2025 22:08:04 GMT
ENV JAVA_VERSION=25-ea+26
# Mon, 09 Jun 2025 22:08:04 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_windows-x64_bin.zip
# Mon, 09 Jun 2025 22:08:05 GMT
ENV JAVA_SHA256=6600725ff08e343ea49db5bdac0cc8ef756053c899efb6a504b5f9e4a2fcc69d
# Mon, 09 Jun 2025 22:08:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 09 Jun 2025 22:08:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40a73470b9f9ad63fd495f460ee0fcb26ee7390bbc1915596a44b3629e4d069`  
		Last Modified: Mon, 09 Jun 2025 22:14:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0e63d9b861c13c668164f2903bdaed1eb5b96068e4b9efb7000b8422aa7a51`  
		Last Modified: Mon, 09 Jun 2025 22:14:52 GMT  
		Size: 360.4 KB (360357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee332543e2070ce2f7ac697bbf44ea9f5db89ef86e291da9e83f68b165d83f13`  
		Last Modified: Mon, 09 Jun 2025 22:14:56 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c835abdf02f16813962564296521b2f8630250e9df74355f07d6297ee67d24a3`  
		Last Modified: Mon, 09 Jun 2025 22:15:02 GMT  
		Size: 312.2 KB (312179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcff9d733c04076556260e0bb709d8ec0d59fa9cca70ece2ff0c3c3cabe8fb0`  
		Last Modified: Mon, 09 Jun 2025 22:15:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0666c4a5e81df20ec8eb367c7a0c1ff7f1c685f9a201dd692952a009a9233e77`  
		Last Modified: Mon, 09 Jun 2025 22:15:12 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ebf4dc0f40d28af7a2d90fdce9ab674888c9208a52b26e79e55a055c2b38a3`  
		Last Modified: Mon, 09 Jun 2025 22:15:15 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c3bc91e56f6a192b9a98f47a45a280f979b7e0cf61e24bdf3c2466f1daf5ef`  
		Last Modified: Mon, 09 Jun 2025 23:06:54 GMT  
		Size: 218.8 MB (218790098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8097dfe449e600ae045372db9bc94fc7a962337b4b35e8e59bc1d5ed337d7de`  
		Last Modified: Mon, 09 Jun 2025 22:15:18 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
