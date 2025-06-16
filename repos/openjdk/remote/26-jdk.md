## `openjdk:26-jdk`

```console
$ docker pull openjdk@sha256:2178730a10a3876236b687627af3073dd9122e1357501b495c51242e6f8e8e8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `openjdk:26-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:f435c58cd39d589948752cf05f19fd11288cb910f25bd3243e553d2041322d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290044123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c3ea5ce6aefe762475a1630a1e09ac8d8ffd71a80390d45ff7bc84dd3f3d22`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Jun 2025 00:36:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 11 Jun 2025 00:36:51 GMT
CMD ["/bin/bash"]
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 14 Jun 2025 00:54:06 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:54:06 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_VERSION=26-ea+2
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='433a629dd1072b3147cce33cf79ae06ba8c7aa9aac53f403330e8f10ec12ca76'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f413ff4f8e92fcdeaf0da5315a51d2165a4017852a4a6c7e2731a8aae19e2e7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20970b710dabff28318bba6125553e1344b7fac9dfb1ceff5fcbd3b7de61de1d`  
		Last Modified: Mon, 16 Jun 2025 17:51:15 GMT  
		Size: 17.8 MB (17776180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d834b6a0f92cc067bba90f5f0ffe487815f03d0641765832e081fa7cc5d030`  
		Last Modified: Mon, 16 Jun 2025 18:30:50 GMT  
		Size: 222.8 MB (222767046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:01a76142cb535ae266afd2ed4a6fe79092b5b58d45aa13f9a333f9f561df0fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2622826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2963b51c96bdc4c33c95855000f06aa9259d430e4ed2904ad5f3c195f48fd09d`

```dockerfile
```

-	Layers:
	-	`sha256:dace497595592b7efe9d7f9dcd97c64ed774a0c838ac9a000717f6c2493d5e5c`  
		Last Modified: Mon, 16 Jun 2025 18:25:15 GMT  
		Size: 2.6 MB (2603105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19438dffc8fb63a3a7da43eba2d2f5cee6915f22688413ee3751b4b0ffd1e380`  
		Last Modified: Mon, 16 Jun 2025 18:25:15 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f435804bc973ba372eb8e323aca37eca30d87a0412cbcf7205936d50129b9edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (286987689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75abde1eccefb24f8ab6cd898793aa7bad06f53e4536e919d65f6e3de4c2768`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Jun 2025 00:37:07 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 11 Jun 2025 00:37:07 GMT
CMD ["/bin/bash"]
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 14 Jun 2025 00:54:06 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:54:06 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_VERSION=26-ea+2
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='433a629dd1072b3147cce33cf79ae06ba8c7aa9aac53f403330e8f10ec12ca76'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f413ff4f8e92fcdeaf0da5315a51d2165a4017852a4a6c7e2731a8aae19e2e7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7e489c978e38b5afa5d393fea94c54ad3525e6f544c411be6e80f47ef76d0a`  
		Last Modified: Thu, 12 Jun 2025 06:41:39 GMT  
		Size: 18.3 MB (18321513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7eaf5a9f5d2efa53320883debff828fb983f74e382a5891b6a91c8506c40fa`  
		Last Modified: Mon, 16 Jun 2025 18:53:30 GMT  
		Size: 220.6 MB (220576381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:24fe49d3e83f50f98dd4a1ad02c3beae167e4fa294a6ed10adeef4460909b330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2622105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0547661e3da4544c893eb5101a4eb434e9f301920e90bd42d94c4d17460049fa`

```dockerfile
```

-	Layers:
	-	`sha256:24d052c31aa1ffa973b17ac76125e8819810260c43801f00ca46c44dec757838`  
		Last Modified: Mon, 16 Jun 2025 18:25:20 GMT  
		Size: 2.6 MB (2602097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edf8b147a23f9ab8a489ff075c1f19d457abe2e81fdcb68bd13a9cf5edd6adc9`  
		Last Modified: Mon, 16 Jun 2025 18:25:21 GMT  
		Size: 20.0 KB (20008 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:e7738f7272419e976a8581a3c4a5fa6e98955c295f86aa2270381f7510dc7174
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3695736242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5e21bf08e798c349acb3630aeeabe546c6cc694e30aacea1cf70f07e0e2d48`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Mon, 16 Jun 2025 17:56:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Jun 2025 17:56:28 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 16 Jun 2025 17:56:30 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 16 Jun 2025 17:56:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 16 Jun 2025 17:56:39 GMT
ENV JAVA_VERSION=26-ea+2
# Mon, 16 Jun 2025 17:56:41 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_windows-x64_bin.zip
# Mon, 16 Jun 2025 17:56:42 GMT
ENV JAVA_SHA256=a9f823b291381b908d5f1a0ffaf16b5ff2b8749780ab76db3b8e8fde9bf04be0
# Mon, 16 Jun 2025 17:57:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 16 Jun 2025 17:57:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb4e9ac69db5330ec2ffd3d7316079b7bc261ee06297d591f1db9147d900212`  
		Last Modified: Mon, 16 Jun 2025 18:00:35 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ffdcb2820a23d8664e4a34410beabcd0966492a0d777f3fed832fda8b2dcb6`  
		Last Modified: Mon, 16 Jun 2025 18:00:36 GMT  
		Size: 404.5 KB (404541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4338a1f01c990f38548885294090261041e8df0fb096952368ff4def12b18b86`  
		Last Modified: Mon, 16 Jun 2025 18:00:36 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5befc4860767a48e07206d6c9da671b09ef2938ca842403b6b50c98241462c41`  
		Last Modified: Mon, 16 Jun 2025 18:00:36 GMT  
		Size: 385.9 KB (385865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17851a54a4189ae5b2c214714d828d4f9f31d9f2b2b4318deb649a6340064185`  
		Last Modified: Mon, 16 Jun 2025 18:00:36 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e7bc921e0e741a0a38f9262ede81743addebfde3a2b16a76ccce87946f9aa2`  
		Last Modified: Mon, 16 Jun 2025 18:00:36 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61dd1d1f15481d0df6d14448c19684684cfe7c3b60652b435aa6543ce210787`  
		Last Modified: Mon, 16 Jun 2025 18:00:36 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00831ed440681c1e666835552e58c0c09f51725973ce406908f40c14a10872c2`  
		Last Modified: Mon, 16 Jun 2025 18:09:16 GMT  
		Size: 218.8 MB (218763814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cc4b232ba17d2136b2d19e322290d951c543023eb1606d659b6ae8361cc92e`  
		Last Modified: Mon, 16 Jun 2025 18:00:37 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-jdk` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:da5ebe55a7bc14889eb772cacf7d5963e7a6dc2d9d1e8bc5ae7de5bf9529b3e7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2499712362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269deda5f817de18fab511fb3eff3e9a213b60e5b8c715e0ad017e8679832fa0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Mon, 16 Jun 2025 18:05:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Jun 2025 18:05:46 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 16 Jun 2025 18:05:47 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 16 Jun 2025 18:05:53 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 16 Jun 2025 18:05:54 GMT
ENV JAVA_VERSION=26-ea+2
# Mon, 16 Jun 2025 18:05:55 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_windows-x64_bin.zip
# Mon, 16 Jun 2025 18:05:55 GMT
ENV JAVA_SHA256=a9f823b291381b908d5f1a0ffaf16b5ff2b8749780ab76db3b8e8fde9bf04be0
# Mon, 16 Jun 2025 18:06:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 16 Jun 2025 18:06:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1044e6971b2fe48a264bf7ed3825934b8aa7c92569023b93d2f0ce6abda98ee2`  
		Last Modified: Mon, 16 Jun 2025 18:07:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947f5518145b35adc8e880d53095263341127912cc5bacd02ecedf4511b7cd7f`  
		Last Modified: Mon, 16 Jun 2025 18:07:49 GMT  
		Size: 365.4 KB (365396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fb5d508ef09978179f15c45c34d1a1508c1ded91dd704da0876ef2ec7eafa9`  
		Last Modified: Mon, 16 Jun 2025 18:07:50 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508e5855a79a9cf7ea2cb8b197ff769328310584d1bafd8ed3b7f9bc073f0351`  
		Last Modified: Mon, 16 Jun 2025 18:07:51 GMT  
		Size: 354.2 KB (354186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf31ca6e1f89f7353c8d51f7c6e84688887e88ccccb82aa27606b5d45ce9908`  
		Last Modified: Mon, 16 Jun 2025 18:07:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de38d3a9ef694c0c3b9f4d7bbc11786e25f48edc62425cef87babd108921f7f1`  
		Last Modified: Mon, 16 Jun 2025 18:07:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51b735e3aba05cbbe2f202104169cffb2e188fde3a20005141db7afbeb007d3`  
		Last Modified: Mon, 16 Jun 2025 18:07:51 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8f8147acacecead3747701c6b251ebff80129cd95e990e1ab2a5d7dfa822ba`  
		Last Modified: Mon, 16 Jun 2025 19:08:23 GMT  
		Size: 218.7 MB (218733441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f05f40c36e66e78de21a43c3bdbc0967fa1519ab5d9027ecdb17adadde068f9`  
		Last Modified: Mon, 16 Jun 2025 18:07:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
