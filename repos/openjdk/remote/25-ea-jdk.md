## `openjdk:25-ea-jdk`

```console
$ docker pull openjdk@sha256:984319654f0164c6da60c125fd0152a6afc660a093c5945209b16c794d2951a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `openjdk:25-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:0058caf455d3abf7ad0aed38e8bb9ec007287e595997f6042e443f27bef55c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300480428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87970d20762c9aeec1703ac4fb7949acf7860a1e24840c634456a287e564d4ad`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Apr 2025 16:26:20 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Apr 2025 16:26:20 GMT
CMD ["/bin/bash"]
# Sat, 03 May 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 03 May 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 03 May 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 03 May 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 03 May 2025 00:48:11 GMT
ENV JAVA_VERSION=25-ea+21
# Sat, 03 May 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='9215df470d2d44c8ea731dcde9e170b6951e29f6e96e90625be983f0f9cfd1ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='23b6cbdac4dedcb1e7d290e7f5e9da01be8c4dcc35b4d296054aae3588d4465a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 03 May 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c2eb5d06bfeaafd2195d3612935e86f925a4620bf5bbcea5112a1fb07138dd80`  
		Last Modified: Tue, 29 Apr 2025 18:16:07 GMT  
		Size: 49.1 MB (49093011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7be8ad57ba147f1faf66dac5dac2e9ac884e3a969758333ac746acaf4af292`  
		Last Modified: Mon, 05 May 2025 17:30:24 GMT  
		Size: 38.1 MB (38107384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e9225792a5800b9744b44cd5267b0d56b1dc94dec4411793aeac4e1e04671e`  
		Last Modified: Mon, 05 May 2025 17:30:27 GMT  
		Size: 213.3 MB (213280033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:cea1729b3cedeb5ea00979f7db7bad192e34d1542a5e2694079f2b1100ed1b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3644252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232a8f1c6575a75d3c8f3a719aa039242eb9351b67b55382786a354e0cff2d21`

```dockerfile
```

-	Layers:
	-	`sha256:f157fb8230d8b278f468ac44d2bc46aecf392ba91e81d7dfecff4b7b40a79ed3`  
		Last Modified: Mon, 05 May 2025 17:30:23 GMT  
		Size: 3.6 MB (3624506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5e6ffde1f745d2e34e380ab2429deaeaf7d25945327de4297372fa29b442c87`  
		Last Modified: Mon, 05 May 2025 17:30:23 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b2280b3bab2f2de7d6f1a3e7cba3c1afff8484a0aab8aca36dacfd15ace20238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297256738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87efebcbe1a20957d10dd989159052e17c3607db7b5762c8c063bb24c9a9887c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Apr 2025 16:27:11 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Apr 2025 16:27:11 GMT
CMD ["/bin/bash"]
# Sat, 03 May 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 03 May 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 03 May 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 03 May 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 03 May 2025 00:48:11 GMT
ENV JAVA_VERSION=25-ea+21
# Sat, 03 May 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='9215df470d2d44c8ea731dcde9e170b6951e29f6e96e90625be983f0f9cfd1ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='23b6cbdac4dedcb1e7d290e7f5e9da01be8c4dcc35b4d296054aae3588d4465a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 03 May 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:88a33dc8906274baf54eb28aeefeba84c17922e3854e6fd41883f273d87d330d`  
		Last Modified: Wed, 30 Apr 2025 01:59:51 GMT  
		Size: 47.7 MB (47672989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b5aea1d0deca854a3762f4e396dad66260211f50004210a8e73e2146af926a`  
		Last Modified: Wed, 30 Apr 2025 07:05:49 GMT  
		Size: 38.5 MB (38500810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f36c2c1656d5723c281ee81a77bc930b13ca626cbab3bb305036c81383e7809`  
		Last Modified: Mon, 05 May 2025 22:36:20 GMT  
		Size: 211.1 MB (211082939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:d1673a59f1d720e561a56604a5933aad0808a422d69c930328a3e2d8ee67c51b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3642301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adbf14971bf9a6e324dc7c864e423bd3f5f26d7360a7f44e1b0a259c5271bedc`

```dockerfile
```

-	Layers:
	-	`sha256:f49b34296ee3272485a455ea939f05363c51a49b839fc79ebe9269a876467bce`  
		Last Modified: Mon, 05 May 2025 22:36:15 GMT  
		Size: 3.6 MB (3622268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:937c60518f6c48ce0425fac72468c506b099eebd0289f6788a049b2c2738c9fb`  
		Last Modified: Mon, 05 May 2025 22:36:14 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk` - windows version 10.0.26100.3781; amd64

```console
$ docker pull openjdk@sha256:28ef61f7f012fb42dd9888549ebe132a0013d93868483dbf842231cbd61e5499
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605190364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a21ade6abdd5b85963089e0cbf7a7a0964f1956f54ed2ba10b3ed852be6d70`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Mon, 05 May 2025 17:35:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 05 May 2025 17:35:48 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 05 May 2025 17:35:51 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 05 May 2025 17:36:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 05 May 2025 17:36:02 GMT
ENV JAVA_VERSION=25-ea+21
# Mon, 05 May 2025 17:36:05 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_windows-x64_bin.zip
# Mon, 05 May 2025 17:36:07 GMT
ENV JAVA_SHA256=50dc1f432a184e23ec8364a00fb4a5f8f791d3eed3a4d36226a041d7de9047e0
# Mon, 05 May 2025 17:36:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 05 May 2025 17:36:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9dc1da20dd7d9d66beced684a90f4859dade9e83ec2aac06a0cda2f32b90418`  
		Last Modified: Mon, 05 May 2025 17:36:38 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385128f8e202473808c7de73ddbf3661a28dc9281ca8149c262b66aed6e68886`  
		Last Modified: Mon, 05 May 2025 17:36:38 GMT  
		Size: 391.6 KB (391590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480086c53bfc672e0ee5d52f9f3ff30bbac7761df23f90c90bb598ec3c089f9c`  
		Last Modified: Mon, 05 May 2025 17:36:38 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9460df07f40ad4c56d41deac5cd729ae9ba4a3b75b5e8ba6564d5800c68fa6b0`  
		Last Modified: Mon, 05 May 2025 17:36:38 GMT  
		Size: 374.7 KB (374711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920e99fd7087652f68664fcf6e5e6e03b0b8e080cb8174697bd6111f7b40593e`  
		Last Modified: Mon, 05 May 2025 17:36:36 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c8169f4efe0081182d1906c41dc6f26ede7dceba957fa5324b0c6c16073e8f`  
		Last Modified: Mon, 05 May 2025 17:36:36 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6562b557d0f6ec04818ed22039d36a565b1df9bdfa6ee808936144715985aaab`  
		Last Modified: Mon, 05 May 2025 17:36:36 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f25f2253c13feacc4b7a68d57791154e5a84c3e8ad367035a719df517e6bf5`  
		Last Modified: Mon, 05 May 2025 17:36:50 GMT  
		Size: 209.3 MB (209254866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d51423187e6601617dfc769b0100176125ff68016f435d4940528a8daead750`  
		Last Modified: Mon, 05 May 2025 17:36:36 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-jdk` - windows version 10.0.20348.3566; amd64

```console
$ docker pull openjdk@sha256:397ca7e38b5b74a81757496212f1c65f26716627eab0d01300acd8a61d39c57f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2483483728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63829a33fd7840bf71ba4f707ba69e91920a6c1052afa4631c9eabd6cd93d54b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Mon, 05 May 2025 17:29:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 05 May 2025 17:31:03 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 05 May 2025 17:31:04 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 05 May 2025 17:31:17 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 05 May 2025 17:31:18 GMT
ENV JAVA_VERSION=25-ea+21
# Mon, 05 May 2025 17:31:19 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_windows-x64_bin.zip
# Mon, 05 May 2025 17:31:20 GMT
ENV JAVA_SHA256=50dc1f432a184e23ec8364a00fb4a5f8f791d3eed3a4d36226a041d7de9047e0
# Mon, 05 May 2025 17:31:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 05 May 2025 17:31:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fe7ba8fcbeae3a54a422b9b8dbf0b9121bb120cf75d491227247c2eb7d58d6`  
		Last Modified: Mon, 05 May 2025 17:31:54 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3b13adf06acb720df564d4777bdda93c0ddb9521686cd8677870f3229c8135`  
		Last Modified: Mon, 05 May 2025 17:31:54 GMT  
		Size: 369.6 KB (369582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0996a0a18f83ff41e65217749193939342b4ea74d255b4a645d15065823a73a`  
		Last Modified: Mon, 05 May 2025 17:31:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0924f0a971e566d029767519052116c9c1b3ac4667631b105ce3c12b204a417`  
		Last Modified: Mon, 05 May 2025 17:31:54 GMT  
		Size: 320.7 KB (320679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26788f68ea4c1ba446d6017ddbc2841a354849cce5f921f582c5ebe8082aebb`  
		Last Modified: Mon, 05 May 2025 17:31:52 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07a9b3d0c7d692bc4ca6b84a3cee100ac2aa34750fcb4cbf3c69fb25cb0b6dc`  
		Last Modified: Mon, 05 May 2025 17:31:52 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e2130f964c70ddd6cb327a0013e1ce68c04bae156f8273d04cbd93b59ee74b`  
		Last Modified: Mon, 05 May 2025 17:31:52 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde7b2a55a26ea1f5f1fa39b4a446354bb74d75e036f4f257a1e691c0f3c66f4`  
		Last Modified: Mon, 05 May 2025 17:32:03 GMT  
		Size: 209.2 MB (209203206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1760b30e3ff436378d8c3d843d51e580027d45e49ccdb3419f611873beed62da`  
		Last Modified: Mon, 05 May 2025 17:31:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-jdk` - windows version 10.0.17763.7249; amd64

```console
$ docker pull openjdk@sha256:e66aeb5929210a4e9cddd4e43bd714ed7b68ca3f803b048b45c88e4072001df8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2375422781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc5435f6646798a88d8e6ca25a9b48ae80d28f6da957ca477cfc77f9f7deae7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Mon, 05 May 2025 17:30:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 05 May 2025 17:33:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 05 May 2025 17:33:45 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 05 May 2025 17:33:58 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 05 May 2025 17:33:58 GMT
ENV JAVA_VERSION=25-ea+21
# Mon, 05 May 2025 17:33:59 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_windows-x64_bin.zip
# Mon, 05 May 2025 17:33:59 GMT
ENV JAVA_SHA256=50dc1f432a184e23ec8364a00fb4a5f8f791d3eed3a4d36226a041d7de9047e0
# Mon, 05 May 2025 17:34:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 05 May 2025 17:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d33ab57eea3ac259c13042d3b5aa44c76b9bb1d5bcb1c32cbbf392de50d776c`  
		Last Modified: Mon, 05 May 2025 17:34:51 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbbd0e4b759e40eac1be5bd24a028ae190614dbf3fdad435620c9d5684e0bef`  
		Last Modified: Mon, 05 May 2025 17:34:51 GMT  
		Size: 364.4 KB (364360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9213bbf4fd86b63c038405e6baec91de91f5b6da81bf611f3ce1e1eb0fafe325`  
		Last Modified: Mon, 05 May 2025 17:34:51 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb44b0f60d0f2e264b4e84d0533e33807c0959829341314bad86b8c8aa7b17b1`  
		Last Modified: Mon, 05 May 2025 17:34:51 GMT  
		Size: 310.3 KB (310270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a86735363a8b94069fc4e440baf6ab80ab63f5af6539587ecaff59c6d7b98e`  
		Last Modified: Mon, 05 May 2025 17:34:50 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3391d2a01efc3c421b9bab859e5e7250e865618a137bcd2b6da4cdec66f754c2`  
		Last Modified: Mon, 05 May 2025 17:34:50 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba209b546131662cef9f0e229addcf58971af17f68894e18334bf52d4f08b95`  
		Last Modified: Mon, 05 May 2025 17:34:50 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04890a83c56695270eac5222fc64d9de84c832020fa510ed221907bd5f77861`  
		Last Modified: Mon, 05 May 2025 17:35:01 GMT  
		Size: 209.2 MB (209214248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f6768314ead34460fa859d056b7fccfd7c8219e61a0da2113cc91bcb0307fb`  
		Last Modified: Mon, 05 May 2025 17:34:50 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
