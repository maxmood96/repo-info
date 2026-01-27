## `openjdk:27-ea-6-jdk`

```console
$ docker pull openjdk@sha256:4a40ea103b2567c455dadfe1ca447facf8910e3c48a7ad900713b40a3b8eff3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `openjdk:27-ea-6-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:eea1ccef564cd0e126101c49f559d930ac65e9c5df2040fdd50d7c53a10b5b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313835437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5aca41f277bf60d05427282e40dae5ddffe26a0343a8ff618fcb340376334a4`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Mon, 26 Jan 2026 22:11:36 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:11:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 26 Jan 2026 22:11:49 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:11:49 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 22:11:49 GMT
ENV JAVA_VERSION=27-ea+6
# Mon, 26 Jan 2026 22:11:49 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='394c8962532cfeb8e27701615449f453f090145d33f7d24947aa6ceed07dcce6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='e516f107cd78b8abf3500494b93d20718e0779fa79a12399f30928c615593789'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 26 Jan 2026 22:11:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca5ec52900c47e04ce91efb280aeef445af57f0045255ebff2c015347d2bf61`  
		Last Modified: Mon, 26 Jan 2026 22:12:10 GMT  
		Size: 38.3 MB (38296468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ab52a7136cd13fb35af48655577a5c75e23cb1b14063fe4d3e3353f19061bb`  
		Last Modified: Mon, 26 Jan 2026 22:12:14 GMT  
		Size: 228.2 MB (228225421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-6-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:88dde1f1fb9a49b797b8767657802d5d4ab86d893e9ef5301e080e4a56b7e725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92a273b06d07c575a328d49d1cde9362bec6e6ad121d9bab3c0f9bc314b4ecf`

```dockerfile
```

-	Layers:
	-	`sha256:ee6cd789ff4bd1f9f0cfaa19af2231661cdc8ded56ba2edc5ba1da86d071c021`  
		Last Modified: Mon, 26 Jan 2026 22:12:09 GMT  
		Size: 3.7 MB (3655359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b4e6b93cbd9172a4d57deb43aebca8159ce8c7a63de8f9f5f026cf5b17c16d3`  
		Last Modified: Mon, 26 Jan 2026 22:12:08 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-6-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8a19ddcc5ecc68f1f932d9c77b00af84de5eb28947672869a428dde1b4fc5d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310750005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2705d607bd384b9eabb07aaca8f219f9950e5dab090212871b72ccb73fdb42e4`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Mon, 26 Jan 2026 22:10:26 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:10:55 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 26 Jan 2026 22:10:55 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:10:55 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 22:10:55 GMT
ENV JAVA_VERSION=27-ea+6
# Mon, 26 Jan 2026 22:10:55 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='394c8962532cfeb8e27701615449f453f090145d33f7d24947aa6ceed07dcce6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='e516f107cd78b8abf3500494b93d20718e0779fa79a12399f30928c615593789'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 26 Jan 2026 22:10:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed60f0093ebb545ea3ec474fd492977af3e25cb518ee3a3f00438b46d8897d`  
		Last Modified: Mon, 26 Jan 2026 22:11:18 GMT  
		Size: 38.7 MB (38699651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bf487714f7623c8cc56a7c6e74159a39af5914ad17478f23fda960ece90ccd`  
		Last Modified: Mon, 26 Jan 2026 22:11:22 GMT  
		Size: 226.1 MB (226148444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-6-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:fc3a783fafb48077612e9fbde5f4f1dc87880b0d2db693deccf18126f040c5f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb61e88edc2fc244fb56a8a22046d2ca74faa1b33a57c8f7166801aecd715b5`

```dockerfile
```

-	Layers:
	-	`sha256:176ea8504218421ad0ebd3087fb6dad686168fa94baaab99df24e1f54bf1ff57`  
		Last Modified: Mon, 26 Jan 2026 22:11:17 GMT  
		Size: 3.7 MB (3653049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:590afeaf8d6ed2fbd36aefde3ce46078aa2789ba24cb7465e4e85d73b890ba54`  
		Last Modified: Mon, 26 Jan 2026 22:11:17 GMT  
		Size: 18.0 KB (18029 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-6-jdk` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:7d859c1b2378ad3253e2b654a7bd6f707fa8ec73eb2fa6c969addfba8c19ee26
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1721185849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651f5f69ec50448acefcd6ebe54218772bd068d9e11033f300e9fee07cda4e39`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:08:33 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:08:34 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 26 Jan 2026 22:08:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:08:39 GMT
ENV JAVA_VERSION=27-ea+6
# Mon, 26 Jan 2026 22:08:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_windows-x64_bin.zip
# Mon, 26 Jan 2026 22:08:41 GMT
ENV JAVA_SHA256=dad15ea855765f796d0a975373f5f6aa7e247d717d129641177c41ee0cbe211c
# Mon, 26 Jan 2026 22:09:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:09:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a1ee0bf0167df6115953b6b1b098fa7a7d283b273426e6102f22f9f9cda0ab`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 403.9 KB (403850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48792ea1b7025d5b1254b2044b585783cbec73f35e438ff315edd7d77db07472`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c729d92fcc29b96e35583ec02da675ce9c8fb502e913f8fec07ceb5600d74a`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 388.8 KB (388796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442a4e75aa3f26e3e8f67ca78b91e4f42f950497956d9d357722aa918051f139`  
		Last Modified: Mon, 26 Jan 2026 22:09:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af94527c78e3478cc47da34e9d0a8333a10af87043c6239e5a3c6c519e3e8116`  
		Last Modified: Mon, 26 Jan 2026 22:09:20 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c936ac13317978a6f488e1712e5c16379ebaae55ef169b5015d4cc0a207c0a`  
		Last Modified: Mon, 26 Jan 2026 22:09:20 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40d0fbb771a150b90d600acb5d48bc7182a335e1011814b69ebe9d6d3c1e882`  
		Last Modified: Mon, 26 Jan 2026 22:09:36 GMT  
		Size: 224.6 MB (224625010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609f3fe84f8db0453942811ffc4bca8a6c16f9244eaddb4132c8cdace10323f9`  
		Last Modified: Mon, 26 Jan 2026 22:09:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-6-jdk` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:f1c30f1c79ce04119ee0f5888fa67eb14e937ca497455edae64f56b283661564
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2061109356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592b8415637416d3e715dbd56186c0e96cb9ab50c9038f9c40ee34c45f9e3878`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:08:48 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:08:49 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 26 Jan 2026 22:08:56 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:08:57 GMT
ENV JAVA_VERSION=27-ea+6
# Mon, 26 Jan 2026 22:08:58 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_windows-x64_bin.zip
# Mon, 26 Jan 2026 22:08:59 GMT
ENV JAVA_SHA256=dad15ea855765f796d0a975373f5f6aa7e247d717d129641177c41ee0cbe211c
# Mon, 26 Jan 2026 22:10:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:10:18 GMT
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
	-	`sha256:d76ff2a09c21b3d7e083854bf410cec2dd68e42740043ac4fdacd0bc8265ef2a`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7334237da746dd9e131c778b3600cb33732f93a96573dc62e7380e5750fd3306`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 503.6 KB (503582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42fb1fae328f7f30004d4efada45f6777936c5d10b6a930d2c3ef352702a331`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec55cedc65038f0cdb1737c1058132c56ccd231620d1285ece72d3d6e91f2228`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 351.9 KB (351912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7dea516e5f8ca3463a39f472c44a87df6eb8aace60d4cb821e963411f9669b`  
		Last Modified: Mon, 26 Jan 2026 22:10:26 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7465b25cd00fe3671ce1b3b27c1bbe25f74fbc623a463ade80b41568f4ea1aee`  
		Last Modified: Mon, 26 Jan 2026 22:10:26 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d20f5d994a0533e7e95525f64fd6104318d4a7203e7d0399b315f433ca2354`  
		Last Modified: Mon, 26 Jan 2026 22:10:26 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60649b02a4261f297ae8ff3516a51c6abc875019bc452e5e29f28023f973d2e`  
		Last Modified: Mon, 26 Jan 2026 22:10:41 GMT  
		Size: 224.6 MB (224586810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4797cbc191a1fe112d4ab6c47be1f2696475a364491bb0240c48d5049e6dc72`  
		Last Modified: Mon, 26 Jan 2026 22:10:26 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
